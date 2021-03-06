---
title: 지원 되는 Microsoft 365 Defender Api
description: 지원 되는 Microsoft 365 Defender Api
keywords: MTP, Api, api
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: b7c0accf2d649d4ad6177260294922ee17783f2c
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844963"
---
# <a name="supported-microsoft-365-defender-apis"></a>지원 되는 Microsoft 365 Defender Api 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

**적용 대상:**
- Microsoft 365 Defender

>[!IMPORTANT] 
>일부 정보는 상업적으로 출시 되기 전에 크게 수정 될 수 있는 prereleased 제품과 관련 되어 있습니다. Microsoft makes no warranties, express or implied, with respect to the information provided here.


### <a name="end-point-uris"></a>끝점 Uri:

- 서비스 기본 URI는 다음과 같습니다. https://api.security.microsoft.com <br>

>[!NOTE]
>성능 향상을 위해 서버를 지리적 위치에 더 가깝게 사용할 수 있습니다.
> - api-us.security.microsoft.com
> - api-eu.security.microsoft.com
> - api-uk.security.microsoft.com

 - 토큰 취득 리소스는 다음과 같아야 합니다. https://api.security.microsoft.com

 - Path 아래의 모든 Api는 ```/api``` OData api입니다. 예:. ```https://api.security.microsoft.com/api/incidents```

## <a name="list-of-available-apis"></a>사용 가능한 Api 목록:

항목 | 설명
:---|:---
[고급 헌팅 API](api-advanced-hunting.md) | API에서 고급 구하기 쿼리를 실행 합니다.
[인시던트 API](api-incident.md) | 인시던트 목록, 업데이트 인시던트 등의 관련 API 호출을 실행 합니다.
