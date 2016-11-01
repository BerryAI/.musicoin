# musicoin

this is the main file structure for the musicoin app.


## How to setup genesis

Execute as `sudo`:
`sudo su -`

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis_1_no_allocation.json`

`rm -r ~/.musicoin/blockdata/geth`

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis_2_with_allocation.json`


`geth --datadir ~/.musicoin/blockdata --networkid 8959898153  --nodiscover console`

`personal.newAccount()`, with passphrase `Berry`

`eth` to check `coinbase` and `account` have been filled

`miner.start()` to start miner



# Running from second node

`geth --bootnodes enode://dc58e18b7fc31ae0357dd5bc9295d2647aea28116eb22727bc780d026f22211fb5beff7ef9005a52a052a84eaebab89e532ecfe0cd728586e08d2e3a79e191a5@104.198.70.194:30303 --networkid 855983 console`
* Note: when node 1 restarts, this enode address needs to be updated

