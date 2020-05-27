### Javascript/Static HTML Boilerplate Docker

__Build and run Javascript/Static HTML via docker.__

__*Where do I start?*__

Two Choices.

#1: Pull image from dockerhub and run

```

  - docker pull gauthamp10/javascript
  - docker run --rm -v /path/to/volume:/usr/share/nginx/html gauthamp10/javascript

```
To add the image in your Dockerfile:

```
FROM gauthamp10/javascript:latest
```

#2: Build your own version from the template *Dockerfile*

At first edit the Dockerfile as per your liking 

```

  - docker build -t javascript .
  - docker run -p 5001:80 --rm -v /path/to/valoume/:/usr/share/nginx/html javascript

```

__*How can I upload my image to docker hub* ?__

Create an account on dockerhub and

```

  - docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
  - docker tag javascript $DOCKER_USERNAME/javascript:$VERSION
  - docker push $DOCKER_USERNAME/javascript:$VERSION

```

Play around with your custom build by

```

  - docker pull $DOCKER_USERNAME/javascript:latest

```