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

`geth --datadir ~/.musicoin/musicoin_data`

