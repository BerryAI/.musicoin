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


`geth --datadir ~/.musicoin/blockdata --networkid 8959898153  --identity Musicoin --port 30305 --nodiscover console`

`personal.newAccount()`, with passphrase `Berry`

`eth` to check `coinbase` and `account` have been filled

`miner.start()` to start miner



# Running from second node

`geth --bootnodes enode://0feaef267fc962c720eeeff6ad83d0709b9adda72a511ce2f2eea2c19a3ffb3c3fe344f7c0a52bbfec738aaaf688822c3abba461baf52e4d2cf078d02b1daeeb@104.198.70.194:30303 --identity Musicoin --networkid 8959898153 console`
* Note: when node 1 restarts, this enode address needs to be updated

