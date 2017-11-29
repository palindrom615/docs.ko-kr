---
title: "예외: invalidArg 함수(F#)"
description: "F # 'invalidArg' 함수에서 인수 예외를 생성 하는 방법을 알아봅니다."
keywords: "visual f#, f#, 함수형 프로그래밍"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: d375b704-6b27-493e-bd1d-ee217a53c4b5
ms.openlocfilehash: 107bef361a6bd034e3d6a2227e18cf64b1b04576
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="exceptions-the-invalidarg-function"></a><span data-ttu-id="bbbd6-104">예외: invalidArg 함수</span><span class="sxs-lookup"><span data-stu-id="bbbd6-104">Exceptions: The invalidArg Function</span></span>

<span data-ttu-id="bbbd6-105">`invalidArg` 함수 인수 예외를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-105">The `invalidArg` function generates an argument exception.</span></span>


## <a name="syntax"></a><span data-ttu-id="bbbd6-106">구문</span><span class="sxs-lookup"><span data-stu-id="bbbd6-106">Syntax</span></span>

```fsharp
invalidArg parameter-name error-message-string
```

## <a name="remarks"></a><span data-ttu-id="bbbd6-107">설명</span><span class="sxs-lookup"><span data-stu-id="bbbd6-107">Remarks</span></span>
<span data-ttu-id="bbbd6-108">위 구문에서 매개 변수 이름 인 인수가 잘못 되었습니다. 매개 변수 이름 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-108">The parameter-name in the previous syntax is a string with the name of the parameter whose argument was invalid.</span></span> <span data-ttu-id="bbbd6-109">*오류 메시지 문자열* 리터럴 문자열 또는 형식의 값은 `string`합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-109">The *error-message-string* is a literal string or a value of type `string`.</span></span> <span data-ttu-id="bbbd6-110">됩니다는 `Message` 예외 개체의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-110">It becomes the `Message` property of the exception object.</span></span>

<span data-ttu-id="bbbd6-111">생성 된 예외 `invalidArg` 는 `System.ArgumentException` 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-111">The exception generated by `invalidArg` is a `System.ArgumentException` exception.</span></span> <span data-ttu-id="bbbd6-112">다음 코드에서는 `invalidArg` 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-112">The following code illustrates the use of `invalidArg` to throw an exception.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6101.fs)]

<span data-ttu-id="bbbd6-113">출력은 다음 (표시 되지 않음) 하는 스택 추적 옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbbd6-113">The output is the following, followed by a stack trace (not shown).</span></span>

```
December
January
System.ArgumentException: Month parameter out of range.
```

## <a name="see-also"></a><span data-ttu-id="bbbd6-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bbbd6-114">See Also</span></span>
[<span data-ttu-id="bbbd6-115">예외 처리</span><span class="sxs-lookup"><span data-stu-id="bbbd6-115">Exception Handling</span></span>](index.md)

[<span data-ttu-id="bbbd6-116">예외 형식</span><span class="sxs-lookup"><span data-stu-id="bbbd6-116">Exception Types</span></span>](exception-types.md)

[<span data-ttu-id="bbbd6-117">예외: `try...with` 식</span><span class="sxs-lookup"><span data-stu-id="bbbd6-117">Exceptions: The `try...with` Expression</span></span>](the-try-with-expression.md)

[<span data-ttu-id="bbbd6-118">예외: `try...finally` 식</span><span class="sxs-lookup"><span data-stu-id="bbbd6-118">Exceptions: The `try...finally` Expression</span></span>](the-try-finally-expression.md)

[<span data-ttu-id="bbbd6-119">예외: `raise` 함수</span><span class="sxs-lookup"><span data-stu-id="bbbd6-119">Exceptions: the `raise` Function</span></span>](the-raise-function.md)

[<span data-ttu-id="bbbd6-120">예외: `failwith` 함수</span><span class="sxs-lookup"><span data-stu-id="bbbd6-120">Exceptions: The `failwith` Function</span></span>](the-failwith-function.md)