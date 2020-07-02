---
title: 얼음 채팅 데이터를 보관 하는 커넥터 설정
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
description: 관리자는 아이스크림 채팅 도구에서 Microsoft 365로 데이터를 가져오고 보관 하기 위한 커넥터를 설정할 수 있습니다. 이를 통해 Microsoft 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리할 수도 있습니다.
ms.openlocfilehash: c4abcc6b3ba8778616e4a9bf72955a6b6c959cd1
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937355"
---
# <a name="set-up-a-connector-to-archive-ice-chat-data-preview"></a><span data-ttu-id="e70ca-104">얼음 채팅 데이터를 보관 하는 커넥터 설정 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="e70ca-104">Set up a connector to archive ICE Chat data (preview)</span></span>

<span data-ttu-id="e70ca-105">Microsoft 365 준수 센터의 네이티브 커넥터를 사용 하 여 ICE Chat 공동 작업 도구에서 금융 서비스 채팅 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-105">Use a native connector in the Microsoft 365 compliance center to import and archive financial services chat data from the ICE Chat collaboration tool.</span></span> <span data-ttu-id="e70ca-106">커넥터를 설정 하 고 구성한 후에는 조직의 ICE (채팅 보안 FTP) 사이트를 매일 한 번씩 연결 하 고 채팅 메시지의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음 해당 항목을 Microsoft 365의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-106">After you set up and configure a connector, it connects to your organization's ICE Chat secure FTP (SFTP) site once every day, converts the content of chat messages to an email message format, and then import those items to mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="e70ca-107">사용자 사서함에 ICE 채팅 데이터가 저장 된 후에는 소송 보존, eDiscovery, 보관, 감사, 통신 준수 및 Microsoft 365 고정 정책과 같은 Microsoft 365 준수 기능을 ICE 채팅 데이터에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-107">After ICE chat data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as litigation hold, eDiscovery, archiving, auditing, communication compliance, and Microsoft 365 retention policies to ICE Chat data.</span></span> <span data-ttu-id="e70ca-108">예를 들어 콘텐츠 검색을 사용 하 여 ICE 채팅 메시지를 검색 하거나, 고급 eDiscovery 사례에서 얼음 채팅 데이터를 포함 하는 사서함을 custodian에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-108">For example, you can search ICE Chat messages using content search or associate the mailbox that contains the ICE Chat data with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="e70ca-109">아이스크림 채팅 커넥터를 사용 하 여 Microsoft 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-109">Using an ICE Chat connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-ice-chat-data"></a><span data-ttu-id="e70ca-110">ICE 채팅 데이터 보관 개요</span><span class="sxs-lookup"><span data-stu-id="e70ca-110">Overview of archiving ICE Chat data</span></span>

<span data-ttu-id="e70ca-111">다음 개요에서는 커넥터를 사용 하 여 Microsoft 365에서 ICE 채팅 데이터를 보관 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-111">The following overview explains the process of using a connector to archive ICE chat data in Microsoft 365.</span></span>

![아이스 채팅 보관 워크플로](../media/ICEChatConnectorWorkflow.png)

1. <span data-ttu-id="e70ca-113">조직에서 얼음 채팅을 사용 하 여 아이스 채팅 SFTP 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-113">Your organization works with ICE Chat to set up an ICE Chat SFTP site.</span></span> <span data-ttu-id="e70ca-114">또한 얼음 채팅을 사용 하 여 온 얼음 채팅을 구성 하 여 얼음 채팅 SFTP 사이트로 채팅 메시지를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-114">You'll also work with ICE Chat to configure ICE Chat to copy chat messages to your ICE Chat SFTP site.</span></span>

2. <span data-ttu-id="e70ca-115">24 시간 마다 한 번씩 얼음 채팅의 채팅 메시지가 ICE Chat SFTP 사이트로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-115">Once every 24 hours, chat messages from ICE Chat are copied to your ICE Chat SFTP site.</span></span>

3. <span data-ttu-id="e70ca-116">Microsoft 365 준수 센터에서 만드는 아이스크림 채팅 커넥터는 매일 ICE 채팅 SFTP 사이트에 연결 하 고 이전 24 시간에서 Microsoft 클라우드의 안전한 Azure Storage 위치로 채팅 메시지를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-116">The ICE Chat connector that you create in the Microsoft 365 compliance center connects to the ICE Chat SFTP site every day and transfers the chat messages from the previous 24 hours to a secure Azure Storage location in the Microsoft Cloud.</span></span> <span data-ttu-id="e70ca-117">또한이 커넥터는 채팅 massage의 콘텐츠를 전자 메일 메시지 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-117">The connector also converts the content of a chat massage to an email message format.</span></span>

4. <span data-ttu-id="e70ca-118">커넥터는 채팅 메시지 항목을 특정 사용자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-118">The connector imports chat message items to the mailboxes of specific users.</span></span> <span data-ttu-id="e70ca-119">그러면 사용자 사서함에 **ICE chat** 라는 새 폴더가 만들어지고 채팅 메시지 항목을 해당 폴더로 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-119">A new folder named **ICE Chat** will be created in the user mailboxes and the chat message items will be imported to that folder.</span></span> <span data-ttu-id="e70ca-120">커넥터는 *SenderEmail* 및 *RecipientEmail* 속성 값을 사용 하 여 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-120">The connector does by using the value of the *SenderEmail* and *RecipientEmail* properties.</span></span> <span data-ttu-id="e70ca-121">모든 채팅 메시지에는 보낸 사람의 전자 메일 주소와 채팅 메시지의 모든 받는 사람/참가자가 채워지는 이러한 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-121">Every chat message contains these properties, which are populated with email address of the sender and every recipient/participant of the chat message.</span></span>

   <span data-ttu-id="e70ca-122">*SenderEmail* 및 *RecipientEmail* 속성의 값을 사용 하는 자동 사용자 매핑 외에, 즉 커넥터가 보낸 사람의 사서함 및 모든 받는 사람의 사서함으로 채팅 메시지를 가져오지만, CSV 매핑 파일을 업로드 하 여 사용자 지정 user mapping을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-122">In addition to automatic user mapping that uses the values of the *SenderEmail* and *RecipientEmail* property (which means that the connector imports a chat message to the sender's mailbox and the mailboxes of every recipient), you can also define custom user mapping by uploading a CSV mapping file.</span></span> <span data-ttu-id="e70ca-123">이 매핑 파일에는 조직의 모든 사용자에 대 한 ICE 채팅 *Imid* 와 해당 Microsoft 365 사서함 주소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-123">This mapping file contains the ICE Chat *ImId* and the corresponding Microsoft 365 mailbox address for every user in your organization.</span></span> <span data-ttu-id="e70ca-124">자동 사용자 매핑을 사용 하도록 설정 하 고 사용자 지정 매핑 파일을 제공 하는 경우 모든 채팅 항목에 대해 커넥터는 먼저 사용자 지정 매핑 파일을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-124">If you enable automatic user mapping and provide a custom-mapping file, for every chat item the connector will first look at the custom-mapping file.</span></span> <span data-ttu-id="e70ca-125">사용자의 아이스크림 채팅 ImId에 해당 하는 유효한 Microsoft 365 사용자 계정을 찾지 못하면 커넥터는 채팅 항목의 *SenderEmail* 및 *RecipientEmail* 속성을 사용 하 여 해당 항목을 채팅 참가자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-125">If it doesn't find a valid Microsoft 365 user account that corresponds to a user's ICE Chat ImId, the connector will use the *SenderEmail* and *RecipientEmail* properties of the chat item to import the item to the mailboxes of the chat participants.</span></span> <span data-ttu-id="e70ca-126">커넥터가 사용자 지정 매핑 파일 또는 *SenderEmail* 및 *RecipientEmail* 속성에서 유효한 Microsoft 365 사용자를 찾지 못하면 항목을 가져오지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-126">If the connector doesn't find a valid Microsoft 365 user in either the custom-mapping file or the *SenderEmail* and *RecipientEmail* properties, the item won't be imported.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e70ca-127">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="e70ca-127">Before you begin</span></span>

<span data-ttu-id="e70ca-128">ICE 채팅 데이터를 보관 하는 데 필요한 여러 구현 단계는 Microsoft 365 외부에 있으므로, 준수 센터에서 커넥터를 만들기 전에 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-128">Many of the implementation steps required to archive ICE Chat data are external to Microsoft 365 and must be completed before you can create the connector in the compliance center.</span></span>

- <span data-ttu-id="e70ca-129">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-129">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="e70ca-130">이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-130">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span> <span data-ttu-id="e70ca-131">3 단계에서 ICE 채팅 커넥터를 성공적으로 만들기 전에이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-131">You must complete this step before you can successfully create the ICE Chat connector in Step 3.</span></span>

- <span data-ttu-id="e70ca-132">얼음 채팅 비용 외부 규정 준수에 대 한 요금입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-132">ICE Chat charges their customers a fee for external compliance.</span></span> <span data-ttu-id="e70ca-133">조직에서는 아이스크림 채팅 판매 그룹에 문의 하 여 토론 하 고, 온 ICE Chat data services 계약에 서명 하 고,이에 대 한 정보를 수집 합니다 [https://www.theice.com/publicdocs/agreements/ICE\_Data\_Services\_Agreement.pdf](https://www.theice.com/publicdocs/agreements/ICE\_Data\_Services\_Agreement.pdf) .</span><span class="sxs-lookup"><span data-stu-id="e70ca-133">Your organization should contact the ICE Chat sales group to discuss, and to sign the ICE Chat data services agreement, which you can obtain at [https://www.theice.com/publicdocs/agreements/ICE\_Data\_Services\_Agreement.pdf](https://www.theice.com/publicdocs/agreements/ICE\_Data\_Services\_Agreement.pdf).</span></span> <span data-ttu-id="e70ca-134">이 계약은 얼음 채팅 및 조직 간의 것 이며 Microsoft와 관련이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-134">This agreement is between ICE Chat and your organization and does not involve Microsoft.</span></span> <span data-ttu-id="e70ca-135">2 단계에서 ICE 채팅 SFTP 사이트를 설정한 후에는 아이스크림 채팅에서 FTP 자격 증명을 조직에 직접 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-135">After you set up an ICE Chat SFTP site in Step 2, ICE Chat provides the FTP credentials directly to your organization.</span></span> <span data-ttu-id="e70ca-136">그런 다음 3 단계에서 커넥터를 설정할 때 이러한 자격 증명을 Microsoft에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-136">Then you who would provide those credentials to Microsoft when setting up the connector in Step 3.</span></span>

- <span data-ttu-id="e70ca-137">3 단계에서 커넥터를 만들기 전에 ICE Chat SFTP 사이트를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-137">You must set up an ICE Chat SFTP site before creating the connector in Step 3.</span></span> <span data-ttu-id="e70ca-138">ICE 채팅을 사용 하 여 SFTP 사이트를 설정한 후에는 아이스크림 채팅에서 데이터를 매일 SFTP 사이트로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-138">After working with ICE Chat to set up the SFTP site, data from ICE Chat is uploaded to the SFTP site every day.</span></span> <span data-ttu-id="e70ca-139">3 단계에서 만든 커넥터가이 SFTP 사이트에 연결 되 고 채팅 데이터를 Microsoft 365 사서함으로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-139">The connector you create in Step 3 connects to this SFTP site and transfers the chat data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="e70ca-140">또한 SFTP는 전송 프로세스 중에 사서함으로 전송 되는 ICE 채팅 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-140">SFTP also encrypts the ICE Chat data that's sent to mailboxes during the transfer process.</span></span>

- <span data-ttu-id="e70ca-141">3 단계 및 1 단계에서 공개 키와 IP 주소를 다운로드 하는 관리자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-141">The admin who creates the ICE Chat connector in Step 3 (and who downloads the public keys and IP address in Step 1) must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="e70ca-142">이 역할은 Microsoft 365 준수 센터의 **데이터 커넥터** 페이지에 커넥터를 추가 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-142">This role is required to add connectors on the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="e70ca-143">기본적으로이 역할은 Exchange Online의 어떤 역할 그룹에도 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-143">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="e70ca-144">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-144">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="e70ca-145">또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-145">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="e70ca-146">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e70ca-146">For more information, see the [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a><span data-ttu-id="e70ca-147">1 단계: SSH 및 PGP 공개 키 획득</span><span class="sxs-lookup"><span data-stu-id="e70ca-147">Step 1: Obtain SSH and PGP public keys</span></span>

<span data-ttu-id="e70ca-148">첫 번째 단계는 SSH (Secure Shell) 용 공개 키와 PGP (매우 좋은 개인 정보)의 복사본을 가져오는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-148">The first step is to obtain a copy of the public keys for Secure Shell (SSH) and Pretty Good Privacy (PGP).</span></span> <span data-ttu-id="e70ca-149">2 단계에서 이러한 키를 사용 하 여 3 단계에서 만든 커넥터에서 SFTP 사이트에 연결 하 고 아이스크림 채팅 데이터를 Microsoft 365 사서함으로 전송 하도록 ICE Chat SFTP 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-149">You use these keys in Step 2 to configure the ICE Chat SFTP site to allow the connector (that you create in Step 3) to connect to the SFTP site and transfer the ICE Chat data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="e70ca-150">또한이 단계에서 ICE Chat SFTP 사이트를 구성할 때 사용 하는 IP 주소도 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-150">You will also obtain an IP address in this step, which you use when configuring the ICE Chat SFTP site.</span></span>

1. <span data-ttu-id="e70ca-151">으로 이동 하 여 [https://compliance.microsoft.com](https://compliance.microsoft.com) 왼쪽 탐색 창에서 **데이터 커넥터** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-151">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="e70ca-152">**데이터 연결선 (미리 보기)** 페이지의 **ICE Chat**에서 **보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-152">On the **Data connectors (preview)** page under **ICE Chat**, click **View**.</span></span>

3. <span data-ttu-id="e70ca-153">**ICE 채팅** 페이지에서 **커넥터 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-153">On the **ICE Chat** page, click **Add connector**.</span></span>

4. <span data-ttu-id="e70ca-154">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-154">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="e70ca-155">1 단계 아래에 있는 **ICE CHAT SFTP 사이트의 자격 증명 추가** 페이지에서 **다운로드 SSH 키**, **PGP 키 다운로드**및 **IP 주소 링크 다운로드** 를 클릭 하 여 각 파일의 복사본을 로컬 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-155">On the **Add credentials for ICE Chat SFTP site** page under step 1, click the **Download SSH key**, **Download PGP key**, and **Download IP address** links to save a copy of each file to your local computer.</span></span> <span data-ttu-id="e70ca-156">이러한 파일에는 2 단계에서 ICE Chat SFTP 사이트를 구성 하는 데 사용 되는 다음 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-156">These files contain the following items that are used to configure the ICE Chat SFTP site in Step 2:</span></span>

   - <span data-ttu-id="e70ca-157">SSH 공개 키:이 키는 커넥터가 ICE Chat SFTP 사이트에 연결할 때 보안 원격 로그인을 사용 하도록 보안 SSH를 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-157">SSH public key: This key is used to configure Secure SSH to enable a secure remote login when the connector connects to the ICE Chat SFTP site.</span></span>

   - <span data-ttu-id="e70ca-158">PGP 공개 키:이 키는 ICE Chat SFTP 사이트에서 Microsoft 365로 전송 되는 데이터의 암호화를 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-158">PGP public key: This key is used to configure the encryption of data that's transferred from the ICE Chat SFTP site to Microsoft 365.</span></span>

   - <span data-ttu-id="e70ca-159">IP 주소: ICE Chat SFTP 사이트는 3 단계에서 만든 ICE 채팅 커넥터에서 사용 하는이 IP 주소 로부터의 연결 요청만 수락 하도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-159">IP address: The ICE Chat SFTP site is configured to accept a connection request only from this IP address, which is used by the ICE Chat connector that you create in Step 3.</span></span>

6. <span data-ttu-id="e70ca-160">**취소** 를 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-160">Click **Cancel** to close the wizard.</span></span> <span data-ttu-id="e70ca-161">3 단계의이 마법사로 돌아와서 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-161">You come back to this wizard in Step 3 to create the connector.</span></span>

## <a name="step-2-configure-the-ice-chat-sftp-site"></a><span data-ttu-id="e70ca-162">2 단계: ICE Chat SFTP 사이트 구성</span><span class="sxs-lookup"><span data-stu-id="e70ca-162">Step 2: Configure the ICE Chat SFTP site</span></span>

<span data-ttu-id="e70ca-163">다음 단계에서는 1 단계에서 가져온 SSH 및 PGP 공개 키와 IP 주소를 사용 하 여 아이스크림 채팅 SFTP 사이트에 대 한 SSH 인증 및 PGP 암호화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-163">The next step is to use the SSH and PGP public keys and the IP address that you obtained in Step 1 to configure SSH authentication and PGP encryption for the ICE Chat SFTP site.</span></span> <span data-ttu-id="e70ca-164">이렇게 하면 3 단계에서 만든 얼음 채팅 커넥터가 ICE chat SFTP 사이트에 연결 하 고, ICE 채팅 데이터를 Microsoft 365로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-164">This lets the ICE Chat connector that you create in Step 3 connect to the ICE Chat SFTP site and transfer ICE Chat data to Microsoft 365.</span></span> <span data-ttu-id="e70ca-165">Ice 채팅 SFTP 사이트를 설정 하려면 ICE Chat customer 지원 서비스를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-165">You need to work with ICE Chat customer support to set up your ICE Chat SFTP site.</span></span>

## <a name="step-3-create-an-ice-chat-connector"></a><span data-ttu-id="e70ca-166">3 단계: ICE 채팅 커넥터 만들기</span><span class="sxs-lookup"><span data-stu-id="e70ca-166">Step 3: Create an ICE Chat connector</span></span>

<span data-ttu-id="e70ca-167">마지막 단계는 Microsoft 365 준수 센터에서 ICE 채팅 커넥터를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-167">The last step is to create an ICE Chat connector in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="e70ca-168">커넥터는 사용자가 제공 하는 정보를 사용 하 여 ICE Chat SFTP 사이트에 연결 하 고 채팅 메시지를 Microsoft 365의 해당 사서함 상자로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-168">The connector uses the information you provide to connect to the ICE Chat SFTP site and transfer chat messages to the corresponding user mailbox boxes in Microsoft 365.</span></span>

1. <span data-ttu-id="e70ca-169">으로 이동 하 여 [https://compliance.microsoft.com](https://compliance.microsoft.com) 왼쪽 탐색 창에서 **데이터 커넥터** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-169">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="e70ca-170">**데이터 커넥터** 페이지의 **ICE Chat**에서 **보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-170">On the **Data connectors** page under **ICE Chat**, click **View**.</span></span>

3. <span data-ttu-id="e70ca-171">**ICE 채팅** 페이지에서 **커넥터 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-171">On the **ICE Chat** page, click **Add connector**.</span></span>

4. <span data-ttu-id="e70ca-172">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-172">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="e70ca-173">**ICE CHAT SFTP 사이트에 대 한 자격 증명 추가** 페이지의 3 단계에서 다음 상자에 필요한 정보를 입력 한 다음 **연결 유효성 검사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-173">On the **Add credentials for ICE Chat SFTP site** page, under Step 3, enter the required information in the following boxes and then click **Validate connection**.</span></span>

   - <span data-ttu-id="e70ca-174">**회사 코드:** ICE Chat SFTP 사이트의 사용자 이름으로 사용 되는 조직의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-174">**Firm code:** The ID for your organization, which is used as the username for the ICE Chat SFTP site.</span></span>

   - <span data-ttu-id="e70ca-175">**암호:** ICE Chat SFTP 사이트의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-175">**Password:** The password for your ICE Chat SFTP site.</span></span>

   - <span data-ttu-id="e70ca-176">**SFTP URL:** ICE Chat SFTP 사이트의 URL (예: sftp.theice.com)입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-176">**SFTP URL:** The URL for the ICE Chat SFTP site (for example, sftp.theice.com).</span></span>

   - <span data-ttu-id="e70ca-177">**SFTP 포트:** ICE Chat SFTP 사이트의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-177">**SFTP port:** The port number for the ICE Chat SFTP site.</span></span> <span data-ttu-id="e70ca-178">커넥터는이 포트를 사용 하 여 SFTP 사이트에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-178">The connector uses this port to connect to the SFTP site.</span></span>

6. <span data-ttu-id="e70ca-179">연결을 확인 한 후에 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-179">After the connection is validated, click **Next**.</span></span>

7. <span data-ttu-id="e70ca-180">**Microsoft 365 사용자에 게 외부 사용자** 매핑 페이지에서 자동 사용자 매핑을 사용 하도록 설정 하 고 필요에 따라 사용자 지정 사용자 매핑을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-180">On the **Map external users to Microsoft 365 users** page, enable automatic user mapping and provide custom user mapping as required.</span></span> <span data-ttu-id="e70ca-181">이 페이지에서는 사용자 매핑 CSV 파일의 복사본을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-181">You can download a copy of the user-mapping CSV file on this page.</span></span> <span data-ttu-id="e70ca-182">파일에 사용자 매핑을 추가한 다음 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-182">You can add the user mappings to the file and then upload it.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e70ca-183">앞에서 설명한 것 처럼 사용자 지정 매핑 파일 CSV 파일에는 각 사용자에 대 한 ICE 채팅 imid와 해당 Microsoft 365 사서함 주소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-183">As previously explained, custom mapping file CSV file contains the ICE Chat imid and corresponding Microsoft 365 mailbox address for each user.</span></span> <span data-ttu-id="e70ca-184">자동 사용자 매핑을 사용 하도록 설정 하 고 사용자 지정 매핑을 제공 하는 경우 모든 채팅 항목에 대해 커넥터는 먼저 사용자 지정 매핑 파일을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-184">If you enable automatic user mapping and provide a custom mapping, for every chat item, the connector will first look at custom mapping file.</span></span> <span data-ttu-id="e70ca-185">사용자의 아이스크림 채팅 imid에 해당 하는 유효한 Microsoft 365 사용자를 찾지 못하면 커넥터는 채팅 항목의 *SenderEmail* 및 *RecipientEmail* 속성에 지정 된 사용자의 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-185">If it doesn't find a valid Microsoft 365 user that corresponds to a user's ICE Chat imid, the connector will import the item to the mailboxes for the users specified in the *SenderEmail* and *RecipientEmail* properties of the chat item.</span></span> <span data-ttu-id="e70ca-186">커넥터가 자동 또는 사용자 지정 사용자 매핑으로 유효한 Microsoft 365 사용자를 찾지 못하면 항목을 가져오지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-186">If the connector doesn't find a valid Microsoft 365 user by either automatic or custom user mapping, the item won't be imported.</span></span>

8. <span data-ttu-id="e70ca-187">**다음**을 클릭 하 고 설정을 검토 한 다음 **마침을** 클릭 하 여 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-187">Click **Next**, review your settings, and then click **Finish** to create the connector.</span></span>

9. <span data-ttu-id="e70ca-188">**데이터 커넥터** 페이지로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e70ca-188">Go to the **Data connectors** page to see the progress of the import process for the new connector.</span></span>