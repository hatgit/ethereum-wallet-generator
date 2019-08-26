# ethereum-wallet-generator

The light ethereum wallet, is a compact ethereum wallet generator that creates single private-public-key pairs to derive a single ethereum address.

>NOTE: This wallet DOES NOT SUPPORT BIP39 mnemonics which can control and derive entire crypto vaults with up to 2 billion addresses (using BIP32) per cryptocurrency and with support for multiple cryptocurrency accounts (using BIP44). For BIP39 tools, see [this repository](https://github.com/iancoleman/bip39). In addition, this wallet may not be compatible with many  cryptocurrency wallets that do not support the importing of private keys in plain text format.

### External Python Library Dependencies

The elliptic curve-related tools are used from the official `eth-keys` library which belongs to the Ethereum Foundation and listed here on Github on the [Ethereum repository](https://github.com/ethereum/eth-keys) and can be installed via the commamnd line on a Mac via the terminal.app using `pip install eth-keys`.
 
The `pysha3` libarary contains the Keccak 256 hashing algorithm using in Ethereum and in the address foramtting stpes and can be found on the [PyPi website](https://pypi.org/project/pysha3/) (and [on Github unwrapped](https://github.com/XKCP/XKCP)) or installed via the commamnd line on a Mac via the terminal.app using `pip install pysha3`. 


## Python Default Library dependencies 

The `secrets` library is used to source 256 bits of entropy and fed into Python's cryptographically-secure pseudo-random number generator (CSPRNG) which is generates the private key (from which all subsequent steps are derived). See [this article](https://docs.python.org/3/library/secrets.html) for more on Python's secrets library. 


### Read more
The eth-keys libary contains a suite of commands available via api, read more here from their [Readme.md file](https://github.com/ethereum/eth-keys/blob/master/README.md).


### Example output: 


The following is an example of what the [light-ethereum-wallet.py](https://github.com/hatgit/ethereum-wallet-generator/blob/master/light-ethereum-wallet.py) file from this repository will print when opened with Python as an exectuable (the values below should never be used on mainnet):

 ```Private_key: 5ab7c35ed259b573e9765b0f499f89ef4f144d9d03415331934647d568174165 
 Private_key_bytes: b'Z\xb7\xc3^\xd2Y\xb5s\xe9v[\x0fI\x9f\x89\xefO\x14M\x9d\x03AS1\x93FG\xd5h\x17Ae' 
 Public_key_hex: 0x7d214afc3071b6dc2421d590e422496bd6035d00b0d6adb5fb785427a453adf86ea9e2dab12140677674ad3959cf5e0dab8e6a9c0dccb5aabdb2f5e885edd1c5 
 Public_key_bytes: b'}!J\xfc0q\xb6\xdc$!\xd5\x90\xe4"Ik\xd6\x03]\x00\xb0\xd6\xad\xb5\xfbxT\'\xa4S\xad\xf8n\xa9\xe2\xda\xb1!@gvt\xad9Y\xcf^\r\xab\x8ej\x9c\r\xcc\xb5\xaa\xbd\xb2\xf5\xe8\x85\xed\xd1\xc5' 
 Full_Keccak_digest: 04a7a8d3bc54ff8acba0e240f23ed954ab1e25ecefda5a3aa47948206d47ab6f 
 Ethereum address: 0xf23ed954ab1e25ecefda5a3aa47948206d47ab6f 
 Checksum Format of Above Ethereum: 0xF23eD954ab1E25EceFDa5A3AA47948206D47AB6F```
