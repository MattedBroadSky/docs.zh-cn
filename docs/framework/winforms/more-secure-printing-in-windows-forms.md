---
title: Windows 窗体中的更加安全的打印
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, printing
- PrintingPermission class [Windows Forms], Windows Forms security
- printing [Windows Forms], security
- security [Windows Forms], printing
ms.assetid: 48fd36ac-872f-4de0-902a-e52969cd4367
ms.openlocfilehash: 5ee170980ed02d90606c774e2a7055f047292e33
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197355"
---
# <a name="more-secure-printing-in-windows-forms"></a>Windows 窗体中的更加安全的打印
Windows 窗体应用程序通常包括打印功能。 [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)]使用<xref:System.Drawing.Printing.PrintingPermission>类控制对打印功能的访问，关联<xref:System.Drawing.Printing.PrintingPermissionLevel>枚举值，以指示的访问级别。 默认情况下，在本地 Intranet 和 Internet 区域中; 默认情况下启用打印但是，在这两个区域受到限制的访问级别。 是否可以打印您的应用程序，需要用户交互或不能打印取决于授予应用程序的权限值。 默认情况下，本地 Intranet 区域接收<xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting>访问权限和 Intranet 区域接收<xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting>访问。  
  
 下表显示了在每个打印的权限级别可用的功能。  
  
|PrintingPermissionLevel|描述|  
|-----------------------------|-----------------|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.AllPrinting>|提供对所有已安装打印机的完全访问权限。|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting>|可以以编程方式打印到默认打印机和限制性的打印对话框通过更安全的打印。 <xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting> 是的子集<xref:System.Drawing.Printing.PrintingPermissionLevel.AllPrinting>。|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting>|仅从更多限制的对话框提供打印。 <xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting> 是的子集<xref:System.Drawing.Printing.PrintingPermissionLevel.DefaultPrinting>。|  
|<xref:System.Drawing.Printing.PrintingPermissionLevel.NoPrinting>|禁止对打印机的访问权限。 <xref:System.Drawing.Printing.PrintingPermissionLevel.NoPrinting> 是的子集<xref:System.Drawing.Printing.PrintingPermissionLevel.SafePrinting>。|  
  
## <a name="see-also"></a>请参阅

- [Windows 窗体中更加安全的文件和数据访问](more-secure-file-and-data-access-in-windows-forms.md)
- [Windows 窗体中额外的安全注意事项](additional-security-considerations-in-windows-forms.md)
- [Windows 窗体中的安全性概述](security-in-windows-forms-overview.md)
- [Windows 窗体安全](windows-forms-security.md)
