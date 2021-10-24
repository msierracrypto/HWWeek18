# Homework Week 18

## Configuration of network

### Generate new nodes
1. Setup node 1:
geth account new --datadir node1
2. Setup node 2:
geth account new --datadir node2

### Use Puppeth to configure genesis block

1. Use Puppeth to generate genesis block with the following command
./puppeth
2. select: Choose Configure new genesis
3. select: Create a new genesis from scratch
4. select: Clique - proof-of-authority
5. select: Manage existing genesis to export the configuration to JSON

### Init your 2 new nodes
1. Init node1: geth init homework18.json --datadir node1
2. Init node2: geth init homework18.json --datadir node2

### Run your 2 new nodes
1. first node command: geth --datadir node1 --unlock "Bb95C92820EAbc622a5897f6De42864F70c84A6c" --mine --miner.threads 1
2. second node command: geth --datadir node2 --port 30304 --http --bootnodes "enode://8e513f3febb7e1d0420c2b6518167e1bfb899e3bc5ff27fda12ddc0dce02b3fdab4f05fb478069f75e06ddeecc2ca1abcbcbe900530176a8f53b0c7efb87ec08@127.0.0.1:30303"