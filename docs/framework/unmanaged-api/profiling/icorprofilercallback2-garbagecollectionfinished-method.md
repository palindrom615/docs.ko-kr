---
title: "ICorProfilerCallback2::GarbageCollectionFinished 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback2.GarbageCollectionFinished
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback2::GarbageCollectionFinished
helpviewer_keywords:
- ICorProfilerCallback2::GarbageCollectionFinished method [.NET Framework profiling]
- GarbageCollectionFinished method [.NET Framework profiling]
ms.assetid: 1a5758ea-2354-43c0-92a3-32c9909d64e1
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 287c33a80144b9b04fd7e0797071d40e46a52454
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback2garbagecollectionfinished-method"></a><span data-ttu-id="93226-102">ICorProfilerCallback2::GarbageCollectionFinished 메서드</span><span class="sxs-lookup"><span data-stu-id="93226-102">ICorProfilerCallback2::GarbageCollectionFinished Method</span></span>
<span data-ttu-id="93226-103">가비지 수집이 완료 되 고 해당 되는 모든 가비지 수집 콜백이 실행 되었음을 프로파일러에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="93226-103">Notifies the profiler that garbage collection has completed and all garbage collection callbacks have been issued for it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93226-104">구문</span><span class="sxs-lookup"><span data-stu-id="93226-104">Syntax</span></span>  
  
```  
HRESULT GarbageCollectionFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="93226-105">설명</span><span class="sxs-lookup"><span data-stu-id="93226-105">Remarks</span></span>  
 <span data-ttu-id="93226-106">최종 위치에 개체 검사를 프로파일러에 대 한 안전 때는 `GarbageCollectionFinished` 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="93226-106">It is safe for the profiler to inspect objects in their final locations when the `GarbageCollectionFinished` method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93226-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="93226-107">Requirements</span></span>  
 <span data-ttu-id="93226-108">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="93226-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93226-109">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="93226-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="93226-110">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93226-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93226-111">**.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93226-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93226-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="93226-112">See Also</span></span>  
 [<span data-ttu-id="93226-113">ICorProfilerCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="93226-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="93226-114">ICorProfilerCallback2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="93226-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)