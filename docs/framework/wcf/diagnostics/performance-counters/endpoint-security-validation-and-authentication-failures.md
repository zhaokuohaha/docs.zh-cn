---
title: "终结点：Security Validation and Authentication Failures（安全验证和身份验证失败次数）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5bad60aa-6084-4c7b-aefd-9b581f04382e
caps.latest.revision: "6"
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.openlocfilehash: 7d1f05ddc4b0fcf93c87e69932f860f3c7e2ff85
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="endpoint-security-validation-and-authentication-failures"></a>终结点：Security Validation and Authentication Failures（安全验证和身份验证失败次数）
计数器名称：Security Validation and Authentication Failures（安全验证和身份验证失败次数）  
  
## <a name="description"></a>描述  
 每当消息由于“Security Calls Not Authorized”（未授权的安全调用次数）计数器中未包括的安全问题而遭到拒绝时，此计数器即会递增。 此类问题包括：  
  
-   无法从消息中读取客户端令牌。  
  
-   客户端令牌身份验证失败（密码错误）。  
  
-   签名验证失败（消息已被篡改）。  
  
-   消息与上一条消息重复，这种情况可能在重放攻击过程中发生。  
  
-   已发生解密失败。  
  
-   消息中缺少一些必需元素（缺少时间戳或加密的数据块）。  
  
-   TLSNEGO/SPNEGO 握手过程中已发生错误。
