---
title: "如何：同步定位时钟"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clocks [WPF], seeking synchronously
- seeking clocks synchronously [WPF]
ms.assetid: e5b7529b-b7d0-40d2-9e1d-fa4b5e736e96
caps.latest.revision: "4"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 8d158629b428bda8e7749df393ad0724225b5a0a
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-seek-a-clock-synchronously"></a>如何：同步定位时钟
使用<xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A>方法要查找的特定点时钟同步。 下面的示例演示<xref:System.Windows.Media.Animation.ClockController.Seek%2A>和<xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A>方法<xref:System.Windows.Media.Animation.ClockController>。  
  
 此示例演示如何查找<xref:System.Windows.Media.Animation.Clock>; 的一个示例，演示如何查找情节提要，请参阅[情节提要同步搜寻](../../../../docs/framework/wpf/graphics-multimedia/how-to-seek-a-storyboard-synchronously.md)。  
  
## <a name="example"></a>示例  
 [!code-csharp[ClockController_procedural_snip#ClockControllerSeekExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ClockController_procedural_snip/CSharp/SeekAlignedToLastTickExample.cs#clockcontrollerseekexample)]
 [!code-vb[ClockController_procedural_snip#ClockControllerSeekExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ClockController_procedural_snip/visualbasic/seekalignedtolasttickexample.vb#clockcontrollerseekexample)]
