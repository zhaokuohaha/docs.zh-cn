---
title: "如何：在 Windows 窗体 TextBox 控件中选择文本"
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
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], selecting text programmatically
- text boxes [Windows Forms], selecting text programmatically
- text [Windows Forms], selecting in text boxes programmatically
ms.assetid: 8c591546-6a01-45c7-8e03-f78431f903b1
caps.latest.revision: "24"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 08ad19f3daca43fb33e845b632ac7d92b00f544c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-select-text-in-the-windows-forms-textbox-control"></a>如何：在 Windows 窗体 TextBox 控件中选择文本
你可在 Windows 窗体中以编程方式选择文本<xref:System.Windows.Forms.TextBox>控件。 例如，如果你创建搜索特定字符串文本的函数，你可以选择要以可视方式警报找到的字符串的位置的读取者的文本。  
  
### <a name="to-select-text-programmatically"></a>若要以编程方式选择文本  
  
1.  设置<xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A>到想要选择的文本开头的属性。  
  
     <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A>属性为一个数字，指示插入点的文本字符串内，则为 0 表示最左边的位置。 如果<xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A>属性设置为值等于或大于的字符数的文本框中，插入点被置于最后一个字符之后。  
  
2.  设置<xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A>属性设置为你想要选择的文本的长度。  
  
     <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A>属性是一个数字值，设置插入点的宽度。 设置<xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A>为大数字不是 0 导致要选择的字符数，从当前的插入点。  
  
3.  （可选）访问通过所选的文本<xref:System.Windows.Forms.TextBoxBase.SelectedText%2A>属性。  
  
     选择下面的代码的文本内容框中时控件的<xref:System.Windows.Forms.Control.Enter>事件发生。 此示例检查文本框中是否具有的值<xref:System.Windows.Forms.TextBox.Text%2A>属性不是`null`或空字符串。 在文本框中接收到焦点，在文本框中的当前文本选择。 `TextBox1_Enter`事件处理程序必须绑定到控件; 有关详细信息，请参阅[如何： 在运行时添加的 Windows 窗体创建事件处理程序](../../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md)。  
  
     若要测试此示例，请按 Tab 键，直到文本框中获得焦点。 如果你单击文本框中，将取消选中文本。  
  
    ```vb  
    Private Sub TextBox1_Enter(ByVal sender As Object, ByVal e As System.EventArgs) Handles TextBox1.Enter  
       If (Not String.IsNullOrEmpty(TextBox1.Text)) Then  
          TextBox1.SelectionStart = 0  
          TextBox1.SelectionLength = TextBox1.Text.Length  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_Enter(object sender, System.EventArgs e){  
       if (!String.IsNullOrEmpty(textBox1.Text))  
       {  
          textBox1.SelectionStart = 0;  
          textBox1.SelectionLength = textBox1.Text.Length;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void textBox1_Enter(System::Object ^ sender,  
          System::EventArgs ^ e) {  
       if (!System::String::IsNullOrEmpty(textBox1->Text))  
       {  
          textBox1->SelectionStart = 0;  
          textBox1->SelectionLength = textBox1->Text->Length;  
       }  
    }  
    ```  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Windows.Forms.TextBox>  
 [TextBox 控件概述](../../../../docs/framework/winforms/controls/textbox-control-overview-windows-forms.md)  
 [如何：在 Windows 窗体 TextBox 控件中控制插入点](../../../../docs/framework/winforms/controls/how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)  
 [如何：使用 Windows 窗体 TextBox 控件创建密码文本框](../../../../docs/framework/winforms/controls/how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)  
 [如何：创建只读文本框](../../../../docs/framework/winforms/controls/how-to-create-a-read-only-text-box-windows-forms.md)  
 [如何：在字符串中添加引号](../../../../docs/framework/winforms/controls/how-to-put-quotation-marks-in-a-string-windows-forms.md)  
 [如何：在 Windows 窗体 TextBox 控件中查看多个行](../../../../docs/framework/winforms/controls/how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)  
 [TextBox 控件](../../../../docs/framework/winforms/controls/textbox-control-windows-forms.md)
