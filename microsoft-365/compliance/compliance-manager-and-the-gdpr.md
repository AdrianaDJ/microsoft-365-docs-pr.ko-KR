---
title: Microsoft 준수 관리자 및 GDPR
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft 준수 관리자는 Microsoft Service Trust Portal의 무료 워크플로 기반 위험 평가 도구입니다. 준수 관리자를 사용 하면 Microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인할 수 있습니다.
ms.openlocfilehash: 69e6551620fb654cb09d46554e6e3c98b6a2fc60
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595805"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="c11f0-104">Microsoft 준수 관리자 및 GDPR</span><span class="sxs-lookup"><span data-stu-id="c11f0-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="c11f0-105">유럽 연합의 GDPR (일반 데이터 보호 규정) 위임 기능은 준수 전략에 영향을 줄 수 있으며 규정 준수 관리자에 사용 되는 사용자 및 고객 정보를 관리 하기 위한 특정 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate specific actions to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="c11f0-106">사용자 개인 정보 설정</span><span class="sxs-lookup"><span data-stu-id="c11f0-106">User Privacy settings</span></span>

<span data-ttu-id="c11f0-107">특정 규정에서는 조직이 사용자 기록 데이터를 삭제할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="c11f0-108">준수 관리자는 관리자가 다음 작업을 수행할 수 있는 **사용자 개인 정보 설정** 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="c11f0-109">사용자 검색</span><span class="sxs-lookup"><span data-stu-id="c11f0-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="c11f0-110">계정 데이터 기록의 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="c11f0-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="c11f0-111">사용자 데이터 기록 삭제</span><span class="sxs-lookup"><span data-stu-id="c11f0-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="c11f0-112">사용자 검색</span><span class="sxs-lookup"><span data-stu-id="c11f0-112">Search for a user</span></span>

<span data-ttu-id="c11f0-113">사용자 계정을 검색하려면</span><span class="sxs-lookup"><span data-stu-id="c11f0-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="c11f0-114">사용자 전자 메일 별칭 (@ 기호 왼쪽에 있는 정보)을 입력 하 고 오른쪽의 도메인 접미사 목록에서 도메인 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="c11f0-115">등록 된 도메인이 여러 개인 조직의 경우 도메인 이름 접미사가 올바른지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="c11f0-116">사용자 이름을 올바르게 입력 한 경우 **검색**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="c11f0-117">사용자 계정이 반환 되지 않은 경우 페이지에 **사용자가 없는 것**으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-117">For user accounts not returned, the page displays **User not found**.</span></span> <span data-ttu-id="c11f0-118">사용자의 전자 메일 주소 정보를 확인 하 고 필요에 따라 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="c11f0-119">다시 시도 하려면 **검색**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="c11f0-120">사용자 계정이 반환 되 면 단추의 텍스트가 **검색** 에서 **지우기**로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="c11f0-121">이는 반환 된 사용자 계정이 추가 기능의 운영 컨텍스트가 고 해당 함수가이 사용자 계정에 적용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="c11f0-122">검색 결과를 지우고 다른 사용자를 검색 하려면 **지우기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="c11f0-123">계정 데이터 기록의 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="c11f0-123">Export a report of account data history</span></span>

<span data-ttu-id="c11f0-124">식별 된 각 사용자 계정에 대해 해당 계정에 연결 된 종속성 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-124">For each user account identified, you can generate a report of dependencies linked to the account.</span></span> <span data-ttu-id="c11f0-125">이 정보를 사용 하 여 열려 있는 작업 항목을 다시 할당 하거나 이전에 업로드 한 증거에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="c11f0-126">보고서를 생성하고 내보내려면:</span><span class="sxs-lookup"><span data-stu-id="c11f0-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="c11f0-127">반환 된 사용자 계정에 현재 할당 된 준수 관리자 제어 작업 항목 및 해당 사용자가 업로드 한 문서 목록에 대 한 보고서를 생성 하 고 다운로드 하려면 **내보내기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="c11f0-128">작업을 할당 하지 않았거나 문서를 업로드 하지 않은 경우에는 "이 사용자에 대 한 데이터가 없습니다." 라는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="c11f0-129">브라우저 다운로드 기록을 확인할 다운로드 팝업이 표시 되지 않는 경우 현재 브라우저 창의 백그라운드에서 보고서가 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="c11f0-130">문서를 열어 보고서 데이터를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c11f0-131">보고서 데이터는 작업 항목 할당 기록에 대 한 상태 변경 내용을 유지 하 고 표시 하는 기록 목록이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-131">The report data is not a historical list that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="c11f0-132">생성 되는 보고서는 보고서가 실행 될 때 할당 된 제어 작업 항목의 스냅숏입니다 (보고서에 날짜 및 시간 스탬프 기록)입니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="c11f0-133">예를 들어 이후에 작업 항목을 다시 할당 하는 경우 동일한 사용자에 대해 보고서가 새로 생성 되는 경우 서로 다른 스냅샷 보고서 데이터가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if the report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="c11f0-134">사용자 데이터 기록 삭제</span><span class="sxs-lookup"><span data-stu-id="c11f0-134">Delete user data history</span></span>

<span data-ttu-id="c11f0-135">반환 된 사용자에 게 할당 된 모든 제어 작업 항목을 ' 지정 되지 않음 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="c11f0-136">반환 된 사용자가 업로드 한 문서에 대해 **업로드** 한 값을 ' 사용자 제거 '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="c11f0-137">사용자 계정 작업 항목 및 문서 업로드 기록을 삭제 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="c11f0-138">**삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-138">Select **Delete**.</span></span>

    <span data-ttu-id="c11f0-139">"*이렇게 하면 선택한 사용자에 대 한 모든 컨트롤 작업 항목 할당 및 문서 업로드 기록이 제거 됩니다. 이 작업은 영구적입니다. 계속*하 시겠습니까? "</span><span class="sxs-lookup"><span data-stu-id="c11f0-139">A confirmation dialog is displayed: "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="c11f0-140">계속 하려면 **확인**을 선택 하 고 그렇지 않으면 **취소**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f0-140">To continue select **OK**, otherwise select **Cancel**.</span></span>