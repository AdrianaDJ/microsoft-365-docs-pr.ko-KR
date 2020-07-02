---
title: Bloomberg 메시지 데이터를 보관 하는 커넥터 설정
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
ms.collection: M365-security-compliance
description: 관리자는 데이터 커넥터를 설정 하 여 Bloomberg 메시지 전자 메일 도구에서 Microsoft 365로 데이터를 가져오고 보관 합니다. 이를 통해 Microsoft 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리할 수도 있습니다.
ms.openlocfilehash: 700a0619d2299fc7254628059787478cc0e168fa
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937365"
---
# <a name="set-up-a-connector-to-archive-bloomberg-message-data-preview"></a><span data-ttu-id="ef9c8-104">Bloomberg 메시지 데이터를 보관 하는 커넥터 설정 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="ef9c8-104">Set up a connector to archive Bloomberg Message data (preview)</span></span>

<span data-ttu-id="ef9c8-105">Microsoft 365 준수 센터의 데이터 커넥터를 사용 하 여 [Bloomberg 메시지](https://www.bloomberg.com/professional/product/collaboration/) 공동 작업 도구에서 금융 서비스 전자 메일 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-105">Use a data connector in the Microsoft 365 compliance center to import and archive financial services email data from the [Bloomberg Message](https://www.bloomberg.com/professional/product/collaboration/) collaboration tool.</span></span> <span data-ttu-id="ef9c8-106">커넥터를 설정 하 고 구성한 후에는 매일 조직의 Bloomberg 보안 FTP (SFTP) 사이트에 연결 하 고 Microsoft 365의 사서함으로 전자 메일 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-106">After you set up and configure a connector, it connects to your organization's Bloomberg secure FTP (SFTP) site once every day, and imports email items to mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="ef9c8-107">Bloomberg 메시지 데이터가 사용자 사서함에 저장 되 면 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사, 통신 준수 및 Microsoft 365 보존 정책과 같은 Microsoft 365 준수 기능을 Bloomberg 메시지 데이터에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-107">After Bloomberg Message data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation hold, content search, In-place archiving, auditing, Communication compliance, and Microsoft 365 retention policies to Bloomberg Message data.</span></span> <span data-ttu-id="ef9c8-108">예를 들어 콘텐츠 검색 도구를 사용 하 여 Bloomberg 메시지 전자 메일을 검색 하거나 고급 eDiscovery 사례의 Bloomberg 메시지 데이터를 포함 하는 사서함을 custodian에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-108">For example, you can search Bloomberg Message emails using the content search tool or associate the mailbox that contains the Bloomberg Message data with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="ef9c8-109">Bloomberg 메시지 커넥터를 사용 하 여 Microsoft 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-109">Using a Bloomberg Message connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-bloomberg-message-data"></a><span data-ttu-id="ef9c8-110">Bloomberg 메시지 데이터 보관 개요</span><span class="sxs-lookup"><span data-stu-id="ef9c8-110">Overview of archiving Bloomberg Message data</span></span>

<span data-ttu-id="ef9c8-111">다음 개요에서는 커넥터를 사용 하 여 Bloomberg 메시지 데이터를 Microsoft 365에 보관 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-111">The following overview explains the process of using a connector to archive Bloomberg Message data in Microsoft 365.</span></span>

![Bloomberg 메시지 가져오기 및 보관 프로세스](../media/BloombergMessageArchiving.png)

1. <span data-ttu-id="ef9c8-113">조직에서 Bloomberg를 사용 하 여 Bloomberg SFTP 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-113">Your organization works with Bloomberg to set up a Bloomberg SFTP site.</span></span> <span data-ttu-id="ef9c8-114">또한 Bloomberg을 사용 하 여 Bloomberg 메시지를 구성 하 여 Bloomberg SFTP 사이트에 전자 메일 메시지를 복사 하는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-114">You'll also work with Bloomberg to configure Bloomberg Message to copy email messages to the Bloomberg SFTP site.</span></span>

2. <span data-ttu-id="ef9c8-115">24 시간 마다 한 번씩 Bloomberg 메시지의 전자 메일 메시지는 Bloomberg SFTP 사이트에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-115">Once every 24 hours, email messages from Bloomberg Message are copied to the Bloomberg SFTP site.</span></span>

3. <span data-ttu-id="ef9c8-116">Microsoft 365 준수 센터에서 만드는 Bloomberg 메시지 커넥터는 매일 Bloomberg SFTP 사이트에 연결 하 고 이전 24 시간에서 Microsoft 클라우드의 안전한 Azure Storage 영역으로 전자 메일 메시지를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-116">The Bloomberg Message connector that you create in the Microsoft 365 compliance center connects to the Bloomberg SFTP site every day and transfers the email messages from the previous 24 hours to a secure Azure Storage area in the Microsoft Cloud.</span></span>

4. <span data-ttu-id="ef9c8-117">커넥터는 전자 메일 메시지 항목을 특정 사용자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-117">The connector imports the email message items to the mailbox of a specific user.</span></span> <span data-ttu-id="ef9c8-118">BloombergMessage 이라는 새 폴더가 특정 사용자의 사서함에 만들어지고이 폴더에 항목을 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-118">A new folder named BloombergMessage will be created in the specific user's mailbox and the items will be imported to it.</span></span> 

   <span data-ttu-id="ef9c8-119">커넥터는 CorporateEmailAddress 속성 값을 사용 하 여이를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-119">The connector does this by using the value of the CorporateEmailAddress property.</span></span> <span data-ttu-id="ef9c8-120">모든 전자 메일 메시지에는 전자 메일 메시지의 모든 참석자의 전자 메일 주소로 채워지는이 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-120">Every email message contains this property, which is populated with the email address of every participant of the email message.</span></span> <span data-ttu-id="ef9c8-121">*CorporateEmailAddress* 속성 값을 사용 하는 자동 사용자 매핑 외에도 CSV 매핑 파일을 업로드 하 여 사용자 지정 매핑을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-121">In addition to automatic user mapping using the value of the *CorporateEmailAddress* property, you can also define a custom mapping by uploading a CSV mapping file.</span></span> <span data-ttu-id="ef9c8-122">이 매핑 파일에는 조직의 각 사용자에 대 한 Bloomberg UUID 및 해당 Microsoft 365 사서함 주소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-122">This mapping file contains a Bloomberg UUID and the corresponding Microsoft 365 mailbox address for each user in your organization.</span></span> <span data-ttu-id="ef9c8-123">자동 사용자 매핑을 사용 하도록 설정 하 고 사용자 지정 매핑을 제공 하는 경우 모든 전자 메일 항목에 대해 커넥터가 사용자 지정 매핑 파일을 먼저 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-123">If you enable automatic user mapping and provide a custom mapping, for every email item the connector will first look at the custom-mapping file.</span></span> <span data-ttu-id="ef9c8-124">사용자의 Bloomberg UUID에 해당 하는 유효한 Microsoft 365 사용자를 찾지 못하면 커넥터는 전자 메일 항목의 *CorporateEmailAddress* 속성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-124">If it doesn't find a valid Microsoft 365 user that corresponds to a user's Bloomberg UUID, the connector uses the *CorporateEmailAddress* property of the email item.</span></span> <span data-ttu-id="ef9c8-125">커넥터가 사용자 지정 매핑 파일 또는 전자 메일 항목의 *CorporateEmailAddress* 속성에서 유효한 Microsoft 365 사용자를 찾지 못하면 항목을 가져오지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-125">If the connector doesn't find a valid Microsoft 365 user in either the custom-mapping file or the *CorporateEmailAddress* property of the email item, the item won't be imported.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ef9c8-126">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="ef9c8-126">Before you begin</span></span>

<span data-ttu-id="ef9c8-127">Bloomberg 메시지 데이터를 보관 하는 데 필요한 많은 구현 단계는 Microsoft 365 외부에 있으므로, 준수 센터에서 커넥터를 만들기 전에 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-127">Many of the implementation steps required to archive Bloomberg Message data are external to Microsoft 365 and must be completed before you can create the connector in the compliance center.</span></span>

- <span data-ttu-id="ef9c8-128">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-128">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="ef9c8-129">이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-129">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span> <span data-ttu-id="ef9c8-130">3 단계에서 Bloomberg 메시지 커넥터를 성공적으로 만들기 전에이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-130">You have to complete this step before you can successfully create the Bloomberg Message connector in Step 3.</span></span>

- <span data-ttu-id="ef9c8-131">[Bloomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA)를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-131">Subscribe to [Bloomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA).</span></span> <span data-ttu-id="ef9c8-132">이는 Bloomberg Anywhere에 로그인 하 여 설정 하 고 구성 해야 하는 Bloomberg SFTP 사이트에 액세스할 수 있도록 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-132">This is required so that you can log in to Bloomberg Anywhere to access the Bloomberg SFTP site that you have to set up and configure.</span></span>

- <span data-ttu-id="ef9c8-133">Bloomberg SFTP (보안 파일 전송 프로토콜) 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-133">Set up a Bloomberg SFTP (Secure file transfer protocol) site.</span></span> <span data-ttu-id="ef9c8-134">Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후에는 Bloomberg 메시지의 데이터가 매일 SFTP 사이트로 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-134">After working with Bloomberg to set up the SFTP site, data from Bloomberg Message is uploaded to the SFTP site every day.</span></span> <span data-ttu-id="ef9c8-135">2 단계에서 만든 커넥터가이 SFTP 사이트에 연결 되 고 전자 메일 데이터를 Microsoft 365 사서함으로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-135">The connector you create in Step 2 connects to this SFTP site and transfers the email data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="ef9c8-136">또한 SFTP는 전송 프로세스 중에 사서함으로 전송 되는 Bloomberg 메시지 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-136">SFTP also encrypts the Bloomberg Message data that is sent to mailboxes during the transfer process.</span></span>

  <span data-ttu-id="ef9c8-137">Bloomberg SFTP에 대 한 자세한 내용은 *BB-sftp*라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-137">For information about Bloomberg SFTP (also called *BB-SFTP*):</span></span>

  - <span data-ttu-id="ef9c8-138">[Bloomberg 지원](https://www.bloomberg.com/professional/support/documentation/)에서 "SFTP 연결 표준" 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-138">See the "SFTP Connectivity Standards" document at [Bloomberg Support](https://www.bloomberg.com/professional/support/documentation/).</span></span>

  - <span data-ttu-id="ef9c8-139">[Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc)에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-139">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).</span></span>

   > [!NOTE]
   > <span data-ttu-id="ef9c8-140">조직에서 인스턴트 Bloomberg 데이터를 보관 하기 위한 커넥터를 이미 배포한 경우에는 다른 SFTP 사이트를 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-140">If your organization already deployed a connector to archive Instant Bloomberg data, you don't need to set up another SFTP site.</span></span> <span data-ttu-id="ef9c8-141">Bloomberg 메시지 커넥터에 대해 동일한 SFTP 사이트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-141">You can use the same SFTP site for the Bloomberg Message connector.</span></span>

- <span data-ttu-id="ef9c8-142">Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후 Bloomberg에서는 Bloomberg 구현 전자 메일 메시지에 응답 한 후 몇 가지 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-142">After you work with Bloomberg to set up an SFTP site, Bloomberg will provide some information to you after you respond to the Bloomberg implementation email message.</span></span> <span data-ttu-id="ef9c8-143">다음 정보의 복사본을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-143">Save a copy of the following information.</span></span> <span data-ttu-id="ef9c8-144">이 도구를 사용 하 여 3 단계에서 커넥터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-144">You use it to set up a connector in Step 3.</span></span>

  - <span data-ttu-id="ef9c8-145">기업 코드-조직의 ID 이며 Bloomberg SFTP 사이트에 로그인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-145">Firm code, which is an ID for your organization and is used to log in to the Bloomberg SFTP site.</span></span>

  - <span data-ttu-id="ef9c8-146">Bloomberg SFTP 사이트의 암호</span><span class="sxs-lookup"><span data-stu-id="ef9c8-146">Password for your Bloomberg SFTP site</span></span>

  - <span data-ttu-id="ef9c8-147">Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-147">URL for Bloomberg SFTP site (for example, sftp.bloomberg.com).</span></span> <span data-ttu-id="ef9c8-148">또한 Bloomberg는 커넥터를 설정 하는 데 사용할 수 있는 Bloomberg SFTP 사이트에 해당 하는 IP 주소를 제공할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-148">In addition, Bloomberg may also provide a corresponding IP address for the Bloomberg SFTP site, which also can be used to set up the connector.</span></span>

  - <span data-ttu-id="ef9c8-149">Bloomberg SFTP 사이트의 포트 번호</span><span class="sxs-lookup"><span data-stu-id="ef9c8-149">Port number for Bloomberg SFTP site</span></span>

- <span data-ttu-id="ef9c8-150">3 단계에서 Bloomberg 메시지 커넥터를 만들고 1 단계에서 공개 키와 IP 주소를 다운로드 하는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-150">The user who creates a Bloomberg Message connector in Step 3 (and who downloads the public keys and IP address in Step 1) must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="ef9c8-151">이는 Microsoft 365 준수 센터의 **데이터 커넥터** 페이지에서 커넥터를 추가 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-151">This is required to add connectors in the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ef9c8-152">기본적으로이 역할은 Exchange Online의 어떤 역할 그룹에도 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-152">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="ef9c8-153">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-153">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="ef9c8-154">또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-154">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="ef9c8-155">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-155">For more information, see the [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>


## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a><span data-ttu-id="ef9c8-156">1 단계: SSH 및 PGP 공개 키 획득</span><span class="sxs-lookup"><span data-stu-id="ef9c8-156">Step 1: Obtain SSH and PGP public keys</span></span>

<span data-ttu-id="ef9c8-157">첫 번째 단계는 SSH (Secure Shell) 용 공개 키와 PGP (매우 좋은 개인 정보)의 복사본을 가져오는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-157">The first step is to obtain a copy of the public keys for Secure Shell (SSH) and Pretty Good Privacy (PGP).</span></span> <span data-ttu-id="ef9c8-158">2 단계에서 이러한 키를 사용 하 여 3 단계에서 만든 커넥터에서 SFTP 사이트에 연결 하 고 Bloomberg 메시지 전자 메일 데이터를 Microsoft 365 사서함으로 전송 하도록 Bloomberg SFTP 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-158">You use these keys in Step 2 to configure the Bloomberg SFTP site to allow the connector (that you create in Step 3) to connect to the SFTP site and transfer the Bloomberg Message email data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="ef9c8-159">또한 Bloomberg SFTP 사이트를 구성할 때 사용 하는이 단계에서 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-159">You also obtain an IP address in this step, which you use when configuring the Bloomberg SFTP site.</span></span>

1. <span data-ttu-id="ef9c8-160">[]으로 이동 하 https://compliance.microsoft.com\ https://compliance.microsoft.com) 고 왼쪽 탐색 창에서 **데이터 커넥터** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-160">Go to [https://compliance.microsoft.com\](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="ef9c8-161">**데이터 커넥터** 페이지의 **Bloomberg 메시지**에서 **보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-161">On the **Data connectors** page under **Bloomberg Message**, click **View**.</span></span>

3. <span data-ttu-id="ef9c8-162">**Bloomberg 메시지** 제품 설명 페이지에서 **커넥터 추가** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-162">On the **Bloomberg Message** product description page, click **Add connector**</span></span>

4. <span data-ttu-id="ef9c8-163">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-163">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="ef9c8-164">1 단계 아래에 있는 **BLOOMBERG SFTP에 대 한 자격 증명 추가 사이트** 에서 **SSH 키 다운로드**, **PGP 키**다운로드 및 **IP 주소 링크 다운로드** 를 클릭 하 여 각 파일의 복사본을 로컬 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-164">On the **Add credentials for Bloomberg SFTP site** under step 1, click the **Download SSH key**, **Download PGP key**, and **Download IP address** links to save a copy of each file to your local computer.</span></span> <span data-ttu-id="ef9c8-165">이러한 파일에는 2 단계에서 Bloomberg SFTP 사이트를 구성 하는 데 사용 되는 다음과 같은 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-165">These files contain the following items that are used to configure the Bloomberg SFTP site in Step 2:</span></span>

   - <span data-ttu-id="ef9c8-166">SSH 공개 키:이 키는 커넥터가 Bloomberg SFTP 사이트에 연결 될 때 보안 원격 로그인을 사용 하도록 보안 셸 (SSH)을 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-166">SSH public key: This key is used to configure Secure Shell (SSH) to enable a secure remote login when the connector connects to the Bloomberg SFTP site.</span></span>

   - <span data-ttu-id="ef9c8-167">PGP 공개 키:이 키는 Bloomberg SFTP 사이트에서 Microsoft 365로 전송 되는 데이터의 암호화를 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-167">PGP public key: This key is used to configure the encryption of data that's transferred from the Bloomberg SFTP site to Microsoft 365.</span></span>

   - <span data-ttu-id="ef9c8-168">IP 주소: Bloomberg SFTP 사이트는 3 단계에서 만든 Bloomberg 메시지 커넥터에서 사용 하는이 IP 주소 로부터의 연결 요청만 수락 하도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-168">IP address: The Bloomberg SFTP site is configured to accept a connection request only from this IP address, which is used by the Bloomberg Message connector that you create in Step 3.</span></span>

6. <span data-ttu-id="ef9c8-169">**취소** 를 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-169">Click **Cancel** to close the wizard.</span></span> <span data-ttu-id="ef9c8-170">3 단계의이 마법사로 돌아와서 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-170">You come back to this wizard in Step 3 to create the connector.</span></span>

## <a name="step-2-configure-the-bloomberg-sftp-site"></a><span data-ttu-id="ef9c8-171">2 단계: Bloomberg SFTP 사이트 구성</span><span class="sxs-lookup"><span data-stu-id="ef9c8-171">Step 2: Configure the Bloomberg SFTP site</span></span>

> [!NOTE]
> <span data-ttu-id="ef9c8-172">앞에서 설명한 것 처럼 조직에서 이전에 Bloomberg SFTP 사이트를 설정 하 여 인스턴트 Bloomberg 데이터를 보관 하는 경우에는 다른 것을 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-172">As previously stated, if you're organization has previously set up a Bloomberg SFTP site to archive Instant Bloomberg data, you don't have to set up another one.</span></span> <span data-ttu-id="ef9c8-173">3 단계에서 커넥터를 만들 때 동일한 SFTP 사이트를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-173">You can specify the same SFTP site when you create the connector in Step 3.</span></span>

<span data-ttu-id="ef9c8-174">다음 단계에서는 1 단계에서 가져온 SSH 및 PGP 공개 키와 IP 주소를 사용 하 여 Bloomberg SFTP 사이트에 대 한 SSH 인증 및 PGP 암호화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-174">The next step is to use the SSH and PGP public keys and the IP address that you obtained in Step 1 to configure SSH authentication and PGP encryption for the Bloomberg SFTP site.</span></span> <span data-ttu-id="ef9c8-175">이렇게 하면 3 단계에서 만든 Bloomberg 메시지 커넥터가 Bloomberg SFTP 사이트에 연결 하 고 Bloomberg 메시지 데이터를 Microsoft 365로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-175">This lets the Bloomberg Message connector that you create in Step 3 connect to the Bloomberg SFTP site and transfer Bloomberg Message data to Microsoft 365.</span></span> <span data-ttu-id="ef9c8-176">Bloomberg SFTP 사이트를 설정 하려면 Bloomberg 고객 지원 서비스를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-176">You need to work with Bloomberg customer support to set up your Bloomberg SFTP site.</span></span> <span data-ttu-id="ef9c8-177">지원 [Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) 에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-177">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) for assistance.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef9c8-178">Bloomberg에서는 1 단계에서 다운로드 한 세 개의 파일을 전자 메일 메시지에 첨부 하 고이를 사용 하 여 Bloomberg SFTP 사이트를 설정 하는 경우 해당 문서를 고객 지원 팀으로 전송 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-178">Bloomberg recommends that you attach the three files that you downloaded in Step 1 to an email message and send it to their customer support team when working with them to set up your Bloomberg SFTP site.</span></span>

## <a name="step-3-create-a-bloomberg-message-connector"></a><span data-ttu-id="ef9c8-179">3 단계: Bloomberg 메시지 커넥터 만들기</span><span class="sxs-lookup"><span data-stu-id="ef9c8-179">Step 3: Create a Bloomberg Message connector</span></span>

<span data-ttu-id="ef9c8-180">마지막 단계는 Microsoft 365 준수 센터에서 Bloomberg 메시지 커넥터를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-180">The last step is to create a Bloomberg Message connector in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="ef9c8-181">커넥터는 제공 하는 정보를 사용 하 여 Bloomberg SFTP 사이트에 연결 하 고 전자 메일 메시지를 Microsoft 365의 해당 사용자 사서함 상자로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-181">The connector uses the information you provide to connect to the Bloomberg SFTP site and transfer email messages to the corresponding user mailbox boxes in Microsoft 365.</span></span>

1. <span data-ttu-id="ef9c8-182">으로 이동 하 여 [https://compliance.microsoft.com](https://compliance.microsoft.com) 왼쪽 탐색 창에서 **데이터 커넥터** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-182">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="ef9c8-183">**데이터 커넥터** 페이지의 **Bloomberg 메시지**에서 **보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-183">On the **Data connectors** page under **Bloomberg Message**, click **View**.</span></span>

3. <span data-ttu-id="ef9c8-184">**Bloomberg 메시지** 제품 설명 페이지에서 **커넥터 추가** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-184">On the **Bloomberg Message** product description page, click **Add connector**</span></span>

4. <span data-ttu-id="ef9c8-185">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-185">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="ef9c8-186">**BLOOMBERG SFTP 사이트에 대 한 자격 증명 추가** 페이지의 3 단계에서 다음 상자에 필요한 정보를 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-186">On the **Add credentials for Bloomberg SFTP site** page, under Step 3, enter the required information in the following boxes and then click **Next**.</span></span>

      - <span data-ttu-id="ef9c8-187">**회사 코드:** Bloomberg SFTP 사이트의 사용자 이름으로 사용 되는 조직의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-187">**Firm code:** The ID for your organization that is used as the username for the Bloomberg SFTP site.</span></span>

      - <span data-ttu-id="ef9c8-188">**암호:** 조직의 Bloomberg SFTP 사이트에 대 한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-188">**Password:** The password for your organization's Bloomberg SFTP site.</span></span>

      - <span data-ttu-id="ef9c8-189">**SFTP URL:** Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-189">**SFTP URL:** The URL for the Bloomberg SFTP site (for example, sftp.bloomberg.com).</span></span>

      - <span data-ttu-id="ef9c8-190">**SFTP 포트:** Bloomberg SFTP 사이트의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-190">**SFTP port:** The port number for the Bloomberg SFTP site.</span></span> <span data-ttu-id="ef9c8-191">커넥터는이 포트를 사용 하 여 SFTP 사이트에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-191">The connector uses this port to connect to the SFTP site.</span></span>

6. <span data-ttu-id="ef9c8-192">**사용자 매핑** 페이지에서 자동 사용자 매핑을 사용 하도록 설정 하 고 필요에 따라 사용자 지정 사용자 매핑을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-192">On the **User-mapping** page, enable automatic user mapping and provide custom user mapping as required</span></span>

7. <span data-ttu-id="ef9c8-193">**다음**을 클릭 하 고 설정을 검토 한 다음 준비를 클릭 하 여 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-193">Click **Next**, review your settings, and then click prepare to create the connector.</span></span>

8. <span data-ttu-id="ef9c8-194">**데이터 커넥터** 페이지로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-194">Go to the **Data connectors** page to see the progress of the import process for the new connector.</span></span>

## <a name="known-issues"></a><span data-ttu-id="ef9c8-195">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="ef9c8-195">Known issues</span></span>

- <span data-ttu-id="ef9c8-196">Microsoft 365로 가져온 Bloomberg 메시지의 스레딩은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-196">Threading of Bloomberg Message email imported to Microsoft 365 isn't supported.</span></span> <span data-ttu-id="ef9c8-197">사용자에 게 전송 된 개별 메시지는 가져오지만, 스레드 대화에서는 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-197">Individual messages sent to a person are imported, but they aren't presented in a threaded conversation.</span></span> <span data-ttu-id="ef9c8-198">Microsoft는 Bloomberg Message data connector의 이후 버전에서 스레딩을 지원 하기 위해 노력 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-198">Microsoft is working to support threading in later versions of the Bloomberg Message data connector.</span></span>