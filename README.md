# Today We are setting up a POA blockchain. Pretty Simple I hope


Step 1: Download Geth
![image](https://user-images.githubusercontent.com/23089346/131228129-43d3c691-8828-415b-9f0a-e3766f5b2a91.png)

Step 2: Get metamask up and all good


Step 3: make 2 nodes
./geth --datadir node1 account new
./geth --datadir node2 account new

Step 4:
Genisis block and POA setup

./puppeth > new blockchain > new genisis > POA


Step 5:
Pre funding

Paste both addy names (no 0x, to promt, to get them pre funded)


Step 6:
Export Genisis config

save those json files


Step 7:
Init those nodes

./geth --datadir node1 init networkname.json
./geth --datadir node2 init networkname.json

Step 8:
Test transactions

use metamask
import wallet

![image](https://user-images.githubusercontent.com/23089346/131228464-5207855c-216a-400d-b899-5852a45f4270.png)

connect to custom RPC
![image](https://user-images.githubusercontent.com/23089346/131228481-0aff961d-f274-44c9-b7c0-a2334f5cc84b.png)


Step 9: Check and see: maybe reactivate?

for both nodes:

./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnoes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable -allow-insecure-unlock
