Docker JupyterLab
=================

# Introduction

DockerFile for [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/).

# Quick start

## Docker Run

```bash
$ docker container run --rm -p 8888:8888 andrespp/jupyterlab
$ docker run --rm -v $(pwd):/opt/app/data -p 8888:8888 andrespp/jupyterlab
```

## Docker compose

* `docker-compose.yaml`
```yaml
version: '3.1'

services:
  jupyterlab:
    image: andrespp/jupyterlab
    ports:
      - "8888:8888"
    volumes:
      - ./data:/opt/app/data
```

* Bring compose up

```bash
$ docker-compose up
```

# Issues

If you have any problems with or questions about this image, please contact me
through a [GitHub issue](https://github.com/andrespp/docker-jupyterlab/issues).
