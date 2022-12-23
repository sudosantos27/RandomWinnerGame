# Random Winner Game

Welcome to the Random Winner DApp! This decentralized application (dApp) allows users to participate in a lottery-style game where a single winner is chosen at random using Chainlink's Verifiable Random Function (VRF). Here's how it works:

## How to Play:
First, make sure you have a web3-enabled browser (such as Chrome with the MetaMask extension) and an account with some Ether.
Visit the dApp website and connect your account to the app.
Once connected, you will see a button to "Enter the lottery". Click on this button and send a small amount of Ether (the entry fee) to the smart contract.
You will now be entered into the lottery. You can view the list of all players and the total Ether they have entered by clicking on the "View Players" button.
When the lottery is closed (either by reaching the maximum number of players or by reaching the deadline set by the contract), a winner will be chosen at random using Chainlink VRF. The winner will receive all of the Ether that was entered into the lottery.
Smart Contract
The dApp is powered by a smart contract deployed on the Mumbai blockchain. The contract contains the logic for using Chainlink VRF to select a random winner and distributing the Ether among the players. It is open source and available for anyone to review.

## About the Smart Contract:
This smart contract is for a decentralized application (dApp) that allows users to participate in a lottery-style game where a single winner is chosen at random using Chainlink's Verifiable Random Function (VRF).

The contract is implemented using the Solidity programming language and makes use of the VRFConsumerBase contract provided by Chainlink, as well as the Ownable contract from OpenZeppelin for providing ownership functionality.

The contract has several variables for storing information about the game, including the list of players, the maximum number of players, the entry fee, and the current game ID. It also has several events for emitting information about the game, including when the game starts, when a player joins, and when the game ends.

The contract has several functions for interacting with it. The startGame function allows the owner of the contract to start a new game by setting the necessary variables and emitting the GameStarted event. The joinGame function allows players to enter the game by sending the required entry fee and adding themselves to the list of players. If the number of players reaches the maximum, the getRandomWinner function is called to choose a winner using Chainlink VRF. Finally, the fulfillRandomness function is called by the VRFCoordinator contract when it has received a valid VRF proof and is used to determine the winner based on the random number generated.

We hope you enjoy playing the Random Winner DApp!




yarn global add @graphprotocol/graph-cli

graph init --contract-name RandomWinnerGame --product hosted-service sudosantos27/learnweb3  --from-contract 0x5Ce686A9fc7b7fF15fe0F9bCB8655fB9e9c54d82  --abi ./abi.json --network mumbai graph