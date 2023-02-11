# Simple-open-auction
This contract is a simple auction contract in **Solidity**, a programming language for the **Ethereum blockchain**. It allows users to bid on an auction by sending Ether (the cryptocurrency of Ethereum) to the contract and specifying their bid amount in the transaction value. The contract has a designated beneficiary, an auction end time, and a highest bidder and bid amount. It also has a mapping to track the pending returns for bids that were overbid. The contract has several functions:

- **bid()** allows users to place a bid on the auction. The bid amount must be higher than the current highest bid. If the bid is successful, the contract updates the highest bidder and highest bid amount and sends any previous highest bidder their pending return.

- **withdraw()** allows users to withdraw their pending return if their bid was overbid.

- **auctionEnd()** ends the auction and sends the highest bid amount to the beneficiary. It can only be called after the auction end time has passed.

- **constructor()** the constructor function is called when the contract is deployed and sets the beneficiary, auction end time, and other initial variables.

The contract also has several events that can be emitted to alert external clients of changes to the contract state, such as when the highest bid is increased or when the auction ends. Finally, it has several error messages that can be thrown in the case of an exception, such as if the auction has already ended or if the bid is not high enough.
