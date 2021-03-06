---
title: Microsoft 365 비즈니스 계획을 보호 하는 10 가지 주요 방법
f1.keywords:
- CSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: de2da300-dbb6-4725-bb12-b85a9d296e75
description: '랜 섬 웨어, 피싱 및 악의적 첨부 파일을 포함 하 여 사이버 위협 으로부터 비즈니스 전자 메일 및 데이터를 보호 합니다. '
ms.openlocfilehash: c74b8a096afe1dbdd0e0d0cdc7ca5ce3fe8f9ea8
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843321"
---
# <a name="top-10-ways-to-secure-microsoft-365-for-business-plans"></a>Microsoft 365 비즈니스 계획을 보호 하는 10 가지 주요 방법

::: moniker range="o365-21vianet"

> [!NOTE]
> 관리 센터가 변경되고 있습니다. 사용자의 환경이 여기에 설명된 세부 정보와 맞지 않는 경우에는 [새 Microsoft 365 관리 센터 정보](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet)를 참조하세요.

::: moniker-end

Microsoft의 비즈니스 계획 중 하나를 사용 하는 중소 규모의 조직이 나 조직의 유형이 사이버 범죄자와 해커의 대상이 되는 경우이 문서의 지침을 사용 하 여 조직의 보안을 강화 합니다. 이 지침은 조직에서 Harvard Kennedy School [Cybersecurity 캠페인 안내서](https://go.microsoft.com/fwlink/p/?linkid=2015598)에 설명 된 목표를 달성 하는 데 도움이 됩니다.

서비스 요금제에 해당 하는 다음 표에 나열 된 작업을 완료 하는 것이 좋습니다.

||작업|Microsoft 365 Business Standard|Microsoft 365 Business Premium|
|---|---|---|---|
|1 |[다단계 인증 설정](secure-your-business-data.md#setup)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|2|[사용자 교육](secure-your-business-data.md#train)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|3(sp3)|[전용 관리자 계정 사용](secure-your-business-data.md#admin)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|4 |[메일에서 맬웨어에 대 한 보호 수준 올리기](secure-your-business-data.md#malware)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|5 |[랜섬웨어로부터 보호](secure-your-business-data.md#ransomware)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|6 |[전자 메일에 대 한 자동 전달 중지](secure-your-business-data.md#forwarding)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|7 |[Office 메시지 암호화 사용](secure-your-business-data.md#encryption)||![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|8 |[피싱 공격 으로부터 전자 메일을 보호 합니다.](secure-your-business-data.md#phishing)||![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|9 |[안전한 첨부 파일을 사용 하 여 악의 있는 첨부 파일과 파일 보호](secure-your-business-data.md#atp)||![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|10  |[안전한 링크를 통한 피싱 공격 으로부터 보호](secure-your-business-data.md#phishingatp)||![시킨](../../media/d238e041-6854-4a78-9141-049224df0795.png)|

시작 하기 전에 Microsoft 365 보안 센터에서 [microsoft 365 보안 점수](https://docs.microsoft.com/microsoft-365/security/mtp/microsoft-secure-score) 를 확인 하세요. 중앙 집중식 대시보드에서 Microsoft 365 id, 데이터, 앱, 장치 및 인프라에 대 한 보안을 모니터링 하 고 향상 시킬 수 있습니다. 권장 되는 보안 기능을 구성 하 고, 보고서 보기와 같은 보안 관련 작업을 수행 하거나, 타사 응용 프로그램 또는 소프트웨어를 사용 하 여 권장 주소를 지정 하기 위한 사항이 제공 됩니다. 보다 광범위 한 Microsoft 제품 및 서비스 집합에 대 한 추가 통찰력과 가시성을 통해 조직의 보안 상태에 대 한 보고를 받을 수 있습니다.

![Microsoft 보안 점수 스크린샷](../../media/secure-score.png)

## <a name="1-set-up-multi-factor-authentication"></a>1: multi-factor authentication 설정
<a name="setup"> </a>

다단계 인증을 사용 하는 것은 조직의 보안을 강화 하는 가장 쉽고 효율적인 방법 중 하나입니다. 사용자가 로그인 하는 것 보다 더 쉬운 기능, 다단계 인증은 사용자가 휴대폰에서 코드를 입력 하 여 Microsoft 365에 액세스 하는 것을 의미 합니다. 이렇게 하면 해커가 사용자의 암호를 알고 있는 경우에는이를 방지할 수 있습니다. Multi-factor authentication은 2 단계 확인이 라고도 합니다. 사용자는 대부분의 계정에 대해 2 단계 인증을 사용자의 Google 또는 Microsoft 계정에 쉽게 추가할 수 있습니다. [두 단계 인증을 개인 Microsoft 계정에 추가](https://go.microsoft.com/fwlink/p/?linkid=2016403)하는 방법은 다음과 같습니다.

Microsoft 365을 사용 하는 회사의 경우 사용자가 다단계 인증을 사용 하 여 로그인 해야 하는 설정을 추가 합니다. 이 변경 작업을 수행 하면 사용자가 다음에 로그인 할 때 전화를 2 단계 인증으로 설정 하 라는 메시지가 표시 됩니다.
MFA를 설정 하는 방법 및 사용자가 설정을 완료 하는 방법에 대 한 교육 비디오를 보려면 [설정 업 mfa](https://support.microsoft.com/office/e12187b8-216a-4490-9e3b-df34a06fb787) 및 [사용자 설정](https://support.microsoft.com/office/a32541df-079c-420d-9395-9d59354f7225)를 참조 하세요.

다단계 인증을 설정 하려면 보안 기본값을 설정 합니다.

대부분의 조직에서 보안 기본값은 적절한 수준의 추가 로그인 보안을 제공합니다. 자세한 내용은 [보안 기본값이란?](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)을 참조하세요.

신규 구독이면 보안 기본값이 이미 자동으로 설정되었을 수 있습니다.

Azure 포털의 Azure Active Directory(Azure AD)에 대해 **속성** 창에서 보안 기본값을 사용하거나 사용하지 않도록 설정할 수 있습니다.

1. 전역  관리자 자격 증명으로 [Microsoft 365 관리 센터](https://admin.microsoft.com)에 로그인합니다.
2. 왼쪽 탐색 메뉴에서 **모두 표시** 를 선택하고 **관리 센터** 에서 **Azure Active Directory** 를 선택합니다.
3. **Azure Active Directory 관리 센터** 에서 **Azure Active Directory** > **속성** 을 선택합니다.
4. 페이지 하단에서 **보안 기본값 관리** 를 선택합니다.
5. 보안 기본값을 사용하도록 설정하려면 **예** 를 선택하고 사용하지 않도록 설정하려면 **아니요** 를 선택한 다음 **저장** 을 선택합니다.

조직에 대한 다단계 인증을 설정한 후에는 사용자가 장치에서 2단계 인증을 설정해야 합니다. 자세한 내용은 [Set up 2-step 확인-Microsoft 365](https://support.microsoft.com/office/ace1d096-61e5-449b-a875-58eb3d74de14)를 참조 하세요.

모든 세부 정보 및 권장 사항에 대 한 자세한 내용은 [사용자에 대 한 다단계 인증 설정을](set-up-multi-factor-authentication.md)참조 하십시오.

## <a name="2-train-your-users"></a>2: 사용자 교육
<a name="train"> </a>

Harvard Kennedy School [Cybersecurity 캠페인 안내서](https://go.microsoft.com/fwlink/p/?linkid=2015598) 에서는 피싱 공격을 식별 하기 위한 교육 사용자를 포함 하 여 조직 내에서 보안을 보다 강력 하 게 인식 하는 방법을 제공 합니다.

이 지침 외에도, 사용자가 [해커 및 맬웨어로부터 계정 및 장치를 보호](https://support.microsoft.com/office/066d6216-a56b-4f90-9af3-b3a1e9a327d6)하는이 문서에서 설명 하는 작업을 수행 하는 것이 좋습니다. 이러한 작업은 다음과 같습니다.

- 강력한 암호 사용

- 장치 보호

- Windows 10 및 Mac Pc에서 보안 기능을 사용 하도록 설정

또한 사용자는 다음 문서에서 권장 하는 작업을 수행 하 여 개인 전자 메일 계정을 보호 하는 것이 좋습니다.

- [Outlook.com 전자 메일 계정 보호](https://support.microsoft.com/office/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

- [2 단계 인증을 사용 하 여 Gmail 계정 보호](https://go.microsoft.com/fwlink/p/?linkid=2015688&)

## <a name="3-use-dedicated-admin-accounts"></a>3: 전용 관리자 계정 사용
<a name="admin"> </a>

Microsoft 365 환경을 관리 하는 데 사용 하는 관리 계정에 상승 된 권한이 포함 되어 있습니다. 해커 및 사이버 범죄자에 게 유용한 목표입니다. 관리 계정만 관리자에 게 사용 합니다. 관리자에 게는 관리 작업과 관련 된 일반 사용을 위한 별도의 사용자 계정이 있어야 하며, 해당 작업 기능과 연결 되는 작업을 완료 하는 데 필요한 경우에만 해당 관리자 계정을 사용 해야 합니다. 추가 권장 사항:

- 관리자 계정도 다단계 인증용으로 설정 해야 합니다.

- 관리 계정을 사용 하기 전에 개인 전자 메일 계정을 포함 하 여 관련 없는 브라우저 세션과 앱을 모두 닫으십시오.

- 관리 작업을 완료 한 후에는 브라우저 세션에서 로그 아웃 해야 합니다.

## <a name="4-raise-the-level-of-protection-against-malware-in-mail"></a>4: 메일에서 맬웨어에 대 한 보호 수준을 올립니다.
<a name="malware"> </a>

Microsoft 365 환경에는 맬웨어에 대 한 보호 기능이 포함 되어 있지만 일반적으로 맬웨어에 사용 되는 파일 형식을 사용 하면이 보호 기능을 향상 시킬 수 있습니다. 전자 메일에서 맬웨어 보호를 강화 하려면 [간단한 교육 비디오](https://support.microsoft.com/office/02b5783a-eea0-42e8-8856-62440718c3f0)를 보거나 다음 단계를 완료 합니다.

1. 으로 이동 하 <https://protection.office.com> 고 관리자 계정 자격 증명으로 로그인 합니다.

2. 보안 & 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리** 에서 **정책** \> **맬웨어 방지** 를 선택 합니다.

3. 기본 정책을 두 번 클릭 하 여이 회사 차원의 정책을 편집 합니다.

4. **설정** 을 선택합니다.

5. **일반 첨부 파일 형식 필터** 에서 **설정** 를 선택 합니다. 차단 되는 파일 형식은이 컨트롤 바로 아래의 창에 나열 됩니다. 필요한 경우 나중에 파일 형식을 추가 하거나 삭제할 수 있습니다.

6. **저장을 선택 합니다.**

자세한 내용은 [EOP의 맬웨어 방지 보호](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-malware-protection)를 참조 하세요.

## <a name="5-protect-against-ransomware"></a>5: 랜 섬 웨어 로부터 보호
<a name="ransomware"> </a>

랜 섬 웨어는 파일 암호화 또는 컴퓨터 화면 잠금을 통해 데이터에 대 한 액세스를 제한 합니다. 그런 다음 "ransom"를 사용 하 여 victims에서 데이터에 액세스 하는 데 사용 하는 것이 좋습니다.

메일 흐름 규칙을 하나 이상 만들어, 랜 섬 웨어에 자주 사용 되는 파일 확장명을 차단 하거나, 전자 메일로 이러한 첨부 파일을 받는 사용자에 게 경고 메시지를 표시 하 여 랜 섬 웨어 로부터 보호를 받을 수 있습니다. 좋은 출발점은 다음과 같은 두 가지 규칙을 만드는 것입니다.

- 매크로를 포함 하는 Office 첨부 파일을 열기 전에 사용자에 게 경고 합니다. 매크로를 사용할 수 없도록이 파일을 사용자에 게 경고 합니다.

- 랜 섬 웨어 또는 기타 악성 코드가 포함 될 수 있는 파일 형식을 차단 합니다. 다음 표에 나열 된 것 처럼 일반적인 실행 파일 목록을 사용 하 여 시작 합니다. 조직에서 이러한 실행 유형 중 하나를 사용 하는 경우 해당 유형이 전자 메일로 전송 될 것으로 예상 되 면이를 이전 규칙 (사용자에 게 경고)에 추가 합니다.

메일 전송 규칙을 만들려면 [간단한 교육 비디오](https://support.microsoft.com/office/a9ecca03-42a6-4867-b9fd-38e3f6bb06ad)를 보거나 다음 단계를 완료 합니다.

1. [Exchange 관리 센터](https://go.microsoft.com/fwlink/p/?linkid=2059104)로 이동합니다.

2. **메일 흐름** 범주에서 **규칙** 을 선택 합니다.

3. **+** 을 선택 하 고 **새 규칙을 만듭니다**.

4. 대화 상자 아래쪽에 있는 * * * *를 선택 하 여 전체 옵션 집합을 표시 합니다.

5. 각 규칙에 대해 다음 표의 설정을 적용 합니다. 설정을 변경 하려는 경우가 아니면 나머지 설정은 기본값으로 유지 합니다.

6. **저장** 을 선택합니다.
    
| 설정 | Office 파일의 첨부 파일을 열기 전에 사용자에 게 경고 표시 | 랜 섬 웨어 또는 기타 악성 코드가 포함 될 수 있는 파일 형식 차단 |
|:-----|:-----|:-----|
|이름  <br/> |랜 섬 웨어 방지 규칙: 사용자에 게 경고 표시  <br/> |랜 섬 웨어 방지 규칙: 파일 형식 차단  <br/> |
|다음 경우에이 규칙을 적용 합니다. . .  <br/> |모든 첨부 파일 . . 일치 하는 파일 확장명 . .  <br/> |모든 첨부 파일 . . 일치 하는 파일 확장명 . .  <br/> |
|단어 또는 구 지정  <br/> |다음 파일 형식을 추가 합니다.  <br/> normal.dotm, .docm, .xlsm, sltm, .xla, xlam, xll, pptm, potm, ppam, ppsm, sltm  <br/> |다음 파일 형식을 추가 합니다.  <br/> ade, adp, ani, bas, bat, chm, cmd, a, m, s, com, cpl, crt, .hlp, ht, mdz, inf, v p v, ini, 작업, js, shs, 모바일,, mde, msi, wsc, .pcd, s p l, exe, .wsf 인  <br/> |
|다음을 수행 합니다. . .  <br/> |고 지 사항 앞에 추가  <br/> |메시지를 차단 합니다. . . 메시지를 거부 하 고 설명 포함  <br/> |
|메시지 텍스트 제공  <br/> |파일에 악성 코드가 포함 되어 있고 보낸 사람이 안전을 확신할 수 없는 경우에는 이러한 유형의 파일을 열지 않는 것이 좋습니다.  <br/> ||
   
> [!TIP]
> 또한 [4 단계](#4-raise-the-level-of-protection-against-malware-in-mail)에서 맬웨어 방지 목록에 차단할 파일을 추가할 수 있습니다.

자세한 내용은 다음을 참조하세요.

- [랜 섬 웨어: 위험을 줄이는 방법](https://www.microsoft.com/security/blog/2020/04/28/ransomware-groups-continue-to-target-healthcare-critical-services-heres-how-to-reduce-risk/)

- [OneDrive 복원](https://support.microsoft.com/office/fa231298-759d-41cf-bcd0-25ac53eb8a15)

## <a name="6-stop-auto-forwarding-for-email"></a>6: 전자 메일에 대 한 자동 전달 중지
<a name="forwarding"> </a>

사용자의 사서함에 대 한 액세스 권한을 획득 하는 해커는 전자 메일을 자동으로 전달 하도록 사서함을 구성 하 여 메일을 exfiltrate 수 있습니다. 사용자의 인식이 없어도이 문제가 발생할 수 있습니다. 메일 흐름 규칙을 구성 하 여 이러한 상황이 발생 하지 않도록 할 수 있습니다.

메일 전송 규칙을 만들려면 다음을 수행 합니다.

1. [Exchange 관리 센터](https://go.microsoft.com/fwlink/p/?linkid=2059104)로 이동합니다.

2. **메일 흐름** 범주에서 **규칙** 을 선택 합니다.

3. **+** 을 선택 하 고 **새 규칙을 만듭니다**.

4. 대화 상자 아래쪽의 **기타 옵션** 을 선택 하 여 전체 옵션 집합을 표시 합니다.

5. 다음 표의 설정을 적용 합니다. 설정을 변경 하려는 경우가 아니면 나머지 설정은 기본값으로 유지 합니다.

6. **저장** 을 선택합니다.

|설정|외부 도메인에 대 한 자동 전달 전자 메일 거부|
|---|---|
|이름|외부 도메인에 대 한 전자 메일 자동 전달 금지|
|다음 경우에이 규칙 적용 ...|보낸 사람입니다. . . 은 외부/내부입니다. . . 조직 내부|
|조건 추가|받는 사람입니다. . . 은 외부/내부입니다. . . 조직 외부|
|조건 추가|메시지 속성 . . 메시지 유형을 포함 합니다. . . 자동 전달|
|다음을 수행 합니다.|메시지를 차단 합니다. . . 메시지를 거부 하 고 설명을 포함 합니다.|
|메시지 텍스트 제공|보안상의 이유로이 조직 외부에서 전자 메일을 자동 전달 하는 것은 허용 되지 않습니다.|

## <a name="7-use-office-message-encryption"></a>7: Office 메시지 암호화 사용
<a name="encryption"> </a>

Office 메시지 암호화는 Microsoft 365에 포함 되어 있습니다. 이미 설정 되어 있습니다. Office 메시지 암호화를 사용 하면 조직에서 조직 내부 및 외부의 사용자 간에 암호화 된 전자 메일 메시지를 보내고 받을 수 있습니다. Office 365 메시지 암호화는 Outlook.com, Yahoo!, Gmail 및 기타 전자 메일 서비스에서 작동 합니다. 전자 메일 메시지 암호화는 의도 된 받는 사람만 메시지 콘텐츠를 볼 수 있도록 합니다.

Office 메시지 암호화는 메일을 보낼 때 두 가지 보호 옵션을 제공 합니다.

- 전달 금지

- #A0

조직에서 기밀과 같은 전자 메일에 레이블을 적용 하는 추가 옵션을 구성 했을 수 있습니다.

### <a name="to-send-protected-email"></a>보호 된 전자 메일을 보내려면

PC 용 Outlook에서 전자 메일의 **옵션** 을 선택 하 고 **사용 권한을** 선택 합니다.

![Outlook의 전자 메일 메시지 암호화](../../media/08e90a7e-a2d2-41a4-bae9-0a46b4ce639a.png)

Outlook.com에서 전자 메일에서 **보호** 를 선택 합니다. 기본 보호는 **전달 되지** 않습니다. 이를 암호화 하도록 변경 하려면 **사용 권한** \> **암호화** 변경을 선택 합니다.

![Outlook.com의 전자 메일 메시지 암호화](../../media/329ccf50-f6b1-4fb8-b249-60b907a82b7e.png)

### <a name="to-receive-encrypted-email"></a>암호화 된 전자 메일을 받으려면

받는 사람이 Outlook 2013 또는 Outlook 2016와 Microsoft 전자 메일 계정을 사용 하는 경우 읽기 창에서 해당 항목의 제한 된 권한에 대 한 알림을 볼 수 있습니다. 메시지를 연 후 받는 사람은 메시지를 다른 것 처럼 볼 수 있습니다.

받는 사람이 Gmail 또는 Yahoo와 같은 다른 전자 메일 클라이언트나 전자 메일 계정을 사용 하는 경우에는 로그인 하 여 전자 메일 메시지를 읽거나 일회용 암호를 요청 하 여 웹 브라우저에서 메시지를 볼 수 있는 링크가 표시 됩니다. 사용자가 전자 메일을 받지 못하는 경우 스팸 또는 정크 폴더를 확인 하도록 합니다.

자세한 내용은 [Outlook FOR PC에서 암호화 된 메시지 보내기, 보기 및 회신을](https://support.microsoft.com/office/eaa43495-9bbb-4fca-922a-df90dee51980)참조 하세요.

## <a name="8-protect-your-email-from-phishing-attacks"></a>8. 피싱 공격 으로부터 전자 메일을 보호 합니다.
<a name="phishing"> </a>

Microsoft 365 환경에 대해 하나 이상의 사용자 지정 도메인을 구성한 경우에는 대상에 대 한 피싱 방지 보호를 구성할 수 있습니다. Microsoft Defender for Office 365의 일부인 피싱 방지 보호 기능을 통해 악의적인 가장 기반 피싱 공격 및 기타 피싱 공격 으로부터 조직을 보호할 수 있습니다. 사용자 지정 도메인을 구성 하지 않은 경우에는이 작업을 수행 하지 않아도 됩니다.

가장 중요 한 사용자와 사용자 지정 도메인을 보호 하는 정책을 만들어이 보호를 시작 하는 것이 좋습니다.

![Microsoft Defender for Office 365에서 피싱 방지 정책 만들기](../../media/security-and-compliance-center.png)

Defender for Office 365에서 피싱 방지 정책을 만들려면 [간단한 교육 비디오](https://support.microsoft.com/office/86c425e1-1686-430a-9151-f7176cce4f2c)를 보거나 다음 단계를 완료 하세요.

1. <https://protection.office.com>으로 이동합니다.

2. 보안 & 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리** 에서 **정책을** 선택 합니다.

3. 정책 페이지에서 **피싱 방지** 를 선택 합니다.

4. 피싱 방지 페이지에서 **+ 만들기** 를 선택 합니다. 피싱 방지 정책을 정의 하는 과정을 안내 하는 마법사가 시작 됩니다.

5. 아래 차트에서 권장 하는 대로 정책에 대 한 이름, 설명 및 설정을 지정 합니다. 자세한 내용은 [Microsoft Defender For Office 365 옵션의 피싱 방지 정책에 대 한](https://docs.microsoft.com/microsoft-365/security/office-365-security/set-up-anti-phishing-policies) 자세한 내용을 참조 하세요.

6. 설정을 검토 한 후에는 **이 정책 만들기** 또는 적절 한 **저장** 을 선택 합니다.

|설정 또는 옵션|권장 설정|
|---|---|
|이름|도메인 및 가장 귀중 한 캠페인 직원|
|설명|가장 중요 한 직원과 해당 도메인이 가장 되 고 있지 않은지 확인 합니다.|
|보호할 사용자를 추가|**조건을 추가 하 고 받는 사람** 을 선택 합니다. 사용자 이름을 입력 하거나 후보, 캠페인 관리자 및 기타 중요 교직원 구성원의 전자 메일 주소를 입력 합니다. 가장을 보호 하려는 최대 20 개의 내부 및 외부 주소를 추가할 수 있습니다.|
|보호할 도메인을 추가|**조건 추가, 받는 사람 도메인** 을 차례로 선택 합니다. Microsoft 365 구독에 연결 된 사용자 지정 도메인 (하나를 정의한 경우)을 입력 합니다. 둘 이상의 도메인을 입력할 수 있습니다.|
|작업 선택|가장 된 사용자가 전자 메일을 보낸 경우: **다른 전자 메일 주소로 메시지 리디렉션을** 선택 하 고 보안 관리자의 전자 메일 주소를 입력 합니다. 예: securityadmin@contoso.com. <br/> 가장 된 도메인에서 전자 메일을 보내는 경우: **메시지 격리** 를 선택 합니다.|
|사서함 인텔리전스|새 피싱 방지 정책을 만들 때 기본적으로 사서함 인텔리전스가 선택됩니다. 최상의 결과를 위해 해당 설정을 **켜짐** 에 둡니다.|
|신뢰할 수 있는 발신자와 도메인 추가|해당 예제에서는 어떠한 재정의도 정의하지 않아야 합니다.|
|적용 대상|**받는 사람의 도메인이 다음과 같음** 을 선택합니다. **이러한 항목 모두** 아래에서 **선택** 을 선택합니다. **+ 추가** 를 선택합니다. 목록에서 도메인 이름 (예: contoso.com) 옆에 있는 확인란을 선택 하 고 **추가** 를 선택 합니다. **완료** 를 선택합니다.|
|

자세한 내용은 [Defender for 피싱 정책에서 Office 365를](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-atp-anti-phishing-policies)참조 하세요.

## <a name="9-protect-against-malicious-attachments-and-files-with-safe-attachments"></a>9: 안전한 첨부 파일이 있는 악의 있는 첨부 파일 및 파일로 보호
<a name="atp"> </a>

사용자가 문서, 프레젠테이션, 스프레드시트 등의 첨부 파일을 정기적으로 보내고 받고 공유 합니다. 전자 메일 메시지를 확인 하기만 하면 첨부 파일이 안전한 지 또는 악의적 임을 쉽게 알 수 있습니다. Microsoft Defender for Office 365에는 안전한 첨부 파일 보호가 포함 되어 있지만이 보호 기능은 기본적으로 설정 되어 있지 않습니다. 이 보호 기능을 사용 하기 시작 하는 새 규칙을 만드는 것이 좋습니다. 이 보호는 SharePoint, OneDrive 및 Microsoft 팀의 파일로 확장 됩니다.

안전한 첨부 파일 정책을 만들려면 [간단한 교육 비디오](https://support.microsoft.com/office/e7e68934-23dc-4b9c-b714-e82e27a8f8a5)를 보거나 다음 단계를 완료 합니다.

1. 으로 이동 하 <https://protection.office.com> 고 관리자 계정으로 로그인 합니다.

2. 보안 & 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리** 에서 **정책을** 선택 합니다.

3. 정책 페이지에서 **안전한 첨부 파일** 을 선택 합니다.

4. 안전한 첨부 파일 페이지에서 **SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 설정** 확인란을 선택 하 여이 보호를 광범위 하 게 적용 합니다.

5. **+** 새 정책을 만들려면 선택 합니다.

6. 다음 표의 설정을 적용 합니다.

7. 설정을 검토 한 후에는 **이 정책 만들기** 또는 적절 한 **저장** 을 선택 합니다.

|설정 또는 옵션|권장 설정|
|---|---|
|이름|검색 된 맬웨어로부터 현재 및 향후 전자 메일을 차단 합니다.|
|설명|검색 된 맬웨어로부터 현재 및 향후 전자 메일 및 첨부 파일을 차단 합니다.|
|첨부 파일 저장 알 수 없는 맬웨어 응답|차단 됨을 선택 하 고 **검색 된 맬웨어로부터 현재 및 앞으로의 전자 메일 및 첨부 파일을 차단** 합니다.|
|검색 시 첨부 파일 리디렉션|리디렉션 사용 (이 상자 선택) <br/> 격리를 위해 관리자 계정 또는 사서함 설정을 입력 합니다. <br/> 첨부 파일에 대 한 맬웨어 검사 시간이 초과 되거나 오류가 발생 하면 (이 상자를 선택 하십시오.) 위의 선택 사항을 적용 합니다.|
|적용 대상|받는 사람 도메인은입니다. . . 도메인을 선택 합니다.|
|

자세한 내용은 [Defender for 피싱 정책에서 Office 365를](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-atp-anti-phishing-policies)참조 하세요.

## <a name="10-protect-against-phishing-attacks-with-safe-links"></a>10: 안전한 링크로 피싱 공격 으로부터 보호
<a name="phishingatp"> </a>

해커는 전자 메일 이나 다른 파일의 링크에서 악성 웹 사이트를 숨기는 경우가 있습니다. Microsoft Defender for Office 365에 포함 된 안전한 링크는 전자 메일 메시지 및 Office 문서에서 웹 주소 (Url)를 클릭 하 여 확인 하는 시간을 제공 하 여 조직을 보호 하는 데 도움이 될 수 있습니다. 보호는 안전한 링크 정책을 통해 정의 됩니다.

다음을 수행 하는 것이 좋습니다.

- 기본 정책을 수정 하 여 보호를 강화 합니다.

- 도메인의 모든 받는 사람을 대상으로 하는 새 정책을 추가 합니다.

안전한 링크를 보려면 [간단한 교육 비디오](https://support.microsoft.com/office/61492713-53c2-47da-a6e7-fa97479e97fa)를 보거나 다음 단계를 완료 하세요.

1. 으로 이동 하 <https://protection.office.com> 고 관리자 계정으로 로그인 합니다.

2. 보안 & 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리** 에서 **정책을** 선택 합니다.

3. 정책 페이지에서 **안전한 링크** 를 선택 합니다.

기본 정책을 수정 하려면 다음을 수행 합니다.

1. 안전한 링크 페이지의 **전체 조직에 적용 되는 정책** 에서 **기본** 정책을 두 번 클릭 합니다.

2. **Office 365에서 콘텐츠에 적용 되는 설정** 아래에서 차단 될 URL (예: _example.com_ )을 입력 하 고을 선택 **+** 합니다.

3. **전자 메일을 제외 하 고 콘텐츠에 적용 되는 설정** 에서 **Office 365 응용 프로그램** 을 선택 하 고, **사용자가 안전한 링크를 클릭 하면 추적 안 함** , 사용자가 안전한 링크를 사용 하 여 **원본 URL로 클릭 하도록 허용 하지** 않음

4. **저장** 을 선택합니다.

도메인의 모든 받는 사람을 대상으로 하는 새 정책을 만들려면 다음을 수행 합니다.

1. 안전한 링크 페이지의 **특정 받는 사람에 게 적용 되는 정책** 에서 **+** 새 정책을 만들도록 선택 합니다.

2. 다음 표에 나와 있는 설정을 적용 합니다.

3. **저장** 을 선택합니다.

|설정 또는 옵션|권장 설정|
|---|---|
|이름|도메인의 모든 받는 사람에 대 한 안전한 링크 정책|
|메시지에서 알 수 없는 잠재적 악성 Url에 대 한 작업 선택|**Url 선택-사용자가 링크를 클릭할 때 알려진 악성 링크 목록에 대해 다시 작성 및 확인** 합니다.|
|의심 스러운 링크에 대 한 실시간 URL 검사 및 파일을 가리키는 링크를 적용 합니다.|이 상자를 선택 합니다.|
|적용 대상|받는 사람 도메인은입니다. . . 도메인을 선택 합니다.|
|

자세한 내용은 [Office 용 Microsoft Defender 365의 안전한 링크](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links)를 참조 하세요.
