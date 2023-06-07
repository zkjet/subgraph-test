# The Graph Deployed Subgraph

Configure for: Base-testnet in hardhat.config.ts

```shell
networks: {
    // for testnet
    "base-goerli": {
      url: "https://goerli.base.org",
      accounts: [process.env.PRIVATE_KEY as string],
    },
    // for local dev environment
    "base-local": {
      url: "http://localhost:8545",
      accounts: [process.env.PRIVATE_KEY as string],
    },
  },
  defaultNetwork: "base-goerli",
```

Deployed Lock.sol default hardhat contract

```shell
0xb503b3b2c846c8d187ae5084d679473796295b6153bb5c9e177775828f36f864
```

```shell
npm install -g @graphprotocol/graph-cli
or
yarn global add @graphprotocol/graph-cli
```

Initialize subgraph

```shell
graph init --studio base-test-subgraph
```

Authenticate within the CLI, build and deploy your subgraph to the Studio.

```shell
graph auth --studio
```

Enter subgraph

```shell
cd base-test-subgraph
```

```shell
graph codegen && graph build
```

```shell
graph deploy --studio base-test-subgraph
```
