---
title: Microsoft Teams
description: 장치에 팀을 설치 하 고 나중에 업데이트 하는 방법
keywords: Microsoft Managed Desktop, Microsoft 365, 서비스, 설명서, 앱, LOB (기간 업무) 앱, 업무용 앱
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
audience: ITPro
ms.openlocfilehash: ea2ef7637a8d360e3b598aec4852425d977ae4ec
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950942"
---
# <a name="microsoft-teams"></a>Microsoft Teams

[팀](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) 은 실시간 공동 작업 및 통신, 모임, 파일 및 앱 공유에 대 한 작업 영역을 제공 하는 조직의 [메시징 앱](https://support.microsoft.com/office/microsoft-teams-basics-6d5f52e6-5306-4096-ac24-c3082b79eaf0) 입니다.

## <a name="initial-deployment"></a>초기 배포

대부분의 하드웨어 공급 업체에는 아직 이미지의 일부로 팀이 포함 되어 있지 않으므로 microsoft Managed Desktop은 Microsoft Intune을 사용 하 여 팀을 장치에 배포 합니다. 모든 관리 되는 장치에는 [팀 .msi 패키지가](https://docs.microsoft.com/MicrosoftTeams/msi-deployment#how-the-microsoft-teams-msi-package-works) 설치 되어 있으므로 장치에 로그인 하는 모든 사용자가 Microsoft 팀을 사용할 준비가 되었는지 확인 합니다. 패키지에서 처음으로 설치를 완료 하면 팀이 자동으로 시작 되 고 바탕 화면에 바로 가기가 추가 됩니다.

### <a name="microsoft-intune-changes"></a>Microsoft Intune 변경 사항

Microsoft Managed Desktop은 Microsoft 팀을 위해 Azure AD 조직에 두 개의 응용 프로그램을 추가 합니다. 이러한 기능은 장치에 맞게 64 비트 또는 32 비트 클라이언트에 배포 됩니다.  

- 현대 회사-팀 컴퓨터의 전체 설치 프로그램 x64  
- 현대 회사-팀 컴퓨터 전체의 설치 관리자 x32

## <a name="updates"></a>업데이트

팀은 엔터프라이즈 용 Microsoft 365 앱과 데스크톱 클라이언트 업데이트 자체의 별도 업데이트 경로를 따릅니다. 팀은 몇 시간 마다 업데이트를 확인 하 고 다운로드 한 다음, 컴퓨터의 유휴 상태를 기다린 후 업데이트를 자동으로 설치 합니다.  

팀 제품 그룹에서는 관리자가 업데이트를 제어할 수 없으므로 Microsoft Managed Desktop은 [표준 자동 업데이트 채널](https://docs.microsoft.com/microsoftteams/teams-client-update#can-admins-deploy-updates-instead-of-teams-auto-updating)을 사용 합니다.

### <a name="manually-updating-teams"></a>수동으로 팀 업데이트

또한 개별 사용자는 **Check for updates**   앱 오른쪽 위의 **프로필**드롭다운 메뉴에서 업데이트 확인을 선택 하 여 업데이트를 다운로드할 수 있습니다   . 업데이트를 사용할 수 있는 경우에는 컴퓨터가 유휴 상태일 때 다운로드 되 고 자동으로 설치 됩니다.

## <a name="delivery-optimization-of-updates"></a>업데이트의 배달 최적화

팀 업데이트에 대 한 배달 최적화는 기본적으로 설정 되어 있으며 관리자 또는 사용자에 게 아무런 작업도 수행 하지 않습니다. 