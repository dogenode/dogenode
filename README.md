# DogeNode Core [NDOGE]
==========================

![Dogenode](https://i.imgur.com/Wh1JpG7.png)

## What is DogeNode?

DogeNode is a PoS-based cryptocurrency. DogeNode is dependent upon libsecp256k1 by sipa, the sources for which can be found here:
https://github.com/bitcoin/secp256k1

RPC - 8552
P2P - 8551 

## Dependencies in ONE LINE

sudo apt-get update && sudo apt-get dist-upgrade && sudo apt-get install libtool autotools-dev autoconf pkg-config && sudo apt-get install software-properties-common && sudo add-apt-repository ppa:bitcoin/bitcoin && sudo apt-get update && sudo apt-get install libminiupnpc-dev libdb4.8-dev libdb4.8++-dev libevent-dev && sudo apt-get install nano ntp zip unzip git build-essential libssl-dev libboost-all-dev libqrencode-dev aptitude && sudo aptitude install miniupnpc libminiupnpc-dev && sudo apt-get install libgmp3-dev

## Compiling DAEMON 

    cd dogenode/src/leveldb
    chmod 755 build_detect_platform
    make clean
    make libleveldb.a libmemenv.a
    cd ..
    make -f makefile.unix
    strip dogenoded
    sudo cp dogenoded /usr/local/bin
    ./dogenoded -daemon

## Configuration DogeNode.conf file

    rpcuser=rpc_login
    rpcpassword=password
    rpcallowip=127.0.0.1
    listen=1
    server=1
    txindex=1
    daemon=1

## Other Commands

    ./dogenoded -daemon # Starts the dogecoin daemon.
    ./dogenoded help # Outputs a list of RPC commands when the daemon is running.
