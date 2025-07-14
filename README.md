## Events in Solidity

In Solidity, an **event** is a mechanism that allows your smart contract to log information on the blockchain.

These logs are stored in a special data structure called the **log** and can be accessed and monitored by off-chain applications such as:

- Decentralized applications (**dApps**)
- Frontend interfaces
- Blockchain indexers and explorers

Events are especially useful for:

- Tracking contract activity
- Emitting information about state changes
- Communicating between on-chain and off-chain components

### 🔧 Example

```solidity
// Define an event
event Transfer(address indexed from, address indexed to, uint256 value);

// Emit the event in a function
function transfer(address to, uint256 amount) public {
    // ...logic...
    emit Transfer(msg.sender, to, amount);
}
```
