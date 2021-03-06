---
title: 고객 Lockbox 요청
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
search.appverid:
- BCS160
- MET150
- MOE150
description: 문제가 발생 하는 경우 Microsoft 지원 엔지니어가 데이터에 액세스 하는 방법을 제어할 수 있도록 하는 고객 Lockbox 요청에 대해 알아봅니다.
ms.openlocfilehash: b475c9af80d0e28961360825788d9e19a426dc69
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48768866"
---
# <a name="customer-lockbox-in-office-365"></a>Office 365의 고객 Lockbox

이 문서에서는 고객 Lockbox에 대 한 배포 및 구성 지침을 제공 합니다. 고객 Lockbox는 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive의 데이터에 액세스 하기 위한 요청을 지원 합니다. 다른 서비스에 대 한 지원을 권장 하려면 [Office 365 UserVoice](https://office365.uservoice.com/)에서 요청을 제출 하십시오.

사용자에 게 라이선스를 부여 하는 데 사용할 수 있는 옵션을 보려면이 항목을 포함 하 여 Microsoft 365 준수 서비스를 제공 하는 경우 (2020), [보안 & 준수에 대 한 microsoft 365 라이선스 지침](https://aka.ms/ComplianceSD)을 참조 하세요.

고객 Lockbox는 명시적인 승인 없이 서비스 작업을 수행 하기 위해 Microsoft가 콘텐츠에 액세스할 수 없도록 합니다. 고객 Lockbox는 콘텐츠에 액세스 하기 위한 요청에 대 한 승인 워크플로를 사용자에 게 제공 합니다.

경우에 따라 Microsoft 엔지니어가 지원 프로세스에서 고객이 보고 한 문제를 해결 하 고 문제를 해결 하는 데 도움이 됩니다. 일반적으로 문제는 Microsoft가 서비스를 위해 마련 된 광범위 한 원격 분석 및 디버깅 도구를 통해 수정 됩니다. 그러나 근본적인 원인을 확인 하 고 문제를 해결 하기 위해 고객 콘텐츠에 액세스 하기 위해 Microsoft 엔지니어가 필요한 경우도 있습니다. 고객 Lockbox에 게는 승인 워크플로의 최종 단계로 고객의 액세스를 요청 하는 엔지니어가 필요 합니다. 조직에서는 이러한 요청을 승인 하거나 거부할 수 있는 옵션을 제공 하 고 고객에 게 직접 액세스 제어 기능을 제공 합니다.

### <a name="customer-lockbox-overview-video"></a>고객 Lockbox 개요 비디오

> [!VIDEO https://www.microsoft.com/videoplayer/embed/8fecf10b-1f03-4849-8b67-76d3d2a43f26?autoplay=false]

## <a name="customer-lockbox-workflow"></a>고객 Lockbox 워크플로

다음 단계에서는 Microsoft 엔지니어가 고객 Lockbox 요청을 시작할 때의 일반적인 워크플로를 간략하게 설명 합니다.

1. 조직의 누군가가 Microsoft 365 사서함에 문제가 발생 합니다.

2. 사용자가 문제를 해결 했지만 수정할 수 없는 경우 Microsoft 지원 서비스를 통해 지원 요청을 엽니다.

3. Microsoft 지원 엔지니어가 서비스 요청을 검토 하 고 Exchange Online에서 문제를 해결 하기 위해 조직의 테 넌 트에 액세스 해야 하는지 확인 합니다.

4. Microsoft 지원 엔지니어가 고객 Lockbox 요청 도구에 로그인 하 고 조직의 테 넌 트 이름, 서비스 요청 번호 및 엔지니어가 데이터에 액세스 하는 데 필요한 예상 시간을 포함 하는 데이터 액세스 요청을 수행 합니다.

5. Microsoft 지원 관리자가 요청을 승인 하면 고객 Lockbox가 조직의 지정 된 승인자에 게 Microsoft의 보류 중인 액세스 요청에 대 한 전자 메일 알림을 보냅니다.

    ![고객 Lockbox 전자 메일 알림의 예](../media/CustomerLockbox1.png)

   Microsoft 365 관리 센터에서 [고객 lockbox 액세스 승인자](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 관리자 역할이 할당 된 모든 사용자는 고객 lockbox 요청을 승인할 수 있습니다.

6. 승인자가 Microsoft 365 관리 센터에 로그인 하 고 요청을 승인 합니다. 이 단계에서는 감사 로그를 검색 하 여 사용할 수 있는 감사 레코드 만들기를 트리거합니다. 자세한 내용은 [고객 Lockbox 요청 감사](#auditing-customer-lockbox-requests)를 참조 하세요.

   고객이 요청을 거부 하거나 12 시간 내에 요청을 승인 하지 않으면 요청이 만료 되 고 Microsoft 엔지니어에 게 액세스 권한이 부여 되지 않습니다.

   > [!IMPORTANT]
   > Microsoft는 Office 365에 로그인 해야 하는 고객 Lockbox 전자 메일 알림의 링크를 포함 하지 않습니다.

7. 조직의 승인자가 요청을 승인한 후에는 Microsoft 엔지니어가 승인 메시지를 수신 하 여 Exchange Online의 테 넌 트에 로그인 하 고 고객의 문제를 해결 합니다. Microsoft 엔지니어가 문제를 해결 하기 위해 요청 된 기간이 지나면 액세스 권한이 자동으로 해지 됩니다.

> [!NOTE]
> Microsoft 엔지니어가 수행한 모든 작업이 감사 로그에 기록 됩니다. 이러한 감사 레코드를 검색 하 고 검토할 수 있습니다.

## <a name="turn-customer-lockbox-requests-on-or-off"></a>고객 Lockbox 요청 설정 또는 해제

Microsoft 365 관리 센터에서 고객 Lockbox 컨트롤을 사용 하도록 설정할 수 있습니다. 고객 Lockbox를 켜면 Microsoft에서 테 넌 트의 콘텐츠를 액세스 하기 전에 조직의 승인을 받아야 합니다.

1. 전역 관리자 또는 **사용자 Lockbox 액세스 승인자** 역할이 할당 된 회사 또는 학교 계정을 사용 하 여로 이동 하 여 [https://admin.microsoft.com](https://admin.microsoft.com) 로그인 합니다.

2. **설정 > 조직 설정을** 선택 합니다.

3. **보안 & 개인 정보**  >  **고객 Lockbox**  >  **편집** 을 선택한 다음 토글을 설정 또는 **On** **해제** 로 이동 하 여 해당 기능을 설정 하거나 해제 합니다.

    ![Require approval for Customer Lockbox](../media/CustomerLockbox4.png)

## <a name="approve-or-deny-a-customer-lockbox-request"></a>고객 Lockbox 요청 승인 또는 거부

1. 전역 관리자 또는 **사용자 Lockbox 액세스 승인자** 역할이 할당 된 회사 또는 학교 계정을 사용 하 여로 이동 하 여 [https://admin.microsoft.com](https://admin.microsoft.com) 로그인 합니다.

2. **고객 Lockbox 요청 > 지원을** 선택 합니다.

    ![지원을 클릭 하 고 고객 Lockbox 요청을 클릭 합니다.](../media/CustomerLockbox5.png)

    고객 Lockbox 요청 목록이 표시 됩니다.

    ![고객 Lockbox 요청 목록](../media/CustomerLockbox6.png)

3. 고객 Lockbox 요청을 선택한 다음 **승인** 또는 **거부** 를 선택 합니다.

    ![고객 Lockbox 요청 승인 또는 거부](../media/CustomerLockbox7.png)

    고객 Lockbox 요청의 승인에 대 한 확인 메시지가 표시 됩니다.

    ![고객 Lockbox 요청 승인 또는 거부](../media/CustomerLockbox8.png)

> [!NOTE]
> Set-AccessToCustomerDataRequest cmdlet을 사용하여 Microsoft 지원 엔지니어의 사용자 데이터에 대한 액세스를 제어하는 Microsoft 365 고객 lockbox를 승인, 거부 또는 취소합니다. 자세한 내용은 [AccessToCustomerDataRequest](https://docs.microsoft.com/powershell/module/exchange/set-accesstocustomerdatarequest)를 참조 하십시오.


## <a name="auditing-customer-lockbox-requests"></a>고객 Lockbox 요청 감사

고객 Lockbox 요청에 해당 하는 감사 레코드가 감사 로그에 기록 됩니다. 보안 & 준수 센터에서 [감사 로그 검색 도구](search-the-audit-log-in-security-and-compliance.md) 를 사용 하 여 이러한 로그에 액세스할 수 있습니다. 고객 Lockbox 요청 수락 또는 거부와 관련 된 작업 및 Microsoft 엔지니어가 수행한 작업 (액세스 요청이 승인 된 경우)이 감사 로그에도 기록 됩니다. 이러한 감사 레코드를 검색 하 고 검토할 수 있습니다.

### <a name="search-the-audit-log-for-activity-related-to-customer-lockbox-requests"></a>고객 Lockbox 요청과 관련 된 작업에 대 한 감사 로그 검색

감사 로그를 사용 하 여 고객 Lockbox에 대 한 요청을 추적할 수 있으므로, 감사 로깅을 설정 하기 위해 몇 가지 단계를 수행 해야 합니다. 자세한 내용은 [Security & 준수 센터에서 감사 로그 검색](https://docs.microsoft.com/office365/securitycompliance/search-the-audit-log-in-security-and-compliance#before-you-begin)을 참조 하십시오. 설치를 완료 한 후 다음 단계를 사용 하 여 고객 Lockbox와 관련 된 감사 레코드를 반환 하는 감사 로그 검색 쿼리를 만듭니다.

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
  
2. 회사 또는 학교 계정을 사용하여 로그인합니다.

3. 보안 & 준수 센터의 왼쪽 창에서 **검색 & 조사**  >  **감사 로그 검색** 을 선택 합니다.

    **감사 로그 검색** 페이지가 표시 됩니다.

    ![감사 로그 검색 페이지](../media/auditlogsearch1.png)
  
4. 다음과 같은 검색 조건을 구성합니다. 

    1. **활동** -검색에서 모든 활동에 대 한 감사 레코드를 반환 하도록이 필드를 비워 둡니다. 이는 고객 Lockbox 요청과 관련 된 감사 레코드와 Microsoft 엔지니어가 수행한 해당 작업을 반환 하는 데 필요 합니다.

    1. **시작 날짜** 및 **종료 날짜** -해당 기간 내에 발생 한 이벤트를 표시 하려면 날짜 및 시간 범위를 선택 합니다.

    1. **사용자** -이 필드를 비워 둡니다.

    1. **파일, 폴더 또는 사이트** -이 필드를 비워 둡니다.

5. **검색** 을 클릭하여 검색 조건을 사용한 검색을 실행합니다. 

    검색 결과가 로드 되 고 몇 분 후에 **감사 로그 검색** 페이지의 **결과** 아래에 표시 됩니다.

6. 검색 결과 페이지에서 **결과 필터링** 을 클릭 하 고 다음 작업 중 하나를 수행 합니다.

   - 조직의 승인자와 관련 된 감사 레코드를 표시 하려면 다음을 수행 합니다. **활동** 열 아래의 상자에 **AccessToCustomerDataRequest** 을 입력 합니다.

   - 승인 된 고객 Lockbox 요청에 대 한 응답으로 Microsoft 엔지니어의 작업을 수행 하는 데 관련 된 감사 레코드를 표시 하려면 **사용자** 열 아래의 상자에 **microsoft Operator** 를 입력 합니다. **활동** 열에는 엔지니어가 수행한 작업이 표시 됩니다.

      ![감사 레코드를 표시 하는 "Microsoft 운영자"에 대 한 필터링](../media/CustomerLockbox10.png)

7. 결과 목록에서 감사 레코드를 클릭 하 여 표시 합니다.

### <a name="audit-record-for-a-customer-lockbox-access-request"></a>고객 Lockbox 액세스 요청에 대 한 감사 레코드

조직의 사용자가 고객 Lockbox 요청을 승인 하거나 거부 하는 경우 감사 레코드가 감사 로그에 기록 됩니다. 이 레코드에는 다음 정보가 포함 됩니다.

| Audit record 속성| 설명|
|:---------- |:----------|
| 날짜       | 고객 인증 키 저장소 요청이 승인 또는 거부 된 날짜 및 시간입니다.
| IP 주소 | 승인자가 요청을 승인 하거나 거부 하는 데 사용 하는 컴퓨터의 IP 주소입니다. |
| 사용자       | 서비스 계정 BOXServiceAccount@ \[ \] customerforest.            |
| 활동   | AccessToCustomerDataRequest; 이는 고객 Lockbox 요청을 승인 하거나 거부할 때 기록 되는 감사 작업입니다.                                |
| 항목       | 고객 Lockbox 요청의 Guid입니다.                             |

다음 스크린샷은 승인 된 고객 Lockbox 요청에 해당 하는 감사 로그 레코드의 예를 보여 줍니다. 고객 Lockbox 요청이 거부 된 경우 **Approvaldecision 결정** 매개 변수의 값은 **Deny** 가 됩니다.

![승인 된 고객 Lockbox 요청에 대 한 감사 레코드](../media/CustomerLockbox9.png)

> [!TIP]
> 감사 레코드에 자세한 정보를 표시 하려면 **추가 정보** 를 클릭 합니다.

### <a name="audit-record-for-an-action-performed-by-a-microsoft-engineer"></a>Microsoft 엔지니어가 수행한 작업에 대 한 감사 레코드

고객 Lockbox 요청이 승인 되 고 고객 콘텐츠에 액세스할 수 있도록 하는 Microsoft 엔지니어가 수행한 작업이 감사 로그에 기록 됩니다. 이러한 레코드에는 다음과 같은 정보가 포함 됩니다.

| Audit record 속성| 설명|
|:---------- |:----------|
| 날짜       | 작업을 수행한 날짜 시간입니다. 이 작업을 수행한 시간은 고객 Lockbox 요청이 승인 된 경우 4 시간 이내입니다.              |
| IP 주소 | Microsoft 엔지니어가 사용 하는 컴퓨터의 IP 주소입니다. |
| 사용자       | Microsoft Operator; 이 값은이 레코드가 고객 Lockbox 요청과 관련 되어 있음을 나타냅니다.                                  |
| 활동   | Microsoft 엔지니어가 수행한 활동의 이름입니다.|
| 항목       | \<empty\>                                             |

## <a name="frequently-asked-questions"></a>질문과 대답

#### <a name="which-microsoft-365-services-does-customer-lockbox-apply-to"></a>고객 Lockbox가 적용 되는 Microsoft 365 서비스는 무엇입니까?

고객 Lockbox는 현재 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive에서 지원 됩니다.

#### <a name="is-customer-lockbox-available-to-all-customers"></a>고객 Lockbox가 모든 고객에 게 제공 됩니까?

고객 Lockbox는 Microsoft 365 또는 Office 365 E5 구독에 포함 되어 있으며, 정보 보호 및 규정 준수 또는 고급 준수 추가 기능 구독을 사용 하 여 다른 계획에 추가할 수 있습니다. 자세한 내용은 [요금제 및 가격 책정](https://products.office.com/business/office-365-enterprise-e5-business-software) 를 참조 하세요.

#### <a name="what-is-customer-content"></a>고객 콘텐츠 란?

고객 콘텐츠는 Microsoft 365 서비스 및 응용 프로그램 사용자가 만든 데이터입니다. 고객 콘텐츠의 예는 다음과 같습니다.

- 전자 메일 본문 또는 전자 메일 첨부 파일

- SharePoint 사이트 콘텐츠

- SharePoint 파일의 본문에 있는 정보

- 비즈니스용 Skype 프레젠테이션 파일 본문

- IM (인스턴트 메시지) 또는 음성 채팅

- 고객 생성 blob 또는 구조적 저장소 데이터 (예: SQL 컨테이너)

- 고객 소유 보안 정보 (예: 인증서, 암호화 키 및 암호)

- Inferences 및 모든 후속 Inferences (고객 콘텐츠가 유지 되는 경우)

Office 365의 고객 콘텐츠에 대 한 자세한 내용은 [office 365 보안 센터](https://products.office.com/business/office-365-trust-center-privacy/)를 참조 하세요.

#### <a name="who-is-notified-when-there-is-a-request-to-access-my-content"></a>콘텐츠에 액세스 하는 요청이 있을 때 사용자에 게 알림을 받는 사람은 누구 인가요?

전역 관리자 및 고객 Lockbox 액세스 승인자 관리자 역할에 할당 된 모든 사용자에 게 알림을 보냅니다. 또한 이러한 사용자는 고객 Lockbox 요청에 대해 승인할 수 있는 것과 동일 합니다.

#### <a name="who-can-approve-or-reject-these-requests-in-my-organization"></a>조직에서 이러한 요청을 승인 하거나 거부할 수 있는 사람은 누구 입니까?

전역 관리자 및 고객 Lockbox 액세스 승인자 관리자 역할이 할당 된 모든 사용자는 고객 Lockbox 요청을 승인할 수 있습니다. 고객은 조직에서 이러한 역할 할당을 제어 합니다.

#### <a name="how-do-i-opt-in-to-customer-lockbox"></a>고객 Lockbox에 옵트인 하려면 어떻게 해야 하나요?

전역 관리자는 Microsoft 365 또는 Microsoft 365 관리 센터에서 고객 Lockbox를 사용 하도록 설정 하 고 구성할 수 있습니다.

#### <a name="if-i-approve-a-customer-lockbox-request-what-can-the-engineer-do-and-how-will-i-know-what-the-microsoft-engineer-did"></a>고객 Lockbox 요청을 승인 하는 경우 엔지니어가 수행할 수 있는 작업과 Microsoft 엔지니어가 수행한 작업을 확인 하는 방법

고객 Lockbox 요청을 승인 하면 Microsoft 엔지니어가 사용자에 게 사전 승인 된 cmdlet을 사용 하 여 고객 콘텐츠에 액세스 하는 데 필요한 권한이 부여 됩니다. 고객 Lockbox 요청에 대 한 응답으로 Microsoft 엔지니어가 수행한 작업이 기록 되 고 보안 & 준수 센터의 감사 로그에 액세스할 수 있습니다.

#### <a name="how-do-i-know-that-microsoft-follows-the-approval-process"></a>Microsoft가 승인 프로세스를 팔 로우 하는지 어떻게 알 수 있나요?

조직의 관리자 및 승인자에 게 전송 되는 전자 메일 승인 알림을 Microsoft 365 관리 센터에서 고객 Lockbox 요청 기록을 사용 하 여 상호 참조할 수 있습니다.

고객 Lockbox는 최신 [SOC 1 SSAE 16 감사 보고서](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports)에 포함 되어 있습니다. 자세한 내용을 보려면 [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=91592749-e86a-43ac-801e-121382614681&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_SOC%20%2F%20SSAE%2016%20Reports)에서 최신 보고서를 찾을 수 있습니다.

#### <a name="can-microsoft-modify-the-list-of-approvers-for-my-tenant-if-not-how-is-it-prevented"></a>Microsoft에서 테 넌 트에 대 한 승인자 목록을 수정할 수 있나요? 그렇지 않은 경우에는 어떻게 차단 됩니까?

조직의 전역 관리자만 고객 Lockbox 요청을 승인할 수 있는 사람을 지정할 수 있습니다. 즉, Azure Active Directory의 전역 관리자 그룹 구성원만 요청을 승인할 수 있는 사람을 지정할 수 있습니다. Azure Active Directory의 전역 관리자 그룹 구성원 자격은 조직에 의해서만 관리 됩니다.

#### <a name="what-if-i-need-more-information-about-a-content-access-request-to-approve-it"></a>콘텐츠 액세스 요청에 대 한 자세한 정보를 승인 하려면 어떻게 해야 하나요?

각 고객 Lockbox 요청에는 Microsoft 365 서비스 요청 번호가 포함 되어 있습니다. Microsoft 지원에 문의 하 여이 서비스 번호를 참조 하 여 요청에 대 한 자세한 정보를 확인할 수 있습니다.

#### <a name="when-a-customer-lockbox-request-is-approved-how-long-are-the-permissions-valid"></a>고객 Lockbox 요청이 승인 되 면 사용 권한이 유효한 기간이 얼마나 걸립니까?

현재 Microsoft 엔지니어에 게 부여 되는 액세스 권한의 최대 기간은 4 시간입니다. Microsoft 엔지니어가 더 짧은 기간을 요청할 수도 있습니다.

#### <a name="how-can-i-get-a-history-of-all-customer-lockbox-requests"></a>모든 고객 Lockbox 요청의 기록을 어떻게 얻을 수 있나요?

모든 고객 Lockbox 요청이 Microsoft 365 관리 센터에 표시 됩니다.

#### <a name="how-do-i-correlate-the-content-access-requests-with-the-related-audit-logs"></a>콘텐츠 액세스 요청과 관련 된 감사 로그를 상호 연관 시키는 방법은 무엇 인가요?

준수 센터 작업 피드에는 고객 Lockbox의 로그 작업이 포함 됩니다. 고객은 수신 된 전자 메일 요청에 대해 작업 피드에서 고객 Lockbox 로그 활동을 상호 참조할 수 있습니다.

#### <a name="what-happens-when-a-customer-doesnt-respond-to-a-customer-lockbox-request"></a>고객이 고객 Lockbox 요청에 응답 하지 않으면 어떻게 되나요?

고객 Lockbox 요청의 기본 기간은 12 시간입니다. 12 시간 내에 요청에 응답 하지 않으면 요청이 만료 됩니다.

#### <a name="what-does-microsoft-do-when-a-customer-rejects-a-customer-lockbox-request"></a>고객이 고객 Lockbox 요청을 거부 한 경우 Microsoft에서 수행 하는 작업은 무엇입니까?

고객이 고객 Lockbox 요청을 거부 하면 고객 콘텐츠에 대 한 액세스 권한이 발생 하지 않습니다. 조직의 사용자가 Microsoft에 문제를 해결 하기 위해 고객 콘텐츠에 액세스 하는 데 필요한 서비스 문제가 계속 발생 하면 서비스 문제가 지속 될 수 있으며 Microsoft는이에 대해 사용자에 게이를 알립니다.

#### <a name="does-customer-lockbox-protect-against-data-requests-from-law-enforcement-agencies-or-other-third-parties"></a>고객 Lockbox가 법률 집행 기관 또는 기타 타사 로부터의 데이터 요청을 보호 합니까?

아니요. Microsoft는 고객 데이터에 대 한 타사 요청을 심각 하 게 받아들입니다. 클라우드 서비스 공급자는 Microsoft는 항상 고객 데이터에 대 한 개인 정보를 대표 합니다. 소환장가 발생 하는 경우 Microsoft는 항상 제 3 자를 고객에 게 리디렉션하여 정보를 취득 하려고 시도 합니다. (Brad Smith의 블로그, 즉 [정부 스누핑에서 고객 데이터를 보호](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)합니다.) Microsoft가 받는 법 집행 요청에 대 한 [자세한 정보](https://www.microsoft.com/corporate-responsibility/lerr) 를 주기적으로 게시 합니다.

자세한 내용은 타사 데이터 요청과 관련 된 [Microsoft 보안 센터](https://www.microsoft.com/trustcenter/default.aspx) 및 [온라인 서비스 약관](https://www.microsoft.com/Licensing/product-licensing/products.aspx) 의 "고객 데이터 공개" 섹션을 참조 하세요.

#### <a name="how-does-microsoft-ensure-that-a-member-of-its-staff-doesnt-have-standing-access-to-customer-content-in-office-365-applications"></a>Microsoft는 직원 구성원이 Office 365 응용 프로그램의 고객 콘텐츠에 대 한 액세스 권한을 보유 하 고 있는지 어떻게 확인 하나요?

Microsoft는 액세스 제어 시스템을 통해 광범위 한 예방 조치를 구현 하며, 이러한 액세스 제어 시스템을 회피 하기 위한 시도를 식별 하 고 해결 하기 위한 조치를 예방용 인지 합니다. Microsoft 365는 최소 권한 및 just-in-time 액세스 원칙을 사용 하 여 작동 합니다. 따라서 Microsoft 직원에 게는 계속 해 서 고객 콘텐츠에 액세스할 수 있는 권한이 없습니다. 권한이 부여 된 경우에는 제한 된 기간 동안만 사용 해야 합니다. 

Microsoft 365에서는 *Lockbox* 라는 액세스 제어 시스템을 사용 하 여 서비스 내에서 작동 및 관리 기능을 수행할 수 있는 권한을 부여 하는 사용 권한에 대 한 요청을 처리 합니다. 운영자는 Lockbox를 사용 하 여 고객 콘텐츠에 대 한 액세스를 요청 해야 하며, 따라서 액세스 권한을 부여 하기 전에 두 번째 사용자가 요청에 대해 작업을 수행 해야 합니다 (예: 승인). 두 번째 사용자는 요청자가 될 수 없으며 고객 콘텐츠에 대 한 액세스를 승인 하도록 지정 해야 합니다. 요청이 승인 된 경우에만 운영자가 고객 콘텐츠에 대 한 임시 액세스 권한을 얻습니다. 권한 상승 기간이 만료 되 면 Lockbox가 액세스 권한을 취소 합니다.

Microsoft 일반 보안 관행에 대 한 자세한 내용은 [온라인 서비스 약관](https://www.microsoft.com/licensing/product-licensing/products) 을 참조 하세요.

#### <a name="under-what-circumstances-do-microsoft-engineers-need-access-to-my-content"></a>어떤 상황에서는 Microsoft 엔지니어가 내 콘텐츠에 액세스 해야 하나요?

Microsoft 엔지니어가 고객 콘텐츠에 액세스 해야 하는 가장 일반적인 시나리오는 고객이 문제 해결에 액세스 해야 하는 지원 요청을 만들 때입니다. Microsoft 365의 기본 원칙은 Microsoft가 고객 콘텐츠에 대 한 액세스 권한 없이 서비스가 작동 하는 것입니다. Microsoft에서 수행 하는 거의 모든 서비스 작업은 완전히 자동화 되 고 고객의 콘텐츠를 벗어나 추상화 되 고 고도로 통제 됩니다. Microsoft 365의 목표는 고객이 Microsoft access에 대 한 특정 요청을 승인할 때까지 해당 서비스를 지원 하기 위한 고객 콘텐츠에 대 한 액세스 권한이 필요 하지 않습니다.

#### <a name="i-already-thought-my-data-was-secure-with-the-microsoft-cloud-so-why-do-i-need-customer-lockbox"></a>Microsoft 클라우드를 사용 하 여 데이터가 안전 하다 고 생각 했을 때 고객 Lockbox가 필요한 이유는 무엇 인가요?

고객 Lockbox는 서비스 작업에 대 한 명시적 액세스 권한 부여를 제공 하는 기능을 고객에 게 제공 하 여 추가 제어 계층을 제공할 수 있습니다. 고객 Lockbox는 명시적인 데이터 액세스 권한 부여를 위한 절차를 제공 하 여 사용자가 HIPAA 및 FEDRAMP와 같은 특정 준수 의무를 충족 하도록 지원 합니다.
