---
title: System.Convert 方法
ms.date: 03/30/2017
ms.assetid: 3ca6c5b6-ea5d-4ab0-b675-f082135b342c
ms.openlocfilehash: 0d98d159c24e1a47723aeb07a9654fe22b1d9464
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198213"
---
# <a name="systemconvert-methods"></a>System.Convert 方法
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 不支持以下<xref:System.Convert>方法。  
  
-   带有 <xref:System.IFormatProvider> 参数的版本。  
  
-   涉及字符数组或字节数组的方法：  
  
    -   <xref:System.Convert.FromBase64CharArray%2A>  
  
    -   <xref:System.Convert.ToBase64CharArray%2A>  
  
    -   <xref:System.Convert.FromBase64String%2A>  
  
    -   <xref:System.Convert.ToBase64String%2A>  
  
-   以下方法：  
  
    -   `public static <Type2> To<Type2>(<Type1> value);` 其中  
  
         `Type1` 并`Type2`是每个`sbyte`， `uint`， `ulong`，或`ushort`。  
  
    -   C#：  
  
         `int To<int type>(string value, int fromBase),`  
  
         `ToString(... value, int toBase)`  
  
    -   Visual Basic：  
  
         `Function To(Of [Numeric])(value as String, fromBase As Integer)`  
  
         `As [Numeric], ToString( value As …, toBase As Integer)`  
  
    -   <xref:System.Convert.IsDBNull%2A>  
  
    -   <xref:System.Convert.GetTypeCode%2A>  
  
    -   <xref:System.Convert.ChangeType%2A>  
  
## <a name="see-also"></a>请参阅

- [数据类型和函数](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
