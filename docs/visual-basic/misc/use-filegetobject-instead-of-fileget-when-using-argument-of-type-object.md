---
title: "使用 &#39;FileGetObject &#39;而不是 &#39;FileGet &#39;当使用自变量的类型和 #39; 对象 &#39;"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: 090b8088-895a-482a-9362-606596bac304
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 996e8a50f90c738bbc64c200125a785c0e9bcd58
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="use-39filegetobject39-instead-of-39fileget39-when-using-argument-of-type-39object39"></a>使用 &#39;FileGetObject &#39;而不是 &#39;FileGet &#39;当使用自变量的类型和 #39; 对象 &#39;
`FileGet` 方法包含 `Object`类型的参数。 应使用`FileGetObject` 替代 `FileGet` ，以避免多义性。  
  
 请注意，与 `My.Computer.Filesystem` 或 `FileGet` 相比， `FileGetObject`提供的功能更易于使用且性能更高。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1.  将 `FileGet` 替换为 `FileGetObject`。  
  
2.  将 `Object` 参数强制转换为一个更明确的类型。  
  
## <a name="see-also"></a>另请参阅  
 [不在生成中： FileGetObject 函数](http://msdn.microsoft.com/en-us/3eda786b-d1ee-4b44-9dd7-0ea6bff072c0)  
 [My.Computer.FileSystem 对象](../../visual-basic/language-reference/objects/my-computer-filesystem-object.md)
