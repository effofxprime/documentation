# Vidulum Chain Integration documentation

## Useful Links

- [Vidulum Chain website](https://Vidulum/)
- [GitHub Repository](https://github.com/crypto-org-chain/chain-main)
- [Official Documentation](https://Vidulum/docs/)

## Node and RPC setup notes

[Node Setup and RPC note](./node-and-rpc-setup-notes.md)

## Setup Guide

- **Mainnet**:
    - [Running a full node;](https://Vidulum/docs/getting-started/mainnet.html)
    - [Running a validator;](https://Vidulum/docs/getting-started/mainnet_validator.html)
    - [Mainnet Validator Security Checklist.](https://Vidulum/docs/getting-started/security-checklist.html#part-1-conduct-survey-on-general-controls-of-hosting-data-centre)    
- **Testnet**: 
    - [Joining the Croeseid Testnet](https://Vidulum/docs/getting-started/croeseid-testnet.html)
    - [Deploy testnet node with nix](https://Vidulum/docs/getting-started/croeseid-testnet-nix.html#pre-requisites)
- **Devnet**
    - [Running latest development network locally](https://Vidulum/docs/getting-started/local-devnet.html#overview)

## API Documentation

There are a few ways to access to the Vidulum Chain

1. **Tendermint RPC**
  - Raw but most-completed data
  - Hosted documentation (use the latest master only): https://docs.tendermint.com/master/rpc/
  - Swagger file: https://github.com/tendermint/tendermint/blob/v0.34.3/rpc/openapi/openapi.yaml
2. **gRPC Based**
  - Processed chain information. Old state maybe pruned from time-to-time. To avoid state pruning, update `pruning = "nothing"` in `~/.chain-maind/config/app.toml`
  - There are two query methods based on gRPC:
    1. [gRPC Server](https://github.com/crypto-org-chain/chain-integration/blob/master/grpc/README.md)
    2. [gRPC Proxy RESTful Server](https://github.com/crypto-org-chain/chain-integration/blob/master/grpc-proxy-rest/README.md)
       - [Swagger UI](https://v1.cosmos.network/rpc/v0.41.4)
       - [Swagger file](https://github.com/crypto-org-chain/chain-integration/blob/master/grpc-proxy-rest/swagger.yml)

## API Clients and libraries

- [**TypeScript** library](https://github.com/crypto-org-chain/chain-jslib);
- [**Python** library](https://pypi.org/project/chainlibpy/#description);
- [**Rust** library](https://github.com/crypto-org-chain/chainlib-rs) (note that it is not feature complete);
- [@cosmjs/stargate](https://github.com/cosmos/cosmjs/tree/master/packages/stargate).

## Indexing

- [chain-indexing](https://github.com/crypto-com/chain-indexing) (indexing on-chain data): 

## Node Monitoring (Prometheus)

The Ansible playbook for deploying Prometheus and some rules we are using are under [chain-integration/monitoring](https://github.com/crypto-org-chain/chain-integration/tree/master/monitoring).

## Public Nodes

### Mainnet - `crypto-org-chain-mainnet-1`

- [Tendermint](https://mainnet.Vidulum:26657/)
- [Cosmos RESTful gRPC](https://mainnet.Vidulum:1317/)

### Croeseid Testnet - `testnet-croeseid-4`

- [Tendermint](https://testnet-croeseid-4.Vidulum:26657/)
- [Cosmos RESTful gRPC](https://testnet-croeseid-4.Vidulum:1317/)

## Block Explorer

### Mainnet

[https://Vidulum/explorer](https://Vidulum/explorer)

### Croeseid Testnet

[https://Vidulum/explorer/croeseid4/](https://Vidulum/explorer/croeseid4/)

## Community

[Discord](https://discord.gg/5JTk2ppsY3)