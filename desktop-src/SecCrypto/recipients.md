﻿---
Description: 'Represents a collection of Certificate objects.'
ms.assetid: 'de9cbf8e-f34c-4e08-89aa-b5ac842aa599'
title: Recipients object
---

# Recipients object

\[The **Recipients** object is available for use in the operating systems specified in the Requirements section. Instead, use the [**CmsRecipientCollection Class**](T:System.Security.Cryptography.Pkcs.CmsRecipientCollection) in the [**System.Security.Cryptography.Pkcs**](frlrfSystemSecurityCryptographyPkcs) namespace.\]

The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects. Each object represents an intended recipient of the enveloped message. Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](security.s_gly#-security-symmetric-key-gly) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate. A recipient with access to the [*private key*](security.p_gly#-security-private-key-gly) associated with a certificate's [*public key*](security.p_gly#-security-public-key-gly) can decrypt the [*session key*](security.s_gly#-security-session-key-gly) and use the decrypted session key to decrypt the actual data.

## When to use

The **Recipients** object is used to perform the following tasks:

-   Add or remove a [**Certificate**](certificate.md) object from the collection.
-   Retrieve the number of certificates in the collection.
-   Retrieve a specific **Recipients** object from the collection.
-   Iterate through the collection.

## Members

The **Recipients** object has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **Recipients** object has these methods.



| Method                              | Description                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Add**](recipients-add.md)       | Adds a [**Certificate**](certificate.md) object to the collection.<br/>         |
| [**Clear**](recipients-clear.md)   | Removes all [**Certificate**](certificate.md) objects from the collection.<br/> |
| [**Remove**](recipients-remove.md) | Removes a [**Certificate**](certificate.md) object from the collection.<br/>    |



 

### Properties

The **Recipients** object has these properties.



| Property                                           | Access type          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Read-only<br/> | Retrieves an [**IEnumVARIANT**](139e3c93-faef-4003-9079-e0e94494db3e) interface on an object that can be used to enumerate the collection. This property is hidden within Visual Basic Scripting Edition (VBScript).<br/> |
| [**Count**](recipients-count.md)<br/>       |                      | The number of objects in the **Recipients** collection.<br/>                                                                                                                                                              |
| [**Item**](recipients-item.md)<br/>         |                      | An indexed object in the collection. This is the default property.<br/>                                                                                                                                                   |



 

## Remarks

The **Recipients** object cannot be created.

## Requirements



|                            |                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistributable<br/> | CAPICOM 2.0 or later on Windows Server 2003 and Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## See also

<dl> <dt>

[**Cryptography Objects**](cryptography-objects.md)
</dt> </dl>

 

 



