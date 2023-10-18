# Simple Bank

This repository clone the [Backend Master Class](https://bit.ly/backendmaster) course by [TECH SCHOOL](https://bit.ly/m/techschool).

## Setup local development

### Install tools

- [Docker desktop](https://www.docker.com/products/docker-desktop)
- [DBeaver](https://dbeaver.com)
- [Golang](https://golang.org/)
- [Homebrew](https://brew.sh/)
- [Migrate](https://github.com/golang-migrate/migrate/tree/master/cmd/migrate)

    ```bash
    brew install golang-migrate
    ```

### Setup infrastructure

- Create the bank-network

    ``` bash
    make network
    ```

- Start postgres container:

    ```bash
    make postgres
    ```

- Create simple_bank database:

    ```bash
    make createdb
    ```

- Run db migration up all versions:

    ```bash
    make migrateup
    ```

- Run db migration down all versions:

    ```bash
    make migratedown
    ```

### How to generate code

- Create a new db migration:

    ```bash
    make new_migration name=<migration_name>
    ```