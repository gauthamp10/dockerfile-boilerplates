## Contributing

### Adding Dockerfile for a new langauge

#### Naming and directory schema

![directory-schema](https://i.imgur.com/bykj2FC.png)

Files should be arranged in the above fashion. Every language must contain:

- Source code
- Dockerfile
- Readme file

The naming of the folders shouldn't be abbreviated from like (javascript to js). 
Always use lowercase for file names. Hypens should be used in between files and folder names instead of space.

#### Source Code

The source code of the specific programming language should be kept as simple as possible like a basic Hello World program so as to just show the program works inside Docker.Never ask input from user and don't print unesserary lines or extra statements.

<ins>References for Hello World!</ins>

- [helloworldcollection](http://helloworldcollection.de/) 
- [leachimm6-helloworld](https://github.com/leachim6/hello-world/)

#### Dockerfile

The docker file must be prepared in such a fashion that it doesn't use any unofficial docker images. Try to stick with alpine or ubuntu as the base image as often as possible.

Please note that the repository files as automatically tested upon commit by Travis-ci and docker images are uploaded to [AUTHOR's](https://github.com/gauthamp10) [docker repository](https://hub.docker.com/u/gauthamp10). So make sure that your code pass some basic unit tests and after the execution, it should reach an exit 0. In most situations , it will exit 0 but in case of a web based program, you have to write a test case to do so. 

Sample unit test in [python](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/python/web/app/app_test.py) and it's [Dockerfile](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/python/web/Dockerfile).

#### Readme

 The Readme file should contain brief information on how to build and run the Dockerfile.