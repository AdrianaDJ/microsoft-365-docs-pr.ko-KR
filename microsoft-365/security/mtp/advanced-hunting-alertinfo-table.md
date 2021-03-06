---
title: 고급 구하기 스키마의 AlertInfo 테이블
description: 고급 구하기 스키마의 AlertInfo 테이블에 있는 경고 생성 이벤트에 대해 자세히 알아보기
keywords: 고급 구하기, 위협 사냥 사이버 위협 검색, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, table, column, AlertInfo, alert,, category, MITRE, AT&T&머리, Microsoft Defender ATP, MDATP, Office 365 ATP, Microsoft Cloud App Security, MCAS 및 Azure ATP
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 7672d974666a381a48da15e0917a46c97df88895
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847671"
---
# <a name="alertinfo"></a>AlertInfo

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**적용 대상:**
- Microsoft 365 Defender



`AlertInfo` [고급 구하기](advanced-hunting-overview.md) 스키마의 표에는 끝점에 대 한 microsoft Defender, Microsoft defender for Office 365, Microsoft Cloud App Security 및 Identity 용 microsoft defender의 경고에 대 한 정보가 포함 되어 있습니다. 이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.

고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.

| 열 이름 | 데이터 형식 | 설명 |
|-------------|-----------|-------------|
| `Timestamp` | datetime | 이벤트가 기록된 날짜와 시간 |
| `AlertId` | 문자열 | 경고의 고유 식별자입니다. |
| `Title` | 문자열 | 경고의 제목입니다. |
| `Category` | 문자열 | 경고로 식별되는 위협 표시기 또는 위반 활동 유형 |
| `Severity` | 문자열 | 경고로 식별되는 위협 표시기 또는 위반 활동의 잠재적인 영향(높음, 중간 또는 낮음)을 표시합니다. |
| `ServiceSource` | 문자열 | 경고 정보를 제공한 제품 또는 서비스 |
| `DetectionSource` | 문자열 | 중요 한 구성 요소 또는 활동을 식별 한 검색 기술 또는 센서 |
| `AttackTechniques` | 문자열 | 경고를 트리거한 활동에 연결 된 MITRE AT&T&접시 헤드 기술 |

## <a name="related-topics"></a>관련 항목
- [고급 헌팅 개요](advanced-hunting-overview.md)
- [쿼리 언어 배우기](advanced-hunting-query-language.md)
- [공유 쿼리 사용](advanced-hunting-shared-queries.md)
- [기기, 전자 메일, 앱 및 ID를 검색합니다.](advanced-hunting-query-emails-devices.md)
- [스키마의 이해](advanced-hunting-schema-tables.md)
- [쿼리 모범 사례 적용](advanced-hunting-best-practices.md)
