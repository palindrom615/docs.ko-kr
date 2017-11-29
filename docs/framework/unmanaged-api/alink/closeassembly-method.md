---
title: "CloseAssembly 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location: alink.dll
api_type: COM
f1_keywords: CloseAssembly
helpviewer_keywords: CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type: apiref
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: be68348b619f342eca4841a6052088bf7152f453
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="closeassembly-method"></a><span data-ttu-id="2e4a7-102">CloseAssembly 메서드</span><span class="sxs-lookup"><span data-stu-id="2e4a7-102">CloseAssembly Method</span></span>
<span data-ttu-id="2e4a7-103">어셈블리 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e4a7-103">Finalizes assembly operations.</span></span> <span data-ttu-id="2e4a7-104">새 어셈블리 또는 바인딩되지 않은 모듈을 시작 하기 전에이 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e4a7-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e4a7-105">구문</span><span class="sxs-lookup"><span data-stu-id="2e4a7-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2e4a7-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e4a7-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="2e4a7-107">어셈블리의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e4a7-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2e4a7-108">반환 값</span><span class="sxs-lookup"><span data-stu-id="2e4a7-108">Return Value</span></span>  
 <span data-ttu-id="2e4a7-109">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e4a7-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2e4a7-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e4a7-110">Requirements</span></span>  
 <span data-ttu-id="2e4a7-111">Alink.h가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2e4a7-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e4a7-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2e4a7-112">See Also</span></span>  
 [<span data-ttu-id="2e4a7-113">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2e4a7-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="2e4a7-114">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2e4a7-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="2e4a7-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="2e4a7-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)