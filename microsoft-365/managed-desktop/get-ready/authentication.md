---
title: Microsoft Managed Desktop의 온-프레미스 리소스 액세스 준비
description: Azure AD가 온-프레미스 AD와 통신 하 여 인증을 제공할 수 있도록 하기 위한 중요 한 단계
keywords: Microsoft Managed Desktop, Microsoft 365, 서비스, 문서
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 7181e81a2db94ce26fb8601f8b9156c65084c439
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289582"
---
#  <a name="prepare-on-premises-resources-access-for-microsoft-managed-desktop"></a>Microsoft Managed Desktop의 온-프레미스 리소스 액세스 준비

Microsoft Managed Desktop에서 장치는 Azure Active Directory (Azure AD)에 자동으로 연결 됩니다. 즉, 온-프레미스 Active Directory를 사용 하는 경우 Azure AD에 연결 된 장치가 온-프레미스 Active Directory와 통신할 수 있는지 몇 가지 사항을 확인 해야 합니다. 

> [!NOTE]  
> *하이브리드* Azure AD 조인은 Microsoft Managed Desktop에서 지원 되지 않습니다.

사용자는 Azure Active Directory를 사용 하 여 SSO (Single Sign-on)를 활용할 수 있는데,이는 일반적으로 리소스를 사용할 때마다 자격 증명을 제공 하지 않아도 된다는 것을 의미 합니다.

Azure Active Directory에 가입 하는 방법에 대 한 자세한 내용은 [방법: AZURE AD join 구현 계획](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan)을 참조 하십시오. Azure AD에 연결 된 장치에 대 한 SSO (Single Sign-on)에 대 한 자세한 내용은 [AZURE ad에 가입 된 장치에서 sso에서 온-프레미스 리소스의 작동 방식을](https://docs.microsoft.com/azure/active-directory/devices/azuread-join-sso#how-it-works)참조 하세요.


이 항목에서는 로컬 Active Directory 연결에 의존 하는 앱 및 기타 리소스가 Microsoft Managed Desktop에서 원활 하 게 작동 하도록 하기 위해 확인 해야 하는 사항에 대해 설명 합니다.


## <a name="single-sign-on-for-on-premises-resources"></a>온-프레미스 리소스에 대 한 Single Sign-on

Microsoft Managed Desktop 장치에서 UPN 및 암호를 사용 하 여 SSO (Single Sign-on)를 기본적으로 사용 하도록 설정 합니다. 그러나 사용자는 비즈니스용 Windows Hello를 사용할 수 있으며,이 경우 몇 가지 추가 설정 단계가 필요 합니다. 

### <a name="single-sign-on-by-using-upn-and-password"></a>UPN 및 암호를 사용 하 여 Single Sign-on

대부분의 조직에서는 사용자가 SSO를 사용 하 여 Microsoft Managed Desktop 장치에서 UPN 및 암호를 통해 인증을 받을 수 있습니다. 그러나이 작업을 제대로 수행 하려면 다음을 두 번 확인 해야 합니다.

- Azure AD Connect가 설정 되었으며 Windows Server 2008 R2 이상 버전을 실행 하는 온-프레미스 Active Directory 서버를 사용 하는지 확인 합니다.
- Azure AD Connect가 지원 되는 버전을 실행 하 고 있으며 이러한 세 가지 특성을 Azure AD와 동기화 하도록 설정 되어 있는지 확인 합니다. 
    - 온-프레미스 Active Directory의 DNS 도메인 이름 (사용자가 있는 경우)
    - 온-프레미스 Active Directory의 NetBIOS (사용자가 있는 위치)
    - SAM 사용자의 계정 이름


### <a name="single-sign-on-by-using-windows-hello-for-business"></a>비즈니스용 Windows Hello를 사용 하 여 Single Sign-on

또한 Microsoft Managed Desktop 장치는 비즈니스용 Windows Hello를 채택 하 여 빠르고, 암호를 덜 제공 합니다. 사용자가 각 UPN과 암호를 제공 하지 않아도 비즈니스용 Windows Hello가 작동 하는지 확인 하려면 [비즈니스용 Windows hello를 사용 하 여 온-프레미스 Single sign-on에 대해 AZURE AD 조인 장치를 구성](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base) 하 여 요구 사항을 확인 한 후에 제공 되는 단계를 따르세요.


## <a name="apps-and-resources-that-use-authentication"></a>인증을 사용 하는 앱 및 리소스

Azure Active Directory에서 작동 하도록 앱을 설정 하는 방법에 대 한 전체 지침은 Azure content set의 [응용 프로그램 및 리소스에 대 한 고려 사항 이해](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#understand-considerations-for-applications-and-resources) 를 참조 하세요. 요약:


- Azure AD 앱 갤러리에 추가 된 것과 같은 **클라우드 기반 앱**을 사용 하는 경우에는 Microsoft Managed Desktop에서 더 이상 준비할 필요가 없습니다. 그러나 WAM (Web Account Manager)를 사용 하지 않는 모든 Win32 앱에서 사용자에 게 인증을 요청할 수도 있습니다.

- **온-프레미스에 호스트**되는 앱의 경우 브라우저의 신뢰할 수 있는 사이트 목록에 해당 앱을 추가 해야 합니다. 이렇게 하면 사용자가 자격 증명을 입력 하 라는 메시지가 표시 되지 않고 Windows 인증이 원활 하 게 작동 합니다. 이 작업을 수행 하려면 [구성 가능한 설정 참조](https://docs.microsoft.com/microsoft-365/managed-desktop/working-with-managed-desktop/config-setting-ref)에서 [신뢰할 수 있는 사이트](https://docs.microsoft.com/microsoft-365/managed-desktop/working-with-managed-desktop/config-setting-ref#trusted-sites) 를 참조 하세요.

- Active Directory 페더레이션 서비스를 사용 하는 경우에는 [AD FS에 대 한 single Sign-on 확인 및 관리](https://docs.microsoft.com/previous-versions/azure/azure-services/jj151809(v=azure.100))의 단계를 사용 하 여 SSO가 사용 하도록 설정 되어 있는지 확인 합니다. 

- 온 **-프레미스 및 오래 된 프로토콜을 사용**하는 앱의 경우에는 장치에서 인증을 위해 온-프레미스 도메인 컨트롤러에 액세스할 수 있는 한 추가 설치가 필요 하지 않습니다. 그러나 이러한 응용 프로그램에 대 한 보안 액세스를 제공 하려면 Azure AD 응용 프로그램 프록시를 배포 해야 합니다. 자세한 내용은 [Azure Active Directory의 응용 프로그램 프록시를 통해 온-프레미스 응용 프로그램에 대 한 원격 액세스](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy)를 참조 하세요.

- 온-프레미스를 실행 하 **고 컴퓨터 인증을 사용** 하는 앱은 지원 되지 않으므로 최신 버전으로 교체 하는 것이 좋습니다.

### <a name="network-shares-that-use-authentication"></a>인증을 사용 하는 네트워크 공유

장치에서 UNC 경로를 사용 하 여 온-프레미스 도메인 컨트롤러에 액세스할 수 있는 한 사용자는 네트워크 공유에 액세스 하는 데 추가 설정이 필요 하지 않습니다.

### <a name="printers"></a>프린터

Microsoft Managed Desktop devices는 [하이브리드 클라우드 인쇄](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy)를 구성 하지 않은 경우 온-프레미스 Active Directory에 게시 된 프린터에 연결할 수 없습니다.

클라우드 전용 환경에서는 프린터를 자동으로 검색할 수 없지만 장치에 온-프레미스 도메인 컨트롤러에 대 한 액세스 권한이 있으면 사용자가 프린터 경로 또는 프린터 큐 경로를 사용 하 여 온-프레미스 프린터를 사용할 수 있습니다.

<!--add fuller material on printers when available-->
