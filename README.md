# waas-flow-sdk-doc

https://waas.w3bstream.com/

## Developer SDK Document

> This is a document outlining the various functions and methods available in the developer SDK for this project.

## `ctx`

> The ctx object contains information about the current context of the application. It has the following properties:

### `input`: An object containing all input parameters passed to the application, including the request body.

## `utils`

> The utils object contains various utility functions that can be used throughout the application. It has the following properties:

### `jwt`: An object that provides JSON Web Token functionality.

### `nanoid`(size: number): A function that generates a unique ID of a specified length.

### `QRCode.toDataURL(text: string)`: A function that generates a QR code image from a given text.

## `sdk`

> The sdk object contains functions that can be used to interact with the application. It has the following properties:

### `log`(params: {level?: string, msg: string}): A function that logs a message to the application's logging system.

- level (optional): A string indicating the level of the log message. Valid values are "debug", "info", "warn", and "error".
- msg: The message to be logged.

### `storeEvent`(params: {data: {id: string, [x: string]: any; chainId: number; contract_address: string, user: string}}): A function that stores an event in the application's database.

- data: An object containing the event data to be stored. This object must have an id property, as well as any additional properties as needed. The chainId, contract_address, and user properties are required.

### `readEventById`(params: {where: {id: string, date_gt?: string; date_lt?: string;}}): A function that reads an event from the application's database based on the given parameters.

- where: An object containing the query parameters. This object must have an id property, and can optionally have date_gt and/or date_lt properties to filter by date.

### `mintNFT`(params: {id?: string, contract_address: string, receiver: string, chainId: number}): A function that mints an NFT and sends it to the specified receiver.

- id: A string representing the ID of the NFT to be minted.It is optional, and if not provided, a unique ID will be generated.
- contract_address: A string representing the address of the NFT contract to use.
- receiver: A string representing the address of the recipient of the NFT.
- chainId: A number representing the ID of the blockchain to use.

### `env`
> The env object contains information about the application's current environment variables. It has the following properties:

#### `get`(key: string): A function that gets the value of an environment variable by its object property name.
- key: A string which is the property name of the environment variable object.

## axios

> The axios object provides functionality for making HTTP requests. It has the following properties:

### `request`(config: {[x: string]: any;}): A function that makes a generic HTTP request with the given configuration.

### `get`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP GET request to the given URL with the given configuration.

### `post`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP POST request to the given URL with the given data and configuration.

### `put`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP PUT request to the given URL with the given data and configuration.

### `delete`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP DELETE request to the given URL with the given configuration.

### `head`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP HEAD request to the given URL with the given configuration.

### `options`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP OPTIONS request to the given URL with the given configuration.

### `patch`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP PATCH request to the given URL with the given data and configuration.
