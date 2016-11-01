# musicoin

this is the main file structure for the musicoin app.


## How to setup genesis

Execute as `sudo`:
`sudo su -`

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin init ~/.musicoin/musicoin_genesis.json`

`geth --datadir ~/.musicoin --networkid 55313716  --identity Musicoin --port 30303 --nodiscover console`

`personal.newAccount()`, with passphrase `Berry`

`eth` to check `coinbase` and `account` have been filled

`miner.start()` to start miner



# Running from second node

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin init ~/.musicoin/musicoin_genesis.json`

`geth --bootnodes enode://b5fc4b1f5e0fb06c7018187181bccea96ea64cab5380aaebdf2d235b66de2ceeacc4cc8dbd83770c8992aa3fd81e9e8c08d4e14fa11ec59f0e5418329d814570@104.198.70.194:30303 --identity Musicoin --networkid 55313716 --datadir ~/.musicoin console`

Note for Windows users: You may need to change your path from `~/.musicoin` to somewhere in your PC.

