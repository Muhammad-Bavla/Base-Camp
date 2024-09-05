# Base-Camp
Skills and Knowledge to build and deploy on any EVM-compatible chain

# Base-Camp (now rebranded as Base Learn) cirriculum:
Ethereum Applications
- Describe the origin and goals of the Ethereum blockchain
- List common types of applications that can be developed with the Ethereum blockchain
- Compare and contrast Web2 vs. Web3 development
- Compare and contrast the concept of "ownership" in Web2 vs. Web3
  
Gas Use in Ethereum Transactions
- Explain what gas is in Ethereum
- Explain why gas is necessary in Ethereum
- Understand how gas works in Ethereum transactions

EVM Diagram
- Diagram the EVM

Setup and Overview
- Install and create a new Hardhat project with Typescript support
- Describe the organization and folder structure of a Hardhat project
- List the use and properties of hardhat.config.ts

Testing with Hardhat and Typechain
- Set up TypeChain to enable testing
- Write unit tests for smart contracts using Mocha, Chai, and the Hardhat Toolkit
- Set up multiple signers and call smart contract functions with different signers

Etherscan
- List some of the features of Etherscan
- Read data from the Bored Apes Yacht Club contract on Etherscan
- Write data to a contract using Etherscan.

Deploying Smart Contracts
- Deploy a smart contract to the Base Sepolia Testnet with hardhat-deploy
- Deploy a smart contract to the Sepolia Testnet with hardhat-deploy
- Use BaseScan to view a deployed smart contract

Verifying Smart Contracts
- Verify a deployed smart contract on Etherscan
- Connect a wallet to a contract in Etherscan
- Use etherscan to interact with your own deployed contact

Hardhat Forking
- Use Hardhat Network to create a local fork of mainnet and deploy a contract to it
- Utilize Hardhat forking features to configure the fork for several use cases

'Introduction to Remix'
- List the features, pros, and cons of using Remix as an IDE
- Deploy and test the Storage.sol demo contract in Remix

Deployment in Remix
- Deploy and test the Storage.sol demo contract in Remix

Hello World
- Construct a simple "Hello World" contract
- List the major differences between data types in Solidity as compared to other languages
- Select the appropriate visibility for a function

Basic Types
- Categorize basic data types
- List the major differences between data types in Solidity as compared to other languages
- Compare and contrast signed and unsigned integers

Test Networks
- Describe the uses and properties of the Base testnet
- Compare and contrast Ropsten, Rinkeby, Goerli, and Sepolia

Deployment to Base Sepolia
- Deploy a contract to the Base Sepolia testnet and interact with it in [BaseScan]

Contract Verification
- Verify a contract on the Base Sepolia testnet and interact with it in [BaseScan]

Control Structures
- Control code flow with if, else, while, and for
- List the unique constraints for control flow in Solidity
- Utilize require to write a function that can only be used when a variable is set to true
- Write a revert statement to abort execution of a function in a specific state
- Utilize error to control flow more efficiently than with require

Storing Data
- Use the constructor to initialize a variable
- Access the data in a public variable with the automatically generated getter
- Order variable declarations to use storage efficiently

How Storage Works
- Diagram how a contract's data is stored on the blockchain (Contract -> Blockchain)
- Order variable declarations to use storage efficiently
- Diagram how variables in a contract are stored (Variable -> Contract)

Arrays
- Describe the difference between storage, memory, and calldata arrays

Filtering an Array
- Write a function that can return a filtered subset of an array

Mappings
- Construct a Map (dictionary) data type
- Recall that assignment of the Map data type is not as flexible as for other data types/in other languages
- Restrict function calls with the msg.sender global variable
- Recall that there is no collision protection in the EVM and why this is (probably) ok

Function Visibility and State Mutability
- Categorize functions as public, private, internal, or external based on their usage
- Describe how pure and view functions are different than functions that modify storage

Function Modifiers
- Use modifiers to efficiently add functionality to multiple functions

Structs
- Construct a struct (user-defined type) that contains several different data types
- Declare members of the struct to maximize storage efficiency
- Describe constraints related to the assignment of structs depending on the types they contain

Inheritance
- Write a smart contract that inherits from another contract
- Describe the impact inheritance has on the byte code size limit

Multiple Inheritance
- Write a smart contract that inherits from multiple contracts

Abstract Contracts
- Use the virtual, override, and abstract keywords to create and use an abstract contract

Imports
- Import and use code from another file
- Utilize OpenZeppelin contracts within Remix

Error Triage
- Debug common solidity errors including transaction reverted, out of gas, stack overflow, value overflow/underflow, index out of range, etc.

The New Keyword
- Write a contract that creates a new contract with the new keyword

'Contract to Contract Interaction'
- Use interfaces to allow a smart contract to call functions in another smart contract
- Use the call() function to interact with another contract without using an interface

Events
- Write and trigger an event
- List common uses of events
- Understand events vs. smart contract storage

Address and Payable in Solidity
- Differentiate between address and address payable types in Solidity
- Determine when to use each type appropriately in contract development
- Employ address payable to send Ether and interact with payable functions

Minimal Token
- Construct a minimal token and deploy to testnet
- Identify the properties that make a token a token

The ERC-20 Token Standard
- Analyze the anatomy of an ERC-20 token
- Review the formal specification for ERC-20

ERC-20 Implementation
- Describe OpenZepplin
- Import the OpenZepplin ERC-20 implementation
- Describe the difference between the ERC-20 standard and OpenZeppelin's ERC20.sol
- Build and deploy an ERC-20 compliant token

The ERC-721 Token Standard
- Analyze the anatomy of an ERC-721 token
- Compare and contrast the technical specifications of ERC-20 and ERC-721
- Review the formal specification for ERC-721

ERC-721 Token
- Analyze the anatomy of an ERC-721 token
- Compare and contrast the technical specifications of ERC-20 and ERC-721
- Review the formal specification for ERC-721
- Build and deploy an ERC-721 compliant token
- Use an ERC-721 token to control ownership of another data structure

Wallet Connectors
- Identify the role of a wallet aggregator in an onchain app
- Debate the pros and cons of using a template
- Scaffold a new onchain app with RainbowKit
- Support users of EOAs and the Coinbase Smart Wallet with the same app

Building an Onchain App
- Identify the role of a wallet aggregator in an onchain app
- Debate the pros and cons of using a template
- Add a wallet connection to a standard template app

The useAccount Hook
- Implement the `useAccount`` hook to show the user's address, connection state, network, and balance
- Implement an isMounted hook to prevent hydration errors

The useReadContract Hook
- Implement wagmi's useReadContract hook to fetch data from a smart contract
- Convert data fetched from a smart contract to information displayed to the user
- Identify the caveats of reading data from automatically-generated getters

Configuring useReadContract
- Use useBlockNumber and the queryClient to automatically fetch updates from the blockchain
- Describe the costs of using the above, and methods to reduce those costs
- Configure arguments to be passed with a call to a pure or view smart contract function
- Call an instance of useReadContract on demand
- Utilize isLoading and isFetching to improve user experience

The useWriteContract hook
- Implement wagmi's useWriteContract hook to send transactions to a smart contract
- Configure the options in useWriteContract
- Display the execution, success, or failure of a function with button state changes, and data display

The useSimulateContract hook
- Implement wagmi's useSimulateContract and useWriteContract to send transactions to a smart contract
- Configure the options in useSimulateContract and useWriteContract
Call a smart contract function on-demand using the write function from useWriteContract, with arguments and a value
