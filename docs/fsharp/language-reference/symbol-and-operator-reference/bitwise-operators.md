---
title: 비트 연산자(F#)
description: 'F # 프로그래밍 언어에서 사용할 수 있는 비트 연산자에 알아봅니다.'
ms.date: 07/20/2018
ms.openlocfilehash: ed76fcf5f9c569a2f288cf260e99dc29fd65ef3b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47205241"
---
# <a name="bitwise-operators"></a>비트 연산자

이 항목에서는 F # 언어에서 사용할 수 있는 비트 연산자를 설명 합니다.

## <a name="summary-of-bitwise-operators"></a>비트 연산자 요약

다음 표에서 F # 언어에서 unboxed 정수 계열 형식에 대 한 지원 되는 비트 연산자를 설명 합니다.

|연산자|노트|
|--------|-----|
|`&&&`|비트 AND 연산자입니다. 결과 비트는 모두 소스 피연산자의 해당 비트가 1 하는 경우에 1 값을 갖습니다.|
|<code>&#124;&#124;&#124;</code>|비트 OR 연산자입니다. 결과 비트의에서 경우 값 1을 가질 원본의 해당 비트의 두 피연산자가 1입니다.|
|`^^^`|비트 배타적 OR 연산자입니다. 결과 비트는 소스 피연산자의 비트 같지 않은 값이 있는 경우에 값 1을 갖습니다.|
|`~~~`|비트 부정 연산자입니다. 단항 연산자 이며는 소스 피연산자의 0 비트가 모두 1 비트 변환 되 고 1 비트가 모두 0 비트로 변환할 결과 생성 합니다.|
|`<<<`|비트 왼쪽 시프트 연산자입니다. Bits 사용 하 여 첫 번째 피연산자는 두 번째 피연산자의 비트 수 만큼 왼쪽 이동 됩니다. 가장 중요 하지 않은 위치에 가장 중요 한 위치에서 벗어나 이동한 비트 회전 되지 않습니다. 최하위 비트는 0으로 채워집니다. 두 번째 인수의 형식이 `int32`합니다.|
|`>>>`|비트 오른쪽 시프트 연산자입니다. 결과 두 번째 피연산자의 비트 수 만큼 오른쪽으로 이동 하는 비트를 사용 하 여 첫 번째 피연산자입니다. 가장 중요 한 위치에 가장 중요 하지 않은 위치에서 벗어나 이동한 비트 회전 되지 않습니다. 부호 없는 형식에 대 한 최상위 비트는 0으로 채워집니다. 음수 값 부호 있는 형식에 대 한 최상위 비트는 1로 채워집니다. 두 번째 인수의 형식이 `int32`합니다.|

형식은 비트 연산자를 사용 하 여 사용할 수: `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`를 `uint32`, `int64`를 `uint64`, `nativeint`, 및 `unativeint`합니다.

## <a name="see-also"></a>참고자료

- [기호 및 연산자 참조](index.md)
- [산술 연산자](arithmetic-operators.md)
- [부울 연산자](boolean-operators.md)
