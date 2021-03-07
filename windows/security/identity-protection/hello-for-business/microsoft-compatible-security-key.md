---
title: Microsoft compatible security key 
description: Windows�10 enables users to sign in to their device using a security key. How is  a microsoft compatible security key different (and better) than any other FIDO2 security key
title: Microsoft-compatible security key 
description: Windows�10 enables users to sign in to their device using a security key. How is  a Microsoft-compatible security key different (and better) than any other FIDO2 security key
keywords: FIDO2, security key, CTAP, Hello, WHFB
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security, mobile
author: aabhathipsay-MS
author: aabhathipsay
ms.author: aathipsa
ms.localizationpriority: medium
ms.date: 10/25/2018
ms.date: 11/14/2018
---
# What is a Microsoft compatible security key? 
Microsoft has been aligned with the [FIDO Alliance](https://fidoalliance.org/) from the start with a mission to replace passwords with an easy to use, strong credential. We have been working with our partners to extensively test and deliver a seamless and secure authentication experience to end users.
# What is a Microsoft-compatible security key? 
> [!Warning]
> Some information relates to pre-released product that may change before it is commercially released.  Microsoft makes no warranties, express or implied, with respect to the information provided here. 

The FIDO2 CTAP specification contains a few optional features and extensions which are crucial to provide that seamless and secure experience. 

Microsoft has been aligned with the [FIDO Alliance](https://fidoalliance.org/) with a mission to replace passwords with an easy to use, strong 2FA credential. We have been working with our partners to extensively test and deliver a seamless and secure authentication experience to end users.

The [FIDO2 CTAP specification](https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html) contains a few optional features and extensions which are crucial to provide that seamless and secure experience. 

A security key **must** implement the following features and extensions from the FIDO2 CTAP protocol to be Microsoft compatible:
A security key **MUST** implement the following features and extensions from the FIDO2 CTAP protocol to be Microsoft-compatible:

| #</br> | Feature / Extension trust</br> | Why is this required? </br> | Relevant Section in FIDO2 CTAP specification</br>| 
| --- | --- | --- | --- |
| 1 | Resident key | This feature enables the security key to be portable, where your credential is stored on the security key | Section XXX |
| 2 | Client pin | This feature enables security keys to protect your credentials with a second factor like PIN </br> We recommend strong multi-factor credentials for authentication to all Microsoft services| Section XXX |
| 3 | hmac-secret | This extension ensures you can sign-in to your device when it's off-line or in airplane mode | Section XXX |
| 4 | Multiple accounts per RP | This feature ensures you can use the same security key across multiple services like MSA and AAD | Section XXX |
| #</br> | Feature / Extension trust</br> | Why is this required? </br> |
| --- | --- | --- | 
| 1 | Resident key | This feature enables the security key to be portable, where your credential is stored on the security key |
| 2 | Client pin | This feature enables you to protect your credentials with a second factor and applies to security keys that do not have an user interface|
| 3 | hmac-secret | This extension ensures you can sign-in to your device when it's off-line or in airplane mode |
| 4 | Multiple accounts per RP | This feature ensures you can use the same security key across multiple services like Microsoft Account (MSA) and Azure Active Directory (AAD) |
 
