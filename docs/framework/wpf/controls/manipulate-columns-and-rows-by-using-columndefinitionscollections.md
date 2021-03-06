---
title: 如何：使用 ColumnDefinitionsCollection 和 RowDefinitionsCollection 操作列和行
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Grid class
- Grid control [WPF], ColumnDefinitionCollection class
- Grid control [WPF], RowDefinitionCollection class
ms.assetid: bfc7160a-45f2-4e17-9961-df414dfb13c5
ms.openlocfilehash: f316cced076223edba1d39c9cfb21b9a504b9eee
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59147727"
---
# <a name="how-to-manipulate-columns-and-rows-by-using-columndefinitionscollections-and-rowdefinitionscollections"></a>如何：使用 ColumnDefinitionsCollection 和 RowDefinitionsCollection 操作列和行
此示例演示如何使用中的方法<xref:System.Windows.Controls.ColumnDefinitionCollection>和<xref:System.Windows.Controls.RowDefinitionCollection>类执行的操作，例如添加、 清除或计数的行或列的内容。 例如，可以<xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A>， <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A>，或<xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A>中包含的项<xref:System.Windows.Controls.ColumnDefinition>或<xref:System.Windows.Controls.RowDefinition>。  
  
## <a name="example"></a>示例  
 下面的示例创建<xref:System.Windows.Controls.Grid>具有元素<xref:System.Windows.FrameworkElement.Name%2A>的`grid1`。 <xref:System.Windows.Controls.Grid>包含<xref:System.Windows.Controls.StackPanel>，它持有<xref:System.Windows.Controls.Button>元素，每个受不同的集合方法。 当您单击<xref:System.Windows.Controls.Button>，则会激活的代码隐藏文件中的方法调用。  
  
 [!code-xaml[ColumnDefinitionsGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml#1)]  
  
 此示例中定义的自定义方法，每个对应于一系列<xref:System.Windows.Controls.Primitives.ButtonBase.Click>中的事件[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]文件。 可以更改的列和中的行数<xref:System.Windows.Controls.Grid>中有多种，其中包括添加或删除行和列; 以及计算行和列的总数。 若要防止<xref:System.ArgumentOutOfRangeException>和<xref:System.ArgumentException>异常，您可以使用错误检查功能的<xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A>方法提供。  
  
 [!code-csharp[ColumnDefinitionsGrid#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ColumnDefinitionsGrid#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ColumnDefinitionsGrid/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.ColumnDefinitionCollection>
- <xref:System.Windows.Controls.RowDefinitionCollection>
