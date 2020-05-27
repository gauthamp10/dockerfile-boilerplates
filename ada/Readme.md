### __Ada Boilerplate Docker__

Build and run Ada code via docker.

__Where do I start?__

✌️ Two Choices.

__#1: Pull the image from dockerhub and run__

```

  - docker pull gauthamp10/ada
  - docker run --rm -v /path/to/volume:/usr/share/nginx/html gauthamp10/ada

```
To add the image in your Dockerfile:

```
FROM gauthamp10/ada:latest
```

__#2: Build your own version from the template *Dockerfile*__

Edit the Dockerfile as per your liking and then 

```

  - docker build -t ada .
  - docker run --rm ada

```

__How can I upload my image to docker hub ?__

Create an account on dockerhub and

```

  - docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
  - docker tag ada $DOCKER_USERNAME/ada:$VERSION
  - docker push $DOCKER_USERNAME/ada:$VERSION

```

Play around with your custom build

```

  - docker pull $DOCKER_USERNAME/ada:latest

```

Contributions are always welcomed. Create a boilerplate / template for any other porgramming langauges which not available in the list by opening a pull request. 