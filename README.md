# Simple-open-auction
This repository contains a simple auction smart contract implemented in Solidity programming language.
## License
This project is licensed under the terms of the GPL-3.0 license. 

## Usage
To use this smart contract, you need to have a compatible Ethereum client and a Solidity compiler installed.

The contract is implemented in Solidity version `0.8.4`, so you need to use a compiler that supports this version or a later one.

To compile the contract, run the following command in your terminal:
`solc --abi --bin SimpleAuction.sol`
This will generate two output files: `SimpleAuction.abi` and `SimpleAuction.bin`.

You can then deploy the contract using your preferred Ethereum client, such as [Ganache](https://trufflesuite.com/ganache/) or [Remix](https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null).

## Contract Details
### Parameters
- `beneficiary`: The address of the beneficiary of the auction.
- `auctionEndTime`: The end time of the auction in Unix timestamp format.
- `highestBidder`: The address of the current highest bidder.
- `highestBid`: The current highest bid.
## Functions
- `bid()`: Allows a user to place a bid on the auction.
- `withdraw()`: Allows a user to withdraw a bid that has been overbid.
- `auctionEnd()`: Ends the auction and sends the highest bid to the beneficiary.
## Events
- `HighestBidIncreased(address indexed bidder, uint256 amount)`: Triggered when a new highest bid is made.
- `AuctionEnded(address indexed winner, uint256 amount)`: Triggered when the auction ends and a winner is determined.
## Errors
- `AuctionAlreadyEnded()`: Indicates that the auction has already ended.
- `BidNotHighEnough(address bidder, uint256 highestBid)`: Indicates that the bid is not high enough.
- `AuctionNotYetEnded()`: Indicates that the auction has not yet ended.
- `AuctionEndAlreadyCalled()`: Indicates that the `auctionEnd()` function has already been called.
