---
title: 111 - CustomTrackingRecordError
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d469fb12-e094-4d6c-9b4d-abd7ce0d17da
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b5914837f8350c39fcf6f490eef44d77913af6f6
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="111---customtrackingrecorderror"></a>111 - CustomTrackingRecordError
## <a name="properties"></a>属性  
  
|||  
|-|-|  
|Id|111|  
|关键字|UserEvents、EndToEndMonitoring、Troubleshooting、HealthMonitoring、WFTracking|  
|级别|错误|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>描述  
 当工作流实例中的某个活动发出属于错误级别的 CustomTrackingRecord 时，ETW 跟踪参与者将发出此事件。  
  
## <a name="message"></a>消息  
 TrackRecord = CustomTrackingRecord, InstanceID = %1, RecordNumber=%2, EventTime=%3, Name=%4, ActivityName=%5, ActivityId=%6, ActivityInstanceId=%7, ActivityTypeName=%8, Data=%9, Annotations=%10, ProfileName = %11  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|描述|  
|--------------------|--------------------|-----------------|  
|InstanceId|xs:GUID|工作流的实例 ID|  
|RecordNumber|xs:long|发出的记录的序列号|  
|EventTime|xs:dateTime|发出该事件时的 UTC 时间|  
|名称|xs:string|CustomTrackingRecord 的名称|  
|ActivityName|xs:string|发出 CustomTrackingRecord 的活动的名称|  
|ActivityId|xs:string|发出 CustomTrackingRecord 的活动的 ID|  
|ActivityInstanceId|xs:string|发出 CustomTrackingRecord 的活动的实例 ID|  
|ActivityTypeName|xs:string|发出 CustomTrackingRecord 的活动的名称|  
|数据|xs:string|在此事件中跟踪的数据。  这些值存储在一个 xml 元素中格式\<项 >\<项名称 ="dataName"type ="> dataValue\</项 > \< /i >。  如果不跟踪任何数据，则该字符串包含\<项 / >。 ETW 事件大小受到 ETW 缓冲区大小或 ETW 事件最大负载的限制。 如果事件大小超出 ETW 限制，则通过丢弃批注并将使用的数据值截断事件\<项 >... \< /i >。  以下类型以从 ToString() 返回时的值存储：string、char、bool、int、short、long、uint、ushort、ulong、System.Single、float、double、System.Guid、System.DateTimeOffset、System.DateTime。  所有其他类型使用 System.Runtime.Serialization.NetDataContractSerializer 进行序列化。|  
|批注|xs:string|已添加到此事件中的批注。  这些值存储在一个 xml 元素中格式\<项 >\<项名称 ="annotationName"type ="> annotationValue\</项 > \< /i >。  如果不指定任何批注，则该字符串包含\<项 / >。 ETW 事件大小受到 ETW 缓冲区大小或 ETW 事件最大负载的限制。 如果事件大小超出 ETW 限制，则通过丢弃批注并将批注值与截断事件\<项 >... \< /i >。|  
|ProfileName|xs:string|导致发出此事件的跟踪配置文件的名称|  
|HostReference|xs:string|对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。  其格式定义为网站名称应用程序虚拟路径 &#124;服务虚拟路径 &#124;ServiceName 示例: 默认网站/CalculatorApplication &#124;/CalculatorService.svc &#124;CalculatorService|  
|AppDomain|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
