---
title: Microsoft 365에서 디렉터리 동기화 상태 보기
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MED150
ms.assetid: 18be3b98-34ae-47be-9337-ab6c3fb372ac
description: 이 문서에서는 Office 365에서 디렉터리 동기화 상태를 확인 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: c77898b58b58c6ae91492debd7ad66f395d80d52
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692630"
---
# <a name="view-directory-synchronization-status-in-microsoft-365"></a><span data-ttu-id="4ea4d-103">Microsoft 365에서 디렉터리 동기화 상태 보기</span><span class="sxs-lookup"><span data-stu-id="4ea4d-103">View directory synchronization status in Microsoft 365</span></span>

<span data-ttu-id="4ea4d-104">온-프레미스 환경을 Microsoft 365와 동기화 하 여 온-프레미스 Active Directory를 Azure AD와 통합 한 경우에도 동기화 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-104">If you have integrated your on-premises Active Directory with Azure AD by synchronizing your on-premises environment with Microsoft 365, you can also check the status of your synchronization.</span></span>
  
## <a name="view-directory-synchronization-status"></a><span data-ttu-id="4ea4d-105">디렉터리 동기화 상태 보기</span><span class="sxs-lookup"><span data-stu-id="4ea4d-105">View directory synchronization status</span></span>

- <span data-ttu-id="4ea4d-106">[Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 하 고 홈 페이지에서 **DirSync 상태** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-106">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) and choose **DirSync Status** on the home page.</span></span>
- <span data-ttu-id="4ea4d-107">또는 **사용자** \> **활성 사용자**로 이동 하 여 **활성 사용자** 페이지에서 **더 많은** \> **디렉터리 동기화**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-107">Alternately, you can go to **Users** \> **Active users**, and on the **Active users** page, choose **More** \> **Directory synchronization**.</span></span> <span data-ttu-id="4ea4d-108">**디렉터리 동기화** 창에서 **DirSync 관리로 이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-108">On the **Directory Synchronization** pane, choose **Go to DirSync management**.</span></span>

## <a name="information-on-the-manage-directory-synchronization-page"></a><span data-ttu-id="4ea4d-109">디렉터리 동기화 관리 페이지에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="4ea4d-109">Information on the Manage directory synchronization page</span></span>

<span data-ttu-id="4ea4d-110">다음 표에서는 페이지에 대 한 정보를 얻을 수 있는 기능을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-110">The following table lists the features you can get information about on the page.</span></span>
  
<span data-ttu-id="4ea4d-111">디렉터리 동기화에 문제가 있으면 오류가이 페이지에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-111">If there is a problem with your directory synchronization, the errors are listed on this page as well.</span></span> <span data-ttu-id="4ea4d-112">발생할 수 있는 다양 한 오류에 대 한 자세한 내용은 [Microsoft 365에서 디렉터리 동기화 오류 파악](identify-directory-synchronization-errors.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-112">For more information about different errors you might encounter, see [Identify directory synchronization errors in Microsoft 365](identify-directory-synchronization-errors.md).</span></span>
  
|<span data-ttu-id="4ea4d-113">**항목**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-113">**Item**</span></span>|<span data-ttu-id="4ea4d-114">**용도**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-114">**What it's for**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ea4d-115">**확인 된 도메인**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-115">**Domains verified**</span></span> | <span data-ttu-id="4ea4d-116">사용자가 본인을 확인 한 Microsoft 365 테 넌 트의 도메인 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-116">Number of domains in your Microsoft 365 tenant that you have verified you own.</span></span> |
|<span data-ttu-id="4ea4d-117">**도메인이 확인 되지 않음**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-117">**Domains not verified**</span></span> | <span data-ttu-id="4ea4d-118">추가한 도메인 (확인 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="4ea4d-118">Domains you have added, but not verified.</span></span> |
|<span data-ttu-id="4ea4d-119">**디렉터리 동기화 사용**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-119">**Directory sync enabled**</span></span> |<span data-ttu-id="4ea4d-120">True 또는 False입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-120">True or False.</span></span> <span data-ttu-id="4ea4d-121">디렉터리 동기화를 사용 하도록 설정 했는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-121">Specifies whether you have enabled directory sync.</span></span> |
|<span data-ttu-id="4ea4d-122">**최신 디렉터리 동기화**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-122">**Latest directory sync**</span></span> | <span data-ttu-id="4ea4d-123">디렉터리 동기화를 마지막으로 실행 한 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-123">Last time directory sync ran.</span></span> <span data-ttu-id="4ea4d-124">마지막 동기화가 3 일 전까지 경고 및 문제 해결 도구에 대 한 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-124">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="4ea4d-125">**암호 동기화 사용**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-125">**Password sync enabled**</span></span> | <span data-ttu-id="4ea4d-126">True 또는 False입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-126">True or False.</span></span> <span data-ttu-id="4ea4d-127">온-프레미스와 Microsoft 365 테 넌 트 간에 암호 해시 동기화가 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-127">Specifies whether you have password hash sync between our on-premises and your Microsoft 365 tenant.</span></span> |
|<span data-ttu-id="4ea4d-128">**마지막 암호 동기화**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-128">**Last Password Sync**</span></span> | <span data-ttu-id="4ea4d-129">암호 해시 동기화를 마지막으로 실행 한 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-129">Last time password hash sync ran.</span></span> <span data-ttu-id="4ea4d-130">마지막 동기화가 3 일 전까지 경고 및 문제 해결 도구에 대 한 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-130">Will display a warning and a link to a troubleshooting tool if the last sync was more than three days ago.</span></span> |
|<span data-ttu-id="4ea4d-131">**디렉터리 동기화 클라이언트 버전**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-131">**Directory sync client version**</span></span> | <span data-ttu-id="4ea4d-132">새 버전의 Azure AD Connect가 릴리스되면 다운로드 링크를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-132">Contains a download link if a new version of Azure AD Connect has been released.</span></span> |
|<span data-ttu-id="4ea4d-133">**디렉터리 동기화 서비스 계정**</span><span class="sxs-lookup"><span data-stu-id="4ea4d-133">**Directory sync service account**</span></span> | <span data-ttu-id="4ea4d-134">Microsoft 365 디렉터리 동기화 서비스 계정의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea4d-134">Displays the name of your Microsoft 365 directory sync service account.</span></span> |