---
title: "&lt;system.runtime.serialization&gt; 的 &lt;dataContractSerializer&gt;"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d9b3d625-be3f-4768-8e0d-1b7e6929f6a8
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 39d24f03bde729e99b629162aee86efe4b60fdd1
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="ltdatacontractserializergt-of-ltsystemruntimeserializationgt"></a>&lt;system.runtime.serialization&gt; 的 &lt;dataContractSerializer&gt;
包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的配置数据。  
  
 \<system.runtime.serialization >  
\<dataContractSerializer >  
  
## <a name="syntax"></a>语法  
  
```xml  
<configuration>  
  <system.runtime.serialization>  
    <dataContractSerializer ignoreExtensionDataObject="Boolean"  
            maxItemsInObjectGraph="Integer">  
      <declaredTypes>  
        <add type="String">  
          <knownType type="String">  
             <parameter index="Integer"  
                        type="String" />  
          </knownType>  
        </add>  
      </declaredTypes>  
    <dataContractSerializer>  
  </system.runtime.serialization>  
</configuration>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|元素|描述|  
|-------------|-----------------|  
|ignoreExtensionDataObject|一个布尔值，指定在对终结点进行序列化或反序列化时，是否要忽略由该终结点提供的数据。 只可对 `<dataContractSerializer>` 元素下的 `<behavior>` 设置此属性。|  
|maxItemsInObjectGraph|一个整数，指定要序列化或反序列化的最大项数。 此属性为 65536。|  
  
### <a name="child-elements"></a>子元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<d d >](../../../../../docs/framework/configure-apps/file-schema/wcf/declaredtypes.md)|包含在进行反序列化时 <xref:System.Runtime.Serialization.DataContractSerializer> 使用的已知类型。<br /><br /> 有关数据协定和已知的类型的详细信息，请参阅[数据协定已知类型](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)。|  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<system.runtime.serialization>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|表示 <xref:System.Runtime.Serialization> 命名空间节的根元素，并包含 <xref:System.Runtime.Serialization.DataContractSerializer> 的设置选项的元素。|  
  
## <a name="remarks"></a>备注  
 有关已知类型的详细信息，请参阅<xref:System.Runtime.Serialization.DataContractSerializer>和[数据协定已知类型](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)。  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>  
 [数据协定已知的类型](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
