---
title: BitLocker for Encryption
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: Office 365에서 BitLocker 암호화를 사용 하 여 분실 하거나 도난당 한 컴퓨터 및 디스크로 인 한 데이터 도난 가능성을 줄이는 방법에 대해 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: cc329a053544ba6cf1753ae07caac642546cad11
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44033626"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>암호화에 대한 BitLocker 및 분산 키 관리자(DKM)

Microsoft 서버는 BitLocker를 사용 하 여 볼륨 수준에서 남은 고객 데이터를 포함 하는 디스크 드라이브를 암호화 합니다. BitLocker 암호화는 Windows에 기본적으로 제공 되는 데이터 보호 기능입니다. BitLocker는 다른 프로세스나 컨트롤에 lapses가 있는 경우 (예: 액세스 제어 또는 하드웨어 재활용) 고객이 고객 데이터를 포함 하는 디스크에 물리적으로 액세스할 수 있도록 하는 데 사용 되는 기술 중 하나입니다. 이 경우 BitLocker는 컴퓨터 및 디스크 분실, 도난 또는 부적절 한 제거로 인 한 데이터 도용 또는 노출을 방지할 수 있습니다.

BitLocker는 Exchange Online, SharePoint Online 및 비즈니스용 Skype의 고객 데이터가 포함 된 디스크에 AES (Advanced Encryption Standard) 256 비트 암호화를 사용 하 여 배포 됩니다. 디스크 섹터는 VMK (볼륨 마스터 키)로 암호화 되는 FVEK (전체 볼륨 암호화 키)로 암호화 되며이는 차례로 서버의 TPM (신뢰할 수 있는 플랫폼 모듈)에 바인딩됩니다. VMK는 FVEK를 직접 보호 하므로 VMK를 보호 하는 것이 중요 합니다. 다음 그림에서는 지정 된 서버 (이 경우에는 Exchange Online server를 사용 하는 경우)에 대 한 BitLocker 키 보호 체인의 예를 보여 줍니다.

다음 표에는 지정 된 서버 (이 경우 Exchange Online server)의 BitLocker 키 보호 체인에 대 한 설명이 나와 있습니다.

| 키 보호기 | 단위가 | 생성 방법 | 어디에 저장 됩니까? | 보호용 |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| AES 256 비트 외부 키 | 서버당 | BitLocker Api | TPM 또는 안전한 보안 | Lockbox/Access Control |
|  |  |  | 사서함 서버 레지스트리 | TPM 암호화 |
| 48 자리 숫자 암호 | 디스크당 | BitLocker Api | Active Directory | Lockbox/Access Control |
| X.509 인증서를 DRA (데이터 복구 에이전트)로 공개 키 보호기 라고도 함 | 환경 (예: Exchange Online 다중 테 넌 트) | Microsoft CA | 빌드 시스템 | 한 명의 사용자에 게 개인 키에 대 한 전체 암호가 없습니다. 암호가 물리적으로 보호 되어 있습니다. |


BitLocker 키 관리에는 Microsoft 데이터 센터에서 암호화 된 디스크의 잠금을 해제/복구 하는 데 사용 되는 복구 키 관리가 포함 됩니다. Microsoft 365에서는 마스터 키를 보안 된 공유에 저장 하며, 스크린 및 승인 된 개인이 액세스할 수 있습니다. 키에 대 한 자격 증명은 액세스 제어 데이터에 대 한 보안 리포지토리에 저장 되며, "비밀 저장소"를 호출 하는 경우에는 높은 수준의 권한 상승 및 관리 승인이 온-just-in-time 액세스 권한 상승 도구를 사용 하 여 액세스 해야 합니다.

BitLocker에서는 두 가지 관리 범주에 해당 하는 키를 지원 합니다.

- BitLocker로 관리 되는 키-일반적으로 수명이 짧고 서버에 설치 된 운영 체제 인스턴스의 수명 및 지정 된 디스크에 연결 됩니다. 이러한 키는 서버 재설치 또는 디스크 포맷 중에 삭제 되 고 다시 설정 됩니다.

- Bitlocker 복구 키-BitLocker 외부에서 관리 되지만 디스크 암호 해독에 사용 됩니다. BitLocker는 운영 체제를 다시 설치 하 고 암호화 된 데이터 디스크가 이미 있는 시나리오에 복구 키를 사용 합니다. 또한 응답자가 디스크 잠금을 해제 해야 할 수 있는 Exchange Online의 관리 되는 가용성 모니터링 프로브 에서도 복구 키를 사용 합니다.

BitLocker로 보호 된 볼륨은 전체 볼륨 암호화 키를 사용 하 여 암호화 되며,이 키는 차례로 볼륨 마스터 키로 암호화 됩니다. BitLocker는 FIPS 호환 알고리즘을 사용 하 여 암호화 키가 전혀 저장 되지 않거나 네트워크를 통해 전송 되지 않도록 합니다. Microsoft 365에서 실시간으로 보호 되는 고객 데이터를 구현 하는 것은 기본 BitLocker 구현에서 벗어난 것입니다.
