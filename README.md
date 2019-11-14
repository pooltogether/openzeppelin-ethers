# OpenZeppelin Ethers Console

Provides an Ethers.js based console to interact with your contracts.

Fairly simple at the moment; does not use the OpenZeppelin SDK network configuration (yet!).

## Installation

```
npm install oz-console
```

## Usage

```
Usage: oz-console [options]

Provides an Ethers.js based console to interact with your OpenZeppelin SDK project.  Supports await syntax.  Includes global variables:
  
  artifacts: Every project contract discovered, including ProxyAdmin
  interfaces: An Ethers interface for each artifact discovered
  contracts: An Ethers contract for each *deployed* artifact.  Includes ProxyAdmin.
  provider: an ethers provider
  ethers: the ethers lib

Options:
  -n, --network <network name or JSON RPC URL>    selects network via ethers.getDefaultProvider(network) or uses the network as a JSON RPC URLs such as http://localhost:8545 (default: "mainnet")
  -c, --networkConfig <oz network config path>    set the network config path.  Defaults to the config corresponding to the network.
  -p, --projectConfig <oz project config path>    sets the project config path (default: "./.openzeppelin/project.json")
  -d, --directory <compiled artifacts directory>  sets the directory containing the compiled artifacts. (default: "./build/contracts")
  -v, --verbose                                   enable verbose logging.  useful for diagnosing errors
  -h, --help                                      shows this help
```