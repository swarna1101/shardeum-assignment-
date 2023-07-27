## Shardeum Test Task


<img width="1432" alt="Yugen Dapp" src="https://www.redwolf.in/image/cache/catalog/marketplace/shardeum/shardeum-official-merchandise-banner-1920-1920x350.png">



- All the scripts and solutions are part of the [scripts](https://github.com/swarna1101/shardeum-assignment/main/scripts) folder.
- Every problem statement has a **.js** file which contains the solution for the problem along with the detailed comments and logs.
- Every problem statement also has a **.approach** file which contains detailed explanation on the thought process, some notes and explorer links the deployed contracts and their transactions.
- Some problem statement also contains some additonal files and the details for these have been covered in the notes.


### Steps to setup this project.

- Clone Project Codebase

```
git clone https://github.com/swarna1101/shardeum-assignment.git
```

- Create a .env file in root folder and paste the following

```
PRIVATE_KEY=ENTER_YOUR_PRIVATE_KEY
POLYGON_RPC_URL=https://dapps.shardeum.org
```

Update PRIVATE_KEY with private key of the wallet to be used for the flow.
It should have enough SHM on Shardeum Sphinx Dapp 1.X

- Install dependencies

```
yarn
```

- Compile

```
yarn run compile
```

- Generate gas report (For problem 3)

```
yarn run test
```


### Instructions to run/test the flow

1. Problem Statement 1

```
yarn run question1
```

- [Script](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question1.js)
- [Approach, Notes and Deployed contracts](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question1.approach)

2. Problem Statement 2

```
yarn run question2
```

- [Script](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question2.js)
- [Approach and Deployed contracts](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question2.approach)
- [Deployed contract and files generated by Openzeppelin upgrades plugin for Shardeum and Mumbai network](https://github.com/swarna1101/shardeum-assignment/tree/main/.openzeppelin)


3. Problem Statement 3

```
yarn run question3
```

- [Script](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question3.js)
- [Approach and Deployed contracts](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/question3.approach)
  [Gas Report](https://github.com/swarna1101/shardeum-assignment/blob/main/scripts/gas_report.txt)



#### Notes
The project and the deployed contracts are done without anything missing in the requirements but there were some recursive errors which occured when some of the contracts get deployed.

-  `Error: invalid value for value.gasLimit`
- `HeadersTimeoutError: Headers Timeout Error`
- `ProviderError: Node not ready for inject, waiting for network account data.`
- `TypeError: Cannot read properties of null (reading 'baseFeePerGas')`

This is not predictable, harder to recreate and has also been mentioned on a support channel on discord.
During deployment all these scripts did not face this issue for the first time. Solving of these errors required manual intervention in scripts and also occasions where Hardhat Web3 was used instead of Hardhat EthersJS, deployer account was changed and sometimes just plain waiting. All this can also be referred inside the approach files for every problem.

