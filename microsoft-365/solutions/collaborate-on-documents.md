---
title: 게스트와 문서 상 공동 작업하기
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: sharepoint-online
ms.collection: SPO_Content
localization_priority: Normal
f1.keywords: NOCSH
description: SharePoint 및 OneDrive에서 문서에 대 한 게스트와 공동 작업 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 139533b2d7bf65ddd9584007a5ac03800c731d0b
ms.sourcegitcommit: 21338a9287017a66298e0ff557e80051946ebf13
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2020
ms.locfileid: "42604782"
---
# <a name="collaborate-with-guests-on-a-document"></a><span data-ttu-id="26d20-103">게스트와 문서 상 공동 작업하기</span><span class="sxs-lookup"><span data-stu-id="26d20-103">Collaborate with guests on a document</span></span>

<span data-ttu-id="26d20-104">SharePoint 또는 OneDrive의 문서를 조직 외부의 사용자와 공동으로 작업 해야 하는 경우 문서에 대 한 공유 링크를 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-104">If you need to collaborate with people outside your organization on documents in SharePoint or OneDrive, you can send them a sharing link to the document.</span></span> <span data-ttu-id="26d20-105">이 문서에서는 조직의 필요에 따라 SharePoint 및 OneDrive에 대 한 공유 링크를 설정 하는 데 필요한 Microsoft 365 구성 단계를 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-105">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up sharing links for SharePoint and OneDrive for the needs of your organization.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="26d20-106">비디오 데모</span><span class="sxs-lookup"><span data-stu-id="26d20-106">Video demonstration</span></span>

<span data-ttu-id="26d20-107">이 비디오에서는이 문서에서 설명 하는 구성 단계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-107">This video shows the configuration steps described in this document.</span></span></br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE450Vt?autoplay=false]

## <a name="azure-organizational-relationships-settings"></a><span data-ttu-id="26d20-108">Azure 조직 관계 설정</span><span class="sxs-lookup"><span data-stu-id="26d20-108">Azure Organizational relationships settings</span></span>

<span data-ttu-id="26d20-109">Microsoft 365의 공유는 Azure Active Directory의 조직 관계 설정에 따라 최상위 수준에서 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-109">Sharing in Microsoft 365 is governed at its highest level by the organizational relationships settings in Azure Active Directory.</span></span> <span data-ttu-id="26d20-110">Azure AD에서 게스트 공유가 사용 하지 않도록 설정 되거나 제한 되 면 Microsoft 365에서 구성한 모든 공유 설정이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-110">If guest sharing is disabled or restricted in Azure AD, this will override any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="26d20-111">조직 관계 설정을 확인 하 여 게스트가 공유 하는 것이 차단 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-111">Check the organizational relationships settings to ensure that sharing with guests is not blocked.</span></span>

![Azure Active Directory 조직 관계 설정 페이지 스크린샷](../media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="26d20-113">조직 관계 설정을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="26d20-113">To set organizational relationship settings</span></span>

1. <span data-ttu-id="26d20-114">Microsoft Azure에 로그인 [https://portal.azure.com](https://portal.azure.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-114">Log in to Microsoft Azure at [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="26d20-115">왼쪽 탐색 창에서 **Azure Active Directory**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-115">In the left navigation, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="26d20-116">**개요** 창에서 **조직 관계**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-116">In the **Overview** pane, click **Organizational relationships**.</span></span>
4. <span data-ttu-id="26d20-117">**조직 관계** 창에서 **설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-117">In the **Organizational relationships** pane, click **Settings**.</span></span>
5. <span data-ttu-id="26d20-118">**Guest inviter 역할의 관리자 및 사용자가 초대** 를 하 고 **구성원은 초대** 를 할 수 있는지 확인 하 고 둘 다 **예**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-118">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="26d20-119">변경한 내용이 있으면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-119">If you made changes, click **Save**.</span></span>

<span data-ttu-id="26d20-120">**공동 작업 제한** 섹션의 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-120">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="26d20-121">공동 작업 하려는 게스트의 도메인이 차단 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-121">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="26d20-122">SharePoint 조직 수준 공유 설정</span><span class="sxs-lookup"><span data-stu-id="26d20-122">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="26d20-123">조직 외부의 사용자가 SharePoint 또는 OneDrive의 문서에 액세스할 수 있도록 하려면 SharePoint 및 OneDrive 조직 수준 공유 설정에서 조직 외부의 사용자와 공유 하는 것을 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-123">In order for people outside your organization to have access to a document in SharePoint or OneDrive, the SharePoint and OneDrive organization-level sharing settings must allow for sharing with people outside your organization.</span></span>

<span data-ttu-id="26d20-124">SharePoint의 조직 수준 설정에 따라 개별 SharePoint 사이트에서 사용할 수 있는 설정이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-124">The organization-level settings for SharePoint determine what settings are available for individual SharePoint sites.</span></span> <span data-ttu-id="26d20-125">사이트 설정은 조직 수준 설정 보다는 더 이상 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-125">Site settings cannot be more permissive than the organization-level settings.</span></span> <span data-ttu-id="26d20-126">OneDrive에 대 한 조직 수준 설정에 따라 사용자의 OneDrive 라이브러리에서 사용할 수 있는 공유 수준이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-126">The organization-level setting for OneDrive determines what level of sharing is available in users' OneDrive libraries.</span></span>

<span data-ttu-id="26d20-127">SharePoint 및 OneDrive의 경우 인증 되지 않은 파일 및 폴더 공유를 허용 하려면 **모든 사용자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-127">For SharePoint and OneDrive, if you want to allow unauthenticated file and folder sharing, choose **Anyone**.</span></span> <span data-ttu-id="26d20-128">조직 외부의 사용자가 인증을 받아야 하는 경우 **신규 및 기존 게스트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-128">If you want to ensure that people outside your organization have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="26d20-129">공유 하는 가장 쉬운 방법은 *사용자* 의 조직 외부 사용자가 인증 없이 링크를 열 수 있으며이를 다른 사람에 게 전달 하는 데 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-129">*Anyone* links are the easiest way to share: people outside your organization can open the link without authentication and are free to pass it on to others.</span></span>

<span data-ttu-id="26d20-130">SharePoint의 경우 조직의 모든 사이트에서 필요한 가장 관대 한 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-130">For SharePoint, choose the most permissive setting that will be needed by any site in your organization.</span></span>

![SharePoint 조직 수준 공유 설정의 스크린샷](../media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="26d20-132">SharePoint 조직 수준 공유 설정을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="26d20-132">To set SharePoint organization level sharing settings</span></span>

1. <span data-ttu-id="26d20-133">Microsoft 365 관리 센터의 왼쪽 탐색에 있는 **관리 센터**에서 **SharePoint**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-133">In the Microsoft 365 admin center, in the left navigation, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="26d20-134">왼쪽 탐색 창의 SharePoint 관리 센터에서 **공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-134">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="26d20-135">SharePoint 또는 OneDrive에 대 한 외부 공유가 **모든 사용자** 또는 **신규 및 기존 게스트로**설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-135">Ensure that external sharing for SharePoint or OneDrive is set to **Anyone** or **New and existing guests**.</span></span> <span data-ttu-id="26d20-136">OneDrive 설정은 SharePoint 설정 보다 더 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-136">(Note that the OneDrive setting cannot be more permissive than the SharePoint setting.)</span></span>
4. <span data-ttu-id="26d20-137">변경한 내용이 있으면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-137">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-organization-level-default-link-settings"></a><span data-ttu-id="26d20-138">SharePoint 조직 수준 기본 링크 설정</span><span class="sxs-lookup"><span data-stu-id="26d20-138">SharePoint organization level default link settings</span></span>

<span data-ttu-id="26d20-139">기본 파일 및 폴더 링크 설정에 따라 파일 또는 폴더를 공유할 때 기본적으로 사용자에 게 표시 되는 링크 옵션이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-139">The default file and folder link settings determine which link option is shown to the user by default when they share a file or folder.</span></span> <span data-ttu-id="26d20-140">원하는 경우 공유 하기 전에 다른 옵션 중 하나로 연결 유형을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-140">Users can change the link type to one of the other options before sharing if desired.</span></span>

<span data-ttu-id="26d20-141">이 설정은 OneDrive 뿐 아니라 조직의 SharePoint 사이트에도 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-141">Keep in mind that this setting affects SharePoint sites in your organization, as well as OneDrive.</span></span>

<span data-ttu-id="26d20-142">사용자가 파일 및 폴더를 공유할 때 기본적으로 선택 되는 링크 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-142">Choose the type of link that's selected by default when users share files and folders:</span></span>

- <span data-ttu-id="26d20-143">**링크를 포함 하는 모든 사용자** 인증 되지 않은 파일 및 폴더 공유를 많이 수행 하려는 경우이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-143">**Anyone with the link** - Choose this option if you expect to do a lot of unauthenticated file and folder sharing.</span></span> <span data-ttu-id="26d20-144">*모든* 링크를 허용 하지만 실수로 인증 되지 않은 공유가 발생 하는 것이 염려 되는 경우에는 다른 옵션 중 하나를 기본값으로 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-144">If you want to allow *Anyone* links but are concerned about accidental unauthenticated sharing, consider one of the other options as the default.</span></span> <span data-ttu-id="26d20-145">이 링크 형식은 **모든 사용자** 가 공유 하도록 설정한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-145">This link type is only available if you've enabled **Anyone** sharing.</span></span>
- <span data-ttu-id="26d20-146">**조직의 사용자만** 조직 내부 사용자와 파일 및 폴더 공유를 사용할 것으로 예상 되는 경우이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-146">**Only people in your organization** - Choose this option if you expect most file and folder sharing to be with people inside your organization.</span></span>
- <span data-ttu-id="26d20-147">**특정 사용자** -게스트와 파일 및 폴더 공유를 많이 수행 해야 하는 경우이 옵션을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="26d20-147">**Specific people** - Consider this option if you expect to do a lot of file and folder sharing with guests.</span></span> <span data-ttu-id="26d20-148">이 유형의 링크는 게스트에서 작동 하며 인증을 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-148">This type of link works with guests and requires them to authenticate.</span></span>
 
![SharePoint 조직 수준 파일 및 폴더 공유 설정 스크린샷](../media/sharepoint-organization-files-folders-sharing-settings.png)


<span data-ttu-id="26d20-150">SharePoint 및 OneDrive 조직 수준 기본 링크 설정을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="26d20-150">To set the SharePoint and OneDrive organization level default link settings</span></span>

1. <span data-ttu-id="26d20-151">SharePoint 관리 센터에서 공유 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-151">Navigate to the Sharing page in the SharePoint admin center.</span></span>
2. <span data-ttu-id="26d20-152">**파일 및 폴더 링크**에서 사용 하려는 기본 공유 링크를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-152">Under **File and folder links**, select the default sharing link that you want to use.</span></span>
3. <span data-ttu-id="26d20-153">변경한 내용이 있으면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-153">If you made changes, click **Save**.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="26d20-154">SharePoint 사이트 수준 공유 설정</span><span class="sxs-lookup"><span data-stu-id="26d20-154">SharePoint site level sharing settings</span></span>

<span data-ttu-id="26d20-155">SharePoint 사이트에 있는 파일 및 fodlers를 공유 하는 경우에는 해당 사이트에 대 한 사이트 수준 공유 설정도 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-155">If you're sharing files and fodlers that are in a SharePoint site, you also need to check the site-level sharing settings for that site.</span></span>

![SharePoint 사이트 외부 공유 설정 스크린샷](../media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="26d20-157">사이트 수준 공유 설정을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="26d20-157">To set site-level sharing settings</span></span>
1. <span data-ttu-id="26d20-158">SharePoint 관리 센터의 왼쪽 탐색 창에서 **사이트**를 확장시키고 **Active 사이트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-158">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="26d20-159">방금 만든 사이트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-159">Select the site that you just created.</span></span>
3. <span data-ttu-id="26d20-160">리본 메뉴에서 **공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-160">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="26d20-161">공유가 **사용자** 또는 **신규 및 기존 게스트로**설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-161">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="26d20-162">변경한 내용이 있으면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-162">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="26d20-163">사용자 초대</span><span class="sxs-lookup"><span data-stu-id="26d20-163">Invite users</span></span>

<span data-ttu-id="26d20-164">이제 게스트 공유 설정이 구성 되므로 사용자가 조직 외부의 사용자와 파일 및 폴더를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26d20-164">Guest sharing settings are now configured, so users can now share files and folders with people outside your organization.</span></span> <span data-ttu-id="26d20-165">자세한 내용은 [OneDrive 파일 및 폴더](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) 공유 및 [SharePoint 파일 또는 폴더 공유](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26d20-165">See [Share OneDrive files and folders](https://support.office.com/article/9fcc2f7d-de0c-4cec-93b0-a82024800c07) and [Share SharePoint files or folders](https://support.office.com/article/1fe37332-0f9a-4719-970e-d2578da4941c) for more information.</span></span>

## <a name="see-also"></a><span data-ttu-id="26d20-166">참고 항목</span><span class="sxs-lookup"><span data-stu-id="26d20-166">See Also</span></span>

[<span data-ttu-id="26d20-167">인증되지 않은 사용자와 파일 및 폴더를 공유하는 모범 사례</span><span class="sxs-lookup"><span data-stu-id="26d20-167">Best practices for sharing files and folders with unauthenticated users</span></span>](best-practices-anonymous-sharing.md)

[<span data-ttu-id="26d20-168">게스트와 공유할 때 파일에 실수로 발생하는 노출을 제한</span><span class="sxs-lookup"><span data-stu-id="26d20-168">Limit accidental exposure to files when sharing with guests</span></span>](share-limit-accidental-exposure.md)