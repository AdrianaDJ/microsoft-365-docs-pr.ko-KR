---
title: Microsoft 365 클라이언트 앱 지원-최신 인증
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: Normal
ms.collection:
- Strat_O365_Enterprise
- M365-subscription-management
search.appverid:
- MET150
f1.keywords:
- NOCSH
description: 이 문서에서는 Microsoft 365에 대 한 최신 인증을 지 원하는 플랫폼, 클라이언트 및 Powershell 모듈에 대해 설명 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: f0357c357de2b8db355c539acda851fca7802d17
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692493"
---
# <a name="microsoft-365-client-app-support---modern-authentication"></a><span data-ttu-id="88b82-103">Microsoft 365 클라이언트 앱 지원-최신 인증</span><span class="sxs-lookup"><span data-stu-id="88b82-103">Microsoft 365 Client App Support - Modern Authentication</span></span>

<span data-ttu-id="88b82-104">*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*</span><span class="sxs-lookup"><span data-stu-id="88b82-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="88b82-105">최신 인증은 여러 플랫폼의 Office 클라이언트 앱에 대해 ADAL (Active Directory 인증 라이브러리) 기반 로그인을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b82-105">Modern Authentication enables Active Directory Authentication Library (ADAL)-based sign-in for Office client apps across different platforms.</span></span> <span data-ttu-id="88b82-106">이를 통해 MFA (Multi-factor Authentication), 스마트 카드 및 인증서 기반 인증과 같은 로그인 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88b82-106">This enables sign-in features such as Multi-Factor Authentication (MFA), smart card, and certificate-based authentication.</span></span>

<span data-ttu-id="88b82-107">[Multi-factor authentication](https://docs.microsoft.com/azure/active-directory/authentication/multi-factor-authentication) 및 [인증서 기반 인증](https://docs.microsoft.com/azure/active-directory/active-directory-certificate-based-authentication-get-started)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="88b82-107">Learn more about [multi-factor authentication](https://docs.microsoft.com/azure/active-directory/authentication/multi-factor-authentication) and [certificate-based authentication](https://docs.microsoft.com/azure/active-directory/active-directory-certificate-based-authentication-get-started).</span></span>

## <a name="supported-platforms"></a><span data-ttu-id="88b82-108">지원되는 플랫폼</span><span class="sxs-lookup"><span data-stu-id="88b82-108">Supported platforms</span></span>

 - <span data-ttu-id="88b82-109">Windows 10 Desktop</span><span class="sxs-lookup"><span data-stu-id="88b82-109">Windows 10 Desktop</span></span>
 - <span data-ttu-id="88b82-110">Windows 10 최신 앱</span><span class="sxs-lookup"><span data-stu-id="88b82-110">Windows 10 Modern Apps</span></span>
 - <span data-ttu-id="88b82-111">웹 브라우저<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="88b82-111">Web browsers<sup>1</sup></span></span>
 - <span data-ttu-id="88b82-112">Android<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="88b82-112">Android<sup>2</sup></span></span>
 - <span data-ttu-id="88b82-113">iOS</span><span class="sxs-lookup"><span data-stu-id="88b82-113">iOS</span></span>
 - <span data-ttu-id="88b82-114">macOS</span><span class="sxs-lookup"><span data-stu-id="88b82-114">macOS</span></span>

<span data-ttu-id="88b82-115">Microsoft 365의 플랫폼 지원에 대 한 자세한 내용은 [microsoft 365의 시스템 요구 사항을](https://products.office.com/office-system-requirements)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88b82-115">For more information about platform support in Microsoft 365, see [System requirements for Microsoft 365](https://products.office.com/office-system-requirements).</span></span>

## <a name="supported-clients"></a><span data-ttu-id="88b82-116">지원되는 클라이언트</span><span class="sxs-lookup"><span data-stu-id="88b82-116">Supported clients</span></span>

<span data-ttu-id="88b82-117">다음 클라이언트의 최신 버전은 최신 인증을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b82-117">The latest versions of the following clients support modern authentication:</span></span>

| | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|
| <span data-ttu-id="88b82-118">![Access 아이콘](../media/o365-access-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-118">![Access icon](../media/o365-access-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-119">Access</span><span class="sxs-lookup"><span data-stu-id="88b82-119">Access</span></span>](https://products.office.com/access) | <span data-ttu-id="88b82-120">![Azure 아이콘](../media/o365-azure-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-120">![Azure icon](../media/o365-azure-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-121">Azure <br> 포털 </span><span class="sxs-lookup"><span data-stu-id="88b82-121">Azure <br> Portal </span></span>](https://azure.microsoft.com/features/azure-portal/) | <span data-ttu-id="88b82-122">![회사 포털 아이콘](../media/o365-microsoft-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-122">![Company portal icon](../media/o365-microsoft-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-123">회사 <br> 포털 </span><span class="sxs-lookup"><span data-stu-id="88b82-123">Company <br> Portal </span></span>](https://docs.microsoft.com/intune-user-help/sign-in-to-the-company-portal) | <span data-ttu-id="88b82-124">![Delve 아이콘](../media/o365-delve-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-124">![Delve icon](../media/o365-delve-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-125">Delve</span><span class="sxs-lookup"><span data-stu-id="88b82-125">Delve</span></span>](https://products.office.com/business/intelligent-search) | <span data-ttu-id="88b82-126">![Dynamics 365 아이콘](../media/o365-dynamics365-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-126">![Dynamics 365 icon](../media/o365-dynamics365-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-127">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="88b82-127">Dynamics 365</span></span>](https://dynamics.microsoft.com) 
| <span data-ttu-id="88b82-128">![에 지 아이콘](../media/o365-edge-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-128">![Edge icon](../media/o365-edge-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-129">면</span><span class="sxs-lookup"><span data-stu-id="88b82-129">Edge</span></span>](https://www.microsoft.com/windows/microsoft-edge) | <span data-ttu-id="88b82-130">![Excel 아이콘](../media/o365-excel-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-130">![Excel icon](../media/o365-excel-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-131">Excel</span><span class="sxs-lookup"><span data-stu-id="88b82-131">Excel</span></span>](https://products.office.com/excel) | <span data-ttu-id="88b82-132">![Forms 아이콘](../media/o365-forms-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-132">![Forms icon](../media/o365-forms-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-133">Forms​​</span><span class="sxs-lookup"><span data-stu-id="88b82-133">Forms</span></span>](https://flow.microsoft.com/connectors/shared_microsoftforms/microsoft-forms/) | <span data-ttu-id="88b82-134">![Kaizala 아이콘](../media/o365-kaizala-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-134">![Kaizala icon](../media/o365-kaizala-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-135">Kaizala</span><span class="sxs-lookup"><span data-stu-id="88b82-135">Kaizala</span></span>](https://products.office.com/en/business/microsoft-kaizala) | <span data-ttu-id="88b82-136">![Office.com 아이콘](../media/o365-office-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-136">![Office.com icon](../media/o365-office-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-137">Office.com</span><span class="sxs-lookup"><span data-stu-id="88b82-137">Office.com</span></span>](https://www.office.com/) 
| <span data-ttu-id="88b82-138">![Office 365 관리 아이콘](../media/o365-o365admin-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-138">![Office 365 Admin icon](../media/o365-o365admin-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-139">Microsoft 365 <br> 관리자</span><span class="sxs-lookup"><span data-stu-id="88b82-139">Microsoft 365 <br> Admin</span></span>](https://products.office.com/business/manage-office-365-admin-app) | <span data-ttu-id="88b82-140">![렌즈 아이콘](../media/o365-lens-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-140">![Lens icon](../media/o365-lens-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-141">Office Lens</span><span class="sxs-lookup"><span data-stu-id="88b82-141">Office Lens</span></span>](https://www.microsoft.com/p/office-lens/9wzdncrfj3t8?activetab=pivot%3Aoverviewtab) | <span data-ttu-id="88b82-142">![비즈니스용 OneDrive 아이콘](../media/o365-OneDrive-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-142">![OneDrive for Business icon](../media/o365-OneDrive-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-143">OneDrive</span><span class="sxs-lookup"><span data-stu-id="88b82-143">OneDrive</span></span>](https://products.office.com/onedrive-for-business/online-cloud-storage) |  <span data-ttu-id="88b82-144">![OneNote 아이콘](../media/o365-OneNote-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-144">![OneNote icon](../media/o365-OneNote-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-145">OneNote</span><span class="sxs-lookup"><span data-stu-id="88b82-145">OneNote</span></span>](https://products.office.com/onenote) | <span data-ttu-id="88b82-146">![Outlook 아이콘](../media/o365-outlook-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-146">![Outlook icon](../media/o365-outlook-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-147">Outlook</span><span class="sxs-lookup"><span data-stu-id="88b82-147">Outlook</span></span>](https://products.office.com/outlook) 
| <span data-ttu-id="88b82-148">![Planner 아이콘](../media/o365-planner-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-148">![Planner icon](../media/o365-planner-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-149">Planner</span><span class="sxs-lookup"><span data-stu-id="88b82-149">Planner</span></span>](https://products.office.com/business/task-management-software) | <span data-ttu-id="88b82-150">![PowerApps 아이콘](../media/o365-powerapps-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-150">![PowerApps icon](../media/o365-powerapps-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-151">PowerApps </span><span class="sxs-lookup"><span data-stu-id="88b82-151">PowerApps </span></span>](https://powerapps.microsoft.com) | <span data-ttu-id="88b82-152">![전원 자동화 아이콘](../media/o365-flow-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-152">![Power Automate icon](../media/o365-flow-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-153">전원 <br> 자동화</span><span class="sxs-lookup"><span data-stu-id="88b82-153">Power <br> Automate</span></span>](https://flow.microsoft.com) | <span data-ttu-id="88b82-154">![PowerBI 아이콘](../media/o365-powerbi-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-154">![PowerBI icon](../media/o365-powerbi-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-155">Power BI</span><span class="sxs-lookup"><span data-stu-id="88b82-155">Power BI</span></span>](https://powerbi.microsoft.com)| <span data-ttu-id="88b82-156">![PowerPoint 아이콘](../media/o365-powerpoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-156">![PowerPoint icon](../media/o365-powerpoint-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-157">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="88b82-157">PowerPoint</span></span>](https://products.office.com/powerpoint) 
| <span data-ttu-id="88b82-158">![Project 아이콘](../media/o365-project-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-158">![Project icon](../media/o365-project-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-159">Project</span><span class="sxs-lookup"><span data-stu-id="88b82-159">Project</span></span>](https://products.office.com/project) | <span data-ttu-id="88b82-160">![Publisher 아이콘](../media/o365-publisher-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-160">![Publisher icon](../media/o365-publisher-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-161">Publisher</span><span class="sxs-lookup"><span data-stu-id="88b82-161">Publisher</span></span>](https://products.office.com/publisher) | <span data-ttu-id="88b82-162">![SharePoint 아이콘](../media/o365-sharepoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-162">![SharePoint icon](../media/o365-sharepoint-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-163">Sharepoint</span><span class="sxs-lookup"><span data-stu-id="88b82-163">Sharepoint</span></span>](https://products.office.com/sharepoint) | <span data-ttu-id="88b82-164">![비즈니스용 Skype 아이콘](../media/o365-skypeforbusiness-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-164">![Skype for Business icon](../media/o365-skypeforbusiness-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-165">비즈니스용 Skype <br> <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="88b82-165">Skype for <br> Business<sup>1</sup></span></span>](https://www.skype.com/business/) | <span data-ttu-id="88b82-166">![StaffHub 아이콘](../media/o365-staffhub-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-166">![StaffHub icon](../media/o365-staffhub-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-167">StaffHub</span><span class="sxs-lookup"><span data-stu-id="88b82-167">StaffHub</span></span>](https://products.office.com/microsoft-staffhub/staff-scheduling-software)
| <span data-ttu-id="88b82-168">![스티커 메모 아이콘](../media/o365-stickynotes-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-168">![Sticky Notes icon](../media/o365-stickynotes-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-169">스티커 메모</span><span class="sxs-lookup"><span data-stu-id="88b82-169">Sticky Notes</span></span>](https://www.microsoft.com/p/microsoft-sticky-notes/9nblggh4qghw) | <span data-ttu-id="88b82-170">![Stream 아이콘](../media/o365-stream-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-170">![Stream icon](../media/o365-stream-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-171">Stream</span><span class="sxs-lookup"><span data-stu-id="88b82-171">Stream</span></span>](https://stream.microsoft.com) | <span data-ttu-id="88b82-172">![Sway 아이콘](../media/o365-sway-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-172">![Sway icon](../media/o365-sway-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-173">Sway</span><span class="sxs-lookup"><span data-stu-id="88b82-173">Sway</span></span>](https://sway.com) | <span data-ttu-id="88b82-174">![Teams 아이콘](../media/o365-teams-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-174">![Teams icon](../media/o365-teams-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-175">Teams</span><span class="sxs-lookup"><span data-stu-id="88b82-175">Teams</span></span>](https://products.office.com/microsoft-teams/group-chat-software) | <span data-ttu-id="88b82-176">![할 일 아이콘](../media/o365-todo-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-176">![To Do icon](../media/o365-todo-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-177">To Do</span><span class="sxs-lookup"><span data-stu-id="88b82-177">To Do</span></span>](https://todo.microsoft.com) 
| <span data-ttu-id="88b82-178">![Visio 아이콘](../media/o365-visio-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-178">![Visio icon](../media/o365-visio-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-179">Visio</span><span class="sxs-lookup"><span data-stu-id="88b82-179">Visio</span></span>](https://products.office.com/visio/flowchart-software) | <span data-ttu-id="88b82-180">![Whiteboard 아이콘](../media/o365-whiteboard-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-180">![Whiteboard icon](../media/o365-whiteboard-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-181">화이트 보드<sup>1</sup>,<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="88b82-181">Whiteboard<sup>1</sup>,<sup>2</sup></span></span>](https://whiteboard.microsoft.com/) | <span data-ttu-id="88b82-182">![Word 아이콘](../media/o365-word-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-182">![Word icon](../media/o365-word-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-183">Word</span><span class="sxs-lookup"><span data-stu-id="88b82-183">Word</span></span>](https://products.office.com/word) | <span data-ttu-id="88b82-184">![Yammer 아이콘](../media/o365-yammer-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-184">![Yammer icon](../media/o365-yammer-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-185">Yammer</span><span class="sxs-lookup"><span data-stu-id="88b82-185">Yammer</span></span>](https://products.office.com/yammer/yammer-overview) | <span data-ttu-id="88b82-186">![Yammer 아이콘](../media/o365-yammer-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-186">![Yammer icon](../media/o365-yammer-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-187">Yammer <br> 알림</span><span class="sxs-lookup"><span data-stu-id="88b82-187">Yammer <br> Notifier</span></span>](https://products.office.com/yammer/yammer-overview) |  |

## <a name="supported-powershell-modules"></a><span data-ttu-id="88b82-188">지원 되는 PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="88b82-188">Supported PowerShell modules</span></span>

| | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|
| <span data-ttu-id="88b82-189">![Azure 아이콘](../media/o365-azure-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-189">![Azure icon](../media/o365-azure-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-190">Azure AD <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="88b82-190">Azure AD <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-2.0) | <span data-ttu-id="88b82-191">![Exchange 아이콘](../media/o365-exchange-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-191">![Exchange icon](../media/o365-exchange-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-192">Exchange Online <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="88b82-192">Exchange Online <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps) | <span data-ttu-id="88b82-193">![SharePoint 아이콘](../media/o365-sharepoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="88b82-193">![SharePoint icon](../media/o365-sharepoint-64x64.png)</span></span> <br> [<span data-ttu-id="88b82-194">SharePoint Online <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="88b82-194">SharePoint Online <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

> [!NOTE]
> <span data-ttu-id="88b82-195"><sup>1</sup> 웹 앱에 대 한 화이트 보드 및 비즈니스용 Skype 지원을 곧 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88b82-195"><sup>1</sup> Support for Whiteboard and Skype for Business on web app available soon.</span></span> <br>
> <span data-ttu-id="88b82-196"><sup>2</sup> Android에서 화이트 보드에 대 한 지원이 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="88b82-196"><sup>2</sup> Support for Whiteboard on Android available soon.</span></span>

## <a name="see-also"></a><span data-ttu-id="88b82-197">참고 항목</span><span class="sxs-lookup"><span data-stu-id="88b82-197">See also</span></span>

[<span data-ttu-id="88b82-198">Microsoft 365 Enterprise 개요</span><span class="sxs-lookup"><span data-stu-id="88b82-198">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)