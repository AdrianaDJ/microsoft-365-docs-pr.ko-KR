---
title: 고급 구하기 스키마의 DeviceInfo 테이블
description: 고급 구하기 스키마의 DeviceInfo 테이블에 있는 OS, 컴퓨터 이름 및 기타 컴퓨터 정보에 대해 자세히 알아봅니다.
keywords: 고급 구하기, 위협 검색, 사이버 위협 사냥, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, table, description, DeviceInfo, device, machine, OS, 플랫폼, 사용자
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
ms.openlocfilehash: 1bb48b4332bc9d60de15bb513f04a503d6a6913b
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48842717"
---
# <a name="deviceinfo"></a>DeviceInfo

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**적용 대상:**
- Microsoft 365 Defender



`DeviceInfo` [고급 구하기](advanced-hunting-overview.md) 스키마의 표에는 OS 버전, 활성 사용자 및 컴퓨터 이름을 비롯 하 여 조직의 컴퓨터에 대 한 정보가 포함 되어 있습니다. 이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.

고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.

| 열 이름 | 데이터 형식 | 설명 |
|-------------|-----------|-------------|
| `Timestamp` | datetime | 이벤트가 기록된 날짜와 시간 |
| `DeviceId` | 문자열 | 서비스에서 시스템의 고유 식별자 |
| `DeviceName` | 문자열 | 컴퓨터의 FQDN(정규화된 도메인 이름) |
| `ClientVersion` | 문자열 | 컴퓨터에서 실행 되는 끝점 에이전트 또는 센서의 버전 |
| `PublicIP` | 문자열 | 등록 컴퓨터에서 Microsoft Defender for Endpoint 서비스에 연결 하는 데 사용 하는 공용 IP 주소입니다. 컴퓨터 자체의 IP 주소, NAT 장치 또는 프록시 일 수 있습니다. |
| `OSArchitecture` | 문자열 | 컴퓨터에서 실행 중인 운영 체제의 아키텍처 |
| `OSPlatform` | 문자열 | 컴퓨터에서 실행 중인 운영 체제의 플랫폼 이는 Windows 10 및 Windows 7과 같은 제품군 내의 변형을 비롯 하 여 특정 운영 체제를 나타냅니다. |
| `OSBuild` | 문자열 | 컴퓨터에서 실행 되는 운영 체제의 빌드 버전 |
| `IsAzureADJoined` | 부울 | 컴퓨터가 Azure Active Directory에 가입 되어 있는지 여부를 나타내는 부울 표시기입니다. |
| `LoggedOnUsers` | 문자열 | JSON 배열 형식의 이벤트가 발생 했을 때 컴퓨터에 로그온 한 모든 사용자의 목록 |
| `RegistryDeviceTag` | 문자열 | 레지스트리를 통해 추가 된 기계 태그 |
| `ReportId` | long | 반복 카운터를 기반으로 하는 이벤트 식별자입니다. 고유 이벤트를 식별 하려면이 열을 장치 이름 및 타임 스탬프 열과 함께 사용 해야 합니다. |
| `OSVersion` | 문자열 | 컴퓨터에서 실행 중인 운영 체제 버전 |
| `MachineGroup` | 문자열 | 컴퓨터의 컴퓨터 그룹입니다. 역할 기반 액세스 제어에서이 그룹을 사용 하 여 컴퓨터에 대 한 액세스를 확인 합니다. |

## <a name="related-topics"></a>관련 항목
- [고급 헌팅 개요](advanced-hunting-overview.md)
- [쿼리 언어 배우기](advanced-hunting-query-language.md)
- [공유 쿼리 사용](advanced-hunting-shared-queries.md)
- [기기, 전자 메일, 앱 및 ID를 검색합니다.](advanced-hunting-query-emails-devices.md)
- [스키마의 이해](advanced-hunting-schema-tables.md)
- [쿼리 모범 사례 적용](advanced-hunting-best-practices.md)
