---
title: 독립 실행형 EOP 서비스 설정
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
ms.custom:
- seo-marvel-apr2020
localization_priority: Normal
ms.assetid: d74c6ddf-11b0-43ee-b298-8bb0340895f0
description: 관리자는 온-프레미스 전자 메일 환경을 보호 하기 위해 독립 실행형 EOP (Exchange Online Protection)를 설정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 53386b700c2a2832cf16d47da0678dfb91c5b6d7
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48197170"
---
# <a name="set-up-your-standalone-eop-service"></a>독립 실행형 EOP 서비스 설정

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


이 항목에서는 독립 실행형 EOP (Exchange Online Protection)를 설정 하는 방법에 대해 설명 합니다. Office 365 도메인 마법사에서 여기로 이동했으며 Exchange Online Protection를 사용하지 않으려면 Office 365 도메인 마법사로 돌아갑니다. 커넥터 구성 방법에 대한 자세한 내용를 보려면 [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow)을 참조하세요.

> [!NOTE]
> 이 항목에서는 온-프레미스 사서함이 있고 EOP을 사용 하 여이를 보호 하려고 한다고 가정 합니다 (독립 실행형 시나리오 라고 함). Exchange Online을 사용 하 여 클라우드의 모든 사서함을 호스팅하려면이 항목의 모든 단계를 완료 하지 않아도 됩니다. [Exchange Online 계획 비교](https://products.office.com/exchange/compare-microsoft-exchange-online-plans) 로 이동 하 여 클라우드 사서함에 등록 하 고 구입 합니다. 온-프레미스의 일부 사서함과 클라우드에서 일부를 호스트 하려는 경우이를 하이브리드 시나리오 라고 합니다. 이를 위해서는 보다 고급 메일 흐름 설정이 필요 합니다. [Exchange Server 하이브리드 배포](https://docs.microsoft.com/exchange/exchange-hybrid) 에서는 하이브리드 메일 흐름에 대해 설명 하 고이를 설정 하는 방법을 보여 주는 리소스에 대 한 링크를 제공 합니다.

## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 이 작업의 예상 완료 시간: 1시간

- 이 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 특히, 기본적으로 MailFlowAdministrator 및 OrganizationManagement (전역 관리자) 역할 그룹에 할당 되는 원격 및 허용 도메인 역할이 필요 합니다. 자세한 내용은 [권한 독립 실행형 EOP의 사용 권한을](feature-permissions-in-eop.md) 참조 하 고 [EAC를 사용 하 여 역할 그룹의 구성원 목록을 수정](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)합니다.

- 아직 EOP에 등록하지 않은 경우 [Exchange Online Protection](https://products.office.com/exchange/exchange-email-security-spam-protection)을 방문하여 서비스를 구입하거나 평가판을 신청합니다.

- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.

> [!TIP]
> 문제가 있나요? [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 포럼에서 도움을 요청하세요.

## <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>1 단계: Microsoft 365 관리 센터를 사용 하 여 도메인 추가 및 확인

1. [Microsoft 365 관리 센터](https://docs.microsoft.com/microsoft-365/admin/admin-overview/about-the-admin-center)에서 **설정** 으로 이동 하 여 서비스에 도메인을 추가 합니다.

2. 도메인 소유권 확인을 위해 해당 DNS 레코드를 DNS 호스팅 공급자에 추가하는 단계를 수행합니다.

> [!TIP]
> [Office 365에 도메인 추가](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) 및 [office 365에 대 한 dns 호스팅 공급자에서 dns 레코드 만들기](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) 는 서비스에 도메인을 추가 하 고 DNS를 구성할 때 참조 해야 하는 유용한 리소스입니다.

## <a name="step-2-add-recipients-and-optionally-enable-dbeb"></a>2단계: 받는 사람을 추가하고 선택적으로 DBEB 사용

메일이 EOP 서비스를 통해 전달되도록 구성하려는 경우 먼저 받는 사람을 서비스에 추가하는 것이 좋습니다. [EOP에서 메일 사용자 관리](manage-mail-users-in-eop.md)에 설명된 것처럼 이러한 방법에는 몇 가지가 있습니다. 또한 받는 사람을 추가한 후에 서비스 내에서 받는 사람 확인을 적용하기 위해 DBEB(디렉터리 기반 Edge 차단)를 사용 가능하게 설정하려면 도메인 유형을 신뢰할 수 있음으로 설정해야 합니다. DBEB에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking)를 참조하세요.

## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>3단계: EAC를 사용하여 메일 흐름 설정

EOP 및 온-프레미스 메일 서버 간의 메일 흐름을 가능하게 하는 커넥터를 EAC(Exchange 관리 센터)에서 만듭니다. 자세한 내용은 [Set up connector to mail to a Microsoft 365와 자체 전자 메일 서버 간에 메일 라우팅를](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail)참조 하세요.

### <a name="how-do-you-know-this-task-worked"></a>이 작업의 작동 여부는 어떻게 확인하나요?

서비스와 환경 간의 메일 흐름을 확인 합니다. 자세한 내용은 [Microsoft 365 커넥터를 확인 하 여 메일 흐름 테스트](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow)를 참조 하세요.

## <a name="step-4-allow-inbound-port-25-smtp-access"></a>4단계: 인바운드 포트 25 SMTP 액세스 허용

커넥터를 구성한 후에는 DNS 레코드 업데이트의 전파를 허용 하는 데 72 시간을 기다립니다. 그런 후에 EOP 데이터 센터(구체적으로는 [Exchange Online Protection IP 주소](https://docs.microsoft.com/microsoft-365/enterprise/urls-and-ip-address-ranges)에 나와 있는 IP 주소)에서 보내는 메일만 수락하도록 방화벽이나 메일 서버의 인바운드 포트 25 SMTP 트래픽을 제한합니다. 이렇게 하면 수신 가능한 인바운드 메시지 범위를 제한하여 온-프레미스 환경을 보호할 수 있습니다. 또한 메일 릴레이를 위한 연결이 허용된 IP 주소를 제어하는 설정이 메일 서버에 있는 경우에는 해당 설정도 업데이트합니다.

> [!TIP]
> 연결 제한 시간을 60초로 지정하여 SMTP 서버의 설정을 구성합니다. 이 설정은 대부분의 상황에서 가능 하며 큰 첨부 파일을 사용 하 여 메시지를 보낼 때 약간의 지연을 허용 하는 등의 작업이 가능 합니다.

## <a name="step-5-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>5 단계: 스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록 확인

스팸(정크) 메일이 각 사용자의 정크 메일 폴더로 라우팅되도록 하려면 몇 가지 구성 단계를 수행해야 합니다. [하이브리드 환경의 정크 메일 폴더에 스팸을 배달 하도록 독립 실행형 EOP 구성](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)에 단계가 제공 됩니다.

각 사용자의 정크 메일 폴더로 메시지를 이동 하지 않으려면 스팸 방지 정책을 편집 하 여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [Office 365의 스팸 방지 정책 구성하기](configure-your-spam-filter-policies.md)를 참조하세요.

## <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>6 단계: Microsoft 365 관리 센터를 사용 하 여 MX 레코드가 EOP를 가리키도록 지정

도메인 구성 단계에 따라 도메인에 대 한 MX 레코드를 업데이트 하 여 인바운드 전자 메일이 EOP를 통해 흐를 수 있도록 합니다. 타사 필터링 서비스가 전자 메일을 EOP로 릴레이할 때와 달리 MX 레코드가 EOP를 직접 가리키도록 해야 합니다. 자세한 내용은 [Office 365용 DNS 레코드 만들기](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider)를 참조하세요.

> [!NOTE]
> MX 레코드가 EOP 앞에 있는 다른 서버 또는 서비스를 가리켜야 하는 경우 [Exchange Online의 커넥터에 대 한 향상 된 필터링](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors)을 참조 하십시오.

### <a name="how-do-you-know-this-task-worked"></a>이 작업의 작동 여부는 어떻게 확인하나요?

이 시점은 제대로 구성된 아웃바운드 온-프레미스 커넥터에 대한 서비스 배달을 확인했으며 MX 레코드가 EOP를 가리키고 있는지 확인한 상태입니다. 이제 다음 추가 테스트를 실행하도록 선택하여 서비스에서 온-프레미스 환경으로 이메일이 전달되는지 확인할 수 있습니다.

- 서비스와 환경 간의 메일 흐름을 확인 합니다. 자세한 내용은 [Microsoft 365 커넥터를 확인 하 여 메일 흐름 테스트](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow)를 참조 하세요.

- 도메인이 서비스에 추가한 도메인과 일치하는 조직의 메일 받는 사람에게 웹 기반 전자 메일 계정에서 전자 메일 메시지를 보냅니다. Microsoft Outlook 또는 다른 전자 메일 클라이언트를 사용하여 온-프레미스 사서함으로의 메시지 배달을 확인합니다.

- 아웃바운드 전자 메일 테스트를 실행하려면 조직 사용자가 웹 기반 전자 메일 계정에 전자 메일을 보내도록 한 다음 메시지 수신을 확인하면 됩니다.

> [!TIP]
> 설정이 완료된 후 EOP에서 스팸 및 맬웨어를 제거하도록 추가 단계를 수행할 필요는 없습니다. EOP는 스팸과 맬웨어를 자동으로 제거합니다. 그러나 비즈니스 요구 사항에 따라 설정을 미세 조정할 수는 있습니다. 자세한 내용은 [Office 365의 스팸 방지 및 맬웨어 방지 보호](anti-spam-and-anti-malware-protection.md) 기능을 참조 하 고 [스푸핑 인텔리전스를 구성](learn-about-spoof-intelligence.md)합니다. <br/><br/> 이제 서비스가 실행 중 이므로 EOP을 설정한 후의 권장 설정 및 고려 사항을 설명 하는 [EOP 구성을 위한 모범 사례](best-practices-for-configuring-eop.md)를 읽는 것이 좋습니다.
