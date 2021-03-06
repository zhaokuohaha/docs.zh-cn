---
title: "如何：从 TextBox 获取线条集合"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: bb771cdb4d12ebaa5160ec16ca57ba6acf011222
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a>如何：从 TextBox 获取线条集合
此示例演示如何获取的从文本的行集合<xref:System.Windows.Controls.TextBox>。  
  
## <a name="example"></a>示例  
 下面的示例演示一个简单的方法，采用<xref:System.Windows.Controls.TextBox>作为自变量，并返回<xref:System.Collections.Specialized.StringCollection>包含中的文本行**文本框中**。  <xref:System.Windows.Controls.TextBox.LineCount%2A>属性用于确定多少行是当前处于**文本框中**，和<xref:System.Windows.Controls.TextBox.GetLineText%2A>方法然后用于提取每个行并将其添加到的行的集合。  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a>另请参阅  
 [TextBox 概述](../../../../docs/framework/wpf/controls/textbox-overview.md)  
 [RichTextBox 概述](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
