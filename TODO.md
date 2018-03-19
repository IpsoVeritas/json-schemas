base:
remove @context from base
remove @subtype from base
merge subtype as hash (anchor) in type uri
@certificateChain change to @certificate in base

action:
removed role
changed mandate to array of mandates
contract - handle separately as this can be signed by the app, and to enable revocation of contracts
changed contract from object to string (compact encoded JWS)
made mandates mandatory, removed role

action-descriptor:
removed binding
removed uiData, can use uiURI as data uri
removed all nonce fields, the action should contain a unique random string as a nonce
scopes, should be linked to the new scope.json schema (done)
added refreshURI

add scope.json schema! (done)
add keypurpose.json schema! (in controller-descriptor go code) (done)

certificate-chain has been changed into a new certificate

contract: check if there is a title
added attachments
refer to part? (also in multipart)

controller-binding:
controllerCertificateChain changed to controllerCertificate
mandate -> mandates

removed document-callback schema

fact:
changed iss to issuer

mandate:
label -> roleName
removed receipentPulicKey
receipient is now public key
removed requestId
removed ttl
added validFrom
added validUntil

mandatetoken:
removed mandate

multipart:
check uri handling in general
removed title

push-message:
consider moving to separate documentation of push messages

realm-descriptor:
removed keyHistory (this issue should be carefully reviewed later)

receipt:
removed role
jwt: investigate, bad design when sharing receipts
look at params

scope-request:
refer to scope document (done)
refer to contract document
removed encryptTo

signature-request:
removed document
added contract, TODO: refer to contract document
