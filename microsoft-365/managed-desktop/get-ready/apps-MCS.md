---
title: Microsoft 컨설팅 서비스 활용
description: 앱을 패키지로 하기 위해 MCS에서 수행 해야 하는 준비 및 단계
keywords: Microsoft Managed Desktop, Microsoft 365, 서비스, 설명서, 앱, MCS, 패키징
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: d2a6c09e1bcb84885e607d133c14e26e08e3c621
ms.sourcegitcommit: 126d22d8abd190beb7101f14bd357005e4c729f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46530166"
---
# <a name="working-with-microsoft-consulting-services"></a>Microsoft 컨설팅 서비스 활용

MCS (Microsoft 컨설팅 서비스)를 사용 하 여 Microsoft Managed Desktop과 함께 사용할 수 있도록 앱 패키지를 가져올 수도 있습니다. 자세한 내용은 계정 담당자와 함께 MCS에 문의 하 여 특정 앱 패키징 프로젝트의 범위를 지정 합니다.

## <a name="roles-and-responsibilities"></a>역할 및 책임

MCS 앱 패키지로 작업 하려면 **다음 요소를 제공 해야 합니다**.

- 원본 설치 관리자 파일 (예: setup.exe 또는 .msi)
- 설치 지침에 따라 최종 설치의 모양에 대 한 세부 정보를 지정 합니다. 예를 들어, 앱에 대 한 바탕 화면 바로 가기가 있어야 하나요? 앱의 표시 유형 앱이 서버에 연결 되는 경우 (있는 경우) 자세한 내용은 [응용 프로그램 패키징 요청 템플릿을](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/managed-desktop/get-ready/downloads/app-packaging-template.docx)참조 하십시오.
- 자체 승인 테스트를 수행 하 여 사용자 환경에서 앱이 필요한 대로 작동 하는지 확인 해야 합니다.

**MCS에서는 다음 작업을 수행 합니다.**

- 앱이 Microsoft Managed Desktop 환경에서 금지 되거나 제한 되는지 확인 합니다.
- 앱의 설치, 시작 및 제거를 테스트 하 여 Windows 10과의 호환성을 확인 합니다. MCS에서 호환성 문제가 발견 되 면 앱이 관리 하기 위한 [데스크톱 앱 보증](https://docs.microsoft.com/fasttrack/win-10-desktop-app-assure) 프로그램에 전달 됩니다.
- 앱을 사양에 패키징 한 다음 Microsoft Intune을 사용 하 여 앱 배포를 테스트 합니다.

## <a name="app-delivery-schedule"></a>앱 배달 일정

Microsoft Managed Desktop portal에 앱 정보를 업로드 하 여 패키지 프로세스를 시작 합니다. 패키지 팀은 목요일 마다 새 제출을 검토 합니다. 검토 및 패키징에 따라 패키징된 앱에는 다음과 같은 금요일이 배달 됩니다. 주당 최대 5 개의 앱을 시작 하도록 패키지할 수 있지만 서비스는 사용자의 요구에 맞게 확장 될 수 있습니다.

![매월 목요일에 앱 유입량을 표시 하는 달력 (이 예에서는 21), 다음 날에 대 한 패키징 (25) 및 이후 금요일 (29 일)에 대 한 앱 배달](../../media/MCS-cal.png)

앱이 전달 되 면 알림을 받을 수 있습니다. 이 시점에서 승인 테스트를 수행 하 고 Microsoft Managed Desktop portal에서 작업을 진행 하는 데 21 일이 소요 됩니다. 승인 테스트 중에 앱에서 문제가 발견 되는 경우 Microsoft Managed Desktop portal에서 앱을 거부 하 고이 문제를 이해 하 고 해결 하기 위해 전자 메일을 통해 MCS 포장기를 통해 연결 합니다.

## <a name="testing-accounts-and-environment"></a>계정 및 환경 테스트

패키징 팀이 Microsoft Intune으로의 마이그레이션을 완료 하려면 특정 사용 권한을 제공 하는 것이 좋습니다.
 
-   앱 추가 및 할당을 위한 포장기 용 Microsoft Intune 앱 배포 기능에 대 한 액세스 권한 
-   앱을 테스트할 수 있도록 packagers에 대 한 테스트 그룹, 사용자 계정 및 라이선스

MCS는 이러한 권한을 사용 하 여 다음 작업을 수행 합니다.
 
-   앱이 Microsoft Managed Desktop에 대해 구성 된 가상 컴퓨터에서 작동 하는지 확인
-   사용자에 게 배포 하기 위해 Microsoft Intune에 앱 업로드

이러한 사용 권한이 없으면 MCS가 앞으로 이동할 수 있지만 사용자 환경에 응용 프로그램을 업로드할 수는 없습니다.


