---
title: TeleMessage 엔터프라이즈 번호 Winrar에서 데이터를 보관 하는 커넥터 설정
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 TeleMessage Enterprise 번호 Winrar에서 SMS 및 MMS 데이터를 가져오고 보관 하도록 커넥터를 설정할 수 있습니다. 이를 통해 Microsoft 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리할 수도 있습니다.
ms.openlocfilehash: 7609d61f70a49da4015cfc68b185fb10be0266c8
ms.sourcegitcommit: ae3aa7f29be16d08950cf23cad489bc069aa8617
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48408798"
---
# <a name="set-up-a-connector-to-archive-enterprise-number-data"></a>Enterprise 번호 데이터를 보관 하는 커넥터 설정

Microsoft 365 준수 센터의 TeleMessage 커넥터를 사용 하 여 엔터프라이즈 번호 Winrar에서 SMS (Short Messaging Service) 및 MMS (멀티미디어 메시징 서비스) 메시지, 채팅 메시지, 음성 통화 기록 및 음성 통화 로그를 가져오고 보관 합니다. 커넥터를 설정 하 고 구성한 후에는 매일 한 번씩 조직의 TeleMessage 계정에 연결 하 고 TeleMessage Enterprise 번호 Winrar를 사용 하 여 직원의 모바일 통신 데이터를 Microsoft 365의 사서함으로 가져옵니다.

TeleMessage 엔터프라이즈 번호 Winrar 커넥터 데이터가 사용자 사서함에 저장 되 면 소송 보존, 콘텐츠 검색, In-Place 보관, 감사, 통신 준수 및 Microsoft 365 보존 정책 등의 Microsoft 365 준수 기능을 Enterprise Number Winrar data에 적용할 수 있습니다. 예를 들어 TeleMessage Enterprise 번호 Winrar는 콘텐츠 검색을 사용 하 여 SMS, MMS 및 음성 통화를 검색 하거나, 엔터프라이즈 번호 Winrar 커넥터 데이터를 포함 하는 사서함을 Advanced eDiscovery 사례의 custodian과 연결할 수 있습니다. 엔터프라이즈 번호 Winrar 커넥터를 사용 하 여 Microsoft 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.

## <a name="overview-of-archiving-enterprise-number-data"></a>Enterprise 번호 데이터 보관 개요

다음 개요에서는 커넥터를 사용 하 여 Microsoft 365에서 엔터프라이즈 네트워크 데이터를 보관 하는 프로세스에 대해 설명 합니다.

![Enterprise 번호 보관 워크플로](../media/EnterpriseNumberConnectorWorkflow.png)

1. 조직에서 TeleMessage를 사용 하 여 엔터프라이즈 번호 Winrar 커넥터를 설정 합니다. 자세한 내용은 [여기](https://www.telemessage.com/office365-activation-for-enterprise-number-archiver/)를 참조 하세요.

2. Microsoft 365 준수 센터에서 만드는 엔터프라이즈 번호 Winrar 커넥터는 매일 TeleMessage 사이트에 연결 하 고 이전 24 시간에서 Microsoft 클라우드의 안전한 Azure Storage 영역으로 전자 메일 메시지를 전송 합니다.

3. 커넥터는 모바일 통신 항목을 특정 사용자의 사서함으로 가져옵니다. 엔터프라이즈 번호 Winrar 라는 새 폴더가 특정 사용자의 사서함에 만들어지고이 폴더에 항목을 가져오게 됩니다. 커넥터는 *사용자의 전자 메일 주소* 속성 값을 사용 하 여 매핑합니다. 모든 전자 메일 메시지에는 전자 메일 메시지의 모든 참석자의 전자 메일 주소로 채워지는이 속성이 포함 되어 있습니다. *사용자의 전자 메일 주소* 속성 값을 사용 하는 자동 사용자 매핑 외에도 CSV 매핑 파일을 업로드 하 여 사용자 지정 매핑을 정의할 수 있습니다. 이 매핑 파일에는 사용자의 휴대폰 번호와 각 사용자의 해당 Microsoft 365 사서함 주소가 포함 되어 있어야 합니다. 자동 사용자 매핑을 사용 하도록 설정 하 고 사용자 지정 매핑을 제공 하는 경우 커넥터는 모든 전자 메일 항목에 대해 사용자 지정 매핑 파일을 먼저 확인 합니다. 사용자 휴대폰 번호에 해당 하는 유효한 Microsoft 365 사용자가 없으면 커넥터는 전자 메일 항목의 사용자 전자 메일 주소 속성을 사용 합니다. 커넥터가 사용자 지정 매핑 파일 또는 전자 메일 항목의 *사용자 전자 메일 주소* 속성에서 유효한 Microsoft 365 사용자를 찾지 못하면 항목을 가져오지 않습니다.

## <a name="before-you-begin"></a>시작하기 전에

엔터프라이즈 번호 Winrar 데이터를 보관 하는 데 필요한 일부 구현 단계는 Microsoft 365 외부에 있으므로, 준수 센터에서 커넥터를 만들기 전에 완료 되어야 합니다.

- [TeleMessage에서 엔터프라이즈 번호 winrar 서비스](https://www.telemessage.com/mobile-archiver/order-mobile-archiver-for-o365) 를 주문 하 고 조직의 유효한 관리 계정을 가져옵니다. 준수 센터에서 커넥터를 만들 때이 계정에 로그인 해야 합니다.

- TeleMessage 계정에 엔터프라이즈 번호 SMS/MMS 네트워크 보관이 필요한 모든 사용자를 등록 합니다. 사용자를 등록할 때 Microsoft 365 계정에 사용 되는 것과 동일한 전자 메일 주소를 사용 해야 합니다.

- 직원의 휴대폰에 TeleMessage Enterprise 번호 Winrar 앱을 설치 하 고 정품 인증 합니다.

- 조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다. 커넥터를 만들 때이 동의를 제공 해야 합니다. 이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Microsoft 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다. 벨 네트워크 커넥터를 성공적으로 만들기 전에이 단계를 완료 해야 합니다.

- Enterprise 번호 Winrar 커넥터를 만드는 사용자에 게 Exchange Online에서 사서함 가져오기 내보내기 역할이 할당 되어야 합니다. 이는 Microsoft 365 준수 센터의 **데이터 커넥터** 페이지에서 커넥터를 추가 하는 데 필요 합니다. 기본적으로이 역할은 Exchange Online의 어떤 역할 그룹에도 할당되지 않습니다. Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.

## <a name="create-an-enterprise-number-archiver-connector"></a>엔터프라이즈 번호 Winrar 커넥터 만들기

이전 섹션에서 설명한 필수 구성 요소를 완료 한 후에는 Microsoft 365 준수 센터에서 엔터프라이즈 번호 Winrar connector를 만들 수 있습니다. 커넥터는 제공 하는 정보를 사용 하 여 TeleMessage 사이트에 연결 하 고 SMS, MMS 및 음성 통화 메시지를 Microsoft 365의 해당 사용자 사서함 상자로 전송 합니다.

1. 로 이동한 [https://compliance.microsoft.com](https://compliance.microsoft.com/) 후 **데이터 커넥터** \> **Enterprise 번호 winrar**를 클릭 합니다.

2. **Enterprise 번호 winrar** 제품 설명 페이지에서 **커넥터 추가** 를 클릭 합니다.

3. **서비스 약관** 페이지에서 **수락**을 클릭 합니다.

4. **TeleMessage 로그인** 페이지의 3 단계에서 다음 상자에 필요한 정보를 입력 하 고 **다음**을 클릭 합니다.

   - **사용자 이름:** 사용자의 TeleMessage 사용자 이름입니다.

   - **암호:** TeleMessage 암호

5. 커넥터를 만든 후에는 팝업 창을 닫고 다음 페이지로 이동할 수 있습니다.

6. **사용자 매핑** 페이지에서 자동 사용자 매핑을 사용 하도록 설정 합니다. 사용자 지정 매핑을 사용 하도록 설정 하려면 사용자 매핑 정보가 포함 된 CSV 파일을 업로드 하 고 **Next (다음**)를 클릭 합니다.

7. 관리자 동의를 제공 하 고 **Next (다음**)를 클릭 합니다.

   관리자의 동의를 제공 하려면 Office 365 전역 관리자의 자격 증명을 사용 하 여 로그인 한 다음 승인 요청을 수락 해야 합니다. 전역 관리자로 로그인 하지 않은 경우 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 이동 하 여 전역 관리자 자격 증명을 사용 하 여 로그인 하 고 요청을 수락할 수 있습니다.

8. 설정을 검토 하 고 **마침을** 클릭 하 여 커넥터를 만듭니다.

9. **데이터 커넥터** 페이지의 커넥터 탭으로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스 진행 상황을 확인 합니다.

## <a name="known-issues"></a>알려진 문제

- 현재로 서는 10mb 보다 큰 첨부 파일 또는 항목을 가져올 수 없습니다. 더 큰 항목에 대 한 지원은 나중에 제공 될 예정입니다.
