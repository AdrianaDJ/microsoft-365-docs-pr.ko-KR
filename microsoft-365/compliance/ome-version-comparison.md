---
title: OME (메시지 암호화) 버전 비교
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: 이 문서는 서로 다른 버전의 Office 365 메시지 암호화 간의 차이점에 대해 설명 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: a52d0c0164dfddb9f678bffa088760a271bc28e3
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754132"
---
# <a name="compare-versions-of-ome"></a>OME 버전 비교

이 문서에서는 레거시 Office 365 메시지 암호화 (OME)와 새 OME 기능 및 Office 365 고급 메시지 암호화를 비교 합니다. 새로운 기능은 OME 및 IRM (정보 권한 관리) 모두의 합병 및 최신 버전입니다. GCC 높음으로 배포할 때의 고유한 특징에 대해서도 설명 합니다. 두 사용자가 조직에 공존할 수 있습니다. 새 기능을 사용 하는 방법에 대 한 자세한 내용은 [Office 365 메시지 암호화 (OME)](ome.md)를 참조 하십시오.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 ITPros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>기능 및 기능의 병렬 비교

|                                   |이전 기능       |                   |새로운 기능              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**기능**                     | **레거시 OME**    | **IRM**           | **새로운 OME 기능** |
|*암호화 된 메일 보내기*        |Exchange 메일 흐름 규칙을 통해|최종 사용자가 Outlook 데스크톱 또는 웹용 Outlook에서 시작 됩니다. 또는 Exchange 메일 흐름 규칙을 통해|최종 사용자가 Outlook 데스크톱, Mac 용 Outlook 또는 웹용 Outlook에서 시작 되었습니다. Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함) 및 DLP (데이터 손실 방지)를 통해|
|*권한 관리 템플릿*       |   해당 없음      |전달 금지 옵션 및 사용자 지정 서식 파일|전달 금지 옵션, Encrypt-Only 옵션 및 사용자 지정 템플릿|
|*받는 사람 유형*                   |내부 및 외부 받는 사람|내부 받는 사람만         |내부 및 외부 받는 사람|
|*내부 받는 사람에 대 한 경험*|받는 사람은 웹 브라우저나 모바일 앱에서 다운로드 하 고 여는 HTML 메시지를 받습니다.|Outlook 클라이언트의 기본 인라인 환경|Outlook 클라이언트를 사용 하는 같은 조직의 받는 사람에 대 한 기본 인라인 환경  받는 사람은 Outlook 이외의 클라이언트 (다운로드 또는 앱이 필요 하지 않은 경우)를 사용 하 여 OME 포털에서 메시지를 읽을 수 있습니다.|
|*외부 받는 사람에 대 한 경험*|받는 사람은 웹 브라우저나 모바일 앱에서 다운로드 하 고 여는 HTML 메시지를 받습니다.|해당 없음|Microsoft 365 받는 사람에 대 한 기본 인라인 환경 다른 모든 받는 사람은 OME 포털에서 메시지를 읽을 수 있습니다 (다운로드 또는 앱이 필요 하지 않음).|
|*첨부 파일 사용 권한*           |첨부 파일에 대 한 제한 없음|첨부 파일이 보호 됨|첨부 파일은 전달 하지 않음 옵션 및 사용자 지정 서식 파일에 대해 보호 됩니다. 관리자는 Encrypt-Only 옵션의 첨부 파일을 보호할 지 여부를 선택할 수 있습니다.|
|*사용자 키 (BYOK) 지원*|없음                |없음               |BYOK 지원 됨          |
||

## <a name="advantages-of-the-new-ome-capabilities-over-legacy-ome"></a>레거시 OME에 비해 새로운 OME 기능을 사용할 경우의 이점

새로운 기능은 다음과 같은 이점을 제공 합니다.

- Encrypt-Only (보안 공동 작업 가능)을 사용 하 고, 전달 하지 않고, 사용자 지정 제한을 사용할 수 있습니다.
- 보낸 사람은 새 기능으로 암호화 된 메일을 Outlook 데스크톱, Outlook for Mac 및 웹용 Outlook 클라이언트에서 수동으로 보낼 수 있습니다.
- Microsoft 365 받는 사람은 지원 되는 Outlook 클라이언트에서 인라인 환경을 사용할 수 있습니다. 또는 관리자가 Microsoft 365 받는 사람에 게 브랜드 환경을 표시 하도록 선택할 수 있습니다.
- Gmail, Yahoo, Microsoft 계정과 같은 Microsoft 365 외부의 계정은 이러한 받는 사람에 게 더 나은 사용자 환경을 제공 하는 OME 포털에 페더레이션 됩니다. 다른 모든 id는 암호화 된 메시지에 액세스 하기 위해 1 회 통과 코드를 사용 합니다.
- 관리자는 브랜딩을 사용자 지정 하 고 여러 브랜딩 서식 파일을 만들 수 있습니다.
- 관리자는 새 기능을 사용 하 여 암호화 된 전자 메일을 해지할 수 있습니다.
- 새 기능은 보안 및 준수 센터를 통해 자세한 사용 현황 보고서를 제공 &amp; 합니다.

## <a name="office-365-advanced-message-encryption-capabilities"></a>Office 365 고급 메시지 암호화 기능

Office 365 Advanced Message Encryption은 새로운 OME 기능에 대 한 추가 기능을 제공 합니다. 고급 메시지 암호화 기능을 사용 하려면 조직에 새로운 Office 365 메시지 암호화 기능이 설정 되어 있어야 합니다. 또한 이러한 기능을 사용 하기 위해 받는 사람은 OME 포털을 통해 보안 메일을 보고 회신 해야 합니다. 고급 기능은 다음과 같습니다.

- 메시지 해지

- 메시지 만료

- 여러 브랜딩 서식 파일

Office 365 고급 메시지 암호화는 GCC (높은)에서 지원 되지 않습니다.

고급 메시지 암호화를 사용 하는 방법에 대 한 자세한 내용은 [Office 365 고급 메시지 암호화](ome-advanced-message-encryption.md)를 참조 하세요.

## <a name="unique-characteristics-of-office-365-message-encryption-in-a-gcc-high-deployment"></a>GCC High 배포의 Office 365 메시지 암호화에 대 한 고유한 특성

GCC High 환경에서 Office 365 메시지 암호화를 사용 하려는 경우에는 받는 사람 환경에 대 한 몇 가지 고유한 특성이 있습니다.

### <a name="encrypted-email-between-gcc-high-and-gcc-high-recipients"></a>GCC High 및 GCC High 받는 사람 사이에 암호화 된 전자 메일

보낸 사람은 Outlook for PC 및 Mac 및 웹용 Outlook에서 전자 메일을 수동으로 암호화할 수 있으며, 조직에서 Exchange 메일 흐름 규칙을 사용 하 여 전자 메일을 암호화 하는 정책을 설정할 수 있습니다.

GCC High 내부의 받는 사람은 다른 모든 사용자와 PC 및 Mac 용 Outlook 및 웹용 Outlook에서 동일한 인라인 읽기 환경을 수신 합니다.

### <a name="encrypted-email-between-gcc-high-and-non-gcc-high-recipients"></a>GCC 고가용성 및 비 GCC 높은 받는 사람 간의 암호화 된 전자 메일

GCC High 내부의 보낸 사람은 GCC 높은 경계 외부에서 암호화 된 전자 메일을 보낼 수 있고 그 반대의 경우도 마찬가지입니다.

상업용 Microsoft 365 사용자, Outlook.com 사용자 및 다른 전자 메일 공급자 (예: Gmail 및 Yahoo)의 기타 사용자를 포함 하 여 GCC를 제외한 모든 받는 사람은 래퍼 메일을 받습니다. 이 래퍼 메일은 받는 사람이 메시지를 읽고 회신할 수 있는 OME 포털로 수신자를 리디렉션합니다. 이는 GCC High 전송 OME 암호화 된 메일의 보낸 사람을 GCC 높음으로 설정 하는 경우에도 마찬가지입니다.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>같은 테 넌 트의 기존 OME 및 새 기능 동시 사용

같은 테 넌 트에서 레거시 OME 및 새 기능을 모두 사용할 수 있습니다. 관리자는 메일 흐름 규칙을 만들 때 사용할 OME 버전을 선택 하 여이 작업을 수행 합니다.

- OME의 레거시 버전을 지정 하려면 Exchange 메일 흐름 규칙 작업을 사용 하 여 **이전 버전의 OME를 적용**합니다.

- 새 기능을 지정 하려면 Exchange 메일 흐름 규칙 작업을 사용 하 여 **Office 365 메시지 암호화 및 권한 보호를 적용**합니다.

사용자는 Outlook 데스크톱, Mac 용 Outlook 및 웹용 Outlook에서 새로운 기능을 사용 하 여 암호화 된 메일을 수동으로 보낼 수 있습니다.

## <a name="migrate-from-legacy-ome-to-the-new-capabilities"></a>레거시 OME에서 새로운 기능으로 마이그레이션

OME의 두 버전을 함께 사용할 수 있는 경우에도 규칙 작업을 사용 하는 이전 메일 흐름 규칙을 편집 하는 것이 새로운 기능을 사용 하기 위해 **이전 버전의 OME를 적용** 하는 것이 좋습니다. 메일 흐름 규칙 동작을 사용 하도록 이러한 규칙 업데이트 **Office 365 메시지 암호화 및 권한 보호를 적용**합니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 참조 하세요.

## <a name="get-started-with-ome"></a>OME 시작

일반적으로 새 OME 기능은 조직에서 자동으로 사용 하도록 설정 됩니다. 조직 내의 새로운 OME 기능에 대 한 자세한 내용은 [Set Up Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md)를 참조 하십시오.

Azure Information Protection을 사용 하도록 설정한 경우 OME의 레거시 버전은 조직에서 자동으로 사용 하도록 설정 됩니다. 이전에는 Azure Information Protection을 사용 하도록 설정 하지 않은 경우에도 레거시 OME 작동 했습니다. 더 이상 이러한 경우는 아닙니다.

레거시 OME 사용을 시작 하려면 Azure Information Protection을 사용할 수 있는 경우 규칙 작업을 사용 하는 메일 흐름 규칙을 구성 하 여 **이전 버전의 OME를 적용**합니다. 자세한 내용은 [전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 참조 하십시오.
