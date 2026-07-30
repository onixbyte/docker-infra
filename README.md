# docker-infra

A collection of Docker infrastructure files for quick deployment of
development services.

## Usage

Each service lives under its own directory within `compose/`. Copy the
`.env.example` to `.env`, adjust the values, then run:

```sh
cd compose/<service>
docker compose up -d
```

## Licence

This project is licensed under the MIT Licence — see [LICENCE](LICENCE) for
details.

Third-party software included in this repository (such as `get-docker.sh`)
remains under its original licence terms.
