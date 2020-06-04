<h1 align="center">Dockerfile Boilerplates For All</h1>

<p align="center">
  <img src="https://i.imgur.com/MvsT3qI.png" alt="Hello World! of Docker"/>
</p>

<a href="https://travis-ci.com/gauthamp10/dockerfile-boilerplates"><img src="https://img.icons8.com/color/48/000000/travis-ci.png"/></a> [![Build Status](https://travis-ci.com/gauthamp10/dockerfile-boilerplates.svg?token=GyGbkGV9nLfsTamsNpS4&branch=master)](https://travis-ci.com/gauthamp10/dockerfile-boilerplates) ![GitHub repo size](https://img.shields.io/github/repo-size/gauthamp10/dockerfile-boilerplates) ![visitors](https://visitor-badge.glitch.me/badge?page_id=gauthamp10.dockerfile-boilerplates)

Docker boilerplates / templates for most common progamming languages. Like a *Hello World!* but for  docker images.

---

Note: Not production quality yet

## __List Of Programming Languages__

[![](https://img.shields.io/badge/ada-%20-blue)](https://img.shields.io/badge/ada-%20-blue) [![](https://img.shields.io/badge/bash-%20-blue)](https://img.shields.io/badge/bash-%20-blue) [![](https://img.shields.io/badge/C-%20-blue)](https://img.shields.io/badge/C-%20-blue) [![](https://img.shields.io/badge/CommonLisp-%20-blue)](https://img.shields.io/badge/CommonLisp-%20-blue) [![](https://img.shields.io/badge/cpp-%20-blue)](https://img.shields.io/badge/cpp-%20-blue) [![](https://img.shields.io/badge/dart-%20-blue)](https://img.shields.io/badge/dart-%20-blue) [![](https://img.shields.io/badge/elixir-%20-blue)](https://img.shields.io/badge/elixir-%20-blue) [![](https://img.shields.io/badge/erlang-%20-blue)](https://img.shields.io/badge/erlang-%20-blue) [![](https://img.shields.io/badge/fortran-%20-blue)](https://img.shields.io/badge/fortran-%20-blue) [![](https://img.shields.io/badge/go-%20-blue)](https://img.shields.io/badge/go-%20-blue) [![](https://img.shields.io/badge/haskell-%20-blue)](https://img.shields.io/badge/haskell-%20-blue) [![](https://img.shields.io/badge/icon-%20-blue)](https://img.shields.io/badge/icon-%20-blue) [![](https://img.shields.io/badge/java-%20-blue)](https://img.shields.io/badge/java-%20-blue) [![](https://img.shields.io/badge/javascript-%20-blue)](https://img.shields.io/badge/javascript-%20-blue) [![](https://img.shields.io/badge/julia-%20-blue)](https://img.shields.io/badge/julia-%20-blue) [![](https://img.shields.io/badge/kotlin-%20-blue)](https://img.shields.io/badge/kotlin-%20-blue) [![](https://img.shields.io/badge/lisp-%20-blue)](https://img.shields.io/badge/lisp-%20-blue) [![](https://img.shields.io/badge/lua-%20-blue)](https://img.shields.io/badge/lua-%20-blue) [![](https://img.shields.io/badge/node-%20-blue)](https://img.shields.io/badge/node-%20-blue) [![](https://img.shields.io/badge/objectiveC-%20-blue)](https://img.shields.io/badge/objectiveC-%20-blue) [![](https://img.shields.io/badge/perl-%20-blue)](https://img.shields.io/badge/perl-%20-blue) [![](https://img.shields.io/badge/php-%20-blue)](https://img.shields.io/badge/php-%20-blue) [![](https://img.shields.io/badge/python-%20-blue)](https://img.shields.io/badge/python-%20-blue) [![](https://img.shields.io/badge/R-%20-blue)](https://img.shields.io/badge/R-%20-blue) [![](https://img.shields.io/badge/rust-%20-blue)](https://img.shields.io/badge/rust-%20-blue) [![](https://img.shields.io/badge/scala-%20-blue)](https://img.shields.io/badge/scala-%20-blue) [![](https://img.shields.io/badge/swift-%20-blue)](https://img.shields.io/badge/swift-%20-blue) 

## __Docker__

Docker is service which provides OS-level virtualization with such ease and compatibility that no virtual machines can offer. It also packs software dependencies within itself and runs independently and flexibly on various platforms.

To know more: [docker.com](https://www.docker.com/)


## __Instructions__

__Where do I start?__

✌️ Two Choices.

__#1: Pull the image from dockerhub and run__

```

  - docker pull gauthamp10/language-name
  - docker run --rm gauthamp10/language-name
  For web app
  - docker run -p 5000:5000 --rm -v /path/to/volume/:/app language-name

  Example:

  - docker pull gauthamp10/java
  - docker run --rm gauthamp10/java

```
To add the image in your Dockerfile:

```
FROM gauthamp10/language-name:latest

Example:

FROM gauthamp10/java

```

__#2: Build your own version from the template *Dockerfile*__

At first edit the Dockerfile as per your liking 

```

  - docker build -t language-name .
  - docker run --rm language-name

Example:

  - docker build -t java .
  - docker run --rm java

```

__How can I upload my image to docker hub?__

Create an account on [dockerhub](https://hub.docker.com/) and then

```

  - docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
  - docker tag language-name $DOCKER_USERNAME/language-name:$BUILD_VERSION
  - docker push $DOCKER_USERNAME/language-name:$BUILD_VERSION

  Example:

  - docker login -u gauthamp10 -p **********
  - docker tag java gauthamp10/java:1.0
  - docker push gauthamp10/java:1.0


```

Play around with your custom build by

```

  - docker pull $DOCKER_USERNAME/language-name:latest

  Example:

  - docker pull gauthamp10/java:latest

```

## __Overview Of Dockerfile__

|     Image Name     |     Language Version     |     Base Image     |     Layers      |     Image Size     |
| :--------------- | :--------------: | :---------------: | :---------------: | ------------------------------------------: |
| [gauthamp10/ada](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/ada/Dockerfile)        |     10.1.0-1     |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/ada.svg)](https://microbadger.com/images/gauthamp10/ada)   |             [![](https://img.shields.io/badge/size-492MB-orange)](https://img.shields.io/badge/size-492MB-orange) |
| [gauthamp10/bash](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/bash/Dockerfile)       |      4.4.20      |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/bash.svg)](https://microbadger.com/images/gauthamp10/bash)   | [![](https://img.shields.io/badge/size-5.61MB-brightgreen)](https://img.shields.io/badge/size-5.61MB-brightgreen) |
| [gauthamp10/c-build](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/c/Dockerfile)          |     9.3.0-r2     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/c-build.svg)](https://microbadger.com/images/gauthamp10/c-build)   |             [![](https://img.shields.io/badge/size-181MB-yellow)](https://img.shields.io/badge/size-181MB-yellow) |
| [gauthamp10/clsip](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/clisp/Dockerfile)      |      2.49.92     |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/clisp.svg)](https://microbadger.com/images/gauthamp10/clisp)   |   [![](https://img.shields.io/badge/size-130MB-yellowgreen)](https://img.shields.io/badge/size-130MB-yellowgreen) |
| [gauthamp10/cpp](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/cpp/Dockerfile)        |     9.3.0-r2     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/cpp.svg)](https://microbadger.com/images/gauthamp10/cpp)   |             [![](https://img.shields.io/badge/size-181MB-yellow)](https://img.shields.io/badge/size-181MB-yellow) |
| [gauthamp10/dart](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/dart/Dockerfile)       |       2.8.2      |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/dart.svg)](https://microbadger.com/images/gauthamp10/dart)   |                   [![](https://img.shields.io/badge/size-628MB-red)](https://img.shields.io/badge/size-628MB-red) |
| [gauthamp10/elixir](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/elixir/Dockerfile)     |     1.10.3-r0    |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/elixir.svg)](https://microbadger.com/images/gauthamp10/elixir)   |     [![](https://img.shields.io/badge/size-40MB-brightgreen)](https://img.shields.io/badge/size-40MB-brightgreen) |
| [gauthamp10/erlang](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/erlang/Dockerfile)     |      23.0-r0     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/erlang.svg)](https://microbadger.com/images/gauthamp10/erlang)   | [![](https://img.shields.io/badge/size-18.4MB-brightgreen)](https://img.shields.io/badge/size-18.4MB-brightgreen) |
| [gauthamp10/fortran](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/fortran/Dockerfile)    |     9.3.0-r2     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/fortran.svg)](https://microbadger.com/images/gauthamp10/fortran)   |             [![](https://img.shields.io/badge/size-210MB-yellow)](https://img.shields.io/badge/size-210MB-yellow) |
| [gauthamp10/go-build](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/go/Dockerfile)         |    1.13.11-r0    |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/go-build.svg)](https://microbadger.com/images/gauthamp10/go-build)   |             [![](https://img.shields.io/badge/size-419MB-orange)](https://img.shields.io/badge/size-419MB-orange) |
| [gauthamp10/haskell](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/haskell/Dockerfile)    |     8.8.3-r0     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/haskell.svg)](https://microbadger.com/images/gauthamp10/haskell)   |                 [![](https://img.shields.io/badge/size-1.08GB-red)](https://img.shields.io/badge/size-1.08GB-red) |
| [gauthamp10/icon](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/icon/Dockerfile)       |       v951       |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/icon.svg)](https://microbadger.com/images/gauthamp10/icon)   |   [![](https://img.shields.io/badge/size-119MB-yellowgreen)](https://img.shields.io/badge/size-119MB-yellowgreen) |
| [gauthamp10/java](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/java/Dockerfile)       |     openjdk8     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/java.svg)](https://microbadger.com/images/gauthamp10/java)   |   [![](https://img.shields.io/badge/size-123MB-yellowgreen)](https://img.shields.io/badge/size-123MB-yellowgreen) |
| [gauthamp10/javascript](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/javascript/Dockerfile) | 1.18.0-r0(nginx) |    nginx:alpine|   [![](https://images.microbadger.com/badges/image/gauthamp10/javascript.svg)](https://microbadger.com/images/gauthamp10/javascript)   | [![](https://img.shields.io/badge/size-19.9MB-brightgreen)](https://img.shields.io/badge/size-19.9MB-brightgreen) |
| [gauthamp10/julia](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/julia/Dockerfile)      |       1.4.1      |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/julia.svg)](https://microbadger.com/images/gauthamp10/julia)   |             [![](https://img.shields.io/badge/size-469MB-orange)](https://img.shields.io/badge/size-469MB-orange) |
| [gauthamp10/kotlin](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/kotlin/Dockerfile)     |      v1.3.72     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/kotlin.svg)](https://microbadger.com/images/gauthamp10/kotlin)   |           [![](https://img.shields.io/badge/size-362MB-orange)](https://img.shields.io/badge/size-326MB-orange) |
| [gauthamp10/lisp](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/lisp/Dockerfile)       |      6.24-3      |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/lisp.svg)](https://microbadger.com/images/gauthamp10/lisp)   |   [![](https://img.shields.io/badge/size-130MB-yellowgreen)](https://img.shields.io/badge/size-130MB-yellowgreen) |
| [gauthamp10/lua](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/lua/Dockerfile)        |       5.2.4      |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/lua.svg)](https://microbadger.com/images/gauthamp10/lua)   | [![](https://img.shields.io/badge/size-6.32MB-brightgreen)](https://img.shields.io/badge/size-6.32MB-brightgreen) |
| [gauthamp10/node](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/node/Dockerfile)       |    12.16.3-r0    |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/node.svg)](https://microbadger.com/images/gauthamp10/node)   | [![](https://img.shields.io/badge/size-37.4MB-brightgreen)](https://img.shields.io/badge/size-37.4MB-brightgreen) |
| [gauthamp10/objc](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/objective-c/Dockerfile)       |     4.9.3.0-1    |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/objc.svg)](https://microbadger.com/images/gauthamp10/objc)   |                   [![](https://img.shields.io/badge/size-917MB-red)](https://img.shields.io/badge/size-917MB-red) |
| [gauthamp10/perl](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/perl/Dockerfile)       |     5.30.2-r0    |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/perl.svg)](https://microbadger.com/images/gauthamp10/perl)   | [![](https://img.shields.io/badge/size-39.8MB-brightgreen)](https://img.shields.io/badge/size-39.8MB-brightgreen) |
| [gauthamp10/php](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/php/Dockerfile)        |        7.4       | php:latest-apache |   [![](https://images.microbadger.com/badges/image/gauthamp10/php.svg)](https://microbadger.com/images/gauthamp10/php) |             [![](https://img.shields.io/badge/size-414MB-orange)](https://img.shields.io/badge/size-414MB-orange) |
| [gauthamp10/python](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/python/worker/Dockerfile)     |       3.6      |   python:3.6-slim|   [![](https://images.microbadger.com/badges/image/gauthamp10/python.svg)](https://microbadger.com/images/gauthamp10/python)   |   [![](https://img.shields.io/badge/size-156MB-yellowgreen)](https://img.shields.io/badge/size-156MB-yellowgreen) |
| [gauthamp10/pythonweb](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/python/web/Dockerfile)  |       3.6     |   python:3.6-slim|   [![](https://images.microbadger.com/badges/image/gauthamp10/pythonweb.svg)](https://microbadger.com/images/gauthamp10/pythonweb)   |   [![](https://img.shields.io/badge/size-165MB-yellowgreen)](https://img.shields.io/badge/size-165MB-yellowgreen) |
| [gauthamp10/r-build](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/r/Dockerfile)          |     3.6.3-r2     |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/r-build.svg)](https://microbadger.com/images/gauthamp10/r-build)   |   [![](https://img.shields.io/badge/size-122MB-yellowgreen)](https://img.shields.io/badge/size-122MB-yellowgreen) |
| [gauthamp10/rust](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/rust/Dockerfile)       |     1.43.1-r1    |   alpine:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/rust.svg)](https://microbadger.com/images/gauthamp10/rust)   |                   [![](https://img.shields.io/badge/size-611MB-red)](https://img.shields.io/badge/size-611MB-red) |
| [gauthamp10/scala](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/scala/Dockerfile)      |      2.13.2      |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/scala.svg)](https://microbadger.com/images/gauthamp10/scala)   |                   [![](https://img.shields.io/badge/size-562MB-red)](https://img.shields.io/badge/size-562MB-red) |
| [gauthamp10/swift](https://github.com/gauthamp10/dockerfile-boilerplates/blob/master/swift/Dockerfile)      |      5.2.3r      |   ubuntu:latest |   [![](https://images.microbadger.com/badges/image/gauthamp10/swift.svg)](https://microbadger.com/images/gauthamp10/swift)   |                 [![](https://img.shields.io/badge/size-2.39GB-red)](https://img.shields.io/badge/size-2.39GB-red) |



## __Note:__ 

This repo is tested with automated builds on commit with TRAVIS-CI. Some image meta data is being pulled using Microbadger.

## __How can I contribute?__ 

Contributions are always welcomed. Create a boilerplate / template for any other programming languages which is not available in the repo by opening a pull request.For more information checkout the [CONTRIBUTING.md](CONTRIBUTING.md) file.

## Contributors 😁💌

<table>
  <tr>
  <td align="center"><a href="https://gauthamp10.github.io/"><img src="https://avatars1.githubusercontent.com/u/31800012?s=460&u=5a57d59caba193f2ffecce05fbf070084885966e&v=4" width="100px;" alt=""/><br /><sub><b>Gautham Prakash</b></sub></a><br /><a href="https://github.com/gauthamp10/dockerfile-boilerplates" title="Documentation">✍️</a></td>
    <td align="center"><a href="https://github.com/joshuawalcher"><img src="https://avatars3.githubusercontent.com/u/2533702?s=400&v=4" width="100px;" alt=""/><br /><sub><b>Joshua Walcher</b></sub></a><br /><a href="https://github.com/gauthamp10/dockerfile-boilerplates" title="Documentation">📖</a></td>
    </tr>
    </table>


## __Author__

 **Gautham Prakash**
 
  My other projects: [github.com/gauthamp10](https://github.com/gauthamp10)

  Website: [gauthamp10.github.io](https://gauthamp10.github.io)

  Blog: [gauthamp10/blog](https://gauthamp10.github.io/blog)

## __License__  

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
