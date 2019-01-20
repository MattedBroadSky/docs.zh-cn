---
title: IXCLRDataProcess::EnumModule 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: fa1e41985444324627c6b66a109b4619d85fc57f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416365"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="4df42-102">IXCLRDataProcess::EnumModule 方法</span><span class="sxs-lookup"><span data-stu-id="4df42-102">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="4df42-103">枚举此进程的模块。</span><span class="sxs-lookup"><span data-stu-id="4df42-103">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="4df42-104">语法</span><span class="sxs-lookup"><span data-stu-id="4df42-104">Syntax</span></span>

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

### <a name="parameters"></a><span data-ttu-id="4df42-105">参数</span><span class="sxs-lookup"><span data-stu-id="4df42-105">Parameters</span></span>

<span data-ttu-id="4df42-106">`handle` [in、 out]枚举模块句柄。</span><span class="sxs-lookup"><span data-stu-id="4df42-106">`handle` [in, out] A handle for enumerating the modules.</span></span>

<span data-ttu-id="4df42-107">`mod` [out]枚举的模块。</span><span class="sxs-lookup"><span data-stu-id="4df42-107">`mod` [out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df42-108">备注</span><span class="sxs-lookup"><span data-stu-id="4df42-108">Remarks</span></span>

<span data-ttu-id="4df42-109">提供的方法属于`IXCLRDataProcess`接口，并对应于虚拟方法表 25 槽。</span><span class="sxs-lookup"><span data-stu-id="4df42-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df42-110">要求</span><span class="sxs-lookup"><span data-stu-id="4df42-110">Requirements</span></span>

<span data-ttu-id="4df42-111">**平台：** 请参阅[系统需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4df42-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="4df42-112">**标头：** 无</span><span class="sxs-lookup"><span data-stu-id="4df42-112">**Header:** None</span></span>  
<span data-ttu-id="4df42-113">**库：** 无</span><span class="sxs-lookup"><span data-stu-id="4df42-113">**Library:** None</span></span>  
<span data-ttu-id="4df42-114">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4df42-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="4df42-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="4df42-115">See Also</span></span>

- [<span data-ttu-id="4df42-116">CLRDataSourceType 枚举</span><span class="sxs-lookup"><span data-stu-id="4df42-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="4df42-117">调试</span><span class="sxs-lookup"><span data-stu-id="4df42-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="4df42-118">IXCLRDataModule 接口</span><span class="sxs-lookup"><span data-stu-id="4df42-118">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
- [<span data-ttu-id="4df42-119">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="4df42-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)