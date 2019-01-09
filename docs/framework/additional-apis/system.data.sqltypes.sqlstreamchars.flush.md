---
title: SqlStreamChars.Flush 方法 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Flush
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: ecaf7932a4e832a88b883ceac4746afe6140b38e
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152740"
---
# <a name="sqlstreamcharsflush-method"></a><span data-ttu-id="d255c-102">SqlStreamChars.Flush 方法</span><span class="sxs-lookup"><span data-stu-id="d255c-102">SqlStreamChars.Flush Method</span></span>

<span data-ttu-id="d255c-103">当在派生类中重写时，将清除该流的所有缓冲区，并使得所有缓冲数据被写入到基础设备。</span><span class="sxs-lookup"><span data-stu-id="d255c-103">When overridden in a derived class, clears all buffers for this stream and causes any buffered data to be written to the underlying device.</span></span> <span data-ttu-id="d255c-104">包含此方法的程序集具有与 SQLAccess.dll 友元关系。</span><span class="sxs-lookup"><span data-stu-id="d255c-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="d255c-105">它被用于 SQL server 上。</span><span class="sxs-lookup"><span data-stu-id="d255c-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="d255c-106">对于其他数据库，使用提供该数据库的宿主机制。</span><span class="sxs-lookup"><span data-stu-id="d255c-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d255c-107">语法</span><span class="sxs-lookup"><span data-stu-id="d255c-107">Syntax</span></span>

```csharp
public abstract void Flush ();
```

## <a name="remarks"></a><span data-ttu-id="d255c-108">备注</span><span class="sxs-lookup"><span data-stu-id="d255c-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="d255c-109">`SqlStreamChars.Flush`方法是私有的不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="d255c-109">The `SqlStreamChars.Flush` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="d255c-110">Microsoft 不支持在生产应用程序在任何情况下使用此字段。</span><span class="sxs-lookup"><span data-stu-id="d255c-110">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="d255c-111">要求</span><span class="sxs-lookup"><span data-stu-id="d255c-111">Requirements</span></span>

<span data-ttu-id="d255c-112">**Namespace**：<xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="d255c-112">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="d255c-113">**程序集：** System.Data （在 System.Data.dll 中)</span><span class="sxs-lookup"><span data-stu-id="d255c-113">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="d255c-114">**.NET framework 版本：** 自 2.0 之后可用。</span><span class="sxs-lookup"><span data-stu-id="d255c-114">**.NET Framework versions:** Available since 2.0.</span></span>