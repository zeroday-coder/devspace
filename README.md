![DevSpace Workflow](docs/website/static/img/header-readme.svg)

# DevSpace - Cloud-Native Development with Kubernetes
[![Build Status](https://travis-ci.org/covexo/devspace.svg?branch=master)](https://travis-ci.org/covexo/devspace)
[![Go Report Card](https://goreportcard.com/badge/github.com/covexo/devspace)](https://goreportcard.com/report/github.com/covexo/devspace)
[![Join the community on Spectrum Chart](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/devspace)

With a DevSpace, you can build, test and run code directly inside any Kubernetes cluster. You can run `devspace up` in any of your projects and the client-only DevSpace CLI will start a DevSpace within your Kubernetes cluster. Keep coding as usual and the DevSpace CLI will sync any code change directly into the containers of your DevSpace. No more waiting for re-building images, re-deploying containers and restarting applications on every source code change. Simply edit your code with any IDE and run your code instantly inside your DevSpace.

## Why use a DevSpace?
Program inside any Kubernetes cluster (e.g. minikube, self-hosted or cloud platform) and:
- iterate quickly: no more re-building and pushing images on every change
- save time with **hot reloading** tools (e.g. nodemon)
- keep your existing workflow: **code with your favorite IDE** and desktop tools
- access cluster-internal services and data with ease
- debug efficiently with port forwarding and terminal proxying
- migrate to Docker & Kubernetes within minutes

## Demo
coming soon

## Installation


## Quickstart
The DevSpace CLI allows you to create a DevSpace for any existing project with just a single command:
```
devspace up
```
Take a look at the [Getting Started Guide](https://devspace.covexo.com/docs/getting-started/quickstart.html) on our documentation page to start coding with a DevSpace.

**Note:** Don't worry, with the cleanup command `devspace reset`, you can easily reset your project and go back to local development.

## Documentation
Here you can find some links to the most important pages of our documentation:
- [Getting Started Guide](https://devspace.covexo.com/docs/getting-started/quickstart.html)
- [CLI Documentation](https://devspace.covexo.com/docs/cli/init.html)
- [Configuration Specification](https://devspace.covexo.com/docs/configuration/dockerfile.html)
- [Architecture Documentation](https://devspace.covexo.com/docs/advanced/architecture.html)

## Architecture
Architecturally, the DevSpace CLI is a client-side software that interacts with services within your Kubernetes cluster. While the DevSpace CLI can deploy required services (e.g. image registry, Tiller server, Kaniko build pods) automatically, you can also configure it to use already deployed or externally hosted services.

![DevSpace CLI Architecture](docs/website/static/img/devspace-architecture.svg)

For a more detailed description of the internals of the DevSpace CLI, take a look at the [Architecture Documentation](https://devspace.covexo.com/docs/advanced/architecture.html).

**Note:** Any interaction between your local computer and your DevSpace is passed through your Kubernetes API server, so you should ensure that your API server is protected with a suitable configuration for using TLS.

## Contributing
As any open source projects, we are looking forward to your contributions.

### Reporting Issues
If you find a bug while working with the DevSpace CLI, please [open an issue on GitHub](https://github.com/covexo/devspace/issues/new?labels=kind%2Fbug&title=Bug:) and let us know what went wrong. We will try to fix it as quickly as we can.

### Feedback & Feature Requests
You are more than welcome to open issues in this project to:
- [give feedback](https://github.com/covexo/devspace/issues/new?labels=kind%2Ffeedback&title=Feedback:)
- [suggest new features](https://github.com/covexo/devspace/issues/new?labels=kind%2Ffeature&title=Feature%20Request:)
- [ask a question](https://github.com/covexo/devspace/issues/new?labels=kind%2Fquestion&title=Question:)

### Contributing Code
This project is mainly written in Golang. To contribute code,
1. Check-out the project: `git clone https://github.com/covexo/devspace && cd devspace`
2. Install the dependencies: `dep ensure -v` (requires [Installing Dep](https://golang.github.io/dep/docs/installation.html))
3. Make changes to the code (add new dependencies to the Gopkg.toml)
4. Build the project, e.g. via `go build -o devspace.exe`

## License
You can use the DevSpace CLI for any private or commercial projects because it is licensed unter the Apache 2.0 open source license.

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fcovexo%2Fdevspace.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fcovexo%2Fdevspace?ref=badge_large)
