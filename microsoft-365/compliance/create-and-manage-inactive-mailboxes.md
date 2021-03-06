---
title: 비활성 사서함 만들기 및 관리
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
ms.custom:
- seo-marvel-apr2020
description: Office 365의 비활성 사서함 기능을 사용 하 여 삭제 된 사서함의 콘텐츠를 유지 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 286c1b363f7ceae42d7eaef13635ccf037bb4b21
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45127545"
---
# <a name="create-and-manage-inactive-mailboxes"></a>비활성 사서함 만들기 및 관리

Microsoft 365을 사용 하면 삭제 된 사서함의 콘텐츠를 보존할 수 있습니다. 이 기능을 [비활성 사서함](inactive-mailboxes-in-office-365.md)이라고 합니다. 비활성 사서함을 사용 하면 조직에서 나간 후에 이전 직원의 전자 메일을 보존할 수 있습니다. 해당 사용자 계정이 삭제 되기 전에 Office 365 또는 Microsoft 365의 보안 및 준수 센터에서 만든 소송 보존 또는 보관 정책이 사서함에 적용 되는 경우 사서함이 비활성화 됩니다. 비활성 사서함의 콘텐츠는 비활성 상태로 설정 되기 전에 사서함에 적용 된 보류 기간 동안 보존 됩니다. 이렇게 하면 관리자, 준수 책임자 및 레코드 관리자가 콘텐츠 검색을 사용 하 여 비활성 사서함의 콘텐츠를 검색 하 고 내보낼 수 있습니다. 비활성 사서함은 전자 메일을 받을 수 없으며 조직의 공유 주소록 또는 기타 목록에 표시되지 않습니다.
  
> [!IMPORTANT]
> 계속 해 서 사서함 콘텐츠를 보존 하는 다양 한 방법을 사용할 때 Exchange 관리 센터에서 원본 위치 유지의 만료를 알리는 것입니다. 즉, 소송 보유 및 보존 정책을 사용 하 여 비활성 사서함을 만들어야 합니다. 2020 년 7 월 1 일부 터 시작 Exchange Online에 새로운 현재 위치 유지를 만들 수 없습니다. 그러나 비활성 사서함에 저장 된 원본 위치 유지의 보존 기간은 여전히 변경할 수 있습니다. 그러나 2020 년 10 월 1 일부 터 시작 하는 경우에는 보존 기간을 변경할 수 없습니다. 원본 위치 유지를 제거 해야만 비활성 사서함을 삭제할 수 있습니다. 원본 위치 유지 상태인 기존 비활성 사서함은 보존을 제거할 때까지 계속 유지 됩니다. 원본 위치 유지의 만료에 대 한 자세한 내용은 [레거시 eDiscovery 도구의 만료](legacy-ediscovery-retirement.md)를 참조 하세요.
  
## <a name="preparations-before-creating-an-inactive-mailbox"></a>비활성 사서함을 만들기 전 준비

- 사서함을 비활성화 하려면이를 삭제 하기 전에 사서함에 적용할 수 있도록 Exchange Online 계획 2 라이선스를 할당 받아야 합니다. Exchange Online 계획 2 라이선스는 Office 365 Enterprise E3 및 E5 구독의 일부입니다. 사서함에 Office 365 E1 및 F1 구독에 각각 포함 된 Exchange Online 계획 1 또는 Exchange Online Kiosk 라이선스가 할당 되 면 사서함을 삭제 하기 전에 해당 보존을 적용할 수 있도록 별도의 Exchange Online 보관 라이선스를 할당 해야 합니다. 자세한 내용은 [Exchange Online 아카이빙](https://go.microsoft.com/fwlink/p/?LinkId=286153)를 참조 하세요.

- 삭제 된 Exchange Online 사서함과 연결 된 라이선스는 해당 사용자 계정을 삭제 한 후에 사용할 수 있습니다. 그런 다음 [해당 라이선스를 다른 사용자에 게 할당할](../admin/manage/assign-licenses-to-users.md)수 있습니다.

- 소송 보존 또는 콘텐츠를 보존 하 고 유지 하 고 삭제 하도록 구성 된 보관 정책이 삭제 되기 전에 사서함에 적용 되지 않은 경우에는 사서함의 내용이 보존 되거나 검색 되지 않습니다. 그러나 삭제 된 사서함은 삭제 후 30 일 이내에 복구할 수 있지만 사서함과 해당 콘텐츠는 복구 되지 않은 경우 30 일 후 영구적으로 삭제 됩니다.

- 소송 보존에 대 한 자세한 내용은 원본 [위치 유지 및 소송 보존](https://go.microsoft.com/fwlink/p/?LinkId=846124)을 참조 하세요. 보존 정책에 대 한 자세한 내용은 [보존 정책 및 보존 레이블에 대 한](retention.md)자세한 정보를 참조 하십시오.
  
## <a name="create-an-inactive-mailbox"></a>비활성 사서함 만들기

사서함을 비활성화 하려면 다음 두 단계를 수행 합니다. 1) 사서함을 소송 보존으로 설정 또는 보관 정책을 적용 하 고 2) 사서함 또는 해당 사용자 계정을 삭제 합니다. 사서함이 비활성 상태가 되 면 보류 또는 보존 정책이 제거 될 때까지 해당 내용이 보존 됩니다.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-a-retention-policy"></a>1 단계: 사서함을 소송 보존으로 설정 또는 보관 정책 적용

사서함을 소송 보존으로 설정 하거나, 콘텐츠를 보존 하거나 보존 하 고 삭제할 수 있도록 구성 된 보관 정책을 적용 하는 경우 삭제 되기 전에 사서함의 내용이 보존 됩니다. 두 가지 유형의 보존은 모두 삭제 된 항목을 비롯 한 모든 사서함 콘텐츠를 유지 합니다. 삭제 및 수정한 항목은 지정 된 기간 동안 비활성 사서함에 보존 되거나 비활성 사서함에 적용 되는 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제할 때까지 유지 됩니다.
  
사서함에 보류가 이미 적용 되어 있거나 보존 정책이 사서함에 이미 있는 경우에는 2 단계에 설명 된 대로 해당 사용자 계정을 삭제 하면 됩니다.
  
사서함을 소송 보존으로 설정 하는 단계별 절차에 대 한 자세한 내용은 다음을 참조 하십시오.
  
- [사서함을 소송 자료 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Office 365의 보존 정책 및 보존 레이블에 대 한 자세한 정보](retention.md)
    
> [!NOTE]
> 소송 보유 및 보존 정책에 대해 무기한 보류 또는 시간 기반 유지를 만들 수 있습니다. 무기한 유지에서는 비활성 사서함의 내용이 영구적으로 보존 되거나 보류가 제거 되거나 보존 기간이 변경 될 때까지 유지 됩니다. 보류 또는 보존 정책이 제거 된 후 (사서함이 30 일을 초과 하 여 삭제 된 것으로 가정) 비활성 사서함이 영구적으로 삭제 되도록 표시 되 고 사서함의 내용이 더 이상 보존 되거나 검색 가능 하지 않게 됩니다. 시간 기반 보류 또는 보존 정책에서는 보류의 기간을 지정 합니다. 이 기간은 항목별로 지정되며 사서함 항목을 받거나 만든 날짜로부터 계산됩니다. 사서함 항목에 대 한 보류가 만료 되 고 해당 항목이 비활성 사서함의 복구할 수 있는 항목 폴더에 이동 된 후에는 삭제 된 항목 보존 기간이 만료 되 면 비활성 사서함에서 항목이 영구적으로 삭제 (제거) 됩니다. 
  
### <a name="step-2-delete-the-mailbox"></a>2단계: 사서함 삭제

사서함이 보류 되거나 보존 정책이 적용 된 후 다음 단계는 사서함을 삭제 하는 것입니다. 사서함을 삭제 하는 가장 좋은 방법은 Microsoft 365 관리 센터에서 해당 사용자 계정을 삭제 하는 것입니다. 사용자 계정을 삭제 하는 방법에 대 한 자세한 내용은 [조직에서 사용자 삭제](https://docs.microsoft.com/microsoft-365/admin/add-users/delete-a-user)를 참조 하십시오.
  
> [!NOTE]
> Exchange Online PowerShell에서 **사서함 제거** cmdlet을 사용 하 여 사서함을 삭제할 수도 있습니다. 자세한 내용은 [Exchange Online에서 사용자 사서함 삭제 또는 복원을](https://go.microsoft.com/fwlink/?linkid=856287)참조 하세요. 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>비활성 사서함 목록 보기

조직의 비활성 사서함 목록을 보려면 다음을 수행 합니다.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동한 후 조직의 관리자 계정 자격 증명을 사용하여 로그인합니다. 
    
2. **정보 거 버 넌 스**  >  **보존**을 클릭 합니다.
    
3. **보존** 페이지에서 **기타** ![ 탐색 모음 줄임표를 클릭 한 ](../media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) 다음 **비활성 사서함**을 클릭 합니다.
    
    ![보존 페이지에서 자세히를 클릭 하 고 비활성 사서함을 클릭 하 여 비활성 사서함 목록을 표시 합니다.](../media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    **비활성 사서함** 페이지가 표시 됩니다. 참고 조직에 있는 비활성 사서함의 총 수가 표시 됩니다. 
    
    ![조직의 모든 비활성 사서함 목록이 표시 됩니다.](../media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
또는 Exchange Online PowerShell에서 다음 명령을 실행 하 여 비활성 사서함 목록을 표시할 수도 있습니다.

```powershell
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

![검색 결과 내보내기 아이콘 ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **내보내기를** 클릭 하 여 조직의 비활성 사서함에 대 한 추가 정보가 포함 된 CSV 파일을 보거나 다운로드할 수 있습니다. 
  
다음 명령을 실행 하 여 비활성 사서함 목록과 기타 정보를 CSV 파일로 내보낼 수도 있습니다. 이 예제에서는 CSV 파일이 현재 디렉터리에 만들어집니다.

```powershell
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```

> [!NOTE]
> 비활성 사서함의 SMTP 주소가 활성 사용자 사서함과 같을 수 있습니다. 이 경우에는 **DistinguishedName** 또는 **ExchangeGuid** 속성 값을 사용 하 여 비활성 사서함을 고유 하 게 식별할 수 있습니다. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>비활성 사서함의 콘텐츠 검색 및 내보내기

보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 비활성 사서함의 콘텐츠에 액세스할 수 있습니다. 비활성 사서함을 검색할 때는 키워드 검색 쿼리를 만들어 특정 항목을 검색하거나 비활성 사서함의 전체 콘텐츠를 반환할 수 있습니다. 검색 결과를 미리 보거나, Outlook 데이터 (PST) 파일 또는 개별 전자 메일 메시지로 검색 결과를 내보낼 수 있습니다. 사서함을 검색 하 고 검색 결과를 내보내는 방법에 대 한 단계별 절차는 다음 항목을 참조 하십시오.
  
- [Office 365의 콘텐츠 검색](content-search.md)
    
- [콘텐츠 검색 결과 내보내기](export-search-results.md)
    
다음은 비활성 사서함을 검색할 때 유의해야 하는 몇 가지 사항입니다.
  
- 콘텐츠 검색에 사용자 사서함이 포함 되어 있고 해당 사서함이 비활성 상태가 되 면 검색을 다시 실행할 때 비활성 사서함을 계속 검색 합니다.
    
- 일부 경우에는 사용자에 게 활성 사서함과 SMTP 주소가 같은 비활성 사서함이 있을 수 있습니다. 이 경우에는 콘텐츠 검색 위치로 선택한 특정 사서함만 검색 됩니다. 즉, 사용자의 사서함을 검색에 추가 하는 경우에는 활성 및 비활성 사서함이 모두 검색 된다고 가정할 수 없습니다. 검색에 명시적으로 추가 하는 사서함만 검색 됩니다.
    
- 동일한 SMTP 주소를 사용하는 활성 사서함과 비활성 사서함은 없는 것이 좋습니다. 비활성 사서함에 현재 할당 되어 있는 SMTP 주소를 다시 사용 해야 하는 경우 비활성 사서함을 복구 하거나 비활성 사서함의 내용을 활성 사서함 (또는 활성 사서함의 보관 함)으로 복원한 다음 비활성 사서함을 삭제 하는 것이 좋습니다.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>비활성 사서함의 보존 기간 변경

사서함이 비활성 상태가 되 면 비활성 사서함에 적용 되는 보존 정책 또는 보류의 기간을 변경할 수 있습니다. 단계별 절차에 대 한 자세한 내용은 [Office 365에서 비활성 사서함에 대 한 보존 기간 변경을](change-the-hold-duration-for-an-inactive-mailbox.md)참조 하십시오.
  
## <a name="recover-an-inactive-mailbox"></a>비활성 사서함 복구

이전 직원이 조직에 반환 되는 경우 또는 이거나 퇴직 한 직원의 직무에 따라 새 직원을 고용 하는 경우 비활성 사서함의 내용을 복구할 수 있습니다. 비활성 사서함을 복구 하는 경우 사서함 새 사서함으로 변환 됩니다 내용과 비활성 사서함의 폴더 구조 유지 되므로 및 사서함을 새 사용자 계정에 연결 됩니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 비활성 사서함을 복구할 때 발생 하는 작업에 대 한 단계별 절차와 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>비활성 사서함의 내용을 다른 사서함으로 복원

다른 직원이 이전 직원의 작업을 수행 하거나 다른 사용자가 비활성 사서함의 콘텐츠에 액세스 해야 하는 경우 비활성 사서함의 내용을 기존 사서함으로 복원 하거나 병합할 수 있습니다. 비활성 사서함을 복원 하는 경우에 내용은 다른 사서함에 복사 됩니다. 비활성 사서함은 유지 하 고 비활성 사서함을 유지 됩니다. EDiscovery를 사용 하 여 비활성 사서함을 검색할 수는 있지만, 해당 콘텐츠를 다른 사서함으로 복원 하거나 나중에 복구 하거나 삭제할 수 있습니다. 단계별 절차에 대 한 자세한 내용은 [Office 365에서 비활성 사서함 복원을](restore-an-inactive-mailbox.md)참조 하십시오.
  
## <a name="delete-an-inactive-mailbox"></a>비활성 사서함 삭제

비활성 사서함의 콘텐츠를 더 이상 보존할 필요가 없는 경우 보존을 제거 하거나 비활성 사서함에 적용 된 보관 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 있습니다. 사서함이 30 일 보다 오래 삭제 된 경우 보존을 제거한 후 사서함이 영구적으로 삭제 되도록 표시 되 고 사서함이 복구할 수 없게 됩니다. 지난 30 일 이내에 사서함을 삭제 한 경우에도 보류 또는 보존 정책을 제거한 후에 사서함을 복구할 수 있습니다. 보류 나 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제 하는 방법에 대 한 단계별 절차는 [delete a 비활성 사서함](delete-an-inactive-mailbox.md)을 참조 하십시오.
