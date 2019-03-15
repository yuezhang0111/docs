---
name: NEARLib.js
route: /lib/js
menu: Client API
---

# NEARlib.js

## KeyPair

This class provides key pair functionality \(generating key pairs, encoding key pairs\).

### Parameters

* `publicKey` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)
* `secretKey` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)

### getPublicKey

Get the public key.

#### Examples

```text
TODO: Add code example(s)
```

### getSecretKey

Get the secret key.

#### Examples

```text
TODO: Add code example(s)
```

### fromRandomSeed

Generate a new keypair from a random seed

#### Examples

```text
TODO: Add code example(s)
```

### encodeBufferInBs58

Encode a buffer as string using bs58

#### Parameters

* `buffer` [**Buffer**](https://nodejs.org/api/buffer.html)

#### Examples

```text
TODO: Add code example(s)
```

## Account

Near account and account related operations.

### Parameters

* `nearClient`

#### Examples

```text
TODO: Add code example(s)
```

### createAccount

Creates a new account with a given name and key,

#### Parameters

* `newAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) id of the new account.
* `publicKey` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) public key to associate with the new account
* `amount` [**number**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) amount of tokens to transfer from originator account id to the new account as part of the creation.
* `originator`
* `originatorAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) existing account on the blockchain to use for transferring tokens into the new account

#### Examples

```text
TODO: Add code example(s)
```

### createAccountWithRandomKey

Creates a new account with a new random key pair. Returns the key pair to the caller. It's the caller's responsibility to manage this key pair.

#### Parameters

* `newAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) id of the new account
* `amount` [**number**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) amount of tokens to transfer from originator account id to the new account as part of the creation.
* `originatorAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) existing account on the blockchain to use for transferring tokens into the new account

#### Examples

```text
TODO: Add code example(s)
```

### viewAccount

#### Parameters

* `accountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) id of the account to look up

#### Examples

```text
TODO: Add code example(s)
```

## WalletAccount

Wallet based account and signer that uses external wallet through the iframe to sign transactions.

### Parameters

* `appKeyPrefix` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) an application prefix to use distinguish between multiple apps under the same origin.
* `walletBaseUrl` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) base URL to the wallet \(optional, default `'https://wallet.nearprotocol.com'`\)

#### Examples

```text
TODO: Add code example(s)
```

### isSignedIn

Returns true, if this WalletAccount is authorized with the wallet.

#### Examples

```text
TODO: Add code example(s)
```

### getAccountId

Returns authorized Account ID.

#### Examples

```text
TODO: Add code example(s)
```

### requestSignIn

Redirects current page to the wallet authentication page.

#### Parameters

* `contract_id` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) contract ID of the application
* `title` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) name of the application
* `success_url` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) url to redirect on success
* `failure_url` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) url to redirect on failure

#### Examples

```text
TODO: Add code example(s)
```

### signOut

Sign out from the current account.

#### Examples

```text
TODO: Add code example(s)
```

### signTransaction

Sign a transaction. If the key for senderAccountId is not present, this operation will fail. Sends a sign request to the wallet through the iframe.

#### Parameters

* `tx` [**object**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object) transaction details object. Should contain body and hash
* `senderAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account ID of the sender

#### Examples

```text
TODO: Add code example(s)
```

## Near

Javascript library for interacting with near.

### Parameters

* `nearClient` **NearClient**

#### Examples

```text
TODO: Add code example(s)
```

### callViewFunction

Calls a view function. Returns the same value that the function returns.

#### Parameters

* `sender` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the sender
* `contractAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the contract
* `methodName` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) method to call
* `args` [**object**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object) arguments to pass to the method

#### Examples

```text
TODO: Add code example(s)
```

### scheduleFunctionCall

Schedules an asynchronous function call. Returns a hash which can be used to check the status of the transaction later.

#### Parameters

* `amount` [**number**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) amount of tokens to transfer as part of the operation
* `originator`
* `contractId`
* `methodName` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) method to call
* `args` [**object**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object) arguments to pass to the method
* `sender` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the sender
* `contractAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the contract

#### Examples

```text
TODO: Add code example(s)
```

### deployContract

Deploys a smart contract to the block chain

#### Parameters

* `originator`
* `contractId`
* `wasmByteArray`
* `sender` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the sender
* `contractAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account id of the contract
* `wasmArray` [**Uint8Array**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array) wasm binary

#### Examples

```text
TODO: Add code example(s)
```

### getTransactionStatus

Get a status of a single transaction identified by the transaction hash.

#### Parameters

* `transactionHash` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) unique identifier of the transaction

#### Examples

```text
TODO: Add code example(s)
```

### loadContract

Load given contract and expose it's methods.

Every method is taking named arguments as JS object, e.g.: `{ paramName1: "val1", paramName2: 123 }`

View method returns promise which is resolved to result when it's available. State change method returns promise which is resolved when state change is succesful and rejected otherwise.

Note that `options` param is only needed temporary while contract introspection capabilities are missing.

#### Parameters

* `contractAccountId` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) contract account name
* `options` [**object**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object) object used to pass named parameters
  * `options.sender` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) account name of user which is sending transactions
  * `options.viewMethods` [**Array**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)**&lt;**[**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)**&gt;** list of view methods to load \(which don't change state\)
  * `options.changeMethods` [**Array**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)**&lt;**[**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)**&gt;** list of methods to load that change state

Returns [**object**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object) object with methods corresponding to given contract methods.

#### Examples

```text
TODO: Add code example(s)
```

### createDefaultConfig

Generate a default configuration for nearlib

#### Parameters

* `nodeUrl` [**string**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) url of the near node to connect to \(optional, default `'http://localhost:3030'`\)

#### Examples

```text
TODO: Add code example(s)
```
