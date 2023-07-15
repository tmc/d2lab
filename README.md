# d2lab

## Getting Started

### Pre-requisites

This codebase requires the following tools to be present on your machine.

- [Docker](https://docs.docker.com/get-docker/)
- [Homebrew](https://brew.sh/)

### Running the Project

To get started with this project:

Populate `dev-harness/.env`.

Run services:
```shell
$ make run-services
```

You should see this in the [Tilt UI](http://localhost:10350/r/react-frontend/overview):
<img width="1582" alt="tilt-harness" src="https://github.com/tmc/hackathon-starter/assets/3977/388b1c95-c5b8-4ab0-83ec-d3eaff911035">

The [React Frontend](http://localhost:3000):
<img width="1582" alt="react-frontend" src="https://github.com/tmc/hackathon-starter/assets/3977/e5b06cf9-7c4d-476b-9371-bd3462b62614">

The [Apollo GraphQL Sandbox](http://localhost:3000/sandbox):
<img width="1582" alt="apollo-graphql-sandbox" src="https://github.com/tmc/hackathon-starter/assets/3977/d2e27ba8-5e86-4ebf-93c1-8d5ab0e4f6c5">


### Accessing Services

- [10350](http://localhost:10350/r/react-frontend/overview) - The Tilt Harness (with the react-frontend selected).
- [3000](http://localhost:3000) - React Frontend.
- [3000](http://localhost:3000/sandbox) - GraphQL Sandbox.
- [4000](http://localhost:4000) - GraphQL Gateway.
- [5432](https://www.postgresql.org/docs/current/app-psql.html) - PostgreSQL database.
- [8080](http://localhost:8080) - Go GraphQL backend
- [6379](https://redis.io/docs/ui/cli/#command-line-usage) - Redis Server.
- [6380](http://localhost:6380) - RedisInsight web UI.
- [16686](http://localhost:16686) - [Jaeger](https://www.jaegertracing.io/docs/1.45/getting-started/) web UI (distributed trace viewer).


## Directory Structure

The project is divided into various directories, each corresponding to a distinct part of the application. Here's a quick breakdown:

- [`./go-graphql-backend`](./go-graphql-backend): This directory contains a backend service implemented in Go with the help of gqlgen, a Go library for building GraphQL servers. It includes support for subscriptions.

- [`./react-frontend`](./react-frontend): This is a frontend application built with React and TypeScript. React is a JavaScript library for building user interfaces, and TypeScript is a statically typed superset of JavaScript that adds optional types.

- [`./gateway`](./gateway): This directory contains a sample setup that combines multiple backend services. 

- [`./dev-harness`](./dev-harness): This directory contains examples of `docker-compose.yml` files showing how to configure Docker Compose to run the various components of this project together.

Each directory contains a `README.md` file with more detailed information about that part of the project. 

## Further Reading

- [Gqlgen Documentation](https://gqlgen.com/)
- [React Documentation](https://reactjs.org/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)

