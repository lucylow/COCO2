# hedera-smart-contract-starter

This repository contains a nft smart contract starter project of Chain of Carbon optimization `COCO.sol` Below is the logic contract and instructions for deploying/upgrading it on the Hedera.


### Set up
1. Edit values for variables in `.env_sample` and save as `.env`

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat compile
npx hardhat test
npx hardhat run deployment/scripts/deploy.ts #Deploy logic and proxy contracts
npx hardhat run deployment/scripts/upgradeProxy.ts #Upgrade to new implementation
```

### Upgrade Flow
1. Deploy `COCO.sol` (v1 logic contract) and `TransparentUpgradeableProxy.sol` (proxy contract)
```
npx hardhat run deployment/scripts/deploy.ts
```

2. Update `COCO.sol` (v2 logic contract)

3. Upgrade deployment
```
npx hardhat run deployment/scripts/upgradeProxy.ts
```
