---
title: 如何：绘制具有线帽的线条
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
- drawing lines [Windows Forms], line caps
ms.assetid: eb68c3e1-c400-4886-8a04-76978a429cb6
ms.openlocfilehash: c4a78569f6c0b14c32154611412d6b3ccd8a84ce
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59146206"
---
# <a name="how-to-draw-a-line-with-line-caps"></a>如何：绘制具有线帽的线条
可以在一个名为线帽的多个形状绘制的开始或结束的行。 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 支持多种线帽，如 round、 正方形、 菱形和箭头。  
  
## <a name="example"></a>示例  
 您可以指定行 （起始端），行 （末端） 的末尾或虚线 (dash cap) 的短划线开头的线帽。  
  
 下面的示例绘制一个行，其中一端箭头和另一端圆端帽。 该图显示了最终得到的行：  
  
 ![显示具有圆端帽的线条的图例。](./media/how-to-draw-a-line-with-line-caps/line-cap-arrowhead-example.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.UsingAPen#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>编译代码  
  
-   创建 Windows 窗体和处理该窗体<xref:System.Windows.Forms.Control.Paint>事件。 示例将代码粘贴到<xref:System.Windows.Forms.Control.Paint>事件处理程序传递`e`作为<xref:System.Windows.Forms.PaintEventArgs>。  
  
## <a name="see-also"></a>请参阅

- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LineCap?displayProperty=nameWithType>
- [Windows 窗体中的图形和绘制](graphics-and-drawing-in-windows-forms.md)
- [使用钢笔绘制线条和形状](using-a-pen-to-draw-lines-and-shapes.md)
