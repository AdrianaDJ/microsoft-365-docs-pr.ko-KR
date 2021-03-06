---
title: Microsoft 365과 Azure 통합
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- M365-identity-device-management
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: a5efce5d-9c9c-4190-b61b-fd273c1d425f
description: 온-프레미스 환경에 암호 동기화 또는 single sign-on을 사용 하려면 Microsoft 365를 Azure AD와 통합 합니다.
ms.openlocfilehash: b1f20ebc692421ed6df0d6f7c31a4d80347133e3
ms.sourcegitcommit: 11d1044c6600b1f568b6dc8a53db9b07f2f0ad1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48384740"
---
# <a name="azure-integration-with-microsoft-365"></a>Microsoft 365과 Azure 통합

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Microsoft 365는 Azure Active Directory (Azure AD)를 사용 하 여 백그라운드에서 사용자 id를 관리 합니다. Microsoft 365 구독에는 온-프레미스 AD DS (Active Directory 도메인 서비스)를 통합 하 여 사용자 계정 및 암호를 동기화 하거나 single sign-on을 설정할 수 있는 무료 Azure AD 구독이 포함 되어 있습니다. 계정을 보다 효율적으로 관리 하기 위해 고급 기능을 구입할 수도 있습니다.
  
또한 Azure AD는 통합 앱 관리와 같은 다른 기능을 제공 하 여 Microsoft 365 구독을 확장 및 사용자 지정 하는 데 사용할 수 있습니다.
  
Microsoft 365 관리 센터의 안내 설치 및 구성 환경에 대해 Azure AD 배포 관리자를 사용할 수 있습니다 (Microsoft 365에 로그인 해야 함).

 - [Azure AD Connect advisor](https://aka.ms/aadconnectpwsync)
 - [AD FS 배포 관리자](https://aka.ms/adfsguidance)
 - [Azure AD 설정 가이드](https://aka.ms/aadpguidance)
  
## <a name="azure-ad-editions-and-microsoft-365-identity-management"></a>Azure AD edition 및 Microsoft 365 id 관리

Microsoft 365에 대 한 유료 구독을 사용 하는 경우에는 무료 Azure AD 구독이 제공 됩니다. Azure AD를 사용 하 여 사용자 및 그룹 계정을 만들고 관리할 수 있습니다. 이 구독을 활성화 하려면 일회성 등록을 완료 해야 합니다. 나중에 Microsoft 365 관리 센터에서 Azure AD에 액세스할 수 있습니다. 

무료 Azure AD 구독을 등록 하는 방법에 대 한 자세한 내용은 [use a Free AZURE ad subscription](../compliance/use-your-free-azure-ad-subscription-in-office-365.md)을 참조 하십시오. Azure.microsoft.com로 직접 이동 하 여 등록 하지 않고 microsoft Azure에 대 한 평가판 또는 유료 구독을 사용 하 여 무료 Azure AD 구독을 마이크로소프트 365과 구분 합니다. 
  
무료 구독을 사용 하 여 온-프레미스 디렉터리와 동기화 하 고 single sign-on을 설정 하 고, Salesforce, DropBox 등 다양 한 소프트웨어와 서비스 응용 프로그램을 동기화 할 수 있습니다.
  
향상 된 AD DS 기능, 양방향 동기화 및 기타 관리 기능을 사용 하려면 무료 구독을 유료 프리미엄 구독으로 업그레이드 하면 됩니다. 자세한 내용은 [Azure Active Directory 버전](https://azure.microsoft.com/pricing/details/active-directory/)을 참조 하십시오.
  
Microsoft 365 및 Azure AD에 대 한 자세한 내용은 [microsoft 365 identity 모델](about-microsoft-365-identity.md)을 참조 하십시오.
  
## <a name="extend-the-capabilities-of-your-microsoft-365-tenant"></a>Microsoft 365 테 넌 트의 기능 확장

|**기능**|**설명**|
|:-----|:-----|
|통합 앱  <br/> |개별 앱에 메일, 일정, 연락처, 사용자, 그룹, 파일 및 폴더와 같은 Microsoft 365 데이터에 대 한 액세스 권한을 부여할 수 있습니다. 또한 전역 관리자 수준에서 이러한 앱에 권한을 부여 하 고 Azure AD에 앱을 등록 하 여 전체 회사에서 사용할 수 있도록 설정할 수도 있습니다. Formore- [Microsoft 365 관리자를 위한 통합 앱 및 AZURE AD](integrated-apps-and-azure-ads.md)를 참조 하세요.  <br/> 또한 [Single sign-on](https://go.microsoft.com/fwlink/p/?LinkId=698604)도 참조 하세요.  <br/> |
|PowerApps  <br/> | Power apps는 SharePoint 목록 및 기타 데이터 앱과 같은 기존 데이터 원본에 연결할 수 있는 모바일 장치에 대 한 중요 한 앱입니다. 자세한 내용은 SharePoint Online 및 [PowerApps 페이지](https://powerapps.microsoft.com/) 의 [목록에 대 한 PowerApp 만들기](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) 를 참조 하세요.  <br/> |
   
## <a name="see-also"></a>참고 항목

[Microsoft 365 Enterprise 개요](microsoft-365-overview.md)
