# eth-blockhashes
This contract provides a map between block number and block hash. The motiviation is to remove the restriction that blockhash(n) function returns the correct block hash, only if block n is one in the 256 most recent blocks. An instance of the contract is in Ropsten testnet https://ropsten.etherscan.io/address/0xb11ea8d6bab4c557a781785425a2c5654f882663

The backend to maintain the contract can be found at https://github.com/Maxilbert/eth-blockhashes-backend

The problem was noticed by Andrew Miller https://github.com/amiller/ethereum-blockhashes. Thanks him, this contract borrowed his solution. This Solidity contract is not as efficient as his Serpent contract, especially the add_old() method. and I will think along the way to assemblize some critical bytes thifting oprations to reduce the gas consuming while adding an old block hash.
