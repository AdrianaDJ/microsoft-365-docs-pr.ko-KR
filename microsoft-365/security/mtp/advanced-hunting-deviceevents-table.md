---
title: 고급 구하기 스키마의 DeviceEvents 테이블
description: 고급 검색 스키마의 기타 장치 이벤트 (DeviceEvents) 테이블에 있는 바이러스 백신, 방화벽 및 기타 이벤트 유형에 대해 알아봅니다.
keywords: 고급 구하기, 위협 검색, 사이버 위협 검색, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, table, column, data type, security 이벤트, antivirus, firewall, 익스플로잇 가드, DeviceEvents
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
ms.openlocfilehash: d3f00e506d34b4c82137f368c8c8f24e52b0247a
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843043"
---
# <a name="deviceevents"></a>DeviceEvents

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**적용 대상:**
- Microsoft 365 Defender



`DeviceEvents` [고급 구하기](advanced-hunting-overview.md) 스키마의 기타 장치 이벤트 또는 테이블에는 Windows Defender 바이러스 백신 및 exploit protection과 같은 보안 컨트롤에서 트리거되는 이벤트를 비롯 하 여 다양 한 이벤트 유형에 대 한 정보가 포함 되어 있습니다. 이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.

>[!TIP]
> 테이블에서 지 원하는 이벤트 유형 (값)에 대 한 자세한 내용은 `ActionType` 보안 센터에서 사용할 수 있는 [기본 제공 스키마 참조](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) 를 사용 하십시오.

고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.


| 열 이름 | 데이터 형식 | 설명 |
|-------------|-----------|-------------|
| `Timestamp` | datetime | 이벤트가 기록된 날짜와 시간 |
| `DeviceId` | 문자열 | 서비스에서 시스템의 고유 식별자 |
| `DeviceName` | 문자열 | 컴퓨터의 FQDN(정규화된 도메인 이름) |
| `ActionType` | 문자열 | 이벤트를 트리거한 작업의 유형입니다. 자세한 내용은 [portal 스키마 참조](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) 를 참조 하세요. |
| `FileName` | 문자열 | 기록된 조치가 적용된 파일의 이름 |
| `FolderPath` | 문자열 | 기록 된 작업이 적용 된 파일을 포함 하는 폴더 |
| `SHA1` | 문자열 | 기록된 조치가 적용된 파일의 SHA-1 |
| `SHA256` | 문자열 | 기록된 조치가 적용된 파일의 SHA-256 일반적으로이 필드는 채워지지 않습니다. 가능한 경우 SHA1 열을 사용합니다. |
| `MD5` | 문자열 | 기록 된 작업이 적용 된 파일의 MD5 해시 |
| `AccountDomain` | 문자열 | 계정의 도메인 |
| `AccountName` | 문자열 | 계정의 사용자 이름입니다. |
| `AccountSid` | 문자열 | 계정의 SID (보안 식별자) |
| `RemoteUrl` | 문자열 | 연결된 URL 또는 FQDN(정규화된 도메인 이름) |
| `RemoteDeviceName` | 문자열 | 영향을 받는 시스템에서 원격 작업을 수행한 컴퓨터의 이름입니다. 보고 되는 이벤트에 따라이 이름은 FQDN (정규화 된 도메인 이름), NetBIOS 이름 또는 도메인 정보가 없는 호스트 이름이 될 수 있습니다. |
| `ProcessId` | int | 새로 만든 프로세스의 PID (프로세스 ID) |
| `ProcessCommandLine` | 문자열 | 새 프로세스를 만드는 데 사용 되는 명령줄 |
| `ProcessCreationTime` | datetime | 프로세스를 만든 날짜 및 시간입니다. |
| `ProcessTokenElevation` | 문자열 | 새로 만든 프로세스에 UAC (사용자 액세스 제어) 권한 상승을 적용 했음을 나타내는 토큰 유형입니다. |
| `LogonId` | 문자열 | 로그온 세션의 식별자입니다. 이 식별자는 다시 시작 하는 경우에만 동일한 컴퓨터에서 고유 합니다. |
| `RegistryKey` | 문자열 | 기록 된 작업이 적용 된 레지스트리 키 |
| `RegistryValueName` | 문자열 | 기록 된 작업이 적용 된 레지스트리 값의 이름입니다. |
| `RegistryValueData` | 문자열 | 기록 된 작업이 적용 된 레지스트리 값의 데이터입니다. |
| `RemoteIP` | 문자열 | 연결된 IP 주소 |
| `RemotePort` | int | 연결 된 원격 장치의 TCP 포트 |
| `LocalIP` | 문자열 | 통신 중에 사용 되는 로컬 컴퓨터에 할당 된 IP 주소 |
| `LocalPort` | int | 통신 중에 사용 되는 로컬 컴퓨터의 TCP 포트 |
| `FileOriginUrl` | 문자열 | 파일을 다운로드 한 URL |
| `FileOriginIP` | 문자열 | 파일을 다운로드 한 IP 주소 |
| `AdditionalFields` | 문자열 | JSON 배열 형식의 이벤트에 대 한 추가 정보 |
| `InitiatingProcessSHA1` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 SHA-1 |
| `InitiatingProcessSHA256` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 SHA-256입니다. 일반적으로이 필드는 채워지지 않습니다. 가능한 경우 SHA1 열을 사용합니다. |
| `InitiatingProcessFileName` | 문자열 | 이벤트를 시작한 프로세스의 이름입니다. |
| `InitiatingProcessFolderPath` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)가 들어 있는 폴더 |
| `InitiatingProcessId` | int | 이벤트를 시작한 프로세스의 PID (프로세스 ID) |
| `InitiatingProcessCommandLine` | 문자열 | 이벤트를 시작한 프로세스를 실행 하는 데 사용 되는 명령줄입니다. |
| `InitiatingProcessCreationTime` | datetime | 이벤트를 시작한 프로세스를 시작한 날짜 및 시간입니다. |
| `InitiatingProcessParentId` | int | 이벤트를 담당 하는 프로세스를 생성 한 상위 프로세스의 PID (프로세스 ID)입니다. |
| `InitiatingProcessParentFileName` | 문자열 | 이벤트를 담당 하는 프로세스를 생성 한 상위 프로세스의 이름입니다. |
| `InitiatingProcessParentCreationTime` | datetime | 이벤트를 담당 하는 프로세스의 부모를 시작한 날짜 및 시간입니다. |
| `InitiatingProcessMD5` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 MD5 해시 |
| `InitiatingProcessAccountDomain` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 도메인입니다. |
| `InitiatingProcessAccountName` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 사용자 이름입니다. |
| `InitiatingProcessAccountSid` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 SID (보안 식별자)입니다. |
| `InitiatingProcessLogonId` | 문자열 | 이벤트를 시작한 프로세스의 로그온 세션에 대 한 식별자입니다. 이 식별자는 다시 시작 하는 경우에만 동일한 컴퓨터에서 고유 합니다. |
| `ReportId` | long | 반복 카운터를 기반으로 하는 이벤트 식별자입니다. 고유 이벤트를 식별 하려면이 열을 장치 이름 및 타임 스탬프 열과 함께 사용 해야 합니다. |
| `AppGuardContainerId` | 문자열 | 응용 프로그램 가드가 브라우저 활동을 격리 하는 데 사용 하는 가상화 된 컨테이너의 식별자입니다. |

## <a name="related-topics"></a>관련 항목
- [고급 헌팅 개요](advanced-hunting-overview.md)
- [쿼리 언어 배우기](advanced-hunting-query-language.md)
- [공유 쿼리 사용](advanced-hunting-shared-queries.md)
- [기기, 전자 메일, 앱 및 ID를 검색합니다.](advanced-hunting-query-emails-devices.md)
- [스키마의 이해](advanced-hunting-schema-tables.md)
- [쿼리 모범 사례 적용](advanced-hunting-best-practices.md)
