# 🌱 Build a Web UI

In this tutorial, we walk through how to set up a React app incorporating CO2.storage. Unlike in the previous tutorial, where you set up your credentials in a .env file, in this case the user will authenticate with their own browser extension wallet.

1\) In the folder where you want the project, run:

```bash
npm init react-app demo-app
```

This will make a new `demo-app` subfolder with React installed.

2\) Navigate to that folder using `cd demo-app` and check that React is working by starting the web app:

```bash
npm run start
```

You should see your app when you go to [http://localhost:3000/](http://localhost:3000/)

3\) In the app folder, install the co2-storage javascript package by running:

```bash
run npm install --save @co2-storage/js-api
```

Now in `demo-app/package.json` you should see `co2-storage/js-api` listed under dependencies:

```json
...
"dependencies": {
    "@co2-storage/js-api": "^X.Y.Z",
    ...
```

Where X.Y.Z is the version installed (at time of writing, 1.2.2).

4\) We can now copy code from the [examples repo folder](https://github.com/protocol/co2-storage/tree/main/cli/src/examples) in order to bring CO2.Storage functionality to our web app!

Open `demo-app/src/App.js` and near the top add this import statement and these constants:

```javascript
import { FGStorage } from '@co2-storage/js-api';

const authType = "metamask"
const ipfsNodeType = "browser"
const ipfsNodeAddr = "/dns4/web2.co2.storage/tcp/5002/https"
const fgApiUrl = "https://web2.co2.storage"

const fgStorage = new FGStorage({authType: authType, ipfsNodeType: ipfsNodeType, ipfsNodeAddr: ipfsNodeAddr, fgApiHost: fgApiUrl})

```

Here, we are:

* Importing the package
* Using the metamask browser plugin for authentication
* Running an ipfs node locally in the web browser and using this to pin and retrieve files
* Connecting to other ipfs nodes running co2-storage
* Instantiating a FGStorage object

5\) For example, if we want to add a button that searches templates we can add this to the HTML in App.js:

```html
<button onClick={SearchTemplates}>search</button>
```

And add the SearchTemplates function below, copying from the [`search_templates.js`](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/search\_templates.js) example:

```javascript
async function SearchTemplates(){

  /**
   * Search templates
   * parameters: (chainName, phrases, cid, name, base, account, offset, limit, sortBy, sortDir)
   * // default data_chain: 'sandbox', phrases: null, cid: null, name: null, base: null, account: null, offset: 0, limit: 10
   */

  let searchTemplatesResponse = await fgStorage.searchTemplates('sandbox')    // ('SP Audits', 'Water')
  if(searchTemplatesResponse.error != null) {
      console.error(searchTemplatesResponse.error)
      // await new Promise(reject => setTimeout(reject, 300));
      // process.exit()
  }

  console.log(searchTemplatesResponse.result)

}
```

When you go to your browser console, this should cause the results of the search to be returned.
