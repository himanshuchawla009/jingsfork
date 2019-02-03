##JINGS COIN Blockchain in Go

Jingscoin Go client is a modified blockchain based on Ethereum protocol in Go language.

##Building the source

Building gjsc(go-jingscoin) requires both a Go and a C compiler. You can install them using your favorite package manager. Once the dependencies are installed, run:

`make all`

##Run Jingscoin client(gjsc)

`gjsc console`

A common error is that gjsc is not executable. Please do chmod +x <path-to-gjc> to avoid this.

If you want to run with RPC, please add more flags accordingly:

gjsc --rpc --rpcapi="db,eth,net,web3,personal" --rpcport "8545" --rpcaddr "127.0.0.1" --rpccorsdomain "localhost" console



##Can't find peers to sync?

Jingscoin has set up some default nodes that you can try to connect as bootstrap nodes. Once connected, the console will start syncing automatically. In case you can't see syncing after a long time, you may have to add peer(s) manually.

In GJSCwget https://storage.googleapis.com/golang/go1.7.1.linux-amd64.tar.gz console, add knowing peer with its enode information:

`> admin.addPeer("{enode info}")`