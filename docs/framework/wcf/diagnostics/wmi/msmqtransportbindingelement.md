---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 706cec5c414197ebabda7939728b95be32582e0f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197927"
---
# <a name="msmqtransportbindingelement"></a>MsmqTransportBindingElement
MsmqTransportBindingElement  
  
## <a name="syntax"></a>语法  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a>方法  
 MsmqTransportBindingElement 类不定义任何方法。  
  
## <a name="properties"></a>属性  
 MsmqTransportBindingElement 类具有以下属性：  
  
### <a name="maxpoolsize"></a>MaxPoolSize  
 数据类型：sint32  
  
 访问类型：只读  
  
 包含内部 MSMQ 消息对象的池的最大大小。  
  
### <a name="queuetransferprotocol"></a>QueueTransferProtocol  
 数据类型：String  
  
 访问类型：只读  
  
 一个枚举值，指示此绑定使用的排队通信通道传输。  
  
### <a name="useactivedirectory"></a>UseActiveDirectory  
 数据类型：Boolean  
  
 访问类型：只读  
  
 返回一个布尔值，该值指示是否应该使用 Active Directory 来转换队列地址。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
