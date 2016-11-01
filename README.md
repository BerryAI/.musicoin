# musicoin

this is the main file structure for the musicoin app.


## How to setup genesis

Execute as `sudo`:
`sudo su -`

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis.json`

`rm -r ~/.musicoin/blockdata`

`mkdir ~/.musicoin/blockdata`

`geth --datadir ~/.musicoin/blockdata`



# Running from second node

`geth --bootnodes enode://36267f976cba2c9365f40395a203ab5be2d49c04c421cbebe094d6bb9ff2295e56537c8f04b9078cd59e692e85c7283d83d98aee4a086979fcb5aa78c0ce3bda@[::]:30303`
* Note: when node 1 restarts, this enode address needs to be updated

