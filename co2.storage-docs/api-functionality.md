# 🏗 API Functionality

Co2.Storage has a Javascript API, which enables users to interact with data schemas and assets in a number of ways. The API is available on NPM here: [CO2.Storage API](https://www.npmjs.com/package/@co2-storage/js-api).

Below are descriptions of the various API endpoints:

* [**Authenticate**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/authenticate.js): this endpoint allows users to authenticate with a private key using the `Auth` class from the `@co2-storage/js-api` library.

    * This endpoint exports a single function called `authenticate()` which returns a `Promise` that resolves to either an `error` or a `result` property.
    * To use the endpoint, users should import the `Auth` class from the `@co2-storage/js-api` library, and then create a new instance of it with the authentication type set to `"pk"`. Once an instance of `Auth` is created, users can call the `authenticate()` function to authenticate with their private key.
    * If the authentication is successful, the `authenticate()` function returns an object with a `result` property that contains the authenticated user's information. If the authentication fails, the `authenticate()` function returns an `error` that explains the reason for the failure.
    * If an error occurs during authentication, the endpoint will log the error to the console and exit the program after 300ms. If authentication is successful, the program waits 1 second before exiting.


* [**Add Template**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/add\_template.js): this endpoint allows the user to add a template to CO2.Storage.

    * The template is defined as a JSON object and must include a `type` and `mandatory` fields for each template attribute.&#x20;
      * The `templateName` is a string that gives the template a name.
      * The `templateBase` is an object that includes a `title` and `reference` fields that define the base of the template.
      * The `templateDescription` is a string that provides a description of the template.
      * The `templateParent` is the CID of the template that the new template should inherit from.
      * &#x20;The `chainName` is a string that defines the branch of the IPLD DAG from which the template was created.
    * The endpoint instantiates a new object with the provided authentication, IPFS node type, IPFS node address, and API URL. The endpoint then calls the `addTemplate()` method of the FGStorage object to add the template to IPFS. The endpoint will return a response containing the added templates CID.
    * If the method call results in an error, an error message is logged to the console and the program exits. If successful, the endpoint logs the result to the console and waits for 1 second before exiting the program.
    * A full list of the supported data types can be found here: [**CO2.Storage Supported Data Types**](https://github.com/protocol/co2\_storage\_schemas/blob/main/Schemas/Instructions.md#currently-supported-data-types)


* [**Add Asset**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/add\_asset.js): this endpoint allows the user to add an asset to CO2.Storage.
  * To use the endpoint, users must import `@co2-storage/js-api` and `fs`.
  * The endpoint requires the following parameters:
    * `assetElements`: a JSON object containing asset data
    * `parent`: a string containing the CID of the asset's parent
    * `name`: a string containing the asset's name
    * `description`: a string containing the asset's description
    * `template`: a string containing the CID of the asset's template
    * `filesUploadStart`: a function that is called when the file upload starts&#x20;
    * `filesUploadProgress`: a function to track file upload progress
    * `filesUploadEnd`: a function that will be called when the file upload ends
    * `assetCreationStart`: a function that will be called when asset creation starts
    * `assetCreationEnd`: a function that will be called when asset creation ends
  * The endpoint will return a response containing the added asset's CID.

* [**Get Template**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/get\_template.js): this endpoint allows users to to search for and retrieve templates from CO2.Storage.

    * This endpoint takes ten optional parameters: `chainName`, `phrases`, `cid`, `name`, `base`, `account`, `offset`, `limit`, `sortBy`, and `sortDir`.
    * By default, the `chainName` parameter is set to `'sandbox'` and the other parameters are set to `null` or `0`.
    * The function returns a response object that includes the search results in `result.templates` or an error in `error`.
    * The `getTemplate` function is used to retrieve a specific template from Co2.Storage. It takes a single parameter, the `block` CID of the desired template.
    * The function returns a response object that includes the template data in `result` or an error in `error`.

    The script uses `searchTemplates` to find the most recently listed template and then uses `getTemplate` to retrieve that template's data. If an error occurs during either function call, the script logs the error and exits. The script waits for 1 second before exiting.

* [**Get Asset**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/get\_asset.js): this endpoint endpoint allows users to search for and retrieve assets stored on CO2.Storage.
  * The API searches for assets using the `searchAssets` method, which takes several optional parameters such as `phrases`, `cid`, `name`, `base`, `account`, `offset`, `limit`, `sortBy`, and `sortDir`.
  * The API retrieves the last listed asset using the block CID returned by the search. The `getAsset` method is used to retrieve the asset, passing in the block CID as the parameter. The retrieved asset is printed to the console using `console.dir`, and the program waits for 1 second before exiting. 

* [**Search Templates**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/search\_templates.js): this endpoint allows users to search for templates on CO2.Storage.
  * The endpoint takes in several parameters, including `chainName`, `phrases`, `cid`, `name`, `base`, `account`, `offset`, `limit`, `sortBy`, and `sortDir`, which can be used to filter and sort the search results.
    * The default values for these parameters are `sandbox`, `null`, `null`, `null`, `null`, `null`, `0`, `10`, `null`, and `null`, respectively.
  * The response returns a JSON object containing information on the searched templates, including the template's name, version, block CID, and metadata.

* [**Search Assets**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/search\_assets.js): this endpoint allows users to search for assets on CO2.Storage.
  * The endpoint takes in parameters including `chainName`, `phrases`, `cid`, `name`, `base`, `account`, `offset`, `limit`, `sortBy`, and `sortDir`, with default values set for several of these parameters.
  * The endpoint returns a JSON response containing a `result` object with information about the assets matching the search parameters, including their names, block IDs, and other metadata. 

* [**Get Account**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/get\_account.js): this endpoint retrieves the details of one account through the `getAccount` function.
  * The endpoint takes one parameter, `chainName`, which is a string indicating the name of the environment where the account is located.
  * The endpoint returns an object with information about the account, including its address, balance, and nonce. 

* [**Get Accounts**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/get\_accounts.js): this endpoint retrieves the details of all accounts in a given environment through the `getAccounts` function.
  * The endpoint requires a `chainName` parameter, which specifies the environment to search for accounts on. 
  * The function returns an object with two properties: `error` and `result`.
    * The `error` property is null if there were no errors, and contains an error message if an error was encountered.&#x20;
    * The `result` property contains an array of objects representing the accounts associated with the specified chain.\

* [**Sign CID's**](https://github.com/protocol/co2-storage/blob/main/cli/src/examples/sign\_cid.js)**: t**his endpoint is for signing a CID of an Asset on CO2.Storage
  * It signs the CID with the private key provided in the authentication step.
  * The endpoint takes two parameters: `blockCid` as a string representing the CID of the block to be signed, and `callback` as a function that takes a `response` object as its parameter.
  * The response object contains the result of the sign CID operation, including the signature and related information. After signing the CID, the function outputs the response object.

