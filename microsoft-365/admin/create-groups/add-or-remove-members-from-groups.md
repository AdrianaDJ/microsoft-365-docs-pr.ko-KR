---
title: Microsoft 365 그룹에서 구성원 추가 또는 제거
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- BSA160
ms.assetid: e186d224-a324-4afa-8300-0e4fc0c3000a
description: Microsoft 365 관리 센터에서 그룹에 구성원을 추가 하 고, 그룹에서 구성원을 제거 하 고, 그룹 소유자 상태를 관리 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: a8739b6cd2005598acbfccbaff6131235ec480ee
ms.sourcegitcommit: 3cdb670f10519f7af4015731e7910954ba9f70dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48753316"
---
# <a name="add-or-remove-members-from-microsoft-365-groups-using-the-admin-center"></a>관리 센터를 사용 하 여 Microsoft 365 그룹에서 구성원 추가 또는 제거

Microsoft 365에서 그룹 구성원은 일반적으로 고유한 그룹을 만들거나, 참가 하려는 그룹에 자신을 추가 하거나, 그룹 소유자의 초대를 받습니다. 그룹 소유권이 변경 되거나 구성원을 추가 또는 제거 해야 하는 경우에도 해당 변경 작업을 수행할 수 있습니다. 전역 관리자, Exchange 관리자, 그룹 관리자 또는 사용자 관리자만 이러한 변경 작업을 수행할 수 있습니다. [Microsoft 365 그룹 이란?](https://support.microsoft.com/office/b565caa1-5c40-40ef-9915-60fdb2d97fa2)

> [!TIP]
> 관리자가 아닌 경우 [Outlook을 사용 하 여 구성원을 추가 하거나 제거할](https://support.microsoft.com/office/3b650f4a-5c9b-4f94-a1bb-0cca4b1091de)수 있습니다.
  
## <a name="add-a-member-to-a-group-in-the-admin-center"></a>관리 센터에서 그룹에 구성원 추가

1. 관리 센터에서 **그룹** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">그룹</a> 페이지로 이동 합니다.  

2. 그룹 이름을 선택 합니다.

3. 세부 정보 창의 **구성원** 탭에서 **구성원 보기 및 모두 관리**를 선택 하 고 **구성원 추가**를 선택 합니다.

4. 추가할 구성원의 이름을 검색하거나 선택합니다.

5. **저장**을 선택합니다.

## <a name="add-a-group-to-a-member-in-the-admin-center"></a>관리 센터에서 구성원에 그룹 추가

1. 관리 센터에서 **사용자** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">활성 사용자</a> 페이지로 이동합니다.  

2. 사용자를 선택 합니다.

3. 세부 정보 창의 **계정** 탭에서 **그룹 관리**를 선택 합니다.

4. 추가할 그룹의 이름을 검색 하거나 선택 합니다.

5. **저장**을 선택합니다.

## <a name="remove-a-member-from-a-group-in-the-admin-center"></a>관리 센터에서 그룹의 구성원 제거

> [!NOTE]
> 비공개 그룹에서 구성원을 제거하는 경우 해당 구성원을 그룹에서 차단하는 데 5분이 소요됩니다(멤버십 변경이 도메인 컨트롤러 간에 완전히 복제된 후).

1. 관리 센터에서 **그룹** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">그룹</a> 페이지로 이동 합니다.

2. 그룹 이름을 선택 합니다.

3. 세부 정보 창의 **구성원** 탭에서 **모두 보기 및 구성원 관리**를 선택 합니다.

4. 제거 하려는 구성원 옆에 있는 X를 선택 합니다.

5. **저장** 을 선택 하 여 구성원을 제거 합니다.

## <a name="manage-group-owner-status"></a>그룹 소유자 상태 관리

기본적으로 그룹을 만든 사람은 그룹 소유자입니다. 그룹에는 종종 백업 지원 또는 기타 이유로 여러 명의 소유자가 있습니다. 구성원은 소유자 상태로 수준이 올라갈 수 있으며 소유자는 구성원 상태로 수준이 낮아질 수 있습니다.
  
### <a name="promote-a-member-to-owner-status-in-the-admin-center"></a>관리 센터에서 구성원을 소유자 상태로 수준 올리기

1. 관리 센터에서 **그룹** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">그룹</a> 페이지로 이동 합니다.

2. 그룹 이름을 선택 합니다.

3. 세부 정보 창의 **구성원** 탭에서 **모두 보기 및 소유자 관리**를 선택 합니다.

4. 구성원을 검색 하거나 **소유자 추가**를 선택 합니다.

5. 추가할 구성원의 이름 옆에 있는 확인란을 선택 합니다.

6. **저장**을 선택한 다음 **닫기를**선택 합니다.

### <a name="remove-owner-status-in-the-admin-center"></a>관리 센터에서 소유자 상태 제거

1. 관리 센터에서 **그룹** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">그룹</a> 페이지로 이동 합니다.

2. 그룹 이름을 선택 합니다.

3. 세부 정보 창의 **구성원** 탭에서 **모두 보기 및 소유자 관리**를 선택 합니다.

4. 소유자 이름 옆에 있는 X를 선택 합니다.

5. **저장**을 선택합니다.

## <a name="more-on-managing-membership"></a>멤버 자격 관리에 대한 추가 정보

- [Azure Active Directory에서 동적으로 그룹 관리](https://go.microsoft.com/fwlink/?linkid=847632): "그룹 멤버 자격을 어떻게 동적으로 관리할 수 있나요?" 단원을 참조하세요.

- 수백 또는 수천 명의 사용자를 그룹에 추가 하려면 [add-unifiedgrouplinks](https://go.microsoft.com/fwlink/p/?LinkId=616191)를 사용 합니다.

- [분리된 그룹에 새 소유자 할당](https://support.microsoft.com/office/86bb3db6-8857-45d1-95c8-f6d540e45732)

## <a name="articles-about-managing-groups"></a>그룹 관리에 대한 문서

- [Outlook에서 Microsoft 365 그룹으로 메일 그룹 업그레이드](../manage/upgrade-distribution-lists.md)

- [Outlook에서 배포 목록을 그룹으로 업그레이드해야 하는 이유](https://support.microsoft.com/office/7fb3d880-593b-4909-aafa-950dd50ce188)

- [Microsoft 365 그룹에서 게스트 액세스 관리](manage-guest-access-in-groups.md)

- [PowerShell을 사용 하 여 Microsoft 365 그룹 관리](https://docs.microsoft.com/microsoft-365/enterprise/manage-microsoft-365-groups-with-powershell):이 문서에서는 주요 cmdlet을 소개 하 고 예제를 제공 합니다.

- [Microsoft 365 그룹 명명 정책](groups-naming-policy.md)