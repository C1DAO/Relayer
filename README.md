# @vmeta3/message-relayer

`message-relayer` is a service that automatically finalizes ("relays") messages sent from Vmeta3 to Ethereum.
This package is meant to be used during local development and should NOT be used on a production network.

## Installation

Clone, install, and build the Vmeta3 monorepo:

```
git clone https://github.com/ethereum-Vmeta3/Vmeta3.git
yarn install
yarn build
```

## Running the relayer (Docker)

The `message-relayer` can be included as part of the [local Vmeta3 development environment](https://community.Vmeta3.io/docs/developers/build/dev-node/).
Although the `message-relayer` is not turned on by default, it can be enabled by [changing this line in docker-compose.yml](https://github.com/ethereum-Vmeta3/Vmeta3/blob/51a527b8e3fe69940fb8c0f5e4aa2e0ae8ee294c/ops/docker-compose.yml#L129) to:

```
replicas: 1
```

## Running the relayer (manual)

The `message-relayer` can also be run manually.
Copy `.env.example` into a new file named `.env`, then set the environment variables listed there.
Once your environment variables have been set, run the relayer via:

```
yarn start
```
