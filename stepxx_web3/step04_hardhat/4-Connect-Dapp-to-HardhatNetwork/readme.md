## Connecting a wallet or Dapp to Hardhat Network

By default, Hardhat will spin up a new in-memory instance of Hardhat Network on startup. It's also possible to run Hardhat Network in a standalone fashion so that external clients can connect to it. This could be a wallet, your Dapp front-end, or a script.

To run Hardhat Network in this way, run npx hardhat node:

**$ npx hardhat node**

Started HTTP and WebSocket JSON-RPC server at http://127.0.0.1:8545/

This will expose a JSON-RPC interface to Hardhat Network. To use it, connect your wallet or application to http://127.0.0.1:8545.

If you want to connect Hardhat to this node, for example, to run a deployment script against it, you simply need to run it using --network localhost.

To try this, start a node with npx hardhat node and re-run the deployment script using the network option:

**npx hardhat run scripts/deploy.ts --network localhost**

Congrats! You have created a project and compiled, tested, and deployed a smart contract.