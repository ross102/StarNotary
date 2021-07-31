# ND1309 C2 Ethereum Smart Contracts, Tokens and Dapps - Project Starter 
**PROJECT: Decentralized Star Notary Service Project** - For this project, you will create a DApp by adding functionality with your smart contract and deploy it on the public testnet.

### Steps to take
For this project, I took the following steps in other to run this project successfully:

### Dependencies
These are the dependencies you need to have to run this project
 and the version I used:
1. **Node and NPM** installed -  node version 14.7.1

2. **Truffle** installed - Truffle v5.3.14 (core: 5.3.14)

3. **open Zeppelin** installed - v 2.3.0
```bash
# Check Node version
node -v
# Check NPM version
npm -v
#check truffle version
truffle -v
```
You can browse through the package.json to see other dependencies.

### Step 1

The folders in this project are structured a bit differently. 
Please ensure you are in the correct directory before running the commands.

1. Cd into project-v2.Please ensure you are in the same 
   directory with the package.json file outside the v2 directory
   run npm install. 
2. cd into the app directory. When in the app directory  run npm install.

3. cd into v2 directory. That is the same directory with your contract folder.

4. When in the v2 directory, Start Truffle by running
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
```

3. Frontend - Once you are ready to start the frontend, run the following from the app folder:
```bash
cd into app directory
npm run dev

You should see the deployed frontend on localhost:8080
```
### Extras

1. My ERC721 name for this project is - `Golden star` and symbol - `GSN`

2. Contract address - 0xDB91471450F511F326859AFff8518686A4dB8306
3. Account - 0x5c2FC92a2cC1ECA29922D12ef84524eF5C044E56

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

## Troubleshoot
#### Error 1 
```
'webpack-dev-server' is not recognized as an internal or external command
```
**Solution:**
- Delete the node_modules folder, the one within the /app folder
- Execute `npm install` command from the /app folder

After a long install, everything will work just fine!


#### Error 2
```
ParserError: Source file requires different compiler version. 
Error: Truffle is currently using solc 0.5.16, but one or more of your contracts specify "pragma solidity >=0.X.X <0.X.X".
```
**Solution:** In such a case, ensure the following in `truffle-config.js`:
```js
// Configure your compilers  
compilers: {    
  solc: {      
    version: "0.5.16", // <- Use this        
    // docker: true,
    // ...


