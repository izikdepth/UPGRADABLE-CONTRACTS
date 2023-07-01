Upgradable smart contracts are a concept within blockchain technology, particularly in the context of smart contract development on platforms like Ethereum. Traditional smart contracts are immutable, meaning that once they are deployed to the blockchain, their code cannot be changed. However, in some cases, the need arises to make updates or fixes to the contract without having to redeploy an entirely new version.

Upgradable smart contracts address this limitation by enabling developers to make changes to the contract's logic while preserving the contract's state and data. The main idea is to separate the contract's state and data from its business logic, allowing the logic to be upgraded independently.

There are several approaches to implementing upgradable smart contracts, and one common technique involves using proxy contracts. Here's a simplified explanation of how it works:

Proxy Contract: A proxy contract acts as a middleman between the user and the actual logic contract. When a user interacts with the smart contract, they interact with the proxy contract instead.

Logic Contract: The actual business logic resides in a separate contract known as the logic contract. This contract contains the code that defines the behavior of the smart contract.

Upgrade: When an upgrade is required, a new version of the logic contract is deployed with the necessary changes or improvements. The proxy contract is then updated to point to the new logic contract, effectively making the smart contract upgradable.

Data Persistence: To ensure that data is not lost during an upgrade, the state data is stored outside of the logic contract. Typically, a separate data storage contract or a data structure called Eternal Storage is used to maintain the state data.

This design pattern allows developers to maintain and improve their smart contracts over time without disrupting the existing functionality or losing the contract's state. It can be particularly beneficial for projects that require bug fixes, security updates, or feature enhancements after the initial deployment.

here, i've build an example of upgradable smart contract with forge, feel free to clone the repo and test it yourself. commands can be found here:
https://book.getfoundry.sh/reference/forge/# Upgradable-smart-contracts-example
