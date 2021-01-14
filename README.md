# switcheocli Docker Build

This is an extremely light weight Docker build for the Switcheo CLI. This can be helpful when it is not required to run a full node and be able to interact with the CLI wallet.

## Mainnet

This is the CLI release only, it doesn't appear that a new CLI gets released on the same schedule as the full node so this has not changed in quite some time.

```
cd mainnet
docker build -t tradehub-mainnet-cli -f Dockerfile .
docker run -it --rm tradehub-mainnet-cli bash
```

## Testnet

I have not found a tesnet specific CLI release so this is the most recent testnet build. It is not required to run the full node or validator to use the CLI.

```
cd testnet
docker build -t tradehub-testnet-cli -f Dockerfile .
docker run -it --rm tradehub-testnet-cli bash
```
