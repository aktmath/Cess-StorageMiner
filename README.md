# Cess-StorageMiner
Storage Miner For Cess

Wallet : https://polkadot.js.org/extension/

Create two new wallet for miner + stake

Add rpc to your polka wallet : https://testnet.cess.cloud/?rpc=wss%3A%2F%2Ftestnet-rpc2.cess.cloud%2Fws%2F#/accounts

Get tokens from faucet : https://cess.cloud/faucet.html

# Set-up

Paste this codes one by one, in order

````
ufw allow 4001
wget https://github.com/CESSProject/cess-nodeadm/archive/v0.5.4.tar.gz
tar -xvf v0.5.4.tar.gz
rm -rf v0.5.4.tar.gz
cd cess-nodeadm-0.5.4/
./install.sh
mkdir -p /opt/cess/storage/disk
````

````
cess config set
````

After this, it will ask some questions, reply in order

1-storage

2-click enter if you wanna use default port, or enter your port

3-Enter miner wallet ADDRESS(only address)

4-Enter mnemonic keys for stake wallet.(seed phrases)

5-ENTER

6-Enter your storage amount(I used 300 gb so typed 300) the more the better

7-4

8-Enter(skip)

9-Enter(skip)

````
cess start
````

# Control

````
docker logs -f chain
````

Wait till your node reaches to current block(check here  https://cloudflare-ipfs.com/ipns/dotapps.io/?rpc=wss%3A%2F%2Ftestnet-rpc0.cess.cloud%2Fws%2F#/explorer )


## Bucket logs

````
docker logs -f bucket
````

## Bucket Stat
````
cess bucket stat
````

## Usefull commands
Check yourself in the miner section : https://substats.cess.cloud/

### Increase Stake Amount
````
cess bucket increase <amount>
````


### Withdraw

````
cess bucket withdraw
````


### Reward info

````
cess bucket reward
````

### Claim

````
cess bucket claim
````

### Update All Services

````
cess pullimg
````

### Stop and Delete the service

````
cess down
````

###Change your miner wallet
````
cess bucket update earnings <wallet address>
````
