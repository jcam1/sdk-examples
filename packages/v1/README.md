# Code Examples for JPYC V1 SDK

We provide code examples that use JPYC V1 SDK as an interface to locally-deployed `JPYCv2` contracts. Please read and follow the instructions below to learn how to set up local environment as well as how to run our code examples.

> [!NOTE]
> Please run the following commands in `/packages/v1` directory.

### 1. Build Packages

The first thing to do is to build packages.

```sh
$ yarn run compile
```

### 2. Run Local Network

Start running local Hardhat network and its accompanying node.

```sh
$ yarn run node
```

### 3. Set Environment Variables

Run the following commands to generate `.env` file.

```sh
$ yarn run env
```

### 4. Deploy Contracts

**Open a different window** and run the following command to deploy JPYCv2 contracts to the local network. Once successfully deployed, a new directory will be created, and you can find deployed contract addresses at `/packages/v1/ignition/deployments/chain-31337/deployed_addresses.json`. Set `LOCAL_PROXY_ADDRESS` in the `.env` file to the value of `JPYCV2Module#FiatTokenV1` at [here](./ignition/deployments/chain-31337/deployed_addresses.json).

```sh
$ yarn run deploy
```

### 5. Run Code Examples

Finally, let's run our code examples!

|                       Command | Description                                             |
| ----------------------------: | :------------------------------------------------------ |
|                        `mint` | Example code: mint new tokens                           |
|                `total-supply` | Example code: get total-supply                          |
|                    `transfer` | Example code: transfer tokens                           |
|                     `approve` | Example code: approve allowance                         |
|                      `permit` | Example code: permit allowance (EIP2612)                |
|               `transfer-from` | Example code: transfer tokens from spender              |
| `transfer-with-authorization` | Example code: transfer tokens with signatures (EIP3009) |
|  `receive-with-authorization` | Example code: receive tokens with signatures (EIP3009)  |
|        `cancel-authorization` | Example code: cancel token authorization (EIP3009)      |

For example, to mint JPYC tokens on local network, run the following.

```sh
$ yarn run mint
```
