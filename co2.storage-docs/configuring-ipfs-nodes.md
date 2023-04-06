# 🎆 Configuring IPFS Nodes

CO2.Storage uses IPFS to transfer data. IPFS nodes on servers run by the Filecoin Green team are used to pin the data that users create, which makes them persistently available on IPFS.&#x20;

In order to transfer data to and from other CO2.storage IPFS nodes, you need a node of your own. This node should be **peered** with other CO2.storage nodes running the service for best performance. When trying to find data on IPFS, a node will check its peers first for the data.

There are two ways to set up your IPFS nodes when using CO2.Storage, indicated by the keywords `'browser'` or `'client'` when you instantiate the [FGStorage](https://github.com/protocol/co2-storage/blob/main/js-api/src/js/storage/FGStorage.js) instance.

You can also use the IPFS nodes provided by CO2.storage directly by inputting their addresses.

### Browser IPFS Nodes

When you run CO2.storage in your browser, the browser implementation will start and peer its IPFS node automatically. In order to see how this is done, look at the functions in [FGStorage.js](https://github.com/protocol/co2-storage/blob/main/js-api/src/js/storage/FGStorage.js) used to set up these node (case 'browser'). These are:\
\
`async ensureIpfsIsRunning()`: Checks that the node is running; starts and configures it if not.

`async startIpfs()`: Starts the node and attaches to peers.

`async stopIpfs()`: detatches node from peers and stops it.

In this case, because the IPFS node is being run in the browser, the parameters `ipfsNodeAddr` is optional when you instantiate the FGStorage instance.

### Client IPFS Nodes

In order to run your own IPFS node and pass it to CO2.storage, you must install IPFS (we recommend [Kubo](https://github.com/ipfs/kubo/#Install)), configure your node, and pass that node to the FGStorage instance. These instructions use MacOSX.

1\) [Install IPFS](https://docs.ipfs.tech/install/command-line/#install-official-binary-distributions). Instructions for your system type are provided. On the Mac terminal using the current latest version (at time of writing), this looks like:

```bash
curl -O https://dist.ipfs.tech/kubo/v0.19.0/kubo_v0.19.0_darwin-amd64.tar.gz
tar -xvzf kubo_v0.19.0_darwin-amd64.tar.gz
cd kubo
sudo bash install.sh
```

2\) Start IPFS and the IPFS daemon by running&#x20;

```bash
ipfs init
ipfs daemon --enable-namesys-pubsub --enable-pubsub-experiment &
```

The pubsub flags [enable IPNS](https://github.com/ipfs/kubo/blob/master/docs/experimental-features.md#ipns-pubsub).

3\) Configure the node to peer with other CO2.storage IPFS nodes. This is done by editing the config file. Here are instructions for doing this in the MacOSX terminal using the nano editor.

Open the file by running `nano ~/.ipfs/config`

Search for the list of peering nodes by pressing `Ctrl+W`. This should highlight the "Peering" key.  Add peers listed here, so that the section looks like this (starting with the "Peering" key):

```json
 "Peering": {
    "Peers": [
      {
        "ID": "12D3KooWGWHSrAxr6sznTpdcGuqz6zfQ2Y43PZQzhg22uJmGP9n1",
        "Addrs": ["/dns4/proxy.co2.storage/udp/4001/quic"]
      },
      {
        "ID": "12D3KooWFBCcWEDW9GYr9Aw8D2QL7hZakPAw1DGfeZCwfsrjd43b",
        "Addrs": ["/dns4/web2.co2.storage/udp/4001/quic"]
      }, 
      { 
        "ID": "12D3KooWJmYbQp2sgKX22vZgSRVURkpMQ5YCSc8vf3toHesJc5Y9",
        "Addrs": ["/dns4/green.filecoin.space/udp/4001/quic"]
      },
      {
        "ID": "12D3KooWCPzmui9TSQQG8HTNcZeFiHz6AGS19aaCwxJdjykVqq7f",
        "Addrs": ["/dns4/web1.co2.storage/udp/4001/quic"]
      }
   ]
  }
```

Press `^x` to exit nano, and save the file on your way out.

4\) You should now be able to quickly fetch CIDs from CO2.storage with the `ipfs dag get <CID>` command.&#x20;

If you want to shut down the node, use `kill -9 <process number>`, using the process number shown when the node started up.

5\) To get the address of your node and pass it to the js API for CO2.storage, run `ipfs id`.



