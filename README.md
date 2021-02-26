## This repository is made for the purpose of testing how Travis works with new releases

Script `hello.go` prints `hello`

## Prerequisites

- [X] Install GO on MacOS:
```shell
$ brew install golang
```

- [X] Install [Travis CLI](https://blog.travis-ci.com/2013-01-14-new-client)

## What's included

The repository includes:

- A [.travis.yml](https://github.com/dlavric/golang-travis-release/blob/main/.travis.yml) configuration file

- A [hello.go](https://github.com/dlavric/golang-travis-release/blob/main/hello.go) go lang script that prints hello

## How to use this repo

- Clone this repo:

```shell
$ git clone https://github.com/dlavric/golang-hello-test-travis
$ cd golang-hello-test-travis
```

- Build and install the program with the go tool:
```shell
$ go mod init example.com/user/hello
$ go install example.com/user/hello
```

- Add the install directory to our PATH to make running binaries easy:
```shell
$ export PATH=$PATH:$(dirname $(go list -f '{{.Target}}' .))
```

- Run `hello.go`:
```shell
$ go run hello.go
```


