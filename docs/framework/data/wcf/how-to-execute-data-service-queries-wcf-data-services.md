---
title: 如何：执行数据服务查询 （WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- querying the data service [WCF Data Services]
- WCF Data Services, querying
- WCF Data Services, accessing data
ms.assetid: 62997821-e0c6-4c4d-9fb7-1273fb5e5d18
ms.openlocfilehash: b68595285eb5ec06be86c771733f7bb9036c9f21
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154968"
---
# <a name="how-to-execute-data-service-queries-wcf-data-services"></a>如何：执行数据服务查询 （WCF 数据服务）
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] 可以从基于.NET Framework 的客户端应用程序的数据服务查询通过使用生成的客户端数据服务类。 可以使用下列方法之一执行查询：  
  
-   针对从 <xref:System.Data.Services.Client.DataServiceQuery%601> 工具所生成的 <xref:System.Data.Services.Client.DataServiceContext> 获取的命名 `Add Data Service Reference` 执行 LINQ 查询。  
  
-   隐式枚举从 <xref:System.Data.Services.Client.DataServiceQuery%601> 工具所生成的 <xref:System.Data.Services.Client.DataServiceContext> 获取的命名 `Add Data Service Reference`。  
  
-   显式调用 <xref:System.Data.Services.Client.DataServiceContext.Execute%2A> 的 <xref:System.Data.Services.Client.DataServiceQuery%601> 方法，或显式调用用于异步执行的 <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A> 方法。  
  
 有关详细信息，请参阅[查询数据服务](../../../../docs/framework/data/wcf/querying-the-data-service-wcf-data-services.md)。  
  
 本主题中的示例使用罗斯文示例数据服务和自动生成的客户端数据服务类。 完成后，将创建此服务和客户端数据类[WCF Data Services 快速入门](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)。  
  
## <a name="example"></a>示例  
 下面的示例演示如何定义和执行针对 Northwind 数据服务返回所有 `Customers` 的 LINQ 查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomersLinq](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#getallcustomerslinq)]
 [!code-vb[Astoria Northwind Client#GetAllCustomersLinq](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#getallcustomerslinq)]  
  
## <a name="example"></a>示例  
 下面的示例演示如何使用“`Add Data Service Reference`”工具所生成的上下文来隐式执行针对 Northwind 数据服务返回所有 `Customers` 的查询。 该上下文自动确定请求的 `Customers` 实体集的 URI。 在发生枚举时隐式执行该查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomers](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#getallcustomers)]
 [!code-vb[Astoria Northwind Client#GetAllCustomers](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#getallcustomers)]  
  
## <a name="example"></a>示例  
 下面的示例演示如何使用 <xref:System.Data.Services.Client.DataServiceContext> 显式执行针对 Northwind 数据服务返回所有 `Customers` 的查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomersExplicit](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#getallcustomersexplicit)]
 [!code-vb[Astoria Northwind Client#GetAllCustomersExplicit](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#getallcustomersexplicit)]  
  
## <a name="see-also"></a>请参阅

- [如何：将查询选项添加到数据服务查询](../../../../docs/framework/data/wcf/how-to-add-query-options-to-a-data-service-query-wcf-data-services.md)
