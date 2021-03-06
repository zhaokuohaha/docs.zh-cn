---
title: "ICLRRuntimeInfo 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo
helpviewer_keywords: ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 287e5ede-b3a7-4ef8-a756-4fca3f285a82
topic_type: apiref
caps.latest.revision: "27"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 86861ae1742cf520d1a5251c70a112b090ec429e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfo-interface"></a>ICLRRuntimeInfo 接口
提供返回有关特定的公共语言运行时 (CLR) 的信息包括版本、 目录和负载状态的方法。 此接口还没有初始化运行时提供特定于运行时的功能。 它包括运行时相对[LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md)方法，则运行时模块特定[GetProcAddress](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md)方法，并通过提供运行时接口[GetInterface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)方法。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[BindAsLegacyV2Runtime 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md)|将此运行时中的所有旧 CLR 版本 2 激活策略决策的绑定。|  
|[GetDefaultStartupFlags 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getdefaultstartupflags-method.md)|获取对 CLR 启动标志和主机配置文件。|  
|[GetInterface 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)|将 CLR 加载到当前进程，并返回运行时接口指针，如[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)， [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)和[IMetaDataDispenser](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)。 此方法取代所有`CorBindTo*`函数。|  
|[GetProcAddress 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md)|获取指定已与此接口关联的 CLR 从导出的函数的地址。 此方法取代[GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md)方法。|  
|[GetRuntimeDirectory 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md)|获取与此接口关联的 CLR 的安装目录。 此方法取代[GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md)方法。|  
|[GetVersionString 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getversionstring-method.md)|获取与关联的公共语言运行时 (CLR) 版本信息给定[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)接口。 此方法取代[GetRequestedRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)和[GetRequestedRuntimeVersion](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)方法。|  
|[IsLoadable 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloadable-method.md)|指示与此接口关联的运行时是否可以加载到当前进程，并考虑可能已加载到进程的其他运行时。|  
|[IsLoaded 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloaded-method.md)|指示是否与关联 CLR [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)接口加载到进程。|  
|[IsStarted 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isstarted-method.md)|指示是否 CLR 与该键相关联[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)接口已开始。|  
|[LoadErrorString 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loaderrorstring-method.md)|HRESULT 值转换为相应的错误消息为指定的区域性。 此方法取代[LoadStringRC](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md)和[LoadStringRCEx](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md)方法。|  
|[LoadLibrary 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md)|从 CLR 所表示的框架目录中加载库[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)接口。 此方法取代[LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md)方法。|  
|[SetDefaultStartupFlags 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-setdefaultstartupflags-method.md)|设置 CLR 启动标志和主机配置文件。|  
  
## <a name="requirements"></a>要求  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** MetaHost.h  
  
 **库：**作为 MSCorEE.dll 中的资源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>另请参阅  
 [承载接口](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [承载](../../../../docs/framework/unmanaged-api/hosting/index.md)
