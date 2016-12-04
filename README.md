# Angular 2 Cli Docker Files

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

After generating a new project with the angular-cli (e.g. `ng new myProject`) these files can be used to dockerize the project.

## Instructions

```bash
ng new myProject

git clone git@github.com:amrtgaber/angular2-cli-docker-files.git
cp angular2-cli-docker-files/* angular2-cli-docker-files/.* myProject/

cd myProject

# Replaces 'APP-NAME-HERE' in the Dockerfile and docker-compose.yml
sed -i 's/APP-NAME-HERE/myProject/g' *

docker-compose up
```

That's it! :tada: :sparkles: :sparkles:

## See it in action

Navigate to `localhost:4200` in your browser.

**NOTE**: For docker toolbox you must replace 'localhost' with the machine ip. You can get the machine ip with the following command.

```bash
docker-machine ip angular2-cli-webpack-docker
```

## Installing dependencies

```bash
npm install --save <dependency>
docker-compose down
docker-compose up --build
```
