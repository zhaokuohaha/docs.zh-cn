---
title: "_EFN_StackTrace 函数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: _EFN_StackTrace
api_location: mscordbi.dll
api_type: COM
f1_keywords: _EFN_StackTrace
helpviewer_keywords: _EFN_StackTrace function [.NET Framework debugging]
ms.assetid: caea7754-867c-4360-a65c-5ced4408fd9d
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 031812b2c286c5647afb9c88882f22e2c7c3addf
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="efnstacktrace-function"></a>_EFN_StackTrace 函数
提供托管堆栈跟踪的文本表示形式以及 `CONTEXT` 记录的数组，其中每项对应非托管代码和托管代码之间的每个转换。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT CALLBACK _EFN_StackTrace(  
    [in]  PDEBUG_CLIENT  Client,  
    [out] WCHAR          wszTextOut[],  
    [out] size_t         *puiTextLength,  
    [out] LPVOID         pTransitionContexts,  
    [out] size_t         *puiTransitionContextCount,  
    [in]  size_t         uiSizeOfContext,  
    [in]  DWORD          Flags  
);  
```  
  
#### <a name="parameters"></a>参数  
 `Client`  
 [in]正在调试客户端。  
  
 `wszTextOut`  
 [out]文本表示形式的堆栈跟踪。  
  
 `puiTextLength`  
 [out]中的字符数的指针`wszTextOut`。  
  
 `pTransitionContexts`  
 [out]转换上下文的数组。  
  
 `puiTransitionContextCount`  
 [out]指向数组中的转换上下文的数的指针。  
  
 `uiSizeOfContext`  
 [in]上下文结构的大小。  
  
 `Flags`  
 [in]设置为 0 或 SOS_STACKTRACE_SHOWADDRESSES (0x01) 以显示 EBP 寄存器和每个前面的输入堆栈指针 (ESP)`module!functionname`行。  
  
## <a name="remarks"></a>备注  
 `_EFN_StackTrace`结构可以从 WinDbg 编程接口进行调用。 参数的用法如下：  
  
-   如果`wszTextOut`为 null 和`puiTextLength`是不为 null，则该函数将返回的字符串长度以`puiTextLength`。  
  
-   如果`wszTextOut`是不为 null，函数将存储中的文本`wszTextOut`所指示的位置到`puiTextLength`。 成功返回如果没有足够的空间中的缓冲区或返回 E_OUTOFMEMORY 如果缓冲区长度不足。  
  
-   如果该函数的转换部分将被忽略`pTransitionContexts`和`puiTransitionContextCount`都为 null。 在这种情况下，函数提供与只有函数名称的文本输出的调用方。  
  
-   如果`pTransitionContexts`为 null 和`puiTransitionContextCount`是不为 null，则该函数将返回所需数量的上下文中的条目`puiTransitionContextCount`。  
  
-   如果`pTransitionContexts`是不为 null，函数会将其视为数组的长度的结构`puiTransitionContextCount`。 通过给定的结构大小`uiSizeOfContext`，而且的大小必须[SimpleContext](../../../../docs/framework/unmanaged-api/debugging/stacktrace-simplecontext-structure.md)或`CONTEXT`体系结构。  
  
-   `wszTextOut`是编写采用以下格式：  
  
    ```  
    "<ModuleName>!<Function Name>[+<offset in hex>]  
    ...  
    (TRANSITION)  
    ..."  
    ```  
  
-   如果以十六进制表示偏移量为 0x0，则写入没有偏移量。  
  
-   如果没有任何托管的代码的线程上当前上下文中，该函数将返回 SOS_E_NOMANAGEDCODE。  
  
-   `Flags`参数为 0 或 SOS_STACKTRACE_SHOWADDRESSES 若要查看每个前面的 EBP 和 ESP`module!functionname`行。 默认情况下，则为 0。  
  
    ```  
    #define SOS_STACKTRACE_SHOWADDRESSES   0x00000001  
    ```  
  
## <a name="requirements"></a>要求  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** SOS_Stacktrace.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>另请参阅  
 [调试全局静态函数](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
