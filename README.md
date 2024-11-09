# Three Dice Decentralized Consensus Algorithm

## Introduction

In a decentralized blockchain network, consensus must be achieved to ensure that all participants (nodes) agree on the current state of the blockchain without trusting any single authority. This is a critical challenge, especially in public blockchains where nodes are often operated by untrusted participants. A new consensus model based on "throwing three dice" introduces a probabilistic approach to achieving consensus. This algorithm aims to establish fairness and randomization in blockchain decision-making, providing a novel way to select a valid blockchain while ensuring transparency and security.

The **Three Dice Decentralized Consensus Algorithm** uses a probabilistic model inspired by the outcome of rolling three dice, where the final decision is based on the likelihood of achieving certain targets. Below is a detailed explanation of the four steps of decentralized consensus in this model, incorporating the concept of rolling three dice.

## Step 1: Independent Verification of Each Transaction

- **Task**: Verify each transaction in the blockchain network.
- **Process**: When a transaction is initiated, each node in the network independently verifies the transaction. This involves ensuring that the sender has enough funds, the transaction is properly signed, and it follows all protocol rules. Once validated, the transaction is broadcast to the network and added to the memory pool, waiting to be included in a new block.
- **Responsibility**: Every full node in the network performs this task.
- **Example**: Alice sends 1 BTC to Bob. Each node checks the transaction to ensure Alice has enough balance, the digital signature is correct, and the transaction is properly formatted before adding it to the memory pool.
- **Role of Three Dice**: In the context of verifying transactions, the "three dice" model can be viewed as a metaphor for the probabilistic nature of transaction validation. Each node might "roll the dice" to assess whether a transaction passes certain thresholds of validation. Although the actual transaction validation does not involve randomness, this serves as the first step towards achieving probabilistic consensus when later selecting the blockchain.

## Step 2: Independent Aggregation of Transactions into Candidate Blocks

- **Task**: Aggregate (mine) transactions into new candidate blocks.
- **Process**: Mining nodes gather transactions from the memory pool and aggregate them into a candidate block. This step typically involves solving a cryptographic puzzle, such as a Proof-of-Work (PoW), to ensure that the block is valid and computationally expensive to produce.
- **Responsibility**: Mining nodes handle this step. Each mining node assembles a block and competes to solve the cryptographic puzzle to add the block to the blockchain.
- **Example**: Alice's transaction to Bob gets included in Block 277,318 after Jing’s mining node successfully mines the block and solves the PoW.
- **Role of Three Dice**: When aggregating transactions into a candidate block, the "three dice" mechanism can be used to assign a probabilistic weight to each transaction's inclusion in the block. The aggregation process may involve a randomization step, where blocks are constructed with a varying likelihood based on the "dice roll" outcome. For example, if the dice roll results in a target number, the block is considered valid.

## Step 3: Independent Verification of Each Block

- **Task**: Verify new candidate blocks.
- **Process**: After a block is mined, every node in the network independently verifies the validity of the block. This includes checking the cryptographic proof, ensuring that the block correctly references the previous block, and verifying that the block's transactions are valid.
- **Responsibility**: Every node in the network is responsible for verifying blocks.
- **Example**: After Block 277,318 is mined, other nodes verify that it contains valid transactions, adheres to the blockchain’s protocol, and is correctly linked to the previous block in the chain.
- **Role of Three Dice**: In this step, the "dice rolls" help determine the probability of a block being accepted by the majority of nodes. For instance, if a node rolls a "high" number (e.g., 16-18), it may choose to accept the block, whereas a "low" roll may result in the block being rejected, based on a predefined probability distribution.

## Step 4: Independent Selection of Blockchain

- **Task**: Select the blockchain to consider as valid.
- **Process**: Once multiple candidate blocks have been mined, nodes may encounter "forks" in the blockchain. The decentralized consensus mechanism must decide which blockchain is the valid one. In the Three Dice model, each node uses a probabilistic method based on rolling three dice to choose which chain to adopt. The blockchain with the highest "dice roll" (i.e., the most favorable outcome based on the number of dice hits) is selected.
- **Responsibility**: Every node in the network independently selects the blockchain to follow based on its own dice rolls.
- **Example**: If a node encounters two competing forks (Fork A and Fork B), it rolls the dice to select which fork it will adopt. The fork with the highest probability of success (based on the dice outcome) will be added to the node’s blockchain.

## Probability Scenarios Using Three Dice

### Simple Target: Probability of Rolling a 12

The probability of rolling a target of 12 with three dice can be calculated by finding all possible outcomes that sum to 12. The total number of possible combinations of three dice is 216 (6^3 = 216). The combinations that sum to 12 are:

- (6, 5, 1)
- (6, 4, 2)
- (6, 3, 3)
- (5, 5, 2)
- (5, 4, 3)
- (4, 4, 4)

There are 6 possible combinations that sum to 12. Thus, the probability is:

\[
\frac{6}{216} = 2.78\%
\]

**Interpretation in Blockchain**: In the context of blockchain consensus, a "12" target might represent a low-probability event, signifying that only a small fraction of blocks would be considered valid based on this outcome.

### Difficult Target: Probability of Rolling a 5

The probability of rolling a target of 5 with three dice can be calculated by finding all possible outcomes that sum to 5. The possible combinations are:

- (1, 1, 3)
- (1, 2, 2)
- (2, 1, 2)
- (3, 1, 1)

There are 4 combinations that sum to 5. Thus, the probability is:

\[
\frac{4}{216} = 1.85\%
\]

**Interpretation in Blockchain**: A "5" target is more difficult to achieve, representing a highly selective consensus outcome, where the chances of successfully adding a block to the blockchain are low.

## Conclusion

The **Three Dice Decentralized Consensus Algorithm** offers a probabilistic approach to selecting valid transactions, blocks, and chains in a decentralized blockchain network. By using the outcomes of three dice rolls to determine the likelihood of selecting certain blocks or chains, the algorithm introduces an element of randomness and fairness, ensuring that consensus is reached even in the presence of untrusted participants. This model could serve as a complementary mechanism to traditional consensus methods, offering a novel perspective on decentralized decision-making.
