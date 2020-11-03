---
title: Microsoft 365에서 Jive 데이터를 보관 하는 커넥터 설정
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 Microsoft 365에서 Globanet의 Jive 데이터를 가져오고 보관 하기 위한 커넥터를 설정할 수 있습니다. 이 커넥터를 사용 하면 Microsoft 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 통해 조직의 타사 데이터를 관리 하는 데 도움이 됩니다.
ms.openlocfilehash: 9017e6a7e26c823243abe188328cf62a22ea91c6
ms.sourcegitcommit: 3c39866865c8c61bce2169818d8551da65033cfe
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2020
ms.locfileid: "48816561"
---
# <a name="set-up-a-connector-to-archive-jive-data"></a><span data-ttu-id="7eaae-104">Jive 데이터를 보관 하는 커넥터 설정</span><span class="sxs-lookup"><span data-stu-id="7eaae-104">Set up a connector to archive Jive data</span></span>

<span data-ttu-id="7eaae-105">Microsoft 365 준수 센터의 Globanet 커넥터를 사용 하 여 공동 작업 플랫폼에서 Microsoft 365 조직의 사용자 사서함으로 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-105">Use a Globanet connector in the Microsoft 365 compliance center to import and archive data from the collaboration platform to user mailboxes in your Microsoft 365 organization.</span></span> <span data-ttu-id="7eaae-106">Globanet는 타사 데이터 원본의 항목을 정기적으로 캡처하여 해당 항목을 Microsoft 365로 가져오는 구성 된 [Jive](https://globanet.com/jive/) 커넥터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-106">Globanet provides a [Jive](https://globanet.com/jive/) connector that is configured to capture items from the third-party data source (on a regular basis) and then import those items to Microsoft 365.</span></span> <span data-ttu-id="7eaae-107">커넥터는 전자 메일 메시지, 채팅, 첨부 파일 등의 콘텐츠를 사용자의 Jive 계정에서 전자 메일 메시지 형식으로 변환한 다음 Microsoft 365에서 해당 항목을 사용자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-107">The connector converts content such as email messages, chats, and attachments from a user's Jive account to an email message format and then imports those items to the user's mailbox in Microsoft 365.</span></span>

<span data-ttu-id="7eaae-108">Jive 데이터가 사용자 사서함에 저장 되 면 소송 보존, eDiscovery, 보존 정책 및 보존 레이블과 통신 준수와 같은 Microsoft 365 준수 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-108">After Jive data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, retention policies and retention labels, and communication compliance.</span></span> <span data-ttu-id="7eaae-109">Jive 커넥터를 사용 하 여 Microsoft 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-109">Using a Jive connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-jive-data"></a><span data-ttu-id="7eaae-110">Jive 데이터 보관 개요</span><span class="sxs-lookup"><span data-stu-id="7eaae-110">Overview of archiving Jive data</span></span>

<span data-ttu-id="7eaae-111">다음 개요에서는 커넥터를 사용 하 여 Microsoft 365에서 Jive 데이터를 보관 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-111">The following overview explains the process of using a connector to archive the Jive data in Microsoft 365.</span></span>

![Jive 데이터에 대 한 보관 워크플로](../media/JiveConnectorWorkflow.png)

1. <span data-ttu-id="7eaae-113">조직에서 jive를 사용 하 여 Jive 사이트를 설정 및 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-113">Your organization works with Jive to set up and configure a Jive site.</span></span>

2. <span data-ttu-id="7eaae-114">24 시간 마다 한 번 Jive의 항목이 Globanet Merge1 사이트에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-114">Once every 24 hours, items from Jive are copied to the Globanet Merge1 site.</span></span> <span data-ttu-id="7eaae-115">또한이 커넥터는 Jive 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-115">The connector also converts the content of Jive items to an email message format.</span></span>

3. <span data-ttu-id="7eaae-116">Microsoft 365 준수 센터에서 만드는 Jive 커넥터는 매일 Globanet Merge1 site에 연결 하 고 콘텐츠를 Microsoft 클라우드의 안전한 Azure Storage 위치로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-116">The Jive connector that you create in the Microsoft 365 compliance center connects to the Globanet Merge1 site every day and transfers the content to a secure Azure Storage location in the Microsoft cloud.</span></span>

4. <span data-ttu-id="7eaae-117">커넥터는 [3 단계](#step-3-map-users-and-complete-the-connector-setup)에서 설명한 대로 자동 사용자 매핑의 *Email* 속성 값을 사용 하 여 변환 된 항목을 특정 사용자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-117">The connector imports the converted items to the mailboxes of specific users by using the value of the *Email* property of the automatic user mapping as described in [Step 3](#step-3-map-users-and-complete-the-connector-setup).</span></span> <span data-ttu-id="7eaae-118">사용자 사서함에 **Jive** 이라는 받은 편지함 폴더의 새 하위 폴더가 만들어지고 해당 폴더로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-118">A new subfolder in the Inbox folder named **Jive** is created in the user mailboxes, and the items are imported to that folder.</span></span> <span data-ttu-id="7eaae-119">커넥터는 *Email* 속성 값을 사용 하 여이를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-119">The connector does this by using the value of the *Email* property.</span></span> <span data-ttu-id="7eaae-120">모든 Jive 항목에는이 속성이 있으며,이 속성은 항목의 모든 참가자의 전자 메일 주소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-120">Every Jive item contains this property, which is populated with the email address of every participant of the item.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="7eaae-121">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="7eaae-121">Before you begin</span></span>

- <span data-ttu-id="7eaae-122">Microsoft 커넥터에 대 한 Globanet Merge1 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-122">Create a Globanet Merge1 account for Microsoft connectors.</span></span> <span data-ttu-id="7eaae-123">이 계정을 만들려면 [globanet 고객 지원](https://globanet.com/ms-connectors-contact/)에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="7eaae-123">To create this account, contact [globanet customer support](https://globanet.com/ms-connectors-contact/).</span></span> <span data-ttu-id="7eaae-124">1 단계에서 커넥터를 만들 때이 계정에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-124">You will sign into this account when you create the connector in Step 1.</span></span>

- <span data-ttu-id="7eaae-125">1 단계에서 Jive 커넥터를 만든 후 3 단계에서 완료 하는 사용자는 Exchange Online의 사서함 가져오기 내보내기 역할에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-125">The user who creates the Jive connector in Step 1 (and completes it in Step 3) must be assigned to the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="7eaae-126">이 역할은 Microsoft 365 준수 센터의 **데이터 커넥터** 페이지에 커넥터를 추가 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-126">This role is required to add connectors on the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="7eaae-127">기본적으로이 역할은 Exchange Online의 역할 그룹에 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-127">By default, this role is not assigned to a role group in Exchange Online.</span></span> <span data-ttu-id="7eaae-128">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-128">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="7eaae-129">또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-129">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="7eaae-130">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7eaae-130">For more information, see the [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-set-up-the-jive-connector"></a><span data-ttu-id="7eaae-131">1 단계: Jive 커넥터 설정</span><span class="sxs-lookup"><span data-stu-id="7eaae-131">Step 1: Set up the Jive connector</span></span>

<span data-ttu-id="7eaae-132">첫 번째 단계는 Microsoft 365 준수 센터의 **데이터 커넥터** 페이지에 액세스 하 여 Jive 데이터에 대 한 커넥터를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-132">The first step is to access to the **Data Connectors** page in the Microsoft 365 compliance center and create a connector for Jive data.</span></span>

1. <span data-ttu-id="7eaae-133">로 이동한 [https://compliance.microsoft.com](https://compliance.microsoft.com/) 후 **데이터 커넥터**  >  **Jive** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-133">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com/) and then click **Data connectors** > **Jive** .</span></span>

2. <span data-ttu-id="7eaae-134">**Jive** 제품 설명 페이지에서 **커넥터 추가** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-134">On the **Jive** product description page, click **Add connector** .</span></span>

3. <span data-ttu-id="7eaae-135">**서비스 약관** 페이지에서 **수락** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-135">On the **Terms of service** page, click **Accept** .</span></span>

4. <span data-ttu-id="7eaae-136">커넥터를 식별 하는 고유한 이름을 입력 한 후 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-136">Enter a unique name that identifies the connector, and then click **Next** .</span></span>

5. <span data-ttu-id="7eaae-137">Merge1 계정에 로그인 하 여 커넥터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-137">Sign in to your Merge1 account to configure the connector.</span></span>

## <a name="step-2-configure-the-jive-connector"></a><span data-ttu-id="7eaae-138">2 단계: Jive 커넥터 구성</span><span class="sxs-lookup"><span data-stu-id="7eaae-138">Step 2: Configure the Jive connector</span></span>

<span data-ttu-id="7eaae-139">두 번째 단계는 Merge1 사이트에서 Jive 커넥터를 구성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-139">The second step is to configure the Jive connector on the Merge1 site.</span></span> <span data-ttu-id="7eaae-140">Jive 커넥터를 구성 하는 방법에 대 한 자세한 내용은 [Merge1 타사 커넥터 사용자 가이드](https://docs.ms.merge1.globanetportal.com/Merge1%20Third-Party%20Connectors%20Jive%20User%20Guide.pdf)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7eaae-140">For information about how to configure the Jive connector, see [Merge1 Third-Party Connectors User Guide](https://docs.ms.merge1.globanetportal.com/Merge1%20Third-Party%20Connectors%20Jive%20User%20Guide.pdf).</span></span>

<span data-ttu-id="7eaae-141">**마침 & 저장** 을 클릭 하면 Microsoft 365 준수 센터의 커넥터 마법사에 있는 **사용자 매핑** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-141">After you click **Save & Finish** , the **User mapping** page in the connector wizard in the Microsoft 365 compliance center is displayed.</span></span>

## <a name="step-3-map-users-and-complete-the-connector-setup"></a><span data-ttu-id="7eaae-142">3 단계: 사용자 매핑 및 커넥터 설정 완료</span><span class="sxs-lookup"><span data-stu-id="7eaae-142">Step 3: Map users and complete the connector setup</span></span>

<span data-ttu-id="7eaae-143">사용자를 매핑하고 Microsoft 365 준수 센터에서 커넥터 설정을 완료 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-143">To map users and complete the connector setup in the Microsoft 365 compliance center, follow the steps below:</span></span>

1. <span data-ttu-id="7eaae-144">**Jive users를 Microsoft 365 사용자에 게 매핑** 페이지에서 자동 사용자 매핑을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-144">On the **Map Jive users to Microsoft 365 users** page, enable automatic user mapping.</span></span> <span data-ttu-id="7eaae-145">Jive 항목에는 조직의 사용자에 대 한 전자 메일 주소를 포함 하는 *email* 이라는 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-145">The Jive items include a property called *Email* , which contains email addresses for users in your organization.</span></span> <span data-ttu-id="7eaae-146">커넥터가이 주소를 Microsoft 365 사용자와 연결할 수 있으면 해당 사용자의 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-146">If the connector can associate this address with a Microsoft 365 user, the items are imported to that user's mailbox.</span></span>

2. <span data-ttu-id="7eaae-147">**관리자 동의** 페이지에서 **동의를 제공** 합니다 .를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-147">On the **Admin Consent** page, click **Provide Consent** .</span></span> <span data-ttu-id="7eaae-148">Microsoft 사이트로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-148">You will be redirected to the Microsoft site.</span></span> <span data-ttu-id="7eaae-149">**수락** 을 클릭 하 여 동의를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-149">Click **Accept** to provide the consent.</span></span>

   <span data-ttu-id="7eaae-150">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-150">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="7eaae-151">관리자의 동의를 제공 하려면 Microsoft 365 전역 관리자의 자격 증명을 사용 하 여 로그인 한 다음 승인 요청을 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-151">To provide admin consent, you must be signed in with the credentials of a Microsoft 365 global admin, and then accept the consent request.</span></span> <span data-ttu-id="7eaae-152">전역 관리자로 로그인 하지 않은 경우 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 이동 하 여 전역 관리자 자격 증명을 사용 하 여 로그인 하 고 요청을 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-152">If you aren't signed in as a global admin, you can go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using global admin credentials to accept the request.</span></span>

3. <span data-ttu-id="7eaae-153">**다음** 을 클릭 하 고 설정을 검토 한 다음 **데이터 커넥터** 페이지로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-153">Click **Next** , review your settings, and go to the **Data connectors** page to see the progress of the import process for the new connector.</span></span>

## <a name="step-4-monitor-the-jive-connector"></a><span data-ttu-id="7eaae-154">4 단계: Jive 커넥터 모니터링</span><span class="sxs-lookup"><span data-stu-id="7eaae-154">Step 4: Monitor the Jive connector</span></span>

<span data-ttu-id="7eaae-155">Jive 커넥터를 만든 후에는 Microsoft 365 준수 센터에서 커넥터 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-155">After you create the Jive connector, you can view the connector status in the Microsoft 365 compliance center.</span></span>

1. <span data-ttu-id="7eaae-156">으로 이동 하 여 [https://compliance.microsoft.com](https://compliance.microsoft.com) 왼쪽 탐색 창에서 **데이터 커넥터** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-156">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="7eaae-157">**연결선** 탭을 클릭 한 다음 **Jive** 연결선을 선택 하 여 플라이 아웃 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-157">Click the **Connectors** tab and then select the **Jive** connector to display the flyout page.</span></span> <span data-ttu-id="7eaae-158">이 페이지에는 커넥터에 대 한 속성 및 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-158">This page contains the properties and information about the connector.</span></span>

3. <span data-ttu-id="7eaae-159">**커넥터 상태 (원본 포함** )에서 **로그 다운로드** 링크를 클릭 하 여 커넥터의 상태 로그를 열거나 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-159">Under **Connector status with source** , click the **Download log** link to open (or save) the status log for the connector.</span></span> <span data-ttu-id="7eaae-160">이 로그에는 Microsoft 클라우드로 가져온 데이터에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-160">This log contains information about the data that has been imported to the Microsoft cloud.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7eaae-161">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="7eaae-161">Known issues</span></span>

- <span data-ttu-id="7eaae-162">현재로 서는 10mb 보다 큰 첨부 파일 또는 항목을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-162">At this time, we don't support importing attachments or items that are larger than 10 MB.</span></span> <span data-ttu-id="7eaae-163">더 큰 항목에 대 한 지원은 나중에 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="7eaae-163">Support for larger items will be available at a later date.</span></span>