# Branch Blockchain 🟩

Repository for the blockchain branch content. 

## Content 👀
Those subjects are progressive in difficulty, designed to learn the fundamental of blockchains as well as the main technologies and tools used in the industry.

### Transactions Quest

*Sometimes science is more art than science. - Rick Sanchez*

Welcome and congratulations for choosing to learn blockchains and cryptocurrencies. 

Today we get a first experience in the most core element, transactions. We will use the actual Bitcoin software to create transactions and send them. We will learn to interact with command lines, APIs and wallets to move cryptocurrencies around.

Most open blockchains offer three categories of networks:
- The main network `mainnet` on which value is transacted
- One or several `testnet`, that work more or less similarly to the mainnet with no value
- Local networks, to test locally with a node. It is called `regtest` on Bitcoin. 

*🚨 Caution 🚨*
You should not use any crypto with value for any exercise of the module. If you already own crypto, we recommend that you use a new separate wallet to avoid any loss of funds. We will never use the main network of any blockchain `mainnet`.

#### Mandatory

1. [sendTransaction](sendTransaction/README.md) _Send a Bitcoin transaction_
2. [retrieveBlockDate](retrieveBlockDate/README.md) _get a block date_
3. [retrieveTransactionValue](retrieveTransactionValue/README.md) _get the value of a transaction_
4. [sendTransactionToPeer](sendTransactionToPeer/README.md) _send a bitcoin transaction to a peer
5. [sendEthTransaction](sendEthTransaction/README.md) _Send a transaction to an address on a testnet_

#### Optional

6. [retrieveTransactionInOut](retrieveTransactionInOut/README.md) _get inputs and outputs from a transaction_






### Crypto Quest

*When in doubt, use brute force. - Ken Thompson*

Today , we will learn the fundamentals of cryptography that underlies all blockchain projects. We will practice binary variables, hash functions and digital signatures. By the end of the quest, you should be able to create a basic wallet to generate keys, store them and sign transaction.

Buffers are a builtin type in nodejs used to represent binary objects. You create a buffer from any object by using the function `Buffer.from()`. As usual in JavaScript there are a lot of implicit conversions. Be aware for instance that a string representing a number is different from the actual number.

For cryptography, you may have heard how it is used the encryption and decryption of messages. While this is often true, in the blockchain and cryptoassets industries this is not how we will primarily use it. The two families of algorithms we will see are:

**Cryptographic hash** functions are algorithms that take as input any data and produce an unique fingerprint of this data. Those functions are meant to be fast, one way, deterministic.

**Digital signatures** allow to identify the author of a message. It relies on asymmetric cryptography. You first generate randomly a key pair with a public key and a private key. The public key is shared publicly. The private key will allow you to sign a message. More precisely the hash of this message. The public key will allow anyone to verify that this message was properly signed.

From a practical point of view, for today, you only need the builtin library `crypto`.

#### Mandatory

1. [Increment](increment/README.md) _Binary variables in nodejs_
2. [hashFile](hashFile/README.md) _Hash functions, file read in nodejs_
3. [hash160](hash160/README.md) _Hash functions, double hash, sha256, Ripemd160_
4. [semiBrute](semiBrute/README.md) _Hash bruteforce_
5. [signer](signer/README.md) _ECDSA_

#### Optional

6. [generateAddress](generateAddress/README.md) _Key generation, Crypto address_
7. [basicWallet](basicWallet/README.md) _Key storage, transaction signature_

#### Integration:

Launch tests with

```sh
node test.mjs <exercices>
```





### Festival Smart Contract Quest

*We didn't take the Bastille to make an opera out of it! - 
Pierre Desproges*

Today we will build our first Smart Contracts. Smart Contracts are programs deployed on a blockchain network to provide additional functionalities. In the context of this quest, we will focus on Ethereum Smart Contracts. There main development language is Solidity.

We will create step by step the functionalities of a Smart Contract. The festival consists of information that will be stored in the smart contract such as a name, a lineup of artists, a date and the Smart Contract will provide the minimal capabilities of buying tickets and share benefits.

Each exercise requires a distinct Smart Contract.

#### Mandatory

1. [NamedFestival](NamedFestival.md)
2. [TimeAndPlace](TimeAndPlace.md)
3. [Lineup](Lineup.md)
4. [OrganizedFestival](OrganizedFestival.md)
5. [BuyTickets](BuyTickets.md)
6. [FunAndProfit](FunAndProfit.md)

#### Optional

7. [ArtistsDoWork](ArtistsDoWork.md)
8. [TimeIsMoney](TimeIsMoney.md)

#### Integration

In this Quest, tests can be run with:

```bash
npm i
npx hardhat test
```
Individual tests can be run with 
```bash
npx hardhat test tests/<exercise>.test.js
```





### Anchoring

A simple use of blockhains is to anchor documents. We will hash documents and store them in a blockchain. 

For this, we will use a local test node and interact with it using JavaScript

#### Mandatory
1. [localNode](localNode.md)
2. [getAccount](getAccount.md)
3. [sendEther](sendEther.md)
4. [sendHash](sendHash.md)
5. [checkDocument](checkDocument.md)
7. [register](register.md)


Keep for later
8. [registerWithEvents](registerWithEvents.md)


#### Integration
In this Quest, tests can be run with
```sh
npm i 
npx hardhat node&
npx mocha sendHash.test.js
```






### Connect Interface

*Any problem in computer science can be solved with another layer of indirection. But that usually will create another problem. - David Wheeler* 

Today we will learn how to create basic interfaces. All those exercises consist in a single HTML page with Javascript. You will need an Ethereum JavaScript Library, ethers.js and web3.js should be suitable. 

#### Mandatory

1. [localNodeInfo](localNodeInfo/README.md)
2. [Random wallet](randomWallet/README.md)
3. [Donation](donation/README.md)
4. [Connect to MetaMask](connectToMetaMask/README.md)
5. [Tip](tip/README.md)

#### Optional
6. [Read a Secret](readSecret/README.md)


#### Integration

In this Quest, tests can be run with
```sh
npm i 
npx hardhat node
npx mocha <exercice>.test.js
```






### Simple Tokens

*Listen, I'm not the nicest guy in the universe because I'm the smartest. And being nice is something stupid people do to hedge their bets. - Rick Sanchez*

On of the key factors of blockchain success over the past years has been the creation of standards. Those token standards allow interoperability and composability of smart contracts. 

Today, We will start by creating a Minimal Token that provides the basic functionalities of a token. From this, we will build basic services using this token. This will allow us to learn more advanced functionalities of Smart Contracts. 

#### Mandatory
1. [Minimal Token](minimalToken/README.md)
2. [Token Sale](tokenSale/README.md)
3. [Usable token](usableToken/README.md)
4. [Basic Swap](basicSwap/README.md)
#### Optional
5. [Eventful token](eventfulToken/README.md)
6. [Transfers History](transfersHistory/README.md)


#### Integration
In this Quest, tests can be run with
```sh
npm i 
npx hardhat test tests/<exercice>.test.js
```









### Non Fungible Cats

Today's quest objective is to master Non Fungible Tokens, NFTs. 

To represent a simple token, we used a smart contract with with each blockchain address amount of tokens. We talk about fungible token because each token has the same value. A Non-Fungible Token is a token with a unique identifier, usually part of a collection. NFTs are used to represent playing cards, works of art, financial securities and even physical objects. 


Internally fungible token that we have seen in the prior quest are represented with a mapping from addresses to an amount: 

    Address    ---> Amount
    0x2FE34         20

Non-Fungible Tokens are represented with a mapping of unique identifiers to an owner

    Identifier ---> Address
    123455          0x2FE34

In addition, each token is linked to an Uniform Resource Identifier (URI) where additional information about the NFT can be found, such as metadata, an image... 

    Identifier ---> Address
    123455          0x2FE34
               ---> URI
                    bafkreiajlq3

#### Mandatory
1. [Napping cats ](nappingCats/README.md)
2. [Showcase](showcase/README.md)
#### Optional
3. [Automated reveal](automatedReveal/README.md)










### Decentralized Finance


*I accidentally killed it - devops199*

It is time for us to advance beyond basic contracts for integrate with actual DeFi smart contrat. For this we will need to use current standards and implementations. 

First, we will create a simple stablecoin, following the ERC20 standart and an oracle. We will then create a decentralised exchange that will allow us to exchange our stablecoin. Finally, we will create the tests for this project. 

#### Content
1. [stablecoin](stablecoin/README.md)
2. [Lending Platform](lendingPlatform/README.md)
3. [Test and coverage](testsAndCoverage/README.md)

#### Integration
-> Audited









#### Exploring blockchains.

*If you don't believe it or don't get it, I don't have the time to try to convince you, sorry. — Satoshi Nakamoto*


While we have focused on fundamentals and the two main public blockchains, other alternatives and projects have been build over the years. I can only recommend you to try and test various alternatives. Most reuse the same principles that we have seen in the previous quests.

In this course, we will focus on two solutions provided by the Hyperledger project. The Hyperledger project is an umbrella that regroup vastly different technical solution. The solutions we will explore are both lego sets that allow you to create varied projects

#### Content
2. [Private network](privateNetwork/README.md)
1. [Command line wallet](clillet/README.md)

#### Integration
-> Audited




- Quest 1: Experiment basic Bitcoin transactions
- Quest 2: Learn fundamental cryptography 
- Quest 3: Create a complete Smart Contract
- Quest 4: Scripted interactions with the Ethereum blockchain
- Quest 5: Create a complete decentralised application
- Raid 1: Create a signing service
- Quest 6: Create a first token
- Quest 7: An NFT based DApp
- Quest 8: Learn the basics of DeFi and security
- Quest 9: Explore other blockchains
- Raid 1: Create a tracking service

## Tests ⚙️
Within the `tests/` folder, `runTests.sh` builds a docker image and run a series of sample tests. Solutions are expected to be in the `tests/student` folder.
```shell
./runTests.sh
```

It is also possible to run tests individually:
```shell
./runTests.sh retrieveBlockDate 
```

### Advanced commands
Advanced commands are available in the `tests/` folder:

**Build the docker image**
```shell
docker build . -t blockchain 
```

**Run an example BTC test**
```shell
docker run --read-only --network none --memory 500M --user 1000:1000 -e DEBUG=true -e EXERCISE=retrieveBlockDate --env HOME=/jail --env TMPDIR=/jail --workdir /jail --tmpfs /jail:size=100M,noatime,exec,nodev,nosuid,uid=1000,gid=1000,nr_inodes=5k,mode=1700 --volume /home/$USER/code/01Branch-Blockchain/tests/student:/jail/student:ro blockchain:latest
```
**Explore the docker image**
```shell
docker run -it --entrypoint /bin/bash blockchain:latest
```

## Authors ✍️
Xavier Lavayssière - [🐙](https://github.com/Xalava) [🐦](https://twitter.com/Xalava)