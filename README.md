# Hello Moby Dock

> Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.

<br>

## Getting my hands dirty with docker.

This project is my way of exploring docker.

Primary sources of references were

- [Docker Docs](https://docs.docker.com/get-started/overview/)
- [The Net Ninja](https://youtube.com/playlist?list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)

## Running on local system

- Clone the repo using the `--recursive` flag to ensure that the submodule is also cloned
- Assuming docker is installed and running in your system use
  `docker-compose up` from the root directory of the project
- Visit http://localhost:3000/, http://localhost:4000/, and http://localhost:5000/ on your browser.

## Learnings

- Basic concepts of docker
- Configuring Dockerfile
- Building images
- Optimising build speed using layer caching
    <div>
    <img src="https://github.com/dwi13L/the_dockerphile/blob/0bd8350cb0e1a4cefae90661e32527854b96707c/Build%20Speed%20Comparison.png" width="500"/>
    </div>

- Mapping volumes
- Creating and running containers
- Using docker compose to define and spin up multiple containerised applications at once
- Sharing docker images via docker hub
  - [visit hello_moby_dock @ hub.docker](https://hub.docker.com/repository/docker/dwi13l/hello_moby_dock)

<br>

### Dockerfile

> Dockerfile: A text document that contains all the commands a user could call on the command line to assemble an image

- Head over to the [dockerphile](https://github.com/dwi13L/the_dockerphile/tree/fa862932e1e64b8282845abd0e56a367fa2a6b8f) submodule.
- Changes to the [Dockerfile](https://github.com/dwi13L/the_dockerphile/blob/2a1eed6312e81da83449dc90aa57d878ea08eb52/Dockerfile) are explained through comments
- We also write Dockerfiles for two other apps

  - A Express API backend (api)
  - A React app that reads data from the backend (myblog)

  <br>

### Docker Compose

> Docker Compose: A tool that was developed to help define and share multi-container applications. With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down

- We define services in the [docker-compose](https://github.com/dwi13L/moby-dock-meets/blob/db65796d9c17e4cc4684f88968691e5b5560ed4d/docker-compose.yaml) file and spin up all our applications at once using the `docker-compose up` command
