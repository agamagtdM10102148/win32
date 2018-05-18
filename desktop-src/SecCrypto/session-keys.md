---
Description: 'Session keys are keys that are generated to be used in a single communication session.'
ms.assetid: '18bf2023-084d-400d-b60d-1ba51ce6a2bc'
title: Session Keys
---

# Session Keys

[*Session keys*](security.s_gly#-security-session-key-gly) are keys that are generated to be used in a single communication session. Session keys are frequently changed and are discarded when they are no longer needed. For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message. Typically a [*symmetric key*](security.s_gly#-security-symmetric-key-gly) is used as the session key.

Session keys are volatile. Applications can save these keys for later use or for transmission to other users. For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).

 

 


