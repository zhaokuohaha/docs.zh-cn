---
title: "-doc（C# 编译器选项）"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords:
- FileProperties.BuildAction
- /doc
helpviewer_keywords:
- comments, C# code
- XML documentation [C#], comments in source files
- doc compiler option [C#]
- Visual C#, XML documentation for
- -doc compiler option [C#]
- /doc compiler option [C#]
ms.assetid: 849eea59-c936-4311-bad8-d07404480f2a
caps.latest.revision: "19"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: ae3d6e1ffdaaa3245a51005070b16041c16dadae
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="doc-c-compiler-options"></a>/doc（C# 编译器选项）
**/doc** 选项可让你在 XML 文件中放置文档注释。  
  
## <a name="syntax"></a>语法  
  
```console  
/doc:file  
```  
  
## <a name="arguments"></a>自变量  
 `file`  
 XML 的输出文件（由编译的源代码文件中的注释填充）。  
  
## <a name="remarks"></a>备注  
 在源代码文件中，可以处理以下内容之前的文档注释，并将其添加到 XML 文件中：  
  
-   作为[类](../../../csharp/language-reference/keywords/class.md)、[委托](../../../csharp/language-reference/keywords/delegate.md)或[接口](../../../csharp/language-reference/keywords/interface.md)的用户定义类型  
  
-   作为字段、[事件](../../../csharp/language-reference/keywords/event.md)、[属性](../../../csharp/programming-guide/classes-and-structs/using-properties.md)或方法的成员  
  
 包含 Main 的源代码文件首先输出到 XML 中。  
  
 若要将生成的 xml 文件与 [IntelliSense](/visualstudio/ide/using-intellisense) 功能配合使用，请将 .xml 文件的文件名设为与要支持的程序集相同的名称，然后确保 .xml 文件与程序集位于同一目录中。 这样，在 Visual Studio 项目中引用程序集时，也会找到 .xml 文件。 有关详细信息，请参阅[提供代码注释](/visualstudio/ide/supplying-xml-code-comments)。  
  
 除非用 [/target:module](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md) 进行编译，否则 `file` 将包含 \<assembly>\</assembly> 标记，以指定包含编译输出文件的程序集清单的文件名。  
  
> [!NOTE]
>  /doc 选项适用于所有输入文件；或者，如果在项目设置中进行设置，则适用于项目中的所有文件。 若要禁用与特定文件或一段代码的文档注释相关的警告，请使用 [#pragma 警告](../../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md)。  
  
 有关从代码中的注释生成文档的方法，请参阅[建议的文档注释标记](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)。  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此编译器选项  
  
1.  打开项目的“属性”页。  
  
2.  单击“生成”选项卡。  
  
3.  修改“XML 文档文件”属性。  
  
 有关如何以编程方式设置此编译器选项的信息，请参阅 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.DocumentationFile%2A>。  
  
## <a name="see-also"></a>另请参阅  
 [C# 编译器选项](../../../csharp/language-reference/compiler-options/index.md)  
 [管理项目和解决方案属性](/visualstudio/ide/managing-project-and-solution-properties)
