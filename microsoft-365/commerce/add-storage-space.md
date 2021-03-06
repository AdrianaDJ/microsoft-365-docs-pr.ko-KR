---
title: 구독에 대 한 저장소 공간 추가
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_TOC
- SPO_Content
ms.custom:
- MAX_CampaignID
- okr_SMB
- AdminSurgePortfolio
search.appverid:
- MET150
description: Microsoft 365 구독에서 파일 저장소를 추가 하 고 줄이는 방법에 대해 알아봅니다. 추가 파일 저장소를 사용 하는 경우 SharePoint Online 및 OneDrive에 더 많은 콘텐츠를 저장할 수 있습니다.
ms.date: ''
ms.openlocfilehash: 7f9973054bfe97beae36e28b73a3eb2025a13e73
ms.sourcegitcommit: 25afc0c34edc7f8a5eb389d8c701175256c58ec8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47324471"
---
# <a name="add-storage-space-for-your-subscription"></a>구독에 대 한 저장소 공간 추가

::: moniker range="o365-21vianet"

> [!NOTE]
> 관리 센터가 변경되고 있습니다. 사용자의 환경이 여기에 설명된 세부 정보와 맞지 않는 경우에는 [새 Microsoft 365 관리 센터 정보](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet)를 참조하세요.

::: moniker-end

SharePoint Online 사이트 모음의 저장소 공간이 부족해지면 해당 플랜에 자격이 있는 경우 구독에 저장소를 추가할 수 있습니다. 사용 가능한 추가 기능 목록에 **Office 365 추가 파일 저장소가** 표시 되지 않으면 계획이 적합 하지 않음을 의미 합니다. 자세한 내용은 [내 요금제를 참조 하세요](#is-my-plan-eligible-for-office-365-extra-file-storage) .

> [!NOTE]
> 볼륨 라이선스 또는 CSP를 통해 구독을 구매한 경우 Microsoft에서 직접 조직의 **Office 365 추가 파일 저장소** 를 구매할 수 없습니다. 담당자 또는 파트너에 게 도움을 요청 하세요.

## <a name="before-you-begin"></a>시작하기 전에

이 문서의 작업을 수행 하려면 전역 또는 SharePoint 관리자 여야 합니다. 자세한 내용은 [관리자 역할 정보](../admin/add-users/about-admin-roles.md)를 참조하세요.

## <a name="view-available-storage"></a>사용 가능한 저장소 보기

::: moniker range="o365-worldwide"

1. SharePoint 관리 센터에서 <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">활성 사이트</a> 페이지로 이동 하 고 조직에 대 한 [관리자 권한이](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) 있는 계정으로 로그인 합니다.

2. 페이지 오른쪽 위에서 모든 사이트에서 사용 되는 저장소의 크기와 구독의 총 저장소를 확인 합니다. 조직에서 Office 365의 다중 Geo를 구성한 경우이 막대에는 모든 지리적 위치에서 사용 된 저장소의 양이 표시 됩니다.

   ![활성 사이트 페이지의 저장소 표시줄](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > 사용 된 저장소에 지난 24-48 시간 동안의 변경 내용은 포함 되지 않습니다.

::: moniker-end

::: moniker range="o365-germany"

1. https://portal.office.de전역 또는 SharePoint 관리자 권한으로 로그인 한 다음 관리 타일을 선택 하 여 관리 센터를 엽니다. 페이지에 액세스할 수 있는 권한이 없다는 메시지가 표시 되 면 조직에 Microsoft 365 관리자 권한이 없다는 것을 의미 합니다.

2. 왼쪽 창의 **관리 센터**에서 **SharePoint**를 선택 합니다. 기존 SharePoint 관리 센터가 나타나는 경우 페이지 위쪽에 있는 **지금 열기**를 선택하여 새 SharePoint 관리 센터를 엽니다.

3. 새 SharePoint 관리 센터의 왼쪽 창에서 **활성 사이트**를 선택합니다.

4. 페이지 오른쪽 위에서 모든 사이트에서 사용 되는 저장소의 크기와 구독의 총 저장소를 확인 합니다.

   ![활성 사이트 페이지의 저장소 표시줄](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > 사용 된 저장소에 지난 24-48 시간 동안의 변경 내용은 포함 되지 않습니다.

::: moniker-end

::: moniker range="o365-21vianet"

1. https://login.partner.microsoftonline.cn/전역 또는 SharePoint 관리자 권한으로 로그인 한 다음 관리 타일을 선택 하 여 관리 센터를 엽니다. (페이지에 액세스할 수 있는 권한이 없다는 메시지가 표시 되 면 조직에 Microsoft 365 관리자 권한이 없다는 것을 의미 합니다.

2. 왼쪽 창의 **관리 센터**에서 **SharePoint**를 선택 합니다. 기존 SharePoint 관리 센터가 나타나는 경우 페이지 위쪽에 있는 **지금 열기**를 선택하여 새 SharePoint 관리 센터를 엽니다.

3. 새 SharePoint 관리 센터의 왼쪽 창에서 **활성 사이트**를 선택합니다.

4. 페이지 오른쪽 위에서 모든 사이트에서 사용 되는 저장소의 크기와 구독의 총 저장소를 확인 합니다.  

   ![활성 사이트 페이지의 저장소 표시줄](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > 사용 된 저장소에 지난 24-48 시간 동안의 변경 내용은 포함 되지 않습니다.

::: moniker-end

사용 중인 저장소의 용량을 확인한 후에는 구독에 대해 저장소 공간을 추가 또는 제거할 수 있습니다. 저장소 공간을 추가 하는 데 드는 비용을 확인 하려면이 문서에 나와 있는 단계를 수행 하 고 구입 하기 전에 가격 산정 정보를 검토 하세요.
  
사이트 모음 저장 용량 제한을 설정 하는 방법에 대 한 자세한 내용은 [사이트 모음 저장 용량 제한 관리](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits)를 참조 하세요.
  
## <a name="add-storage-to-your-subscription"></a>구독에 저장소 추가

구독에 대 한 추가 저장소를 아직 구입 하지 않은 경우이 작업을 수행할 수 있습니다.

::: moniker range="o365-worldwide"

1. 관리 센터에서 **결제** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">구매 서비스</a> 페이지로 이동 합니다.
2. **서비스 구매** 페이지 아래쪽에서 **추가 기능**을 선택 합니다.
3. **Office 365 추가 파일 저장소**를 선택 합니다.
4. 표시 되는 경우 **Office 365 추가 파일 저장소** 페이지에서 기본 구독을 선택한 다음 추가할 저장소의 기가바이트 수를 입력 합니다.
5. **지금 체크 아웃**을 선택 합니다.
6. 표시 **방법** 페이지에서 선택한 저장소의 기가바이트 수를 확인 하 고 가격 정보를 검토 한 후 **다음**을 선택 합니다.
7. **전체 순서** 페이지에서 합계를 확인 합니다. 변경 작업을 수행 해야 하는 경우에는 **순서 편집**을 선택 합니다. 주문에 신용 검사가 필요한 경우 확인란을 선택 합니다. 작업이 완료 되 면 " **주문** " \> **을 선택 하 고 관리 홈으로 이동**합니다.

::: moniker-end

::: moniker range="o365-germany"

1. 관리 센터에서 **청구** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">구독</a> 페이지로 이동 합니다.  

2. **구독** 페이지에서 저장소 공간을 추가 하려는 구독을 선택 하 고 **추가 기능**을 선택 합니다.

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > **추가 기능이**표시 되지 않는 경우 파트너를 통해 구독을 구매한 경우 **볼륨 라이선스 서비스 센터 (VLSC)** 를 선택 합니다.
  
3. **추가 기능 구입**을 선택 합니다.

    ![관리 센터의 구독 페이지에서 추가 기능 구입 링크를 사용 하세요.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. **서비스 구매** 페이지에서 **Office 365 추가 파일 저장소**를 마우스로 가리키거나 탭 한 다음 **지금 구입**을 선택 합니다.
  
5. 필요한 사용자 라이선스 수를 입력 하 고 표시 되는 경우 기본 구독을 선택 합니다. **지금 체크 아웃**을 선택 합니다.
  
6. 표시 **방법** 페이지에서 선택한 저장소의 기가바이트 수를 확인 하 고 가격 정보를 검토 한 후 **다음**을 선택 합니다.

7. **전체 순서** 페이지에서 **주문을**선택 합니다.

::: moniker-end

::: moniker range="o365-21vianet"

1. 관리 센터에서 **청구** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">구독</a> 페이지로 이동합니다.

2. **구독** 페이지에서 저장소 공간을 추가 하려는 구독을 선택 하 고 **추가 기능**을 선택 합니다.

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > **추가 기능이**표시 되지 않는 경우 파트너를 통해 구독을 구매한 경우 **볼륨 라이선스 서비스 센터 (VLSC)** 를 선택 합니다.
  
3. **추가 기능 구입**을 선택 합니다.

    ![관리 센터의 구독 페이지에서 추가 기능 구입 링크를 사용 하세요.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. **서비스 구매** 페이지에서 **Office 365 추가 파일 저장소**를 마우스로 가리키거나 탭 한 다음 **지금 구입**을 선택 합니다.
  
5. 필요한 사용자 라이선스 수를 입력 하 고 표시 되는 경우 기본 구독을 선택 합니다. **지금 체크 아웃**을 선택 합니다.
  
6. 표시 **방법** 페이지에서 선택한 저장소의 기가바이트 수를 확인 하 고 가격 정보를 검토 한 후 **다음**을 선택 합니다.

7. **전체 순서** 페이지에서 **주문을**선택 합니다.

::: moniker-end

## <a name="increase-or-decrease-storage"></a>저장소 확대 또는 축소

**Office 365 추가 파일 저장소** 추가 기능을 통해 추가 파일 저장소를 이미 구매한 경우 이러한 단계를 사용 하 여 구독에 대 한 추가 저장소 공간을 늘리거나 낮출 수 있습니다. 저장소 용량을 1gb로 줄일 수 있습니다. 추가 저장 공간을 모두 제거 하려면 [지원 서비스에 문의 하세요](../admin/contact-support-for-business-products.md).

::: moniker range="o365-worldwide"

1. 관리 센터에서 **결제**\> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">내 상품</a>페이지로 이동하세요.
2. **제품** 탭에서 **Office 365 기타 파일 저장소** 추가 기능을 포함 하는 구독을 선택 합니다.
3. 제품 세부 정보 페이지의 **추가** 기능 섹션에서 **추가 기능 관리**를 선택 합니다.
4. **추가 기능 관리** 창의 **추가 기능** 목록에서 **Office 365 기타 파일 저장소**를 선택 합니다.
5. **수량** 텍스트 상자에 구독에 사용할 저장 공간의 GBs 수를 입력 합니다.
6. **저장**을 선택합니다.

::: moniker-end

::: moniker range="o365-germany"

1. 관리 센터에서 **청구** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">구독</a> 페이지로 이동합니다.

2. **구독** 페이지에서 **추가 기능**을 선택 합니다.

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > **추가 기능이**표시 되지 않는 경우 파트너를 통해 구독을 구매한 경우 **볼륨 라이선스 서비스 센터 (VLSC)** 를 선택 합니다.
  
3. **Office 365 추가 파일 저장소**에서 **수량 변경을**선택 합니다.

    ![수량 변경 링크](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. 오른쪽 창에서 필요한 총 기가바이트 수를 입력 한 다음 **제출을**선택 합니다.

    예를 들어, 현재 추가 파일 저장소가 200기가바이트인데 100기가바이트만 필요한 경우 이 상자에 **100**을 입력할 수 있습니다.

5. **닫기**를 선택합니다.

::: moniker-end

::: moniker range="o365-21vianet"

1. 관리 센터에서 **청구** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">구독</a> 페이지로 이동합니다.

2. **구독** 페이지에서 **추가 기능**을 선택 합니다.

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > **추가 기능이**표시 되지 않는 경우 파트너를 통해 구독을 구매한 경우 **볼륨 라이선스 서비스 센터 (VLSC)** 를 선택 합니다.
  
3. **Office 365 추가 파일 저장소**에서 **수량 변경을**선택 합니다.

    ![수량 변경 링크](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. 오른쪽 창에서 필요한 총 기가바이트 수를 입력 한 다음 **제출을**선택 합니다.

    예를 들어, 현재 추가 파일 저장소가 200기가바이트인데 100기가바이트만 필요한 경우 이 상자에 **100**을 입력할 수 있습니다.

5. **닫기**를 선택합니다.

::: moniker-end

## <a name="is-my-plan-eligible-for-office-365-extra-file-storage"></a>내 요금제로 Office 365 추가 파일 저장소를 사용할 수 있나요?

Office 365 추가 파일 저장소는 다음 구독에서 사용할 수 있습니다.
  
- Office 365 Enterprise E1

- Office 365 Enterprise E2

- Office 365 Enterprise E3

- Office 365 Enterprise E4

- Office 365 Enterprise E5

- SharePoint 계획 1을 사용 하는 웹의 Office

- SharePoint 계획 2를 사용 하는 웹의 Office

- SharePoint Online 요금제 1

- SharePoint Online 요금제 2

- Microsoft 365 Business Basic

- Microsoft 365 Business Standard

- Microsoft 365 Business Premium

- Microsoft 365 E3

- Microsoft 365 E5

- Microsoft 365 F1

> [!NOTE]
> Office 365 GCC, GCC High 및 DOD 계획에도 추가 파일 저장소를 사용할 수 있습니다.

## <a name="related-content"></a>관련 콘텐츠

[사이트 저장 용량 제한 관리](ttps://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits) (문서) \
[OneDrive 사용자에 대 한 기본 저장소 공간 설정](https://docs.microsoft.com/onedrive/set-default-storage-space)(문서)
