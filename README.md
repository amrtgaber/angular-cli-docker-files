# Angular Cli Docker Files

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

After generating a new project with the angular-cli (e.g. `ng new myProject`) these files can be used to dockerize the project.

## Table of Contents
* [Instructions](#instructions)
* [See it in action](#see-it-in-action)
* [Installing dependencies](#installing-dependencies)
* [Add yourself as the maintainer](#add-yourself-as-the-maintainer)

## Instructions

```bash
ng new myProject

git clone git@github.com:amrtgaber/angular-cli-docker-files.git
cp angular-cli-docker-files/.dockerignore myProject/
cp angular-cli-docker-files/docker-compose.yml myProject/
cp angular-cli-docker-files/Dockerfile myProject/

cd myProject

# Replaces 'APP-NAME-HERE' in the Dockerfile and docker-compose.yml
sed -i 's/APP-NAME-HERE/myProject/g' *

docker-compose up
```

That's it! :tada: :sparkles: :sparkles:

## See it in action

Navigate to [localhost:4200](localhost:4200) in your browser.

**NOTE**: For docker toolbox you must replace `localhost` with the machine ip. You can get the machine ip with the following command.

```bash
docker-machine ip myProject
```

## Installing dependencies

```bash
npm install --save <dependency>
docker-compose down
docker-compose up --build
```

## Add yourself as the maintainer
In the `Dockerfile` after the `FROM` line, add the line:

```Dockerfile
LABEL maintainer="Your name/organization <email or homepage>"
```
