# ETC Docker

## What
Repository contains a `docker-compose.yml` that launches the following containers:
* [emerald-vault](https://github.com/ETCDEVTeam/emerald-vault) - ETCDEV CLI tool for managing accounts
* [sputnikvm-dev](https://github.com/ETCDEVTeam/sputnikvm-dev) - ETCDEV testrpc on port 8545
* [emerald-explorer](https://github.com/ETCDEVTeam/emerald-explorer) - ETCDEV explorer available on http://localhost:3000/blocks

## Usage

Run ```docker-compose up``` to bootstrap the containers.

It might make sense to have `emerald-vault` installed also on the container you develop on.

### TODO
* Make sure vault has permissions to write
* Add a container for a wallet interface?
* Think if using docker volume for testrpc makes sense
* Add a container for development that includes `emerald-vault` and other useful tools (perhaps deploy stuff)
* Add support to generate a wallet with a passphrase from docker-compose

    You can probably use `emerald-vault` as is done here https://github.com/ETCDEVTeam/emerald/blob/master/index.js#L74-L100
* Check if it makes sense to merge `emerald-vault` and `sputnikvm-dev` containers

## Disclamer
Use at your own risk.
