---
title: "Calls Faulted（出错的调用次数）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: bb9e8045-6aeb-4b7f-a825-8283c44252a1
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 23016861eb5385d8383a68e90e23211aec4bde38
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="calls-faulted"></a>Calls Faulted（出错的调用次数）
计数器名称：Calls Faulted（出错的调用次数）  
  
## <a name="description"></a>描述  
 向此操作返回的出错的调用次数。 在 [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] 应用程序中，服务方法使用 SOAP 错误消息来传递处理错误信息。 SOAP 错误是包括在服务操作元数据中的消息类型，因此会创建一个错误协定，客户端可使用该协定来使执行更加可靠或更具交互性。 由于 SOAP 错误在客户端以 XML 格式表示，因此具有高度的互操作性。  
  
## <a name="see-also"></a>另请参阅  
 [在协定和服务中指定并处理错误](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
