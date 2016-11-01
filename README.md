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

`geth --datadir ~/.musicoin/blockdata`



# Running from second node

`geth --bootnodes enode://0f2f8c04c6e53f8ee5545e7849f8239c6f33cf868e2599a468cf256884c72ab89501f3686e357adbcbd92974ec3a6f486804660d9ede834a814bb39695aeea1a@104.198.70.194:30303`
* Note: when node 1 restarts, this enode address needs to be updated

