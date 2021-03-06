---
title: Microsoft 365 Business Premium 설정
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- TRN_SMB
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- OKR_SMB_M365
- TRN_M365B
- OKR_SMB_Videos
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: 도메인 및 사용자 추가, 보안 정책 설정 등 Microsoft 365 Business Premium의 설치 단계를 알아봅니다.
ms.openlocfilehash: cc20637d7a78bd34ecb61a4ed46eb06d564d63df
ms.sourcegitcommit: 25afc0c34edc7f8a5eb389d8c701175256c58ec8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47324499"
---
# <a name="set-up-microsoft-365-business-premium-in-the-setup-wizard"></a>설치 마법사에서 Microsoft 365 Business Premium 설정

이 비디오에서 Microsoft 365 Business Premium 설치에 대 한 개요를 시청 하세요.<br><br>

## <a name="add-your-domain-users-and-set-up-policies"></a>도메인, 사용자 및 정책 설정 추가

Microsoft 365 Business Premium을 구입 하는 경우 소유 하 고 있는 도메인을 사용 하거나 [등록](sign-up.md)중에 하나를 구입 하는 옵션이 있습니다.

- 등록할 때 새 도메인을 구입하면 도메인이 모두 설정되어 [사용자 추가 및 라이선스를 할당](#add-users-and-assign-licenses)으로 이동할 수 있습니다.

### <a name="add-your-domain-to-personalize-sign-in"></a>로그인 개인 설정을 위한 도메인 추가

1. 전역 관리자 자격 증명을 사용하여 [Microsoft 365 관리 센터](https://admin.microsoft.com)에 로그인합니다. 

2. **설정으로 이동**을 선택해 마법사를 시작합니다.

    ![설정으로 이동을 선택 합니다.](../media/gotosetupinadmincenter.png)

3. **Office 앱 설치** 페이지에서 컴퓨터에 선택적으로 앱을 설치할 수 있습니다.
    
4. **도메인 추가** 단계에서 사용할 도메인 이름(예: contoso.com)을 입력합니다.

    > [!IMPORTANT]
    > 등록할 때 도메인을 구입한 경우에는 **도메인 추가** 단계가 표시되지 않습니다. 대신 [사용자 추가](#add-users-and-assign-licenses)로 이동합니다.

    ![로그인 페이지를 개인 설정 합니다.](../media/adddomain.png)

    
4. 마법사의 단계에 따라 도메인을 소유 하 고 있는지 확인 하는 [dns 호스팅 공급자 (Microsoft 365)에 대 한 dns 레코드를 만듭니다](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) . 도메인 호스트를 알고 있는 경우 [호스트 관련 지침](https://docs.microsoft.com/office365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions)을 참조하세요.

    호스팅 공급자가 GoDaddy이거나 [도메인 연결](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect)을 사용하는 다른 호스트를 사용하는 경우에는 프로세스가 간단하며, 자동으로 로그인하라는 메시지가 표시되고 Microsoft가 사용자를 대신하여 인증하도록 합니다.

    ![GoDaddy 액세스 확인 페이지에서 승인을 선택합니다.](../media/godaddyauth.png)

### <a name="add-users-and-assign-licenses"></a>사용자 추가 및 라이선스 할당

마법사에서 사용자를 추가하거나 관리 센터에서 [나중에 사용자를 추가](add-users-m365b.md)할 수도 있습니다. 또한 로컬 도메인 컨트롤러를 사용하는 경우 [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)를 사용하여 사용자를 추가할 수 있습니다.

#### <a name="add-users-in-the-wizard"></a>마법사에서 사용자 추가

마법사에서 추가 하는 모든 사용자는 Microsoft 365 Business Premium 라이선스를 자동으로 할당 받습니다.

![마법사의 새 사용자 추가 페이지 스크린샷](../media/addnewuserspage.png)

1. Microsoft 365 Business Premium 구독에 기존 사용자가 있는 경우 (예: Azure AD Connect를 사용한 경우) 지금 라이선스를 할당 하는 옵션이 제공 됩니다. 해당 사용자에게도 라이선스를 추가합니다.

2. 해당 사용자를 추가한 후 새로 추가한 사용자와 자격 증명을 공유하는 옵션도 여기에 표시됩니다. 자격 증명을 인쇄, 전자 메일로 전송 또는 다운로드할 수 있습니다.

### <a name="connect-your-domain"></a>도메인 연결

> [!NOTE]
> .onmicrosoft 도메인을 사용하거나 Azure AD Connect를 사용하여 사용자를 설정하는 경우에는 이 단계가 표시되지 않습니다.
  
서비스를 설정하려면 DNS 호스트 또는 도메인 등록 기관에서 레코드를 업데이트해야 합니다.
  
1. 설정 마법사는 일반적으로 사용자의 등록 기관을 감지하여 등록 기관 웹 사이트에서 NS 레코드를 업데이트하기 위한 단계별 지침의 링크를 제공합니다. 그렇지 [않은 경우 이름 서버를 변경 하 여 도메인 등록자와 함께 Microsoft 365을 설정](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/change-nameservers-at-any-domain-registrar)합니다. 

    - 기존 웹 사이트와 같은 기존 DNS 레코드를 사용하지만 DNS 호스트를 [도메인 연결](https://docs.microsoft.com/office365/admin/get-help-with-domains/domain-connect)에서 사용할 수 있는 경우 **레코드 추가**를 선택 합니다. **온라인 서비스 선택** 페이지에서 모든 기본값을 적용하고 **다음**을 선택한 후 DNS 호스트의 페이지에서 **승인**을 선택합니다.
    - 도메인 연결 사용이 설정되지 않은 다른 DNS 호스트에서 기존 DNS 레코드를 사용하는 경우 기존 서비스를 계속 연결할 수 있도록 DNS 레코드를 관리하는 것이 좋습니다. 자세한 내용은 [도메인 기본 사항](https://docs.microsoft.com/office365/admin/get-help-with-domains/dns-basics)을 참조하세요.

        ![레코드 활성화 페이지](../media/activaterecords.png)

2. 마법사의 단계를 따르면 전자 메일 및 기타 서비스가 설정됩니다.

### <a name="protect-your-organization"></a>조직 보호 

마법사에서 설정한 정책이 *모든 사용자*라는 [보안 그룹](https://docs.microsoft.com/office365/admin/create-groups/compare-groups#security-groups) 에 자동으로 적용 됩니다. 관리 센터에서 정책을 할당 하는 추가 그룹을 만들 수도 있습니다.

1. **고급 사이버 위협 으로부터 보호를 강화**하려면 기본값을 사용 하 여 [Office 365 advanced Threat protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp) 이 office 앱에서 파일 및 링크를 검사 하도록 하는 것이 좋습니다.

    ![보호 기능 향상 페이지 스크린샷](../media/increasetreatprotection.png)


2. **중요 한 데이터의 누출 방지** 페이지에서 OFFICE 365 DLP (데이터 손실 방지)를 설정 하 여 office 앱에서 중요 한 데이터를 추적 하 고 조직 외부에서 실수로 공유 하지 않도록 하는 기본값을 적용 합니다.

3. **비즈니스용 Office의 데이터 보호** 페이지에서 모바일 앱 관리를 유지 하 고 설정을 확장 하 고 검토 한 다음, **모바일 앱 관리 정책 만들기**를 선택 합니다.

    ![Mobile 용 Office의 데이터 보호 페이지 스크린샷](../media/protectdatainmobile.png)


## <a name="secure-windows-10-pcs"></a>Windows 10 Pc 보안

왼쪽 탐색 창에서 **설치** 를 선택 하 고 **로그인 및 보안**에서 **Windows 10 컴퓨터 보안**을 선택 합니다. 시작 하려면 **보기** 를 선택 합니다. 전체 지침은 [Windows 10 컴퓨터 보안](secure-win-10-pcs.md) 을 참조 하세요.

## <a name="deploy-office-365-client-apps"></a>Office 365 클라이언트 앱 배포

설치 중에 Office 앱을 자동으로 설치 하도록 선택한 경우 앱은 사용자가 자신의 Windows 장치에서 Azure AD에 로그인 한 후 회사 자격 증명을 사용 하 여 Windows 10 장치에 설치 됩니다.

모바일 iOS 또는 Android 장치에 Office를 설치 하려면 [Set up 모바일 장치 For Microsoft 365 Business Premium users](set-up-mobile-devices.md)를 참조 하세요.

Office를 개별적으로 설치할 수도 있습니다. 자세한 내용은 [PC 또는 Mac에 Office 설치](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) 를 참조 하세요.

## <a name="see-also"></a>참고 항목

[Microsoft 365 Business 교육 비디오](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
