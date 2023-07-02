# 🏗 Setting Up the CLI

The steps below will walk you through installing the js implementation of CO2.Storage, setting up your environment variables, and testing everything. You'll then be able to use CO2.Storage  to search, load, create and sign assets and templates in your javascript projects.

This assumes you have git and node-js installed. The tutorial was developed on macOS using the Terminal.

## Installing CO2.Storage

1\) Download the repo by running:

<pre class="language-bash"><code class="lang-bash"><strong>git clone https://github.com/protocol/co2-storage.git
</strong></code></pre>

2\) Navigate to the cli folder:

```bash
cd co2-storage
cd cli
```

3\) Install dependencies:

```bash
npm install
```

For reference, see the npm package [co2-storage/js-api](https://www.npmjs.com/package/@co2-storage/js-api)

## Set Up Environment Variables

4\) In `co2-storage/cli`, you should find a file named `.env.example`. Copy it, and rename to `.env`

{% hint style="info" %}
We're going to use the `.env` file to store private keys. If handled properly, this will not expose your keys. The .env file is included in [.gitignore](https://github.com/protocol/co2-storage/blob/main/.gitignore), which will prevent it from being uploaded to git. If you want to check how the private keys are used, examine the function `authenticateWithPK` in [Auth.js](https://github.com/protocol/co2-storage/blob/main/js-api/src/js/auth/Auth.js). If this is unfamiliar to you, use test accounts.
{% endhint %}

5\) You should have a file that looks like this image. We're going to fill in the private keys necessary to use co2.storage.

<figure><img src="../.gitbook/assets/Screenshot 2023-03-15 at 5.17.42 PM.png" alt=""><figcaption></figcaption></figure>

6\) Get "PK" from Metamask. In the browser plugin, go to menu > Account details > Export Private Key. Metamask will ask you for your account password. Copy the Metamask private key into PK in the .env file.

<div>

<figure><img src="../.gitbook/assets/Screenshot 2023-03-15 at 5.19.51 PM.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Screenshot 2023-03-15 at 5.20.12 PM.png" alt=""><figcaption></figcaption></figure>

</div>

7\) Get ESTUARY\_API\_KEY and FG\_TOKEN from co2.storage. Log in to co2.storage with the same Metamask account you just got PK from. Click on the green button in the upper right hand corner, which should be labeled with your walled address 0x...

<figure><img src="../.gitbook/assets/Screenshot 2023-03-15 at 5.26.48 PM.png" alt=""><figcaption></figcaption></figure>

This will take you to a page with two different tokens. Use "My API token" as FG\_TOKEN and "My Estuary Key" as ESTUARY\_API\_KEY.&#x20;

The Estuary key should start with "EST" and end with "ARY" because the Estuary engineering team is clever.

8\) Almost done! For the last key, you need an Infura account. Go to [infura.io](https://www.infura.io/) and log in or make a new account.&#x20;

Go to Dashboard > API Keys. Click on the name of your account, which in the image below is CO2\_storage\_test. Copy the key to INFURA\_API\_KEY.\


9\) Check the keys in your `.env` file. All four should have different formats. If two of the keys look the same, you probably had a problem copy pasting. It happens. Save the file.

## Try Out Examples

Test out some of the example scripts in [co2-storage/cli/src/examples](https://github.com/protocol/co2-storage/tree/main/cli/src/examples) to make sure that your environment is set up properly and see how to use the js api!

{% hint style="info" %}
There are two ways of using the js-api: either with your own IPFS node, or with the IPFS node provided by co2.storage. In step 10, we assume you haven't set up your own IPFS node and tell the example scripts to use the co2.storage node. If you do want to run your own IPFS node, see [Configuring IPFS Nodes](configuring-ipfs-nodes.md).
{% endhint %}

10\) To run search\_templates using the co2.storage ipfs node, first open `search_templates.js` in the examples folder. Comment out lines 5 and 6, which tell the script to use local addresses for the IPFS node and for the FG API. Then un-comment lines 7-8, which will tell the script to use the co2.storage node.&#x20;

The lines should look like this:

```javascript
// const ipfsNodeAddr = "/ip4/127.0.0.1/tcp/5001"
// const fgApiUrl = "http://localhost:3020"
const ipfsNodeAddr = "/dns4/web1.co2.storage/tcp/5002/https"
const fgApiUrl = "https://web1.co2.storage"
```

11\) Going back to the command line, make sure you're in the folder co2-storage/cli. Then run:

```bash
npm run search_templates
```

Within a few seconds, this should give you a list of templates available on the `'sandbox'` chain 🎉

12\) To run other scripts in the examples folder, you'll have to configure each one to use the co2.storage IPFS node or use your own node. If you've done this and set up the .env file correctly, you should be able to run all of the scripts.&#x20;

Scripts like `add_asset` and `add_template` require authentication, because co2-storage tracks who added what information using the index chain. Scripts that are read only, like `search_templates` and `get_asset`, do not require authentication so you should be able to use them without setting up the .env file as above.
