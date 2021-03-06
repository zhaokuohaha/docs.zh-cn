---
title: "如何：访问 Windows 窗体 DataGridViewComboBoxCell 下拉列表中的对象"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], accessing objects in combo box cells
- combo boxes [Windows Forms], in DataGridView control
- combo boxes [Windows Forms], accessing objects in DataGridViewComboBoxCell drop-down lists
ms.assetid: bcbe794a-d1fa-47f8-b5a3-5f085b32097d
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: a0fac2e73e76ad49a5b1ce6942f3ae2b4c0584e3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-access-objects-in-a-windows-forms-datagridviewcomboboxcell-drop-down-list"></a>如何：访问 Windows 窗体 DataGridViewComboBoxCell 下拉列表中的对象
如<xref:System.Windows.Forms.ComboBox>控件，<xref:System.Windows.Forms.DataGridViewComboBoxColumn>和<xref:System.Windows.Forms.DataGridViewComboBoxCell>类型使你能够将任意对象添加到他们的下拉列表。 使用此功能，可以表示下拉列表中的复杂状态，而无需在一个单独的集合中存储相应的对象。  
  
 与不同<xref:System.Windows.Forms.ComboBox>控件，<xref:System.Windows.Forms.DataGridView>类型不具有<xref:System.Windows.Forms.ComboBox.SelectedItem%2A>用于检索当前所选的对象的属性。 相反，必须设置<xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A?displayProperty=nameWithType>或<xref:System.Windows.Forms.DataGridViewComboBoxCell.ValueMember%2A?displayProperty=nameWithType>到业务对象上的属性名称的属性。 当用户进行的选择时，业务对象的指定的属性设置的单元格<xref:System.Windows.Forms.DataGridViewCell.Value%2A>属性。  
  
 若要检索单元格的值，通过业务对象`ValueMember`属性必须指示该属性返回对业务对象本身的引用。 因此，如果业务对象的类型不是受你控制，必须添加此属性，通过扩展通过继承的类型。  
  
 下面的过程演示如何使用填充业务对象下拉列表和检索对象到单元格<xref:System.Windows.Forms.DataGridViewCell.Value%2A>属性。  
  
### <a name="to-add-business-objects-to-the-drop-down-list"></a>若要将业务对象添加到下拉列表  
  
1.  创建一个新<xref:System.Windows.Forms.DataGridViewComboBoxColumn>和填充其<xref:System.Windows.Forms.DataGridViewComboBoxColumn.Items%2A>集合。 或者，可以将列设置<xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A>到业务对象集合的属性。 在这种情况下，但是，你不能添加"未分配"下拉列表而无需在你的集合中创建相应的业务对象。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewComboBoxObjectBinding#110](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/CS/form1.cs#110)]
     [!code-vb[System.Windows.Forms.DataGridViewComboBoxObjectBinding#110](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/vb/form1.vb#110)]  
  
2.  设置 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DisplayMember%2A> 和 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A> 属性。 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DisplayMember%2A>指示要在下拉列表中显示的业务对象的属性。 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A>指示返回到业务对象的引用的属性。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewComboBoxObjectBinding#115](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/CS/form1.cs#115)]
     [!code-vb[System.Windows.Forms.DataGridViewComboBoxObjectBinding#115](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/vb/form1.vb#115)]  
  
3.  请确保你的业务对象类型包含一个属性，返回对当前实例的引用。 此属性必须具有值分配给名为<xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A>上一步中。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewComboBoxObjectBinding#310](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/CS/form1.cs#310)]
     [!code-vb[System.Windows.Forms.DataGridViewComboBoxObjectBinding#310](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/vb/form1.vb#310)]  
  
### <a name="to-retrieve-the-currently-selected-business-object"></a>若要检索当前所选的业务对象  
  
-   获取单元格<xref:System.Windows.Forms.DataGridViewCell.Value%2A>属性并将其转换到业务对象类型。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewComboBoxObjectBinding#120](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/CS/form1.cs#120)]
     [!code-vb[System.Windows.Forms.DataGridViewComboBoxObjectBinding#120](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/vb/form1.vb#120)]  
  
## <a name="example"></a>示例  
 完整的示例演示如何使用下拉列表中的业务对象。 在示例中，<xref:System.Windows.Forms.DataGridView>控件绑定到的集合`Task`对象。 每个`Task`对象具有`AssignedTo`属性，指示`Employee`对象当前分配给该任务。 `Assigned To`列显示`Name`每个属性值分配员工或"未分配"如果`Task.AssignedTo`属性值是`null`。  
  
 若要查看此示例的行为，请执行以下步骤：  
  
1.  更改分配给在`Assigned To`通过从下拉列表中选择不同的值或按 CTRL + 0，在组合框单元格的列。  
  
2.  单击`Generate Report`以显示当前的分配。 此示例，演示中的更改`Assigned To`列自动更新`tasks`集合。  
  
3.  单击`Request Status`按钮以调用`RequestStatus`当前方法`Employee`该行的对象。 此示例演示已成功检索所选的对象。  
  
 [!code-csharp[System.Windows.Forms.DataGridViewComboBoxObjectBinding#000](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/CS/form1.cs#000)]
 [!code-vb[System.Windows.Forms.DataGridViewComboBoxObjectBinding#000](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewComboBoxObjectBinding/vb/form1.vb#000)]  
  
## <a name="compiling-the-code"></a>编译代码  
 此示例需要：  
  
-   对 System 和 System.Windows.Forms 程序集的引用。  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridViewComboBoxColumn>  
 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.Items%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewComboBoxCell>  
 <xref:System.Windows.Forms.DataGridViewComboBoxCell.Items%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewComboBoxCell.DataSource%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewComboBoxCell.ValueMember%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewCell.Value%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.ComboBox>  
 [在 Windows 窗体 DataGridView 控件中显示数据](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
