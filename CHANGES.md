# CHANGES

## Changes from protocol version 1 to version 2

Date: 2018-07-24

**NOTE:** These changes are not backwards compatible with version 1.

### @base

* Removed @context
* Remove @subtype
* Merged subtype as hash (anchor) in type uri
* @certificateChain change to @certificate

### action

* Removed role
* Changed mandate to an array of mandates
* contract - handle separately as this can be signed by the app, and to enable revocation of contracts
* Changed contract from object to string (compact encoded JWS)
* Mandates are now mandatory, removed role

### action-descriptor

* Removed binding
* Removed uiData, can use uiURI as data uri
* Removed all nonce fields, the action should contain a unique random string as a nonce
* scopes are now linked to the new scope schema
* Added refreshURI

### scope

* Added this schema.

### keypurpose

Added the keypurpose schema

### certificate

"certificate-chain" has been changed into a new certificate schema

### contract

* Changed from a text string to attachments with specific encodings

### controller-binding

* controllerCertificateChain changed to controllerCertificate
* mandate -> mandates

### document-callback

* removed

### fact

* changed iss to issuer

### mandate

* Changes label to roleName
* Removed receipentPulicKey
* receipient is now public key
* Removed requestId
* Removed ttl
* Added validFrom
* Added validUntil
* Removed recipientName

### mandatetoken

* Removed mandate

### multipart

* removed title

### realm-descriptor

* Removed name
* Removed description
* Added label
* Removed keyHistory
* Removed endPoints (now resolved via public action descriptors)

### receipt

* Removed role
* Removed action

### scope-request

* Refer to scope schema
* Refer to contract schema
* Removed encryptTo

### signature-request

* Removed document
* Added contract
