# waas-sdk-doc
https://waas.w3bstream.com/

## Developer SDK Document
> This is a document outlining the various functions and methods available in the developer SDK for this project.

## `ctx`

> The ctx object contains information about the current context of the application. It has the following properties:

 - `input`: An object containing all input parameters passed to the application, including the request body.
utils
The utils object contains various utility functions that can be used throughout the application. It has the following properties:

 - `jwt`: An object that provides JSON Web Token functionality.
 - `nanoid`(size: number): A function that generates a unique ID of a specified length.
 - `QRCode.toDataURL(text: string)`: A function that generates a QR code image from a given text.

## `sdk`
> The sdk object contains functions that can be used to interact with the application. It has the following properties:

 - `log`(params: {level?: string, msg: string}): A function that logs a message to the application's logging system.
 - `storeEvent`(params: {data: {id: string, [x: string]: any; chainId: number; contract_address: string, user: string}}): A function that stores an event in the application's database.
- `readEventById`(params: {where: {id: string, date_gt?: string; date_lt?: string;}}): A function that reads an event from the application's database based on the given parameters.
- `mintNFT`(params: {id: string, contract_address: string, receiver: string, chainId: number}): A function that mints an NFT and sends it to the specified receiver.

## axios
> The axios object provides functionality for making HTTP requests. It has the following properties:

- `request`(config: {[x: string]: any;}): A function that makes a generic HTTP request with the given configuration.
- `get`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP GET request to the given URL with the given configuration.
- `post`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP POST request to the given URL with the given data and configuration.
- `put`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP PUT request to the given URL with the given data and configuration.
- `delete`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP DELETE request to the given URL with the given configuration.
- `head`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP HEAD request to the given URL with the given configuration.
- `options`(url: string, config?: {[x: string]: any;}): A function that makes an HTTP OPTIONS request to the given URL with the given configuration.
- `patch`(url: string, data?: any, config?: {[x: string]: any;}): A function that makes an HTTP PATCH request to the given URL with the given data and configuration.
