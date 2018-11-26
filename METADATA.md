# Metedata Guidelines



## Company Rules

- A user must consent to uploading their data with Metadata.
- Metadata associated with any record will be permanent, searchable and public and therefore there needs to be consent.
- It is best that unconsented Metadata is not appended to Stow Smart Contracts. 
- This functionality should be at App Level and if a user does not consent then data uploaded to Stow Protocol should be void of Metadata. 
- Please take caution, show examples of Metadata and be completely transparent in how a user's data and Metadata are uploaded to the application. It is in the best interest of everyone involved that the privacy of the user is maintained at all times. 



# Specifications

The Stow Protocol stores Metadata for every record that is added to the protocol. This Metadata is public and is used to query the data and understand what is stored in every record without really having access to the data inside.

The following specifications are recommended by the Stow Team.

## Example

```json
{
    "dataFormat": "json",
    "domain": "social media",
    "storage": "IPFS",
    "encryptionScheme": "x25519-xsalsa20-poly1305",
    "encryptionPublicKey": "hQYhHJpzZH/tGhz1wtqSjkL17tJSnEEC4yVGyNTHNQY=",
    "stowjsVersion": "0.1.4",
    "providerName": "Facebook",
    "providerEthereumAddress": "0x349e31e92027f86b0ffeb5cd5e07003c7f229872",
    "keywords": [ "facebook", "friends list", "people" ],
    "timeframe": "2018-06-07T10:30,2018-06-08T10:30"
}
```



## Specifications

The Metadata should be in JSON format and the following are the properties that should have:

| property                | type          | options                     |                                                              |
| ----------------------- | ------------- | --------------------------- | ------------------------------------------------------------ |
| dataFormat              | string        | 'json'   'csv' 'plain_text' | Format of the data                                           |
| domain                  | string        |                             | Domain of the content                                        |
| storage                 | string        |                             | Storage                                                      |
| encryptionScheme        | string        |                             | Encryption Scheme used to encrypt the data                   |
| encryptionPublicKey     | string        |                             | Encryption Public Key used to encrypt the data               |
| stowjsVersion           | string        |                             | If the data was uploaded using Stow js, this field will contain the version of the library used for compatibility reasons |
| providerName            | string        |                             | The name or identity of the data provider if it was not uploaded by the same owner |
| providerEthereumAddress | address       |                             | The Ethereum Address of the provider if it was not uploaded by the same owner |
| keywords                | array[string] |                             | An array of keywords in order to be able to search           |
| timeframe               | comma separated ISO 8601 strings |          | Two comma separated ISO 8601 that represent the timeframe in which the record is relevant
