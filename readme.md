# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## Running project locally

I am using linux machine (ubuntu 20.04 LTS)

### step-1: - clone repo

clone [Anythink-Market-e09g5.git](https://github.com/ObelusFamily/Anythink-Market-e09g5.git) repo

### step-2: - understanding git flow

- add CODEOWNERS file to repo.
- create and branch.
- make a commit with brif message about changings.
- before pushing you need to setup your github account. (add credentials and you may need a personal access token)
- visite [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) for personal access token explaination.
- push the changes.
- make a pull request and `@vanessa-cooper` will approve it.
  these steps are also explained by @Ness at Anythink.

### step-3 - install docker

first check the [system-requirements](https://docs.docker.com/desktop/install/linux-install/#system-requirements)

- check if your system support [KVM virtualization](https://docs.docker.com/desktop/install/linux-install/#kvm-virtualization-support)
  and also don't forget to setup device user permissions.

- complete [Prerequisites](https://docs.docker.com/desktop/install/ubuntu/#prerequisites)

- setup [docker's package repository](https://docs.docker.com/engine/install/ubuntu/#set-up-the-repository)

- [Download](https://desktop.docker.com/linux/main/amd64/docker-desktop-4.11.0-amd64.deb?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-linux-amd64) debian package

- install the package with apt by running following commands.

```
 sudo apt-get update
 sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```

for further information see the [link](https://docs.docker.com/desktop/install/ubuntu/#install-docker-desktop)

### step-4: - lauch Docker

- Now It's time to launch Docker Desktop
  you have two options here lauch Docker Desktop either using cli or application icon

for cli run following command.

```
 systemctl --user start docker-desktop
```

for using icon go to application search for Docker Desktop and run it

you can run following commands to verify if installation was sucessful or not

```
 docker compose version
    Docker Compose version v2.7.0
 docker --version
    Docker version 20.10.17, build 100c701
 docker version
    lient: Docker Engine - Community
    Cloud integration: v1.0.28
    Version:           20.10.17
    API version:       1.41
    Go version:        go1.17.11
    ...
```

for further information visit following [link](https://docs.docker.com/desktop/install/ubuntu/#launch-docker-desktop)

### step-5: - run project

open terminal

```
cd `path to project root dir`
```

run following command

```
docker compose up
```

To check if both backend running.
go to following address in browser.

```
http://localhost:3000/api/ping
```

for frontend type this.

```
http://localhost:3001/register
```

If you see and register form and you are able to register yourself. that means Everything is ok.

Hurrah! if you reached here then congratulations you're a developer now(just kidding :))
