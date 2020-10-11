***cartel.finance***  
  
**Highlights**  
*-Compliant ERC-20 token following best practices. Uses Solidity version 6.9. No burn or rebase.*  
*-Total supply of 50,000. 1000 token airdrop to 49 most dedicated DeFi Crypto Cartel members (49,000).*  
*-Fully and evenly distributed airdrop. No ICO. No mint function. No lockup. No dev fund.*  
*-Contract address: *  
  
**To Do**
-Write script to deploy the contracts. Use truffle-flattener if it helps. 
-Use @nomiclabs/buidler-etherscan to try to have etherscan verify contract code.
-Learn/setup everything needed to fork the next cool token project
-Add logo to Uniswap  

  
**Roadmap (tentative)**  
-Bamboo Relay Exchange listing  
-Layer 2 Exchange listing  
  
**Setup:**  
1. `npm install`  (install dependencies)  
2. `npm install -g truffle` (install truffle globally)  
3. Install VS Code and install *juanblanco.solidity* extension using Solidity *version v0.6.9+commit.3e3065ac.js* https://ethereum.stackexchange.com/a/63102/28140  
     
**Local Setup:**  
1. Install Ganache (https://www.trufflesuite.com/ganache) and setup environment at 127.0.0.1 port 7545  
2. `truggle migrate`  (deploy contracts)
3. `truffle console`  (console to run commands. Try these commands using CryptoCartel instead of MetaCoin https://www.trufflesuite.com/docs/truffle/quickstart#interacting-with-the-contract)  
  
**Ropsten/Kovan/Live Testnet Setup:**  
1. Create secrets.json in this directory:  
```javascript
{  
    "mnemonic":"MNEMONIC PRIVATE KEY HERE"  
    "infuraApiKey":"INFURA API KEY"
    "pk":"OPTIONAL PRIVATE KEY USED FOR BUIDLER"
    "etherscanApiKey": "OPTIONAL VERIFY CONTRACT TO ETHERSCAN" 
}  
```
2. `truffle migrate --network ropsten`  
3. `truffle console --network ropsten`  
  

**Call contract to send tokens**
1. `truffle console --network ropsten`
2. let instance = await CartelFinance.deployed()
3. instance.transfer("<YOURADDRESS>", 500000000)