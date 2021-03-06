---
title: 보안 전자 메일 권장 정책-엔터프라이즈에 대 한 Microsoft 365 | Microsoft Docs
description: 메일 정책과 구성을 적용하는 방법에 관한 Microsoft 권장 정책을 설명합니다.
ms.author: josephd
author: JoeDavies-MSFT
manager: Laurawi
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.reviewer: martincoetzer
ms.custom:
- it-pro
- goldenconfig
ms.collection:
- M365-identity-device-management
- M365-security-compliance
- remotework
- m365solution-identitydevice
- m365solution-scenario
ms.openlocfilehash: f2d3b9180ad5ab58e92812ed7b2d4f7ba07e2971
ms.sourcegitcommit: 474bd6a86c3692d11fb2c454591c89029ac5bbd5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/19/2020
ms.locfileid: "49357112"
---
# <a name="policy-recommendations-for-securing-email"></a>메일을 보호하기 위한 정책 권장 사항

이 문서에서는 최신 인증 및 조건부 액세스를 지 원하는 조직 전자 메일 및 전자 메일 클라이언트를 보호 하기 위해 권장 되는 id 및 장치 액세스 정책을 구현 하는 방법을 설명 합니다. 이 지침은 [일반 id 및 장치 액세스 정책](identity-access-policies.md) 에 대해 구축 되며 몇 가지 추가 권장 사항도 포함 되어 있습니다.

이러한 권장 사항은 **기본**, **중요** 및 **높은 규제** 의 요구 사항에 따라 적용할 수 있는 세 가지 다른 보안 및 보호 계층을 기반으로 합니다. [권장되는 보안 정책 및 구성 소개](microsoft-365-policies-configurations.md)에서 이러한 권장 사항을 참조하여 이러한 보안 계층, 권장되는 클라이언트 운영 체제에 대해 더 자세히 알아볼 수 있습니다.

이러한 권장 사항을 적용 하려면 사용자가 모바일 장치에서 iOS 및 Android 용 Outlook을 비롯 한 최신 전자 메일 클라이언트를 사용 해야 합니다. IOS 및 Android 용 Outlook에서는 Office 365의 최상의 기능을 지원 합니다. 이러한 모바일 Outlook 앱은 모바일 사용을 지원 하 고 다른 Microsoft 클라우드 보안 기능과 함께 사용할 수 있는 보안 기능으로도 설계 되었습니다. 자세한 내용은 [iOS 및 Android 용 OUTLOOK FAQ](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/outlook-for-ios-and-android/outlook-for-ios-and-android-faq)를 참조 하세요.

## <a name="update-common-policies-to-include-email"></a>전자 메일을 포함 하도록 일반 정책 업데이트

다음 다이어그램에서는 전자 메일을 보호 하기 위해 일반 id 및 장치 액세스 정책에서 업데이트할 정책을 보여 줍니다.

[![팀 및 해당 종속 서비스에 대 한 액세스를 보호 하기 위한 정책 업데이트 요약](../../media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)

[이 이미지의 더 큰 버전 보기](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)

Exchange Online에 대 한 새 정책을 추가 하 여 ActiveSync 클라이언트를 차단 하는 방법에 유의 하세요. 이렇게 하면 Outlook mobile을 사용 하 게 됩니다.

정책을 설정할 때 정책 범위에 Exchange Online과 Outlook을 포함 한 경우에는 ActiveSync 클라이언트를 차단 하는 새 정책만 만들면 됩니다. 다음 표에 나와 있는 정책 들을 검토 하 고 권장 되는 추가 내용을 확인 하거나 이미 포함 되어 있는 것을 확인 합니다. 각 정책은 [일반 id 및 장치 액세스 정책의](identity-access-policies.md)관련 구성 지침에 연결 됩니다.

|보호 수준|정책|추가 정보|
|---|---|---|
|**기준**|[로그인 위험이 *보통* 또는 *높을* 때 MFA 필요](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|클라우드 앱 할당에 Exchange Online 포함|
||[최신 인증을 지원하지 않는 클라이언트 차단](identity-access-policies.md#block-clients-that-dont-support-modern-authentication)|클라우드 앱 할당에 Exchange Online 포함|
||[앱 데이터 보호 정책 적용](identity-access-policies.md#apply-app-data-protection-policies)|Outlook이 앱 목록에 포함 되어 있어야 합니다. 각 플랫폼의 정책 (iOS, Android, Windows)을 업데이트 해야 합니다.|
||[승인 된 앱 및 앱 보호 필요](identity-access-policies.md#require-approved-apps-and-app-protection)|클라우드 앱 목록에 Exchange Online 포함|
||[호환 PC 필요](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|클라우드 앱 목록에 Exchange Online 포함|
||[ActiveSync 클라이언트 차단](#block-activesync-clients)|새 정책 추가|
|**중요**|[로그인 위험이 *낮은* *경우 MFA* 필요 *high*](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|클라우드 앱 할당에 Exchange Online 포함|
||[준수 Pc *및* 모바일 장치 요구](identity-access-policies.md#require-compliant-pcs-and-mobile-devices)|클라우드 앱 목록에 Exchange Online 포함|
|**매우 엄격한 규제**|[*항상* MFA 필요](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|클라우드 앱 할당에 Exchange Online 포함|
|

## <a name="block-activesync-clients"></a>ActiveSync 클라이언트 차단

이 정책은 ActiveSync 클라이언트가 다른 조건부 액세스 정책을 무시할 수 없도록 합니다. 정책 구성은 ActiveSync 클라이언트에만 적용 됩니다. 이 정책은 **[앱 보호 정책 필요](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-grant#require-app-protection-policy)** 를 선택 하 여 ActiveSync 클라이언트를 차단 합니다. 이 정책 만들기에 대 한 자세한 내용은 [조건부 액세스를 사용한 클라우드 앱 액세스에 대 한 앱 보호 정책 필요](https://docs.microsoft.com/azure/active-directory/conditional-access/app-protection-based-conditional-access)를 참조 하세요.

- 시나리오 1의 "2 단계: ActiveSync를 사용 하 여 Azure AD 조건부 액세스 정책 구성 (EAS)" [: Office 365 앱은 앱 보호 정책과 함께 승인 된 앱이 필요](https://docs.microsoft.com/azure/active-directory/conditional-access/app-protection-based-conditional-access#scenario-1-office-365-apps-require-approved-apps-with-app-protection-policies)하므로 기본 인증을 사용 하는 exchange ActiveSync 클라이언트에서 exchange Online에 연결할 수 없습니다.

인증 정책을 사용 하 여 [기본 인증을 사용 하지 않도록 설정](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/disable-basic-authentication-in-exchange-online)하 여 모든 클라이언트 액세스 요청이 최신 인증을 사용 하도록 할 수도 있습니다.

## <a name="limit-access-to-exchange-online-from-outlook-on-the-web"></a>웹용 Outlook에서 Exchange Online에 대 한 액세스 제한

사용자가 umnanaged 장치에서 웹에 있는 첨부 파일을 다운로드 하는 기능이 제한 될 수 있습니다. 이러한 장치에서 사용자는 파일을 누설 및 저장 하지 않고 Office Online을 사용 하 여 이러한 파일을 보고 편집할 수 있습니다. 또한 사용자가 관리 되지 않는 장치에서 첨부 파일을 볼 수 없도록 차단할 수도 있습니다.

단계는 다음과 같습니다.

1. [Exchange Online 원격 PowerShell 세션에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)합니다.
2. 아직 OWA 사서함 정책이 없는 경우에는 [set-owamailboxpolicy](https://docs.microsoft.com/powershell/module/exchange/new-owamailboxpolicy) cmdlet을 사용 하 여 하나를 만듭니다.
3. 다운로드 하지 않고 첨부 파일을 볼 수 있도록 허용 하려면 다음 명령을 사용 합니다.

   ```powershell
   Set-OwaMailboxPolicy -Identity Default -ConditionalAccessPolicy ReadOnly
   ```

4. 첨부 파일을 차단 하려면 다음 명령을 사용 합니다.

   ```powershell
   Set-OwaMailboxPolicy -Identity Default -ConditionalAccessPolicy ReadOnlyPlusAttachmentsBlocked
   ```

5. Azure portal에서 다음 설정을 사용 하 여 새 조건부 액세스 정책을 만듭니다.

   **배정** \> **사용자 및 그룹**: 포함 하거나 제외할 적절 한 사용자 및 그룹을 선택 합니다.

   **배정** \> **클라우드 앱 또는 작업** \> **클라우드 앱** \> **포함** \> **앱 선택**: **Office 365 Exchange Online** 선택

   **액세스 제어** \> **세션**: **앱 적용 제한 사용** 을 선택 합니다.

## <a name="require-that-ios-and-android-devices-must-use-outlook"></a>IOS 및 Android 장치에서 Outlook을 사용 해야 함

IOS 및 Android 장치 사용자가 iOS 및 Android 용 Outlook을 사용 하 여 회사 또는 학교 콘텐츠에만 액세스할 수 있도록 하려면 이러한 잠재적 사용자를 대상으로 하는 조건부 액세스 정책이 필요 합니다.

[IOS 및 Android 용 Outlook을 사용 하 여 메시징 공동 작업 액세스 관리]( https://docs.microsoft.com/mem/intune/apps/app-configuration-policies-outlook#apply-conditional-access)에서이 정책을 구성 하는 단계를 참조 하세요.

## <a name="set-up-message-encryption"></a>메시지 암호화 설정

Azure Information Protection의 보호 기능을 활용 하는 새로운 Office 365 메시지 암호화 (OME) 기능을 사용 하면 조직에서 모든 장치에 있는 모든 사용자와 보호 된 전자 메일을 쉽게 공유할 수 있습니다. 사용자는 Outlook.com, Gmail 및 기타 전자 메일 서비스를 사용 하는 고객 뿐만 아니라 다른 Microsoft 365 조직과의 보호 된 메시지를 주고 받을 수 있습니다.

자세한 내용은 [Set Up Office 365 Message Encryption capabilities](https://docs.microsoft.com/microsoft-365/compliance/set-up-new-message-encryption-capabilities)를 참조 하십시오.

## <a name="next-steps"></a>다음 단계

![4 단계: Microsoft 365 클라우드 앱에 대 한 정책](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

다음에 대 한 조건부 액세스 정책 구성:

- [Microsoft Teams](teams-access-policies.md)
- [SharePoint](sharepoint-file-access-policies.md)
