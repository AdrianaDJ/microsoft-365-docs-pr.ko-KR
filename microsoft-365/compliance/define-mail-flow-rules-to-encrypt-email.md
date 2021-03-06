---
title: 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365 메시지 암호화를 사용 하 여 메시지를 암호화 하 고 암호를 해독 하는 메일 흐름 규칙 (전송 규칙)을 만드는 방법을 알 수 있습니다.
ms.openlocfilehash: 28486f601a79e294550bbceb48ad57069024fd5a
ms.sourcegitcommit: ae3aa7f29be16d08950cf23cad489bc069aa8617
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48408608"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages"></a>전자 메일 메시지를 암호화 하는 메일 흐름 규칙 정의

전역 관리자는 보내는 전자 메일 메시지를 보호 하는 데 도움이 되는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. 규칙을 설정 하 여 보내는 전자 메일 메시지를 암호화 하 고 조직 내부에서 전송 되는 암호화 된 메시지에서 또는 조직이 보낸 암호화 된 메시지에 대 한 암호화를 제거할 수 있습니다. EAC (Exchange 관리 센터) 또는 Exchange Online PowerShell을 사용 하 여 이러한 규칙을 만들 수 있습니다. 전체 암호화 규칙 외에도 최종 사용자에 대한 개별 메시지 암호화 옵션을 사용할지 여부를 선택할 수도 있습니다.

조직 외부의 보낸 사람 으로부터 인바운드 메일을 암호화할 수는 없습니다.

최근에 Active Directory RMS에서 Azure Information Protection으로 마이그레이션한 경우 기존 메일 흐름 규칙을 검토 하 여 새 환경에서 계속 작동 하는지 확인 해야 합니다. 또한 Azure Information Protection을 통해 새 Office 365 메시지 암호화 (OME) 기능을 활용 하려는 경우 기존 메일 흐름 규칙을 업데이트 해야 합니다. 그렇지 않으면 사용자는 새로운 OME 환경이 아닌 이전 HTML 첨부 파일 형식을 사용 하는 암호화 된 메일을 계속 받게 됩니다. 아직 OME을 설정 하지 않은 경우 정보를 보려면 [새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md) 참조 하십시오.

메일 흐름 규칙을 만드는 구성 요소와 메일 흐름 규칙의 작동 방식에 대 한 자세한 내용은 [메일 흐름 규칙 (전송 규칙)에서 Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)을 참조 하십시오. 메일 흐름 규칙이 Azure Information Protection과 함께 작동 하는 방식에 대 한 자세한 내용은 [Azure Information protection 레이블에 대 한 Exchange Online 메일 흐름 규칙 구성을](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules)참조 하세요.

> [!IMPORTANT]
> 하이브리드 Exchange 환경에서는 온-프레미스 사용자가 전자 메일을 Exchange Online을 통해 라우팅되는 경우에만 OME를 사용 하 여 암호화 된 메일을 보내고 받을 수 있습니다. 하이브리드 Exchange 환경에서 OME을 구성 하려면 먼저 [하이브리드 구성 마법사를 사용 하 여 하이브리드를 구성한](https://docs.microsoft.com/Exchange/exchange-hybrid) 다음 [office 365에서 전자 메일 서버로 이동](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-1-configure-mail-to-flow-from-office-365-to-your-on-premises-email-server) 하 고 [전자 메일 서버에서 office 365로](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)메일을 전송 하도록 메일을 구성 해야 합니다. Office 365를 통해 메일이 전송 되도록 구성한 후에는이 지침을 사용 하 여 OME에 대 한 메일 흐름 규칙을 구성할 수 있습니다.

## <a name="create-mail-flow-rules-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 메일 흐름 규칙 만들기

EAC를 사용 하 여 새 OME 기능으로 메시지 암호화를 트리거하는 메일 흐름 규칙을 정의할 수 있습니다.

### <a name="use-the-eac-to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능을 사용 하 여 전자 메일 메시지를 암호화 하는 규칙 만들기

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC에서 **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 **New** 아이콘을 선택 하 여 ![ ](../media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙을 만듭니다**. EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.

5. **이름**에 DrToniRamos@hotmail.com에 대 한 메일 암호화와 같은 규칙의 이름을 입력 합니다.

6. 다음의 **경우이 규칙 적용**에서 조건을 선택 하 고 필요한 경우 값을 입력 합니다. 예를 들어 DrToniRamos@hotmail.com에 보내는 메시지를 암호화하려면 다음을 수행합니다.

   1. **다음의 경우 이 규칙 적용**에서 **받는 사람이 다음과 같음**을 선택합니다.

   2. 연락처 목록에서 기존 이름을 선택하거나 **이름 확인** 상자에 새 전자 메일 주소를 입력합니다.

      - 기존 이름을 선택하려면 목록에서 이름을 선택한 다음 **확인**을 클릭합니다.

      - 새 이름을 입력 하려면 **이름 확인** 상자에 전자 메일 주소를 입력 하 고 **이름** 확인 \> **을**선택 합니다.

7. 조건을 더 추가 하려면 **기타 옵션** 을 선택한 다음 **조건 추가** 를 선택 하 고 목록에서를 선택 합니다.

   예를 들어 받는 사람이 조직 외부에 있는 경우에만이 규칙을 적용 하려면 **조건 추가** 를 선택한 다음 받는 사람이 조직 외부에 있는 **외부/내부에** \> **Outside the organization** \> **OK**있습니다 .를 선택 합니다.

8. 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장**을 선택한 다음 **확인**을 선택 합니다.
  
  서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다. 목록이 비어 있으면 [새 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 Office 365 메시지 암호화를 새로운 기능으로 설정 했는지 확인 합니다. 기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.

  다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.

### <a name="use-the-eac-to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능을 사용 하도록 기존 메일 흐름 규칙 업데이트

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.

5. 메일 흐름 규칙 목록에서 새 OME 기능을 사용 하도록 수정할 규칙을 선택 하 고 편집 아이콘 **편집** 을 선택 ![ ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) 합니다.

6. 새 OME 기능을 사용 하 여 암호화를 사용 하도록 설정 하려면 **다음 작업을 수행**하 고 **메시지 보안 수정을** 선택한 다음 **Office 365 메시지 암호화 및 권한 보호 적용**을 선택 합니다. 목록에서 RMS 템플릿을 선택 하 고 **저장** 을 선택한 다음 **확인**을 선택 합니다.

   서식 파일 목록에는 모든 기본 서식 파일 및 옵션 뿐 아니라 Office 365에서 사용 하기 위해 만든 사용자 지정 서식 파일도 포함 됩니다. 목록이 비어 있으면 Office 365 메시지 암호화가 [Azure Information Protection의 새로운 office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)에 설명 된 대로 새로운 기능을 사용 하 여 설정 했는지 확인 합니다. 기본 서식 파일에 대 한 자세한 내용은 [Azure Information Protection의 템플릿 구성 및 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지** 않음 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 전달 옵션 안 함](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **암호화 전용** 옵션에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.

   다른 작업을 지정 하려는 경우 **작업 추가** 를 선택할 수 있습니다.

7. 다음 작업 **수행** 목록에서 **메시지 보안을 수정** 하도록 할당 된 모든 작업을 제거 하 \> **여 이전 버전의 OME을 적용**합니다.

8. **저장**을 선택합니다.

## <a name="create-mail-flow-rules-to-remove-encryption-for-outgoing-email-messages-with-the-new-ome-capabilities"></a>새 OME 기능을 사용 하 여 보내는 전자 메일 메시지에 대 한 암호화를 제거 하는 메일 흐름 규칙 만들기

EAC를 사용 하 여 새 OME 기능으로 제거 메시지 암호화를 트리거하는 메일 흐름 규칙을 정의할 수 있습니다.

### <a name="use-the-eac-to-create-a-rule-to-remove-encryption-from-email-messages-with-the-new-ome-capabilities"></a>EAC를 사용 하 여 새 OME 기능을 사용 하 여 전자 메일 메시지에서 암호화를 제거 하는 규칙 만들기

1. 웹 브라우저에서 전역 관리자 권한이 부여 된 회사 또는 학교 계정을 사용 하 여 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)합니다.

2. **관리** 타일을 선택 합니다.

3. Microsoft 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택 합니다.

4. EAC에서 **메일 흐름** \> **규칙** 으로 이동 하 고 새로 만들기 **New** 아이콘을 선택 하 여 ![ ](../media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙을 만듭니다**. EAC를 사용 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하세요.

5. **이름**에 규칙의 이름을 입력 합니다 (예: 보내는 메일에서 암호화 제거).

6. **다음의 경우이 규칙 적용**에서 암호화를 메시지에서 제거할 조건을 선택 합니다. 조직 내부에 **있는 보낸 사람** \> **Inside the organization**추가 이제 **받는** 사람이 \> **조직 외부**에 있는 것과 같은 특정 받는 사람을 대상으로 하는 조건을 더 추가 합니다.

7. **다음 작업을 수행**합니다 .에서 **메시지 보안 수정** \> **Office 365 메시지 암호화 및 권한 보호 제거**를 선택 합니다.

8. **저장**을 선택합니다.

## <a name="create-mail-flow-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>새 기능 없이 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 만들기

아직 조직을 새 OME 기능으로 이동 하지 않은 경우에는 조직에 적합 한 즉시 새 OME 기능으로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능 설치](set-up-new-message-encryption-capabilities.md)를 참조 하세요. 그렇지 않은 경우 [새 OME 기능을 사용 하지 않는 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 정의](legacy-information-for-message-encryption.md#defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities)를 참조 하세요.

## <a name="related-topics"></a>관련 항목

[Office 365의 암호화](encryption.md)

[새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)

[암호화된 메시지에 브랜딩 추가](add-your-organization-brand-to-encrypted-messages.md)

[Exchange Online의 메일 흐름 규칙 (전송 규칙)](https://go.microsoft.com/fwlink/p/?LinkId=506707)

[Exchange Online Protection의 메일 흐름 규칙(전송 규칙)](https://go.microsoft.com/fwlink/p/?LinkId=506708)
