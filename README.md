### Version 2.0.0 is in alpha. Do not use it on production.
Forknote 2.0.0 has major bugs and problem with calculating the correct difficulty.<br />
For production use the latest version in the "Release" section:
https://github.com/forknote/forknote-pool/releases/tag/1.1.4



### About
Forknote is innovative way to create Cryptonote (https://cryptonote.org) based cryptotokens. It gives the users the ability to create cryptotokens just by creating a simple configuration file.

### Dependencies
* GCC 4.7.3 or later     (http://gcc.gnu.org/)
* CMake 2.8.6 or later   (http://www.cmake.org/)
* Boost 1.55 or later    (http://www.boost.org/)
* MSVC 2013 (Windows only)

Step by step Windows instructions:
https://github.com/forknote/cryptonote-generator/blob/master/docs/windows-requirements-install.md

Ubuntu (tested on Ubuntu 14.04) / Mac dependencies install script:
https://github.com/forknote/cryptonote-generator/blob/master/configure.sh


### Usage
1. Download or compile the binaries
2. Create configuration file. The easiest way is to use the form on http://forknote.net
3. Start the daemon:
```
./forknoted --config-file PATH_TO_YOUR_CONFIG
```

### Configuration parameters
Use http://forknote.net to create configuration files.

All fields supported:
```
GENESIS_COINBASE_TX_HEX=     // REQUIRED. Use " ./forknoted --config-file PATH_TO_CONFIG --print-genesis-tx " to generate 
CRYPTONOTE_NAME=my_coin
p2p-bind-port=33669
rpc-bind-port=33670
seed-node=127.0.0.1:33669    // format:  IP:PORT
seed-node=127.0.0.2:33669    
UPGRADE_HEIGHT_V2=1             // REQUIRED. Use 1 for new cryptotokens
UPGRADE_HEIGHT_V3=2             // REQUIRED. Use 2 for new cryptotokens
MONEY_SUPPLY=18446744073709551615
EMISSION_SPEED_FACTOR=18
GENESIS_BLOCK_REWARD=0           // premined coins. Default: 0
DIFFICULTY_TARGET=120
CRYPTONOTE_DISPLAY_DECIMAL_POINT=12
DEFAULT_DUST_THRESHOLD=1000000
MINIMUM_FEE=1000000
CRYPTONOTE_MINED_MONEY_UNLOCK_WINDOW=10
CRYPTONOTE_BLOCK_GRANTED_FULL_REWARD_ZONE=20000
CRYPTONOTE_PUBLIC_ADDRESS_BASE58_PREFIX=120
BYTECOIN_NETWORK=b2889400-e6f5-b62d-8d37-8fa91779dc7e
P2P_STAT_TRUSTED_PUB_KEY=4d26c4df7f4ca7037950ad026f9ab36dd05d881952662992f2e4dcfcafbe57eb
CHECKPOINT=10000:70d2531151529ac00bf875281e15f51324934bc85e5733dcd92e1ccb1a665ff8   // format: HEIGHT:BLOCK_ID
CHECKPOINT=20000:80d2dd05d8819526629235722e15f5f9ab36dd05d881952662992f2e4dcfcafb

// simplewallet parameters
wallet-rpc-bind-ip=127.0.0.1        // instead rpc-bind-ip
wallet-rpc-bind-port=33671          // instead rpc-bind-port
SYNC_FROM_ZERO=1                    // to sync the wallet from block 0. Used for premine coins or brain wallets
```

---
This code is generated by Cryptonote generator - https://github.com/forknote/cryptonote-generator
Seed source - https://github.com/amjuarez/bytecoin