# docker-infra

A collection of Docker infrastructure files for quick deployment of
development services.

## Contents

- **`compose/`** — Docker Compose files for various services
  - [`sql-server-2025`](compose/sql-server-2025/) — Microsoft SQL Server 2025
- **`get-docker.sh`** — Docker Engine installation script for Linux, synchronised
  weekly from upstream

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
