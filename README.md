# MyToken Solidity Smart Contract

This is a basic Ethereum ERC-20 token contract named `MyToken` that allows minting and burning of tokens. It includes functionalities for managing token details, balances, minting, and burning.

## Contract Details

- **Token Name:** CRAFTERS
- **Token Abbreviation:** CRT
- **Total Supply:** 0

## Functions

### Mint
        The `mint` function allows for the creation of new tokens. It takes two parameters: an address and a value. The total supply is increased by the specified value, and the balance of the specified address is also increased by that amount.

    ```solidity
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

### Burn
        The burn function allows for the destruction of tokens. Similar to the mint function, it takes an address and a value. The total supply is decreased by the specified value, and the balance of the specified address is decreased by that amount, but only if the balance is greater than or equal to the burning amount.

    solidity
    Copy code
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }


