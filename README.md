# Decentralized Star Notary Service Project
A Simple Star notary Service DApp deployed on the public Rinkeby testnet.

## Development framework
Below are the versions used for developing and testing
```
Truffle v5.5.3 (core: 5.5.3)
Ganache v7.0.1
Solidity v0.5.16 (solc-js)
Node v17.6.0
Web3.js v1.5.3
openzeppelin-solidity 2.3
truffle-hdwallet-provider ^1.0.17
```

## Token Details
ERC-721 Token Name - Lynx
ERC-721 Token Symbol - LYN
Token Address on the Rinkeby Network - https://rinkeby.etherscan.io/address/0x53f7e7c218dde7b1ded43c401096460129e03e05

## Dependencies
For this project, you will need to have:
1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version
node -v
# Check NPM version
npm -v
```
2. **Metamask: 5.3.1** - If you need to update Metamask just delete your Metamask extension and install it again.
3. [Ganache](https://www.trufflesuite.com/ganache) - Make sure that your Ganache and Truffle configuration file have the same port.
4. **Other mandatory packages**:
```bash
cd app
# install packages
npm install --save  openzeppelin-solidity@2.3
npm install --save  truffle-hdwallet-provider@1.0.17
npm install webpack-dev-server -g
npm install web3
```

### Run the application
1. Clean the frontend 
```bash
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
```


2. Start Truffle by running
```bash
# For starting the development console
truffle develop
# truffle console

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test

# to deploy to Rinkeby testnet
truffle migrate --reset --network rinkeby
```

3. Frontend - Once you are ready to start your frontend, run the following from the app folder:
```bash
cd app
npm run dev
```

---

### Important
When you will add a new Rinkeyby Test Network in your Metamask client, you will have to provide:

| Network Name | New RPC URL | Chain ID |
|---|---|---|
|Private Network 1|`http://127.0.0.1:9545/`|1337 |

The chain ID above can be fetched by:
```bash
cd app
node index.js
```
