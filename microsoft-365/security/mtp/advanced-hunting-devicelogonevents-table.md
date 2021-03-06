---
title: 고급 구하기 스키마의 DeviceLogonEvents 테이블
description: 고급 구하기 스키마의 DeviceLogonEvents 테이블에 있는 인증 또는 로그인 이벤트에 대해 자세히 알아보기
keywords: 고급 구하기, 위협 사냥, 사이버 위협 검색, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, table, column, data type, description, logonevents, DeviceLogonEvents, authentication, logon, 로그인
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
ms.openlocfilehash: acdc9f1e17e163f075616e74fdc4f94865c2f38d
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48842705"
---
# <a name="devicelogonevents"></a>DeviceLogonEvents

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**적용 대상:**
- Microsoft 365 Defender



`DeviceLogonEvents` [고급 구하기](advanced-hunting-overview.md) 스키마의 표에는 사용자 로그온 및 장치에 대 한 기타 인증 이벤트에 대 한 정보가 포함 되어 있습니다. 이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.

>[!TIP]
> 테이블에서 지 원하는 이벤트 유형 (값)에 대 한 자세한 내용은 `ActionType` 보안 센터에서 사용할 수 있는 [기본 제공 스키마 참조](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) 를 사용 하십시오.

고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.

| 열 이름 | 데이터 형식 | 설명 |
|-------------|-----------|-------------|
| `Timestamp` | datetime | 이벤트가 기록된 날짜와 시간 |
| `DeviceId` | 문자열 | 서비스에서 시스템의 고유 식별자 |
| `DeviceName` | 문자열 | 컴퓨터의 FQDN(정규화된 도메인 이름) |
| `ActionType` | 문자열 |이벤트를 트리거한 작업의 유형입니다. |
| `AccountDomain` | 문자열 | 계정의 도메인 |
| `AccountName` | 문자열 | 계정의 사용자 이름입니다. |
| `AccountSid` | 문자열 | 계정의 SID (보안 식별자) |
| `LogonType` | 문자열 | 로그온 세션의 유형 (특히 다음과 같습니다.<br><br> - **대화형** -사용자가 로컬 키보드 및 화면을 사용 하 여 컴퓨터와 물리적으로 상호 작용 합니다.<br><br> - **RDP (원격 대화형) 로그온** -사용자가 원격 데스크톱, 터미널 서비스, 원격 지원 또는 기타 RDP 클라이언트를 사용 하 여 원격으로 컴퓨터와 상호 작용 합니다.<br><br> - PsExec를 사용 하 여 컴퓨터에 액세스 하거나 프린터 및 공유 폴더와 같은 컴퓨터의 공유 리소스에 액세스 하는 경우 **네트워크** 세션이 시작 됨<br><br> - 예약 된 작업에 의해 시작 되는 **일괄** 세션<br><br> - **서비스** 시작 시 서비스에 의해 시작 된 세션<br> |
| `LogonId` | 문자열 | 로그온 세션의 식별자입니다. 이 식별자는 다시 시작 하는 경우에만 동일한 컴퓨터에서 고유 합니다. |
| `RemoteDeviceName` | 문자열 | 영향을 받는 시스템에서 원격 작업을 수행한 컴퓨터의 이름입니다. 보고 되는 이벤트에 따라이 이름은 FQDN (정규화 된 도메인 이름), NetBIOS 이름 또는 도메인 정보가 없는 호스트 이름이 될 수 있습니다. |
| `RemoteIP` | 문자열 | 연결된 IP 주소 |
| `RemoteIPType` | 문자열 | IP 주소 유형 (예: Public, Private, Reserved, 루프백, Teredo, FourToSixMapping 및 브로드캐스트) |
| `RemotePort` | int | 연결 된 원격 장치의 TCP 포트 |
| `AdditionalFields` | 문자열 | JSON 배열 형식의 이벤트에 대 한 추가 정보 |
| `InitiatingProcessAccountDomain` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 도메인입니다. |
| `InitiatingProcessAccountName` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 사용자 이름입니다. |
| `InitiatingProcessAccountSid` | 문자열 | 이벤트를 담당 하는 프로세스를 실행 한 계정의 SID (보안 식별자)입니다. |
| `InitiatingProcessIntegrityLevel` | 문자열 | 이벤트를 시작한 프로세스의 무결성 수준입니다. Windows에서는 인터넷 다운로드에서 시작 된 경우와 같이 특정 특성에 따라 프로세스에 무결성 수준을 할당 합니다. 이러한 무결성 수준은 리소스에 대 한 사용 권한에 영향을 줍니다. |
| `InitiatingProcessTokenElevation` | 문자열 | 이벤트를 시작한 프로세스에 UAC (사용자 액세스 제어) 권한 상승이 적용 되었는지 여부를 나타내는 토큰 유형입니다. |
| `InitiatingProcessSHA1` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 SHA-1 |
| `InitiatingProcessSHA256` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 SHA-256입니다. 이 필드는 대개 채워지지 않으며, 가능한 경우 SHA1 열을 사용 합니다. |
| `InitiatingProcessMD5` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)의 MD5 해시 |
| `InitiatingProcessFileName` | 문자열 | 이벤트를 시작한 프로세스의 이름입니다. |
| `InitiatingProcessId` | int | 이벤트를 시작한 프로세스의 PID (프로세스 ID) |
| `InitiatingProcessCommandLine` | 문자열 | 이벤트를 시작한 프로세스를 실행 하는 데 사용 되는 명령줄입니다. |
| `InitiatingProcessCreationTime` | datetime | 이벤트를 시작한 프로세스를 시작한 날짜 및 시간입니다. |
| `InitiatingProcessFolderPath` | 문자열 | 이벤트를 시작한 프로세스 (이미지 파일)가 들어 있는 폴더 |
| `InitiatingProcessParentId` | int | 이벤트를 담당 하는 프로세스를 생성 한 상위 프로세스의 PID (프로세스 ID)입니다. |
| `InitiatingProcessParentFileName` | 문자열 | 이벤트를 담당 하는 프로세스를 생성 한 상위 프로세스의 이름입니다. |
| `InitiatingProcessParentCreationTime` | datetime | 이벤트를 담당 하는 프로세스의 부모를 시작한 날짜 및 시간입니다. |
| `ReportId` | long | 반복 카운터를 기반으로 하는 이벤트 식별자입니다. 고유 이벤트를 식별 하려면이 열을 장치 이름 및 타임 스탬프 열과 함께 사용 해야 합니다. |
| `AppGuardContainerId` | 문자열 | 응용 프로그램 가드가 브라우저 활동을 격리 하는 데 사용 하는 가상화 된 컨테이너의 식별자입니다. |
| `IsLocalAdmin` | 부울 | 사용자가 컴퓨터의 로컬 관리자 인지 여부를 나타내는 부울 표시기입니다. |

## <a name="related-topics"></a>관련 항목
- [고급 헌팅 개요](advanced-hunting-overview.md)
- [쿼리 언어 배우기](advanced-hunting-query-language.md)
- [공유 쿼리 사용](advanced-hunting-shared-queries.md)
- [기기, 전자 메일, 앱 및 ID를 검색합니다.](advanced-hunting-query-emails-devices.md)
- [스키마의 이해](advanced-hunting-schema-tables.md)
- [쿼리 모범 사례 적용](advanced-hunting-best-practices.md)
