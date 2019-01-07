# {#whitepaper}

<center>
  <h1>Matic Whitepaper</h1>
</center>

<center>
  [Whitepaper Version 1.1]<br><br>
  Jaynti Kanani <<a href='mailto:jdkanani@matic.network'>jdkanani@matic.network</a>><br>
  Sandeep Nailwal <<a href='mailto:sandeep@matic.network'>sandeep@matic.network</a>><br>
  Anurag Arjun <<a href='mailto:anurag@matic.network'>anurag@matic.network</a>><br>
</center>

# {#Abstract}
<center>
  <h3>Abstract</h3>
</center>

<div style="text-align: justify; max-width: 600px; margin: 0 auto;">
Smart contract platforms and cryptocurrencies have captured mass attention but still have not been able to achieve mass adoption due to scalability and user experience issues. Even on Ethereum, which is the most widely used smart contracts platform, there have not been many examples of DApps which have seen mass adoption. There have been a few cases where one or the other particular application temporarily succeeded in achieving a significant user base, but it led to crippling of the entire network during the high network load times. Essentially this means that even the most advanced and widely used platforms are not ready for mass adoption yet.
<br/><br/>
On the other hand, there are a few smart contract platforms which boast of higher transaction throughput, but they compromise on decentralization in order to improve transaction speeds. Also, many of the upcoming solutions propose developing their own blockchains, neglecting the billions of dollars of market cap that DApps and other projects have already created on platforms like Ethereum and others. More importantly, they neglect the massive developer community and developer ecosystem that currently exists on platforms like Ethereum.
<br/><br/>
<b>Matic Network strives to solve the scalability and usability issues, while not compromising on decentralization and leveraging the existing developer community and ecosystem. It is an ​off/side chain scaling solution for existing platforms to provide scalability and superior user experience to DApps/user functionalities.</b>
<br/><br/>
<b>The Matic development team has chosen Ethereum as the first platform to showcase its scalability and already has a working implementation for Ethereum on Kovan Testnet.</b> It is expected to allow near-instant transfers, exchange and conversion of digital assets (e.g. crypto tokens) and cryptocurrencies in the future. The Matic Network is an adapted implementation of the Plasma framework for Ethereum to start with, but the “vision” of the Matic development team is to provide off/side chain scaling solutions for blockchains in general. Matic foundation intends to provide Matic wallet, payment APIs & SDKs, products, identity solutions and other enabling solutions that will allow developers to design, implement and migrate DApps built on base platforms like Ethereum. One of the key pillars that form the basis of Matic Network’s ideology is the improvement of user experience, this area is poorly developed for Blockchain applications as of now. The Matic Development team has already built high quality user experience Mobile/Web browser libraries which will enable businesses to create real world end user applications on a large scale. The development roadmap of the Matic Network also includes supporting cross-chain transfers and third-party Decentralized exchanges, liquidity pools etc.
</div>

# Why Matic? {#whymatic}

Decentralized Apps are being proposed in large numbers, but the current blockchain ecosystem is not prepared to scale to match the demands of end user applications with mass adoption. Moreover the user experience of DApps is very poor and in no way conducive for average users. Slow block confirmations, high transaction fees, low scalability and poor user experience are some of the key roadblocks for the mass adoption of blockchain applications. The following section explains the problems prevailing in the current blockchain ecosystem and how the Matic Network intends to solve them. **Detailed technical specification are provided in the further sections of the white paper.**

### Slow Transactions {#slowt}

Blockchain transactions are typically very slow and have a very limited throughput. Most PoW ([Proof-of-Work](https://en.wikipedia.org/wiki/Proof-of-work_system)) based blockchain protocols have a limit on the block size and it takes a certain amount of time to generate a block. Each transaction also has to wait for multiple block confirmations due to potential chain re-organizations.<br/>

PoS ([Proof-of-Stake](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQs#what-is-proof-of-stake)) based blockchains try to counter these limitations using a staking mechanism, but the blockchains that are able to achieve high throughput with PoS are able to do so at the cost of decentralization. These limitations are often a necessary condition for public blockchains to ensure security and decentralization where a block needs to be propagated through the network and validated by all the nodes to achieve finality.<br/>

The Matic Network solves this problem by using a high throughput blockchain with consensus provided by a selected set of delegates, chosen for every checkpoint by a set of Stakers. It then uses a Proof Of Stake layer to **validate the blocks and publish periodic proofs (merkle roots) of the blocks produced by the Block Producers to the Ethereum mainchain. This helps in achieving high level of decentralization while maintaining an extremely fast (< 2 seconds) block confirmation times.**


### Low Transaction Throughput {#ltt}

Public blockchains have to maintain a certain amount of time lag between the production of adjacent blocks so as to ensure ample time for block propagation. Also, the block size needs to be small so as to ensure quick propagation of the block through the network. This entails that the number of transactions in a particular block need to be fairly limited.<br />

The Matic Network solves this problem by using a **Delegate layer from its DPos system to produce the blocks.** Delegates enable the system to produce blocks at a very fast rate. The system ensures decentralization using PoS checkpoints which are pushed to the Mainchain (Ethereum serves as the mainchain for a start).**This enables The Matic Network to theoretically achieve up to $$2^{16}$$  transactions per second on a single side chain.**

### Scalability {#scalability}

As discussed in the previous section, The Matic Network easily achieves a theoretical speed of up to $$2^{16}$$ transactions per second on a single side chain. **In future, The Matic Network is expected to be able to easily add more side chains horizontally to increase the total number of transactions on the Matic Chain while using the same decentralized PoS layer.**

Theoretically the Matic Network has the capacity for millions of transactions per second with the usage of multiple side chains. Also, the mechanism to do so has already been demonstrated with the first Matic proof-of-concept with the first Matic side-chain and new chains can be added in due course of time.

### Size of Blockchain {#sob}

Each block on the blockchain and/or compute state in case of a smart contract based blockchain must be validated by multiple nodes. Each node has to manage a copy of the state and the blocks. While the chain increases in size as the days go by, maintaining and validating the whole blockchain becomes difficult and resuls in fewer full nodes in public blockchains, which poses a risk for decentralization.<br/>

For the Matic Network, the primary layer which provides decentralization may choose to store only the blocks of Matic Chain from the previous checkpoint to the next checkpoint. All previous transaction/block proofs have been submitted to the mainchain. **This enables extremely low fidelity PoS nodes which can be run in very low-cost machines with low storage. In future, The Matic Network intends to enable mobile device based PoS miners too.**

### Multiple micropayment channels with other off-chain solutions {#loooong}

Some payment channel solutions have proposed solutions to solve the problem of micro-payments. However, the process of opening and managing channels with multiple DApps or users is complex. Additionally, the speed and convenience of mediated payments over channels is still up for debate.

Since **The Matic Network uses a state-based architecture on an EVM (Ethereum Virtual Machine), it does not require payment channels to be opened between two parties. In fact, any valid Ethereum address is a valid Matic Address and a receiver does not need to be on the Matic chain to receive payment. They would only need to have a Matic Wallet when they want to retrieve the payments on the main chain or spend it in the ecosystem on the Matic Network.**

### High Transaction Fees {#htf}

With the rapid growth of the blockchain ecosystem, new crypto assets are increasingly being created, transferred, and sold, often involving multiple crypto tokens. Also, most decentralized apps have their own token and economy. Paying tokens for the services or doing any kind of transaction on blockchains requires on-chain transfers. Every blockchain has a transaction cost structure. For example, Ethereum charges gas fees on each transaction.

The amount of fees is an important factor to incentivize validators and prevent certain kinds of security attacks such as DoS. However, there is the problem of variation of fees (Depending upon the pending transaction pool) due to the limited block size.

**The Matic Network enables low cost transactions through achieving economies of scale by doing a large number of transactions on the Delegate layer which ensures low cost, and then subsequently batching the proofs of the Matic blocks using the Merkle root of the blocks** to a highly decentralized mainchain (for ex. Ethereum) using a decentralized layer of PoS Stakers.

### Poor Usability {#pf}

User interactions on DApps are often poor compared to their centralized counterparts. For the Decentralization revolution to achieve mass adoption, the user experience of DApps has to be on par with, if not better than, their centralized counterparts.

The Matic Development team is expected to work on various Mobile and Web browser integration tools and is pioneering protocols in this domain. It intends to build a ubiquitous mobile/browser app, which will act as a secured interaction layer for blockchain interactions. The Matic Development team will be publishing the designs and prototypes of these soon.


# Introducing the Matic Network {#imn}

As discussed in brief in the section above, the Matic Network aims to solve the problems faced by the blockchain ecosystem through building a decentralized platform using an adapted version of [Plasma](https://plasma.io/) framework. This provides for fast and extremely low cost transactions with finality on a mainchain. The current working Testnet and alpha-Mainnet of the Matic Network works with Ethereum as a mainchain. <br/>

The Matic Development team is also building a product ecosystem including user friendly mobile apps, desktop wallets and browser extensions which will provide a seamless experience for all users. It is envisaged that users will be able to pay, transfer or hold crypto assets without worrying about the complexity of the underlying system.

# Architecture {#architecture}

Since the Matic Network's core focus is on mass user adoption, it is ideal that a deep dive into the Matic Network's technical architecture should start from a user journey.

When a user is transferring ETH or ERC20 tokens on the Ethereum network, they have to wait for the confirmation of the block which ranges from 14 seconds to 20 seconds. Even then the users have to wait for multiple block confirmations to be sure of the finality of the transaction. Let’s say you are buying a coffee or paying tokens to watch a movie. On each transaction you are not only paying a high fee, but also waiting for it to be confirmed. That serves as a deterrent for users wanting to use the service.

Moreover, during peak loads, a large number of transactions clog the Ethereum network and gas fees increase on each transaction in order to obtain faster confirmations. The Matic Network is proposed as a solution to overcome these problems.

Here is how the Matic Network will function: <br/>

1. A user deposits a cryptographic asset in the Matic contract on the mainchain (currently implemented with Ethereum blockchain only).
2. Once deposited, tokens get confirmed on the main chain, tokens will appear on the Matic Chain using Matic Deposit bridge (technical details explained in a dedicated section below).
3. The user can now transfer tokens to anyone they want almost instantly (Matic Chain has faster blocks - approximately 1 second or less) for almost negligible fees.
4. Whenever the user wishes to, they can withdraw tokens to the main Ethereum chain by establishing proof of remaining tokens on Root contract (contract deployed on Ethereum chain).

The same method will work for any ERC-20 token or other fungible crypto assets on the Ethereum blockchain.
The Matic Development Team has already created a demo version, available at: https://github.com/maticnetwork/contracts

We expect the alpha version of the mainnet to go live very soon.

## Actors {#actors}

The ecosystem of The Matic Network will have the following actors :

1. End Users
2. DApp developers : Developers are expected to use The Matic Network to scale their applications and provide a better UI/UX to their end users
3. Stakers : Stakers will play a very important role in the Matic Network. They validate the transactions and propose checkpoints on the mainchain using PoS consensus mechanism with a ⅔ majority. They also choose Delegates amongst themselves, who satisfy a certain criteria, to act as block producers.
4. Delegates : These are block producers chosen by Stakers who in turn enable faster blockchain generation times. They have to provide a stake to be nominated as delegates.

## Consensus {#con}

The Matic Network uses a dual strategy of Proof of Stake at the checkpointing layer and Delegates at the block producer layer to achieve faster blocktimes while ensuring a **high degree of decentralization by achieving finality on the main chains using the checkpoints and fraud proof mechanisms.**

![Matic checkpoints](matics.png)

Through this mechanism, The Matic Network achieves high transcation speed with a high degree of decentralization and finality on Mainchain. In the first version which has Ethereum only as the base chain, Ethereum root contract enforces solvency and finality through header block(checkpoints) very efficiently. The various elements and mechanisms of the system are described below:

## Checkpointing Layer {#checklayer}

Basically, anyone can stake their Matic Tokens on root contract to become a Staker in the PoS checkpointing layer (contract deployed on Ethereum chain). This provides a highly decentralized base layer for Matic Chain.

## Delegates

At the blockchain layer of the Matic Network, there are Delegates selected by PoS Stakers on the base layer with Proof of Solvency who will be creating the Matic Blocks. To achieve faster block generation times, these Delegates will be low in number. **This layer is expected to achieve ~1 second block generation times at extremely low to negligible transaction fees.**

## Checkpointing Mechanism

On Matic Network’s checkpointing layer, the basis of Matic Network's PoS mechanism, for every few blocks on the block layer of the Matic Network, a proposer will be chosen among the stakeholders to propose a checkpoint on the main chain. These checkpoints are created by the proposer after validating all the blocks on the block layer of the Matic Network and creating the Merkle tree of the block hashes since the last checkpoint. The Merkle root is then broadcasted to the Staker network for their signatures. The other stakeholders also verify the proof. They will approve the proposed block, if it is valid, by providing their signatures.

The system needs the approval of ⅔ of the stakeholders to propose a “header block” to the root contract. Once the checkpoint is proposed on the mainchain, anyone on the Ethereum mainchain can challenge the proposed checkpoint within a specified period of time. If no one challenges it and the challenge period ends, the checkpoint is formally included as a valid checkpoint on the main chain.

Apart from providing finality on the mainchain, Checkpoints have a very important role to play in withdrawals as they contain the proof-of-burn (withdrawal) of tokens in the event of user withdrawal. It enables the users to prove their remaining tokens on root contract using Patricia Merkle proof and header block proof. Note that to prove remaining tokens, the header block must be committed to the Root Chain through PoS (Stakeholders). The withdrawal process will incur Ethereum gas fees as usual.

Through this mechanism, The Matic Network achieves a high transaction speed, a high degree of decentralization and finality on Mainchain. In its first version which has Ethereum as the base chain, the Ethereum root contract enforces solvency and finality through header blocks (checkpoints) very efficiently.

## Delegate Selection

Delegates are chosen by Stakers in the checkpointing layer through voting on the mainchain. A Delegate is selected for a pre-determined interval of time until slashed/removed by the network consensus mechanism or if it is unable to participate in the block production due to any external issue.

### Seeding of the network
```
1. Matic Network will ask for applications from the public to run the Delegate nodes
2. It will also run 3 Block Producer nodes itself during the seed stage of the network
3. At the epoch, the public stakers will select a total of 5-7 block producer nodes
4. These nodes will be kickstarted with a Matic Chain N(number of) genesis configuration
```

### Delegate application process
```
1. The Delegates have to apply by staking the Delegate Stake requirement amount in Matic Tokens on the mainchain
2. Delegates need to demonstrate a Proof of Computing Capacity
3. The Network will maintain a pool of interested Delegates (An incentive system for the Delegate nominees would be devised to keep ample number of Delegates in the pipeline)

Criteria on the basis on which Stakers will decide to vote for a particular nominee Delegate are as follows:

- Uptime history
- Technical specifications
- Dynamic scaling capability
- Location diversity
- Other factors under consideration (e.g. [Zcash Board Nominations](https://github.com/ZcashFoundation/Elections/blob/master/2018-Q2/Board-Nominations/Sokolov_selfnomination.md) )
```

### Selection through Voting at tenure completion
```
1. Voting process is scheduled and completed one week before the completion of one tenure
2. Existing Delegates can re-appear in the elections
3. Stakers vote for Delegates from the pool of Nominees
```

### Replacement of a Delegate during the ongoing tenure

In an event of untimely removal/incapability of a Delegate to take part in block production, a new Delegate from the transient pool will be recruited. An appropriate incentive mechanism to have a prioritized/preferred list of Delegates as per the stakers' vote will be devised to maintain a healthy pool of Delegates.

## Multi Chain Support (Horizontal Sharding) {#multichain}

The Matic Network public checkpointing layer supports multiple side chains by design. Theoretically there can be an infinite number of side chains working under the secured and decentralized layer of checkpoints. Businesses can have their dedicated side chains connected to the public checkpointing layer having full control of their execution environments, while still retaining the immutability, provability and security of transactions via the checkpointing mechanism.

Key factors influencing design of this sharding process are expected to be:
1. Scheduling of checkpointing layer to periodically propose checkpoints for different side chains
2. Movement of assets across multiple side chains
   2.1 User will be able to send assets across side chains using chain ids and receipts
   2.2 Users will be provided with an intuitive wallet interface to perform inter-chain transactions
   2.3 Developers will be provided with API/SDKs to build programmable interfaces for inter-chain transactions
3. Movement of the assets from one chain to another will be managed at the checkpointing layer and may not require any interaction with the mainchain. Research is currently underway to facilitate faster (possibly instant) inter sidechain transfers.

## Interoperability {#interoper}

As mentioned earlier in the whitepaper, the Ethereum mainchain is the first base/mainchain that Matic Network securely integrates with, using an adapted implementation of the Plasma framework. In addition, the Matic network intends to integrate multiple leading smart contract platforms cryptocurrencies such as Bitcoin and others to provide an universal platform for the users to be able to use/exchange their assets from various blockchains.

It can also provide a strong foundation for large DEXs (Decentralized exchanges) hosting assets from multiple blockchains. Also having a single platform with assets from multiple blockchains can also give rise to dramatically new use-cases, which the developer ecosystems can conceptualize their future products on. It is an exciting area of exploration for the Matic Development team.

Judging from the proliferation of Layer 1 blockchains, it is a given that there might be more than 2-3 public blockchains that will be adopted by the mainstream eventually, rather than only a single winning blockchain platform. Therefore, the Matic Development Team expects to see hitherto unseen use-cases, arising from the Decentralized application movement across these blockchains. The vision of the Matic Development Team is to provide infrastructure and interfaces such that anyone who wishes to build decentralized applications on any blockchain, will be able to do it easily - and communicate and transfer value across multiple blockchains.

## Generalized State Scaling {#genscaling}

Generalized State scaling is the next frontier for the Matic Network, once the Matic Development Team is done with implementing micropayments, asset transfers and swaps in the first phase of development of the Matic Network. The team is working along side leading partner firms to solve this problem as well. This is a research problem, and it will take time and effort to accomplish a breakthrough here. However, one of the approaches that the team has been following is very promising.

One of the main approaches that the Matic Development Team have taken involves a Plasma sidechain implementation that can run EVM-compatible smart contracts - i.e. the Matic Virtual Machine. Since the philosophy of the Matic Network heavily revolves around an incentive mechanism of security deposits on the main chain, it can be instructive to think about an efficient way of identifying the data involved in fraud challenges.

Validation of consensus rules can be enforced through a system of challenges, using a [TrueBit](https://truebit.io/)-like verification. The main motivation is to run software in a similar manner as we currently do on the Ethereum mainchain. The security deposit makes it easier to estimate the security of the sidechain in monetary terms. When working correctly, the stakers will frequently commit the sidechain blocks to the root chain.

A set of validations is expected to keep the stakers honest. There are a number of insurance contracts incentivizing the verification of the chain. Together these contracts combined would make for a complete set of consensus validation rules on the root blockchain. Such rules include:

  - Withholding challenges: The Delegates might have submitted blocks to the blockchain but have withheld the contents. The stakers must present a preimage or risk getting slashed.
  - Parsing challenges: The delegates submitted an invalid block structure.
  - Transaction censorship: Submit a transaction on the root chain, requesting for it to be included in the sidechain within a certain timeframe.
  - Invalid block signature: The stakers provided an invalid signature of the block.
  - Invalid previous block hash, height, or previous state, among other block verifications.
  - Any other consensus failure checks, like transaction receipts posting an invalid after state.
  - Invalid transaction execution: an on-chain way to verify a transaction.

The last step is the most complex technically, but using a Truebit-like binary search, there would only be a need to verify one EVM state transition.

A precompile is required to run the EVM inside an EVM. This is done through a stepper contract that can compute a EVM state transition.

Some work on this already started (see [solevm](https://github.com/Ohalo-Ltd/solevm)), but the focus will be to correctly encode the whole EVM state in such a way that it can fit inside a transaction in the root chain, for the purposes of verifying it with an interactive Truebit game. The Matic Development Team believes that a large security deposit, plus other economic interests that participants might have in the correct operation of the sidechain, would lead to less risks.

Overall, if one can efficiently identify the problematic EVM state transition for verification, through an EVM-in-an-EVM construction, one can subject it to challenges, and thereby securing it.

# Security

## Fraud Proofs {#fraud}

To enhance the security of the transactions, Matic Network also provides Fraud Proofs on the mainchain. The mechanism enables any individual on the mainchain to submit the details of the transactions which he/she thinks is fraudulent. If the challenge is successful, the stakes of the parties involved in the fraud are slashed and the challenger receives the slashed funds as an incentive for detecting the fraud. This can be considered as an always-running high reward bounty program for any parties who wish to investigate the veracity of the transactions on the Matic Network.

### Basic proofs {#basicp}

Each proof must be submitted with the following corresponding proofs whenever necessary:

  - Merkle proof for transaction inclusion: This type of proof is needed to prove that the given transaction is included in the block

  - Merkle proof for block inclusion: This type of proof is needed to prove that the block is included in the given checkpoint

### Block {#blockp}

This proof is needed to prove that the block is in sequence with a valid referenced hash.

### Transaction

#### Single level txn proof {#singletp}

```js
  // validate ERC20 TX
  function validateERC20TransferTx(
    uint256 headerNumber,
    bytes headerProof,

    uint256 blockNumber,
    uint256 blockTime,
    bytes32 txRoot,
    bytes32 receiptRoot,
    bytes path,

    bytes txBytes,
    bytes txProof,

    bytes receiptBytes,
    bytes receiptProof
  ) public {
    // validate tx receipt existence
  }
```

#### Nonce validation {#noncevp}

  - To check if there are transactions with duplicate nonces

  - To check for transactions with missing nonce values (skipping multiple nonces in between)
    This is an interactive fraud proof. The Delegate must submit missing nonce transaction in certain amount of time when challenged for this type of transaction.

  - To check for transactions with non-ordered nonces

```js
  function validateMisMatchedNonce(
    bytes tx1,
    bytes tx2
  ) public {
    // check if both transactions are not the same    
    ...

    // validate first transaction
    ...

    // validate second transaction
    ...

    // check if sender is the same in both transactions
    ...

    // make sure 2 is included after tx1    
    ...

    // check if both nonce values are same or nonce2 < nonce1, just call slasher    
    ...

    // revert the operation    
    ...
}
```

#### Receipt validation {#recvalp}

  - To check receipt fields, events, topics and data types in given receipt

#### Deposit {#depositp}

- Validate deposit transactions
  Validates deposit transaction on the mainchain and see if it matches with DepositBlock object in rootchain.

- Duplicate deposit transactions
  This proof validates if there are duplicate transactions that have the same DepositId and that each DepositID is included only once

- Validate deposited amount and the depositor address

#### ERC20 transfer {#erc20tp}

  - To validate ERC20 transaction data, receipt logs and values

  - To check if UTXO-style input in log receipt log equals that of an UTXO-style output of a recent transaction log receipt

### Iterative txn proof
Details to be updated in a later version of the whitepaper

# Network Economics {#economics}

## Transaction Fee Determinative Factors and Trade-off
1. Block Size = (Average Transaction Amount)/(Block)
  - 100Txs/Block is insanely expensive.
  - ETH is 600~1000Txs/Block
  - If The Matic Network permits 3000Txs/Block, this variable is going to be predominant factor over other factors. But network layer censorship-resistance will be harmed like BCH-Tor problem.

2. Number of Delegates
  - If there are more Delegates, transaction fee allocation will be more.
  - Delegate setting of 7 is cost efficient.
  - If the number of Delegates is increased to say, 120, the transaction fee increases.

3. Number of Checkpoint stakers
  - If number of stakers is 10,000, then it will be expensive to structure incentives.
  - 100-150 stakers will result in an optimum transaction fee.
  - Fewer stakers are better, but decentralization in such a setup is slightly lower.

4. Block Time
  - The Matic Development team could assign 2~3sec for block time.
  - 0.5sec block time still works with regards to block propagation, and it has no effect on user experience.
  - Let's say, a single Matic sidechain aims to achieve ~35k Tx/sec on a chain. If node through-put is the bottleneck, then blocksize would be 70k~105k Tx/Block. This is about ~10MB/Block.

5. Checkpoint duration
  - A checkpoint duration of 3600sec has been determined to be optimum.
  - A shorter duration means faster Maliciousness detection, but it also means a higher committed Gas fee.
  - If a Byzantine behavior (e.g. Double Spend through Tx deletion) occurs just after checkpoint creation, this duration is the worst-case time until the Ceremony. If some Delegates delete transactions, The Matic Network can recover the cancelled Tx, and the double spend attack would be foiled.

# Focus on User Experience {#usere}

The Matic Development Team is developing a wallet by implementing the [WalletConnect](https://walletconnect.org/) protocol, which is an open protocol to connect web-based distributed applications to mobile crypto assets.

This wallet will help users to interact with DApps and sign transactions easily, while still helping users keep their private keys safe on their mobile. This should go a long way in making blockchains accessible to mainstream users.

Other than this, the team is also looking at Context specific ether less accounts and Gas relay abstraction on identity to enable ether-less sign transactions, which can be a huge boost for mainstream user adoption.

# Matic Stack {#stack}

This section details out various parts of the Matic chain and components in the Ethereum chain.

## Matic Deposit Bridge {#mdb}

The bridge(s) of the Matic Network are part of Delegate nodes that listen to the RootContract events on the mainchain and monitor any token/ether transfer events happening to the RootContract. This bridge utilizes Matic Network’s famous tool named [Dagger](https://github.com/maticnetwork/eth-dagger.js). Once the bridge detects a deposit on the mainchain, it fires a Deposit event on the Matic chain and the user’s address on the Matic Network is allocated the deposited amount.

### Matic PoS {#mpos}

The checkpointing mechanism of the Matic Network is a PoS enabled layer which has Stakers who propose the checkpoints to the mainchain. There will be about 100-150 Stakers at the checkpointing layer. In future with the advent of more efficient signatures on Ethereum blockchain, The Matic Network will be able to significantly increase its number of stakers on the checkpointing layer which is expected to further increase its degree of decentralization, perhaps rivalling that of the leading public blockchains like Ethereum and Bitcoin.

More details of the PoS checkpoint layers will be given in a later version of the Whitepaper.

### Delegate Layer {#bplay}

At the base layer, The Matic Network has Delegate nodes chosen by the Stakers of the PoS layer through voting for every checkpointing interval. These Delegates will be required to have Proof of Solvency. These Delegates will also run the Matic Deposit bridge.

Delegates accept transactions through the Matic VM and are expected to create a block every 1 second.

More technical and code level details of the Block Producer layer will be added in a later version of the whitepaper.

### Matic Virtual Machine {#vm}

The Matic Network uses a standard EVM based state machine, which is run by the Delegate nodes to generate blocks. Using the EVM allows the Matic Network to be able to build and deploy protocols such as ERC protocols as well as other protocols like Kyber Network, ZRX etc.

The beauty of the Matic Network architecture is that since it uses an EVM-compatible state machine, it becomes very easy to port DApps and smart contracts running on the Ethereum blockchain to the Matic Network. The Matic Development Team intends to support generalized state transitions on the Matic Network, and this architecture provides a smooth foundation to build upon.

### Matic Withdrawal Bridge {#mvb}

When an address on the Matic Network submits a withdrawal request to the network, the corresponding tokens are burnt (withdrawn from) on the Matic chain and this transaction is pushed on to the Matic chain. After the specified checkpoint interval, the PoS checkpoint layer will publish the checkpoint to the main chain, which will include the proof of burn (withdrawal) of these tokens on the Matic chain. Once this checkpoint is committed on the mainchain, the user can claim their withdrawn tokens.

## Spam Protection {#spam}

The Delegates running the block producer layer of the Matic Network will watch the transfer state of the assets to identify frivolous transactions. They reject any incoming transactions with zero amount in payments thereby foiling any DoS/spam attacks with zero cost transactions. Even if the Matic tokens are very low in cost and the fees being very low, due to the high TPS of Matic Network, it would not be economically viable to run sustained DoS attacks on the Matic Network.

The Matic Network maintains payment transfer event logs in a UTXO-like data structure, which allows for efficient verification of inputs and outputs. This allows for a variety of security measures.

Additional checks are run to mitigate spam based on this:

- For each input, the referenced output must exist and cannot already be spent
- Check if the sum of input values is less than sum of output values.
- Check if transaction fee is too low.
- Check for duplicate transactions with same outputs in the transaction pool.
- Check for duplicate transactions with same transaction fee in the pool.

# Potential Use Cases {#potential}

Matic Network Pte. Ltd. (The Governing body) is committed to provide a scalable and user- friendly ecosystem for third party Decentralized applications to thrive on. The governing body, like Ethereum and other platform foundations, will promote various Base chain DApps (like DApps built on Ethereum currently, and NEO, EOS in future) to build and migrate their user facing applications / transactions on the Matic Network. It will also award grants and funding to third party app developers to build various use cases on top of the Matic Network like:

### Payments {#payment}

The Matic Network will provide an interface for users, payment APIs and SDKs for DApps, merchant and users to instantly accept or pay in crypto assets (e.g., ERC20 tokens, Ethers).

the Matic Development Team has plans to roll-out this system in three phases:
1. Ethereum and ERC20 token payments
2. Multi-asset cross chain transfer and payment through atomic swaps and liquidity providers
3. Fiat enabled payment system through fiat liquidity providers

### Atomic Swaps {#atom}

Matic contract allows users to pay with any crypto token they prefer, and receiver will receive payment in assets they prefer. The Matic Network can handle conversation through atomic swaps between cross-chain crypto assets.

### Liquidity providers {#liquidity}

Third parties can use the Matic Network to exchange any tokens for other tokens by leveraging 0x liquidity pool or other liquidity providers while transferring crypto assets. In the case of fiat, the Matic Development Team is planning to collaborate with fiat liquidity providers in currencies of major countries.

### Decentralized Exchange (DEX) {#dex}

The Matic Network is expected to have all characteristics which an exchange platform should have — faster and cheaper trades. The Matic Network is capable of supporting decentralized exchanges and enabling trust-less, reliable and easy crypto trades. The decentralized exchange is the future for digital assets and provides better security and solvency than the centralized exchanges.

### Lending & Credit Scoring platform {#lcsp}

The Matic Network will enable platforms for merchants to assess the creditworthiness of connected users via their transaction history. This enables merchants to lend tokens to users on the network when transacting with users that do not have sufficient funds. The Matic Network expects to use the Dharma protocol to provide tokenized debt to users.

### Identity {#identity}

Users need a utilitarian yet user-friendly interface where MetaMask or web3 enabled browsers are not required. They do not need to understand how Ethereum works under the hood.

Decentralized apps need a way to sign transactions, but that must happen without submitting private keys on each DApp on web browsers or mobile apps. The Matic Development Team believes that users must have control over their private keys without worrying about the security. The Matic Network will solve that with an Open-Identity system and will deliver a seamless experience to users.

This system will also provide a way to auto-approve certain kind of transactions depending upon the criteria chosen by the users. This will drive the recurring payments on the Matic Network.

### Securing Personal Data {#spd}

Building upon the Identity feature of the Matic Network, users will be able to secure their personal data on the Identity chain. This data will be encrypted and queried using zero-knowledge proofs only, thereby limiting access to sensitive, personal data by external services.

Currently, each third-party service stores data in their servers for each customer, which poses a tremendous security risk for the users in case of a data breach, as well as huge reputational risks for the service. The Matic Network is expected to reduce the need to have user's personal data shared with each service, and provide a tiered, auditable mechanism to track sharing of personal data. Businesses will also find that storing less personal data reduces the overall cost of maintaining user data securely.

Currently, most users do not even know the extent of data that is shared with publishers and how much value they lose in trading convenience or free application usage for their personal data. The Matic Network expects to enable easy porting of data from third-party services to the Identity chain, wherein even the Matic Network itself will not have access to the personal data.

Users can also choose to share their data with publishers in a much more transparent manner and can also look to monetize the usage of their data by charging a sharing fee. This could be done via a multi-tier sharing mechanism, with data such as location tracking being offered a higher fee, etc.


### Infrastructure {#infrastructure}

The Matic Development Team will act on the simple mantra - make it simple and seamless.  For that, the team will provide new infrastructure around the Matic Network including user-friendly wallets for individual users and merchants, payroll dashboards, payment SDKs and other open source tools.

### Dagger {#dagger}

The Matic Development Team already has started building infrastructure for developers, starting with Dagger. [Dagger](https://matic.network/dagger) is a tool or engine to track Ethereum accounts and events in real-time.

Developers can use Dagger to track their own smart contracts, accounts, and transactions. They can create custom service or integrate with third-party services through IFTTT or Zapier.

Further information about Dagger can be found here:

https://medium.com/matic-network/ethereum-in-realtime-dagger-98ee2d717c76<br/>
and check how it works:<br/>
https://medium.com/matic-network/understanding-dagger-453d90480c51

# Matic Tokens
The native digital cryptographically-secured utility token of the Matic Network (Matic Token) is a major component of the ecosystem on the Matic Network, and is designed to be adopted for use as the primary token on the network. Matic Token will be issued as ERC-20 standard compliant digital tokens on the Ethereum blockchain.<br/>

Matic Token is designed to be a utility token which functions as the unit of payment and settlement between participants who interact within the ecosystem on the Matic Network. Matic Token does not in any way represent any shareholding, participation, right, title, or interest in the Governing body, the Issuer, its affiliates, or any other company, enterprise or undertaking, nor will Matic Token entitle token holders to any promise of fees, dividends, revenue, profits or investment returns, and are not intended to constitute securities in Singapore or any relevant jurisdiction. Ownership of Matic Token carries no rights, express or implied, other than that which may be afforded by the Matic Network and/or any other third parties whom may use such Tokens.<br/>

Matic Tokens are expected to provide the economic incentives to encourage participants to contribute and maintain the ecosystem on the Matic Network. Computational resources are required for performing various functions on the Matic Network such as validating blocks and publishing proofs), thus providers of these services / resources would be rewarded with Matic tokens for providing these resources to the network (i.e. "mining" on the Matic Network) to maintain network integrity. Matic Token will be used as the unit of exchange to quantify and pay the costs of the consumed computational resources. Matic Token is an integral and indispensable part of the Matic Network, because without Matic Token, there would be no incentive for users to expend resources to participate in activities or provide services for the benefit of the entire ecosystem on the Matic Network. Only users which have actually contributed to network maintenance would receive token incentives. Users of the Matic Network and/or holders of Matic Token which did not actively participate will not receive any Matic Token as rewards.<br/>

In order to participate in the consensus process on the Matic Network, users would be required to stake Matic Token as an indication of that user's commitment to the process. Matic Token would thus also be used as a deterrent for punishing stakers for various offences (e.g. invalid blocks, illegally verifying blocks, or invalid transaction execution) by requiring them to first put up a stake of Matic Token before being entitled to participate in the ecosystem. Matic Token would be deducted in the event that an offence was committed by a staker.<br/>

In particular, it is highlighted that Matic Token:<br/>
1. is non-refundable and cannot be exchanged for cash (or its equivalent value in any other virtual currency) or any payment obligation by the Governing body, the Issuer or any affiliate;
2. does not represent or confer on the token holder any right of any form with respect to the Governing body, the Issuer (or any of its affiliates), or its revenues or assets, including without limitation any right to receive future dividends, revenue, shares, ownership right or stake, share or security, any voting, distribution, redemption, liquidation, proprietary (including all forms of intellectual property or licence rights), or other financial or legal rights or equivalent rights, or intellectual property rights or any other form of participation in or relating to the Matic Network, the Governing body, the Issuer and/or their service providers;
3. is not intended to represent any rights under a contract for differences or under any other contract the purpose or pretended purpose of which is to secure a profit or avoid a loss;
4. is not intended to be a representation of money (including electronic money), security, commodity, bond, debt instrument or any other kind of financial instrument or investment;
5. is not a loan to the Governing body, the Issuer or any of its affiliates, is not intended to represent a debt owed by the Governing body, the Issuer or any of its affiliates, and there is no expectation of profit; and
6. does not provide the token holder with any ownership or other interest in the Governing body, the Issuer or any of its affiliates.

The contributions in the token sale will be held by the Issuer(or its affiliate) after the token sale, and contributors will have no economic or legal right over or beneficial interest in these contributions or the assets of that entity after the token sale. To the extent a secondary market or exchange for trading Matic Token does develop, it would be run and operated wholly independently of the Governing body, the Issuer, the sale of Matic Token and the Matic Network. Neither the Governing body nor the Issuer will create such secondary markets nor will either entity act as an exchange for Matic Token.

# Challenges, security concerns and mitigation {#challenges}

1. Block withholding after deposit or deposit is not processed by a Delegate due to unavailability of the Matic bridge

  - Each deposit will create new id (uint256 counter) associated with a Deposit event

  - Delegate must process deposit within the next 5 checkpoints

  - If not processed, deposit amount will be eligible for Withdrawal

2. Block withholding after deposit, relay and before transfer

  There are two ways this can be solved:

  - "Withdraw only" mode: The Matic Network can go into withdraw only mode after a certain time with no checkpoints (~ around 2 days). All users must start the exit process (ref #13) by proving their token holdings from last known checkpoints. The problem with this approach would be the "loss of valid transactions from the last checkpoints"

  - Start ceremony (ref #12) to choose next set of Delegates: Ceremony will start to select next round of Delegates and selected Delegates will resume chain from last checkpoints and start validating pending transactions (if any)

3. Checkpoint withholding after burning (withdrawing) tokens from the Matic Network

  This will only happen when there is fraud on Matic chain. Mitigation would be the same as 2.

4. A Delegate changes token balance while relaying deposits.

  Mitigation would be the same as 2.

5. A Delegate changes token balance during transfer.

  Mitigation would be the same as 2.

6. A Delegate generates tokens for particular address

  Mitigation would be the same as 2.

7. A Delegates generates, transfers and burns (withdraws) tokens between two checkpoints

  Mitigation would be the same as 2.

8. A rationale of how a Delegate can be a trustless entity

  - Use appcoin security for Delegate collateral and discourage Matic Token damaging + short selling

  - Make Solvency Proof mandatory before assigning one as a Delegate. A wealthy entity can game with this Solvency Proof but appcoin above will mitigate the attack

  - Validator-level censorship can be mitigated via forcing Delegates to include TX in next 5 (or so) checkpoints

  - If a government gets to know who is maintaining the Matic chain and bans that entity’s activity, slash that node and choose alternative from outside of that country

9. Discrepancy between balances of users and total balances of the root contract

   At any given point in time, what if there is a discrepancy between total of users’ balances and root contract’s total balances? What if the root contract allows certain users to withdraw more tokens than intended (possible hack)? How one can detect that there has been a hack or fraud on the Matic Network?

   Solvency proof of balances comes handy in this case. For more info on solvency proof and single use seals, see
   https://petertodd.org/2016/commitments-and-single-use-seals

10. Transaction censorship

    To resolve this, a possible solution could be following:

    Anyone can add transaction data directly to the main chain contract. That transaction must be added in next 5 checkpoints by Delegates.

    The following might happen next -

      - If a Delegate does not include Tx within the next 5 checkpoints, the Tx owner can start a challenge through locking some ETH as a bond (staked value) to prevent frivolous challenges. After a certain amount of time, the Delegate would not be able to produce inclusion proof, and this results in the Delegates getting slashed and the transaction owner will receive the slashed amount + bond (Locked to initiate challenge)

      - If Delegate includes the transaction, but the transaction owner decides to initiate a challenge anyway - in this case, Delegate produces a inclusion proof and gets bond amount put as collateral by the transaction owner.

11. DDoS

  - One way to prevent DDoS is to check state validation when the user submits the transaction (before tx goes to pending pool)
  - Node must handle the state validation check portion while accepting transactions. If any node decides to skip this implementation, other nodes will ignore all future transactions from particular node.

12. Ceremony

  - The Matic Network has the same level of security as Ethereum until the latest checkpoint. But after the latest checkpoint, some blocks will not be as robust in terms of security as Ethereum. Now, if a Byzantine party controls 51% of dPoS Delegates by locking a large amount of collateral, he can cancel his specific deposit transaction to deceive centralized exchanges (e.g. updating 10~20 confirmations).

  - The Matic Network is able to detect withholding, censorship, or any fraudulent activity via checkpoint voting. These voters are independent from Byzantine Delegates party.

  -Byzantine Delegates are slashed and removed, while their staked funds are redistributed to community.

  - In order to make ceremony smooth, online Delegates must be queued in the event that multiple Byzantine delegates have to be removed.

  - The frequency of ceremony could be mitigated through fast restarts, fraudulent record recovery, and collateral/stake slashing. Furthermore, once the Matic Network gains popularity, security of Matic chain is going to be robust as well.

13. Exit

  - As mentioned in #2, The Matic Network only uses exit procedures when a checkpoint is not signed by enough checkpoint-stakers as a form of anomaly handling. Otherwise it is a normal system and hence one is able to use "Simple Fast Withdrawal"-esque construction (a.k.a. Matic Withdrawal Bridge).

  - As mentioned in #2, when the checkpoint-stakers are Byzantine, the Matic Network will go to "withdraw only mode". It means that the Matic Network does not to conduct Mass Exits as defined in the Plasma security model. When Transaction-chain's Delegates are byzantine, the Ceremony will be conducted, and it is seamless compared to the "withdraw only mode". This 2-phase construction is virtue of the simple and seamless design philosophy of the Matic Network.

# Future Research {#future}

The Matic Development team expects to conduct various additional research based on topics proposed by the community, including but not limited to:

1. Generalized states and fraud proofs for the same.
2. Evaluate the approach to expand Staker base in the checkpointing layer with the future Threshold based signatures implementations on Ethereum, if any.
3. Robust structure and design pattern for upgradeable smart contracts.
4. Context specific Ether less accounts and Gas Relay Abstractions on Identity
5. Privacy-enabled transactions
6. Blockchain interoperability
7. State channels on top of the sidechain

# Team {#team}

- Jaynti Kanani. Co-founder and Chief Executive Officer. Contributor to Web3, Plasma, WalletConnect. Previously data scientist at Housing.com.<br/>
https://www.linkedin.com/in/jdkanani/
- Anurag Arjun. Co-founder and Chief Product Officer. Previously AVP (Product Management), IRIS Business. Stints at SNL Financial, Dexter Consultancy and Cognizant Tech.<br/>
https://www.linkedin.com/in/anuragarjun/
- Sandeep Nailwal. Co-founder and Chief Operating Officer. Blockchain Programmer and Entrepreneur. Previously CEO Scopeweaver, CTO (Ecommerce) Welspun Group.<br/>
https://www.linkedin.com/in/sandeep-nailwal-60709a33/
