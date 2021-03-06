---
title: Microsoft Managed Desktop 역할 및 책임
description: 이 문서에서는 microsoft Managed Desktop에 대해 Microsoft에서 제공 하는 역할과 책임에 대해 설명 합니다.
keywords: Microsoft Managed Desktop, Microsoft 365, 서비스, 문서
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: de0bc092c35c7f48c562da8d4218f7a638abe1d5
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847783"
---
# <a name="microsoft-managed-desktop-roles-and-responsibilities"></a>Microsoft Managed Desktop 역할 및 책임


<!--This topic is the target for a "Learn more" link in the Admin Portal (aka.ms/admin-access); do not delete.-->
<!-- from Roles and responsibilities -->

조직이 Microsoft Managed Desktop에 등록 되 면 Microsoft에서 어떤 작업을 수행 하나요? 조직의 책임은 무엇 인가요?

## <a name="microsofts-roles-and-responsibilities"></a>Microsoft의 역할 및 책임

Microsoft는 다음과 같은 주요 역할 및 책임을 제공 합니다.

역할 또는 책임 | 설명
--- | ---
MDM 정책 관리 | Microsoft는 모범 사례에 따라 MDM 정책을 적용 하 고 정책 변경에 대 한 요청을 고려 합니다. 또한 [장치 정책](../service-description/device-policies.md)에 지정 된 대로 테 넌 트를 변경 하 게 됩니다.
사용자 지원 | 모든 Microsoft 관리 되는 데스크톱 장치에 사전 설치 된 도움말 보기 앱을 통해 모든 등록 된 사용자에 대해 장치, Windows 및 Microsoft 365 앱 제품군에 대 한 사용자 지원 서비스를 제공 합니다. 
Microsoft Managed Desktop 서비스 지원 | Microsoft는 Microsoft 관리 데스크톱 운영 팀을 통해 IT 부서를 지원 합니다. 이 팀은 고객의 Microsoft Managed Desktop 환경에 대 한 기술 문제 해결, 변경 요청 및 문제 관리를 지원 합니다. 자세한 내용은 [Microsoft Managed Desktop에 대 한 관리자 지원을](../working-with-managed-desktop/admin-support.md)참조 하세요.
보안 모니터링 | Microsoft는 끝점에 대해 Microsoft Defender를 사용 하 여 Microsoft Managed Desktop devices를 모니터링 합니다. Microsoft Managed Desktop (데스크톱 보안 작업 센터)이 위협을 감지 하면 사용자에 게 알림을 제공 하 고, 장치를 격리 하 고, 원격으로 문제를 수정 합니다. 자세한 내용은 [Security](../service-description/security.md)를 참조 하십시오.
모니터링 및 관리 업데이트 | Microsoft 관리 데스크톱 장치를 적극적으로 모니터링 하 여 Microsoft Windows 및 Microsoft Office에 대 한 최신 품질 및 기능 업데이트가 설치 되어 있는지 확인 합니다. 자세한 내용은 [업데이트를 처리 하는 방법을](../service-description/updates.md)참조 하세요.
사용자 및 장치 그룹화 | Microsoft Managed Desktop operations team은 IT 작업의 일부로 필요한 장치 및 사용자 그룹을 만들고 관리 합니다. 이러한 그룹에는 멤버 자격 또는 구성 변경이 허용 되지 않습니다. 이러한 그룹을 변경 하면 예기치 않은 장치를 구성 하 고 기능 손실을 유발할 수 있습니다. 이러한 그룹에 대 한 문제나 의문 사항이 일단 설정 되 면 IT 관리자는 Microsoft Managed Desktop 작업에 문의할 수 있습니다. 자세한 내용은 [Microsoft Managed Desktop에 대 한 관리자 지원을](../working-with-managed-desktop/admin-support.md)참조 하세요.

## <a name="your-roles-and-responsibilities"></a>사용자의 역할 및 책임

이 추가 일반적인 역할 및 책임 집합은 배포에 필요 하지만 Microsoft에서는 제공 되지 않습니다. 이 기능은 포괄적이 지는 않지만 대부분의 조직에 적용 됩니다. 사용자와 Microsoft가 공유 하는 항목에는 몇 가지가 있습니다. 

역할 또는 책임 | 설명
--- | ---
변경 관리 | Microsoft는 Microsoft의 관리 되는 데스크톱 환경을 변경 해야 하는 경우이에 대 한 알림을 고객에 게 미리 알립니다. 자세한 내용은 [서비스 변경 및 통신](../service-description/servicechanges.md)을 참조 하십시오.<br><br>자신의 변경 관리 프로세스를 수행 하 고 Microsoft Managed Desktop Operations team을 사용 하 여 연락처를 설정 해야 합니다. 또한 이러한 변경 내용을 검토 하 고 승인할 리소스가 있어야 합니다. 자세한 내용은 [작업 및 모니터링](../service-description/operations-and-monitoring.md)를 참조 하세요.  
Id 관리 | 사용자 계정을 만들고, 그룹에 사용자를 할당 하 고, 메타 데이터를 최신 상태로 유지 하는 일을 담당 합니다. 
엔터프라이즈 구성 및 관리를 위한 Microsoft 365 앱 | Microsoft는 사용자에 게 Office 응용 프로그램을 배포 하 고 해당 응용 프로그램을 최신 상태로 유지 하 고 있는지를 담당 합니다. <br><br> Exchange Online 관리 책임을 포함 하 여 Microsoft 365 서비스 및 정책을 관리 해야 합니다.<br>-전자 메일 관리<br>-사서함 및 규칙 구성<br>-Exchange 온-프레미스 관리<br><br>또한 Microsoft 365 관리 센터에서 설정 된 공동 작업 도구, SharePoint server 관리, 도메인 관리 및 보안 및 정보 정책을 담당 합니다. 
사용자 지원 | 사용자는 다음에 대해 지원을 제공 해야 합니다. <br>-현장 인프라: 모든 네트워크 및 인터넷 연결, VPN 인프라 및 클라이언트 구성, 로컬 전화 회의 대화방 장비, 프린터, 프록시 서버 및 구성 및 방화벽<br><br>-회사 전체의 클라우드 리소스: 전자 메일, SharePoint, 공동 작업 서비스 및 회사 전체의 기술 공간과 관련 된 기타 클라우드 인프라<br><br>-업무용 및 기타 모든 회사 관련 응용 프로그램입니다.
앱 | 역할 및 책임은 Microsoft Managed Desktop과 제공 하는 앱의 일부로 제공 되는 앱에 따라 약간씩 다릅니다. <br><br>Microsoft에서 제공 하는 앱 (microsoft 365 for enterprise Word, Excel, PowerPoint, Outlook, Publisher, Access, 비즈니스용 Skype, 팀 및 OneNote)의 경우 microsoft에서 배포, 업데이트 및 지원에 대 한 전체 **서비스를 제공** 합니다. 이러한 앱에 대 한 라이선스를 얻고 할당 하 고, 보안 그룹에 사용자를 추가 하 고, 수명 종료를 관리 하 고, 필요한 추가 기능을 **배포 해야 합니다** .<br><br>사용자가 제공 하는 앱 (lob (기간 업무))에 대해 직접 패키지 하거나 Microsoft 제품이 아닌 다른 공급 업체에 참여 하 든 관계 없이 다음 작업을 수행 **해야** 합니다. <br><br>-대상 사용자 그룹에 필요한 응용 프로그램 식별<br>-앱 배포를 위해 Azure AD 그룹 만들기 및 관리<br>-Microsoft Intune 배포 표준을 충족 하도록 앱 패키징<br>-Microsoft Intune에 앱 업로드<br>-Microsoft Managed Desktop environment에서 앱 테스트<br>-사용자와 앱 테스트<br>-응용 프로그램에 대 한 사용자 관리 및 할당<br>-Microsoft Intune을 통해 응용 프로그램 업데이트 확인 및 배포<br>-중지 된 응용 프로그램 제거 및 제거<br>-조달 및 라이선스 할당<br>-기간 업무 (lob) 앱에 대 한 사용자 지원 제공<br>-원격으로 앱 설정 관리<br><br>**Microsoft** 는 응용 프로그램을 원격 클라이언트로 배달 하는 microsoft Intune 배포 도구를 제공 합니다.<br><br>자세한 내용은 [Apps](../get-ready/apps.md)를 참조 하세요.
보안 모니터링 및 대응 | Microsoft 관리 데스크톱 장치가 아닌 장치에 대 한 인시던트를 조사 및 해결 하 고 Microsoft Managed Desktop Operations 팀에 서비스에 영향을 줄 수 있는 문제에 대 한 정보를 제공 하는지 확인 해야 합니다.
운영 지원 | 조직의 기본 설정 연락처 및 주제 전문가 목록을 제공 해야 합니다. Microsoft Managed Desktop과 관련 되지 않은 운영 사고가 발생 한 경우에는 이러한 사항이 필요 합니다. <br><br>또한 Microsoft Managed Desktop에 없는 장치 및 서비스에 대 한 인시던트를 조사 및 해결 하 고 Microsoft 관리 되는 데스크톱 운영 팀이 항상 통보 되도록 해야 합니다.
VPN을 포함 한 네트워크 인프라 | 인터넷 연결, 네트워크 컨트롤, 프록시 구성 및 원격 연결 인프라를 포함 하 여 모든 네트워킹 관련 인프라 및 서비스의 설치, 구성 및 관리 (문제 해결 및 디버깅 포함)를 담당 합니다.<br><br>프록시 (하드웨어 또는 소프트웨어)가 구성 된 경우에는 프록시에서 허용 해야 하는 Url의 컬렉션이 있습니다. 여러 프록시로 인 한 충돌 또는 비 호환성 문제를 해결 해야 합니다. 구성 가능한 설정을 사용 하 여 조직에 특정 한 네트워크 프록시를 추가할 수 있습니다. 자세한 내용은 [구성 가능한 설정을](../working-with-managed-desktop/config-setting-ref.md#proxy)참조 하십시오.<br><br>자세한 내용은 [프록시 구성을](../get-ready/network.md)참조 하세요.
인쇄할 | 프린터 및 인쇄 큐를 설치, 유지 관리 및 관리 해야 합니다. 클라우드 인쇄는 권장 되는 솔루션 이지만 필수 사항은 아닙니다. 




