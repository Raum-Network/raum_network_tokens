# raum_network_tokens
Raum Network ERC20 tokens for the starknet

An ERC20 comprises the following major methods:

name() -> (name: felt) — which returns the name of the token.

symbol() -> (symbol: felt) — which returns the token’s symbol.

decimals() -> (decimals: felt) — which returns the token’s decimals.

totalSupply() -> (totalSupply: Uint256) — which returns the token’s total supply.

balanceOf(account: felt) -> (balance: Uint256) — which queries and returns the balance of a particular account.

allowance(owner: felt, spender: felt) -> (remaining: Uint256) — which queries and returns the allowance assigned to a spender by an owner.

transfer(recipient: felt, amount: Uint256) -> (success: felt) — which transfers a certain amount of tokens from a sender to the specified recipient.

transferFrom(sender: felt, recipient: felt, amount: Uint256) -> (success: felt) — which allows a spender to transfer a certain amount of tokens allowed to be spent by the owner/sender to the specified recipient.

approve(spender: felt, amount: Uint256) -> (success: felt) — which approves a spender to spend a certain amount of tokens from the owner’s wallet.

# Deployment

## Build the contract
```
protostar build
```

## Declaring your ERC20 token
```
export PROTOSTAR_ACCOUNT_PRIVATE_KEY=[YOUR PRIVATE KEY HERE]
```

## Declare the contract
```
protostar declare ./build/ERC20.json --network testnet --account 0x0691622bBFD29e835bA4004e7425A4e9630840EbD11c5269DE51C16774585b16 --max-fee auto
```

## Deploy the contract
```
protostar deploy 0x07eebd55ccb32c39f4b762b17d4b1f637567de11868b779ee3a59f8043356504 --network testnet --account 0x0691622bBFD29e835bA4004e7425A4e9630840EbD11c5269DE51C16774585b16 --max-fee auto --inputs 1000 0x0005F1480c0bF0B7cEf2Cabab03bD3e4901bB5AB2D632A27c5EC40A86d91482A
```

Reference --> argent.xyz/blog/writing-and-deploying-your-first-erc20-token-on-starknet/
