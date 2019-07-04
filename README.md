# rescalecli-docker
Run [Rescale CLI](https://docs.rescale.com/articles/rescale-cli/) on Docker

## Usage
Pull from [Docker Hub](https://hub.docker.com/r/takashiratori/rescalecli), or built Docker image locally

### Pull from Docker Hub
```bash
$ docker run -it -v $(pwd):/home/rescale takashiratori/rescalecli:1.0.95-177015c /bin/bash
$ java -jar /usr/local/bin/rescale.jar -v
1.0.95-177015c
$ java -jar /usr/local/bin/rescale.jar -h
usage: Rescale Client App [-h] [-X API-BASE-URL] [--profile API-PROFILE] [--no-prompt] [-q] [-v]

Client app for running jobs on Rescale

optional arguments:
  -h, --help             show this help message and exit
  -X API-BASE-URL, --api-base-url API-BASE-URL
                         The Rescale platform url. Eg: https://platform.rescale.com or https://itar.rescale.com
  --profile API-PROFILE  The name of the CLI configuration profile to use. (default: default)
  --no-prompt            Never open an interactive prompt (implied by --quiet) (default: false)
  -q, --quiet            Suppress informational logging output (default: false)
  -v, --version
```

### Built Docker image locally
Clone this repository, and build the image
```bash
$ git clone git@github.com:TakahisaShiratori/rescalecli-docker.git
$ cd rescalecli-docker/1.0.95-177015c/
$ docker build -t rescalecli:1.0.95-177015c .
```
Run the built image
```bash
$ docker run -it -v $(pwd):/home/rescale rescalecli:1.0.95-177015c /bin/bash
```
