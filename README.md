# gasCosts-AA : Gas costs for Biconomy AA Modules : ETH/POLY/BNB

## This branch is for userOps without Paymaster data
## For other variations, see other branches

Using Foundry's Fork Testing Environment to get gas snapshot report for transactions using Biconomy AA Ownerless Module </br>
Test Cases to Cover by forking ETH-Mainnet : </br>
- [ ] Write tests for ETH Mainnet using Paymaster in separate branch
- [ ] Write tests for Polygon POS using Paymaster in separate branch
- [ ] Replicate ECDSA/Paymaster without paymaster for BNB Chain in this branch
- [ ] Restructure README to showcase GasCosts according to what the branch specifies
- [ ] Write gas costs in this branch chain-wise
- [X] Replicate ECDSA/Paymaster without paymaster for Polygon Mainnet
- [X] DAI Transfer :: `ECDSA : 160981,182882` `SA Ownership : 177790,199690`
- [ ] Native ETH Transfer
- [X] Wallet Deployment
- [X] NFT Transfer :: `ECDSA : 157366,181766` `SA Ownership : 174175,198575`
- [X] NFT Mint ::  `ECDSA : 178708,214608` `SA Ownership : 195513,231413`
- [X] Uniswap Swap :: `ECDSA : 301008` `SA Ownership : 317908`
- [X] Do all with SAOwnershipAuthModule
- [ ] AAVE deposit Collateral
- [ ] Uniswap V3 Mint Position
- [ ] Lido Finance Deposit Ether


</br>
Gas report generated by `forge test` is inflated as it also accounts for gas associated with constructing the userOp. </br>
Value of `gasleft()` is cached before sending the UserOp to EntryPoint and used just after the operation and consoled logged out. </br>

Run the following commands : </br>

```
forge install
forge test -vv
```
