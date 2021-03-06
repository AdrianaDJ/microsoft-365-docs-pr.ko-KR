---
title: 끝점에 대 한 Microsoft Defender에서 고급 구하기 쿼리 마이그레이션
description: Microsoft 365 Defender에서 사용할 수 있도록 끝점 쿼리에 대 한 Microsoft Defender를 조정 하는 방법을 알아봅니다.
keywords: 고급 구하기, 위협 검색, 사이버 위협 사냥, microsoft threat protection, microsoft 365, mtp, m365, microsoft defender atp, mdatp, search, query, 원격 분석, 사용자 지정 검색, 스키마, kusto, microsoft 365, mapping
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
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8b69dff94cc5d3ba3331fd6d13b1d7de1402ac47
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846859"
---
# <a name="migrate-advanced-hunting-queries-from-microsoft-defender-for-endpoint"></a>끝점에 대 한 Microsoft Defender에서 고급 구하기 쿼리 마이그레이션

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

**적용 대상:**
- Microsoft 365 Defender

고급 구하기 워크플로를 Microsoft Defender for Endpoint에서 더 넓은 데이터 집합을 사용 하 여 위협에 대 한 사전 사냥으로 이동 합니다. Microsoft 365 Defender에서는 다음을 비롯 한 다른 Microsoft 365 보안 솔루션의 데이터에 액세스할 수 있습니다.

- 엔드포인트용 Microsoft Defender
- Microsoft Defender for Office 365
- Microsoft Cloud App Security
- ID용 Microsoft Defender

>[!NOTE]
>끝점 고객에 대 한 대부분의 Microsoft Defender는 [추가 라이선스 없이 microsoft 365 Defender를 사용할](prerequisites.md#licensing-requirements)수 있습니다. Defender for Endpoint에서 고급 구하기 워크플로 전환을 시작 하려면 [Microsoft 365 Defender를 켜십시오](mtp-enable.md).

기존 Defender for Endpoint 워크플로에 영향을 주지 않으면 서 전환할 수 있습니다. 저장 된 쿼리는 그대로 유지 되며 사용자 지정 검색 규칙은 계속 실행 되 고 경고를 생성 합니다. 그러나 Microsoft 365 Defender에도 표시 됩니다. 

## <a name="schema-tables-in-microsoft-365-defender-only"></a>Microsoft 365 Defender 전용의 스키마 테이블
[Microsoft 365 Defender advanced 사냥 스키마](advanced-hunting-schema-tables.md) 는 다양 한 Microsoft 365 보안 솔루션의 데이터를 포함 하는 추가 테이블을 제공 합니다. 다음 표는 Microsoft 365 Defender 에서만 사용할 수 있습니다.

| 테이블 이름 | 설명 |
|------------|-------------|
| [AlertEvidence](advanced-hunting-alertevidence-table.md) | 알림과 연결 된 파일, IP 주소, Url, 사용자 또는 장치 |
| [AlertInfo](advanced-hunting-alertinfo-table.md) | 끝점에 대 한 Microsoft defender, microsoft Defender for Office 365, Microsoft Cloud App Security 및 Id 용 microsoft Defender에 대 한 알림 (심각도 정보 및 위협 범주 포함)  |
| [AppFileEvents](advanced-hunting-appfileevents-table.md) | 클라우드 앱 및 서비스의 파일 관련 활동 |
| [EmailAttachmentInfo](advanced-hunting-emailattachmentinfo-table.md) | 전자 메일에 첨부 된 파일에 대 한 정보 |
| [EmailEvents](advanced-hunting-emailevents-table.md) | 전자 메일 배달 및 차단 이벤트를 비롯 한 Microsoft 365 전자 메일 이벤트 |
| [EmailPostDeliveryEvents](advanced-hunting-emailpostdeliveryevents-table.md) | Microsoft 365이 전자 메일을 받는 사람 사서함으로 배달 한 후 배달 후 발생 하는 보안 이벤트 |
| [EmailUrlInfo](advanced-hunting-emailurlinfo-table.md) | 전자 메일의 Url에 대 한 정보 |
| [IdentityDirectoryEvents](advanced-hunting-identitydirectoryevents-table.md) | AD (Active Directory)를 실행 하는 온-프레미스 도메인 컨트롤러를 포함 하는 이벤트 이 표에서는 도메인 컨트롤러의 id 관련 이벤트 및 시스템 이벤트 범위를 설명 합니다. |
| [IdentityInfo](advanced-hunting-identityinfo-table.md) | Azure Active Directory를 비롯 한 다양 한 원본의 계정 정보 |
| [IdentityLogonEvents](advanced-hunting-identitylogonevents-table.md) | Active Directory 및 Microsoft online services의 인증 이벤트 |
| [IdentityQueryEvents](advanced-hunting-identityqueryevents-table.md) | Active Directory 개체에 대 한 쿼리 (예: 사용자, 그룹, 장치 및 도메인) |

## <a name="map-devicealertevents-table"></a>지도 DeviceAlertEvents 테이블
`AlertInfo`및 `AlertEvidence` 테이블은 `DeviceAlertEvents` Microsoft Defender for Endpoint schema의 테이블을 대체 합니다. 이러한 두 테이블은 장치 경고에 대 한 데이터 외에도 id, 앱 및 전자 메일에 대 한 경고에 대 한 데이터를 포함 합니다.

다음 표를 사용 하 여 `DeviceAlertEvents` 열이 및 테이블의 열에 매핑되는 방식을 확인 `AlertInfo` `AlertEvidence` 합니다.

>[!TIP]
>다음 표에는 열 외에도 `AlertEvidence` 다양 한 원본의 알림을 보다 광범위 하 게 나타내는 다양 한 열이 포함 되어 있습니다. [모든 AlertEvidence 열 보기](advanced-hunting-alertevidence-table.md) 

| DeviceAlertEvents 열 | Microsoft 365 Defender에서 동일한 데이터를 찾을 수 있는 위치 |
|-------------|-----------|-------------|-------------|
| `AlertId` | `AlertInfo` 및  `AlertEvidence` 테이블 |
| `Timestamp` | `AlertInfo` 및  `AlertEvidence` 테이블 |
| `DeviceId` | `AlertEvidence` 목차가 |
| `DeviceName` | `AlertEvidence` 목차가 |
| `Severity` | `AlertInfo` 목차가 |
| `Category` | `AlertInfo` 목차가 |
| `Title` | `AlertInfo` 목차가 |
| `FileName` | `AlertEvidence` 목차가 |
| `SHA1` | `AlertEvidence` 목차가 |
| `RemoteUrl` | `AlertEvidence` 목차가 |
| `RemoteIP` | `AlertEvidence` 목차가 |
| `AttackTechniques` | `AlertInfo` 목차가 |
| `ReportId` | 이 열은 일반적으로 Microsoft Defender for Endpoint에서 다른 테이블에서 관련 레코드를 찾는 데 사용 됩니다. Microsoft 365 Defender에서는 테이블에서 직접 관련 데이터를 가져올 수 있습니다 `AlertEvidence` . |
| `Table` | 이 열은 일반적으로 Microsoft Defender for Endpoint for 끝점에서 다른 표에 있는 추가 이벤트 정보에 사용 됩니다. Microsoft 365 Defender에서는 테이블에서 직접 관련 데이터를 가져올 수 있습니다 `AlertEvidence` . |

## <a name="adjust-existing-microsoft-defender-for-endpoint-queries"></a>끝점 쿼리에 대 한 기존 Microsoft Defender 조정
끝점 쿼리에 대 한 Microsoft Defender는 테이블을 참조 하지 않는 한 그대로 작동 합니다 `DeviceAlertEvents` . Microsoft 365 Defender에서 이러한 쿼리를 사용 하려면 다음 변경 내용을 적용 합니다.

- `DeviceAlertEvents`로 대체 `AlertInfo` 합니다.
- `AlertInfo`와 테이블을 조인 `AlertEvidence` 하 여 `AlertId` 동등한 데이터를 가져옵니다.

### <a name="original-query"></a>원래 쿼리
다음 쿼리는 끝점에 대해 Microsoft Defender를 사용 하 여 `DeviceAlertEvents` _powershell.exe_ 관련 된 경고를 가져옵니다.

```kusto
DeviceAlertEvents
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" and FileName == "powershell.exe"
```
### <a name="modified-query"></a>수정 된 쿼리
다음 쿼리는 Microsoft 365 Defender에서 사용 하도록 조정 되었습니다. 파일 이름을 직접 확인 하는 대신 `DeviceAlertEvents` `AlertEvidence` 해당 테이블에서 파일 이름을 조인 하 고 확인 합니다.

```kusto
AlertInfo 
| where Timestamp > ago(7d) 
| where AttackTechniques has "PowerShell (T1086)" 
| join AlertEvidence on AlertId
| where FileName == "powershell.exe"
```

## <a name="related-topics"></a>관련 항목
- [Microsoft 365 Defender 켜기](advanced-hunting-query-language.md)
- [고급 헌팅 개요](advanced-hunting-overview.md)
- [스키마의 이해](advanced-hunting-schema-tables.md)
- [끝점에 대 한 Microsoft Defender의 고급 구하기](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)