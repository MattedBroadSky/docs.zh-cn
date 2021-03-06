---
title: 如何：使用通道工厂以异步方式调用操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cc17dd47-b9ad-451c-a362-e36e0aac7ba0
ms.openlocfilehash: 0662b82661e4fb3cde85930c2c4544f541d3a2a8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59202724"
---
# <a name="how-to-call-operations-asynchronously-using-a-channel-factory"></a>如何：使用通道工厂以异步方式调用操作
本主题介绍客户端如何在使用基于 <xref:System.ServiceModel.ChannelFactory%601> 的客户端应用程序时以异步方式访问服务操作。 （当使用 <xref:System.ServiceModel.ClientBase%601?displayProperty=nameWithType> 对象调用服务时，可以使用事件驱动的异步调用模型。 有关详细信息，请参阅[如何：以异步方式调用服务操作](../../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md)。 有关基于事件的异步调用模型的详细信息，请参阅[基于事件的异步模式 (EAP)](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md)。)  
  
 本主题中的服务可实现 `ICalculator` 接口。 客户端可以在此接口上以异步方式调用操作，这意味着像 `Add` 这样的操作将拆分为两个方法：`BeginAdd` 和 `EndAdd`。前一个方法启动调用，而后一个方法在操作完成时检索结果。 有关演示如何在服务中异步实现操作的示例，请参阅[如何：实现异步服务操作](../../../../docs/framework/wcf/how-to-implement-an-asynchronous-service-operation.md)。 有关同步和异步操作的详细信息，请参阅[同步和异步操作](../../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md)。  
  
## <a name="procedure"></a>过程  
  
#### <a name="to-call-wcf-service-operations-asynchronously"></a>以异步方式调用 WCF 服务操作  
  
1.  运行[ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)工具用于`/async`选项，如以下命令中所示。  
  
    ```  
    svcutil /n:http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples http://localhost:8000/servicemodelsamples/service/mex /a  
    ```  
  
     这将生成该操作的服务协定的异步客户端版本。  
  
2.  创建一个异步操作完成时将要调用的回调函数，如下面的示例代码所示。  
  
     [!code-csharp[C_How_To_CF_Async#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#2)]
     [!code-vb[C_How_To_CF_Async#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#2)]  
  
3.  若要以异步方式访问服务操作，请创建客户端、调用 `Begin[Operation]`（例如 `BeginAdd`），并指定一个回调函数，如下面的示例代码所示。  
  
     [!code-csharp[C_How_To_CF_Async#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#3)]
     [!code-vb[C_How_To_CF_Async#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#3)]  
  
     执行该回调函数时，客户端将调用 `End<operation>`（例如 `EndAdd`）以检索结果。  
  
## <a name="example"></a>示例  
 上面过程中的客户端代码使用的服务可实现 `ICalculator` 接口，如下面的代码所示。 在服务端`Add`和`Subtract`协定的操作同步调用通过 Windows Communication Foundation (WCF) 运行时，即使前面的客户端步骤在客户端上以异步方式调用也是如此。 在服务端，`Multiply` 和 `Divide` 操作用于在服务端以异步方式调用服务，即使客户端以同步方式调用这两个操作也是如此。 此示例将 <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A> 属性设置为 `true`。 此属性设置与 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 异步模式的实现一起，可让运行库以异步方式调用该操作。  
  
 [!code-csharp[C_How_To_CF_Async#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/service.cs#4)]
 [!code-vb[C_How_To_CF_Async#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/service.vb#4)]  
