---
title: 콘텐츠를 자동으로 보존하거나 삭제하는 보존 정책과 레이블에 대해 자세히 알아보기
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: 필요한 항목을 보존하고 필요하지 않은 항목을 삭제하는 데 도움을 주는 보존 정책과 보존 레이블에 대해 알아봅니다.
ms.openlocfilehash: b67320af6f388386d7b7723bbe3f645b46eed8e7
ms.sourcegitcommit: f7566dd6010744c72684efdc37f4471672330b61
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/15/2020
ms.locfileid: "45138216"
---
# <a name="learn-about-retention-policies-and-retention-labels"></a><span data-ttu-id="d1ea6-103">보존 정책 및 보존 레이블에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-103">Learn about retention policies and retention labels</span></span>

><span data-ttu-id="d1ea6-104">*[보안 및 규정 준수를 위한 Microsoft 365 라이선싱 지침](https://aka.ms/ComplianceSD)*</span><span class="sxs-lookup"><span data-stu-id="d1ea6-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="d1ea6-p101">대부분의 조직에서는 전자 메일, 문서, 인스턴트 메시지 등을 비롯하여 데이터의 양과 복잡성이 계속해서 매일 증가하고 있습니다. 이러한 정보를 효과적으로 관리하거나 제어하는 일은 다음 작업을 수행해야 하므로 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-p101">For most organizations, the volume and complexity of their data is increasing daily—email, documents, instant messages, and more. Effectively managing or governing this information is important because you need to:</span></span>
  
- <span data-ttu-id="d1ea6-107">최소 기간 동안 콘텐츠를 보존하도록 요구하는 **산업 규정 및 내부 정책을 사전에 준수**합니다. 예를 들어 Sarbanes-Oxley Act는 7년 동안 특정 유형의 콘텐츠를 보존하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-107">**Comply proactively with industry regulations and internal policies** that require you to retain content for a minimum period of time—for example, the Sarbanes-Oxley Act might require you to retain certain types of content for seven years.</span></span> 
- <span data-ttu-id="d1ea6-108">**소송 또는 보안 위반 시 위험 감소** - 더 이상 보존할 필요가 없는 오래된 콘텐츠를 영구적으로 삭제</span><span class="sxs-lookup"><span data-stu-id="d1ea6-108">**Reduce your risk in the event of litigation or a security breach** by permanently deleting old content that you're no longer required to keep.</span></span> 
    
- <span data-ttu-id="d1ea6-109">**조직에서 효과적이면서 좀 더 민첩하게 지식을 공유하도록 지원** - 사용자가 관련이 있는 최신 콘텐츠만 사용하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-109">**Help your organization to share knowledge effectively and be more agile** by ensuring that your users work only with content that's current and relevant to them.</span></span> 
    
<span data-ttu-id="d1ea6-110">사용자가 구성한 보존 설정은 이러한 모든 목표를 달성하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-110">Retention settings that you configure can help you achieve all these goals.</span></span> <span data-ttu-id="d1ea6-111">콘텐츠 관리에는 일반적으로 다음과 같은 두 가지 작업이 요구됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-111">Managing content commonly requires two actions:</span></span>
  
- <span data-ttu-id="d1ea6-112">**보존** - 콘텐츠가 보존 기간이 끝나기 전에 영구적으로 삭제되지 않도록 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-112">**Retaining** content so that it can't be permanently deleted before the end of the retention period.</span></span> 
    
- <span data-ttu-id="d1ea6-113">**삭제** - 보존 기간이 끝나면 콘텐츠를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-113">**Deleting** content permanently at the end of the retention period.</span></span> 
    

<span data-ttu-id="d1ea6-114">이러한 두 가지 보존 작업을 통해 다음 결과에 대한 보존 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-114">With these two retention actions, you can configure retention settings for the following outcomes:</span></span>

- <span data-ttu-id="d1ea6-115">보존 전용: 콘텐츠를 영구적으로 또는 지정된 기간 동안 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-115">Retain-only: Retain content forever or for a specified period of time.</span></span>
- <span data-ttu-id="d1ea6-116">삭제 전용: 지정된 기간이 지난 후 콘텐츠를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-116">Delete-only: Delete content after a specified period of time.</span></span>
- <span data-ttu-id="d1ea6-117">보존한 다음 삭제: 지정된 기간 동안 콘텐츠를 보존한 다음 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-117">Retain and then delete: Retain content for a specified period of time and then delete it.</span></span>

<span data-ttu-id="d1ea6-118">이러한 보존 설정은 규정 준수를 이유로 콘텐츠를 보존해야 할 때 추가 저장소를 만들고 구성하는 추가 오버헤드를 절약하는 콘텐츠와 함께 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-118">These retention settings work with content in place that saves you the additional overheads of creating and configuring additional storage when you need to retain content for compliance reasons.</span></span> <span data-ttu-id="d1ea6-119">또한 이 데이터를 복사 및 동기화하기 위해 사용자 지정된 프로세스를 구현할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-119">In addition, you don't need to implement customized processes to copy and synchronize this data.</span></span>

## <a name="how-retention-settings-work-with-content-in-place"></a><span data-ttu-id="d1ea6-120">보존 설정이 콘텐츠와 함께 작동하는 방법</span><span class="sxs-lookup"><span data-stu-id="d1ea6-120">How retention settings work with content in place</span></span>

<span data-ttu-id="d1ea6-121">콘텐츠에 보존 설정이 할당된 경우 해당 콘텐츠는 원래 위치에 그대로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-121">When content has retention settings assigned to it, that content remains in its original location.</span></span> <span data-ttu-id="d1ea6-122">사용자는 아무것도 변경된 사항이 없는 것처럼 계속해서 문서나 사서함을 사용하여 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-122">People can continue to work with their documents or mail as if nothing's changed.</span></span> <span data-ttu-id="d1ea6-123">그러나 사용자가 보존 정책에 포함된 콘텐츠를 편집하거나 삭제하는 경우에는 해당 보존 설정이 적용된 시점의 콘텐츠 사본이 자동으로 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-123">But if they edit or delete content that's included in the retention policy, a copy of the content is automatically retained as it existed when you applied the retention settings.</span></span>
  
- <span data-ttu-id="d1ea6-124">SharePoint 및 OneDrive 사이트의 경우: 사본은 **자료 보존** 라이브러리에 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-124">For SharePoint and OneDrive sites: The copy is retained in the **Preservation Hold** library.</span></span>

- <span data-ttu-id="d1ea6-125">Exchange 사서함의 경우: **복구 가능한 항목** 폴더에 사본이 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-125">For Exchange mailboxes: The copy is retained in the **Recoverable Items** folder.</span></span> 

- <span data-ttu-id="d1ea6-126">Teams 채널 및 채팅 메시지의 경우: 사본은 Exchange **복구 가능한 항목** 폴더 내의 숨겨진 폴더에 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-126">For Teams channel and chat messages: The copy is retained in a hidden folder within the Exchange **Recoverable Items** folder.</span></span>

> [!NOTE]
> <span data-ttu-id="d1ea6-127">자료 보존 라이브러리는 사이트의 저장소 할당량에서 제외되지 않은 저장소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-127">The Preservation Hold library consumes storage that isn't exempt from a site's storage quota.</span></span> <span data-ttu-id="d1ea6-128">SharePoint 및 Microsoft 365 그룹에 대한 보존 설정을 사용하는 경우 저장소를 늘려야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-128">You might need to increase your storage when you use retention settings for SharePoint and Microsoft 365 groups.</span></span>
> 
<span data-ttu-id="d1ea6-129">대부분의 사용자는 해당 보안 위치와 보존된 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-129">These secure locations and the retained content are not visible to most people.</span></span> <span data-ttu-id="d1ea6-130">대부분의 경우 사용자는 해당 콘텐츠에 보존 설정이 적용되어 있다는 사실을 알 필요도 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-130">In most cases, people do not even need to know that their content is subject to retention settings.</span></span>

<span data-ttu-id="d1ea6-131">다양한 워크로드에 대해 보존 설정이 작동하는 방법에 대한 자세한 내용은 다음의 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-131">For more detailed information about how retention settings work for different workloads, see the following articles:</span></span>

- [<span data-ttu-id="d1ea6-132">SharePoint 및 OneDrive의 보존에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-132">Learn about retention for SharePoint and OneDrive</span></span>](retention-policies-sharepoint.md)
- [<span data-ttu-id="d1ea6-133">Microsoft Teams의 보존에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-133">Learn about retention for Microsoft Teams</span></span>](retention-policies-teams.md)
- [<span data-ttu-id="d1ea6-134">Exchange의 보존에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-134">Learn about retention for Exchange</span></span>](retention-policies-exchange.md)

## <a name="retention-policies-and-retention-labels"></a><span data-ttu-id="d1ea6-135">보존 정책 및 보존 레이블</span><span class="sxs-lookup"><span data-stu-id="d1ea6-135">Retention policies and retention labels</span></span>

<span data-ttu-id="d1ea6-136">보존 정책과 보존 레이블을 모두 사용하여 보존 설정을 콘텐츠에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-136">You can use both retention policies and retention labels to assign your retention settings to content.</span></span> 

<span data-ttu-id="d1ea6-137">보존 정책을 사용하여 사이트 또는 사서함 수준에서 콘텐츠에 대해 같은 보존 설정을 할당하고, 보존 레이블을 사용하여 항목 수준(폴더, 문서, 전자 메일)에 보존 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-137">Use a retention policy to assign the same retention settings for content at a site or mailbox level, and use a retention label to assign retention settings at an item level (folder, document, email).</span></span>

<span data-ttu-id="d1ea6-138">예를 들어 SharePoint 사이트의 모든 문서를 5년 동안 보존해야 하면, 해당 사이트의 모든 문서에 동일한 보존 레이블을 적용하는 것보다 보존 정책을 사용하여 이 작업을 수행하는 것이 더욱 효율적입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-138">For example, if all documents in a SharePoint site should be retained for five years, it's more efficient to do this with a retention policy than apply the same retention label to all documents in that site.</span></span> <span data-ttu-id="d1ea6-139">하지만 해당 사이트의 일부 문서는 5년 동안 보존해야 하고 다른 문서는 10년 동안 보존해야 할 때는 보존 정책으로 이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-139">However, if some documents in that site should be retained for five years and others retained for ten years, a retention policy wouldn't be able to do this.</span></span> <span data-ttu-id="d1ea6-140">항목 수준에서 보존 설정을 지정해야 하는 경우에는 보존 레이블을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-140">When you need to specify retention settings at the item level, use retention labels.</span></span> 

<span data-ttu-id="d1ea6-141">보존 정책과 달리 보존 레이블의 보존 설정은 콘텐츠를 다른 Microsoft 365 위치로 복사하거나 이동해도 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-141">Unlike retention policies, retention settings from retention labels persist with the content if it’s copied or moved to a different Microsoft 365 location.</span></span> <span data-ttu-id="d1ea6-142">또한, 보존 레이블에는 보존 정책에서는 지원되지 않는 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-142">In addition, retention labels have the following capabilities that retention policies don't support:</span></span> 
 
- <span data-ttu-id="d1ea6-143">콘텐츠의 기간 또는 콘텐츠가 마지막으로 수정된 시간 외에도 콘텐츠에 레이블이 지정된 시간으로부터 또는 이벤트를 기반으로 보존 기간을 시작하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-143">Options to start the retention period from when the content was labeled or based on an event, in addition to the age of the content or when it was last modified.</span></span>

- <span data-ttu-id="d1ea6-144">[학습 가능한 분류자](classifier-getting-started-with.md)를 사용하여 콘텐츠를 레이블로 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-144">Use [trainable classifiers](classifier-getting-started-with.md) to identify content to label.</span></span>

- <span data-ttu-id="d1ea6-145">SharePoint 문서에 대해 기본 레이블을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-145">Apply a default label for SharePoint documents.</span></span>

- <span data-ttu-id="d1ea6-146">콘텐츠를 영구적으로 삭제하기 전에 검토할 수 있는 [처리 검토](disposition-reviews.md) 를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-146">Support [disposition review](disposition-reviews.md) to review the content before it's permanently deleted.</span></span>

- <span data-ttu-id="d1ea6-147">콘텐츠를 레이블 설정의 일부로 [레코드](records.md)로 표시하고, 보관 기간이 끝나 콘텐츠가 삭제된 경우 항상  [처리 증명](disposition.md#disposition-of-records) 이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-147">Mark the content as a [record](records.md) as part of the label settings, and always have [proof of disposition](disposition.md#disposition-of-records) when content is deleted at the end of its retention period.</span></span>

### <a name="retention-policies"></a><span data-ttu-id="d1ea6-148">보존 정책</span><span class="sxs-lookup"><span data-stu-id="d1ea6-148">Retention policies</span></span>

<span data-ttu-id="d1ea6-149">보존 정책은 다음 위치에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-149">Retention policies can be applied to the following locations:</span></span>
- <span data-ttu-id="d1ea6-150">Exchange 전자 메일</span><span class="sxs-lookup"><span data-stu-id="d1ea6-150">Exchange email</span></span>
- <span data-ttu-id="d1ea6-151">SharePoint 사이트</span><span class="sxs-lookup"><span data-stu-id="d1ea6-151">SharePoint site</span></span>
- <span data-ttu-id="d1ea6-152">OneDrive 계정</span><span class="sxs-lookup"><span data-stu-id="d1ea6-152">OneDrive accounts</span></span>
- <span data-ttu-id="d1ea6-153">Microsoft 365 그룹</span><span class="sxs-lookup"><span data-stu-id="d1ea6-153">Microsoft 365 groups</span></span>
- <span data-ttu-id="d1ea6-154">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="d1ea6-154">Skype for Business</span></span>
- <span data-ttu-id="d1ea6-155">Exchange 공용 폴더</span><span class="sxs-lookup"><span data-stu-id="d1ea6-155">Exchange public folders</span></span>
- <span data-ttu-id="d1ea6-156">Teams 채널 메시지</span><span class="sxs-lookup"><span data-stu-id="d1ea6-156">Teams channel messages</span></span>
- <span data-ttu-id="d1ea6-157">Teams 채팅</span><span class="sxs-lookup"><span data-stu-id="d1ea6-157">Teams chats</span></span>

<span data-ttu-id="d1ea6-158">단일 정책을 여러 위치 또는 특정 위치 또는 사용자에게 효율적으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-158">You can very efficiently apply a single policy to multiple locations, or to specific locations or users.</span></span>
    
<span data-ttu-id="d1ea6-159">모든 콘텐츠 또는 특정 조건을 충족하는 콘텐츠(예: 특정 키워드 또는 [중요한 정보 유형](sensitive-information-type-entity-definitions.md)을 포함하는 콘텐츠)에 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-159">You can also apply a policy to all content or to content when it meets specific conditions, such as content that contains keywords or [sensitive information types](sensitive-information-type-entity-definitions.md).</span></span>

#### <a name="use-preservation-lock-to-comply-with-regulatory-requirements"></a><span data-ttu-id="d1ea6-160">보존 잠금을 사용하여 규정 요구 사항을 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-160">Use Preservation Lock to comply with regulatory requirements</span></span>

<span data-ttu-id="d1ea6-161">일부 조직에서는 보존 정책을 설정한 후에 해제하거나 제한 사항이 거의 없이 설정할 수 없는 SEC(증권 거래 위원회) 규칙 17a-4와 같은 규제 기구에서 정의한 규칙을 준수해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-161">Some organizations might need to comply with rules defined by regulatory bodies such as the Securities and Exchange Commission (SEC) Rule 17a-4, which requires that after a retention policy is turned on, it cannot be turned off or made less restrictive.</span></span> 

<span data-ttu-id="d1ea6-162">보존 잠금은 조직이 관리자를 비롯하여 어떠한 사용자도 정책을 해제하거나, 삭제하거나, 제한 사항이 거의 없이 설정할 수 없도록 보존 정책을 잠그기 때문에 관련 규정 요구 사항을 충족할 수 있도록 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-162">Preservation Lock ensures your organization can meet such regulatory requirements because it locks a retention policy so that no one—including the administrator—can turn off the policy, delete the policy, or make it less restrictive.</span></span>
  
<span data-ttu-id="d1ea6-163">보존 정책이 잠기는 경우:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-163">When a retention policy is locked:</span></span>

- <span data-ttu-id="d1ea6-164">누구도 해당 정책을 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-164">No one can it turn off</span></span>
- <span data-ttu-id="d1ea6-165">위치는 추가할 수 있지만 제거할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-165">Locations can be added but not removed</span></span>
- <span data-ttu-id="d1ea6-166">보존 기간 동안에 해당 정책이 적용된 콘텐츠를 수정하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-166">Content subject to the policy can't be modified or deleted during the retention period</span></span>
- <span data-ttu-id="d1ea6-167">보존 기간을 연장할 수 있지만 줄일 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-167">You can extend a retention period but not decrease it</span></span>

<span data-ttu-id="d1ea6-168">요약하면 잠겨 있는 정책은 늘리거나 확장할 수 있지만 줄이거나 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-168">In summary, a locked retention policy can be increased or extended, but it can't be reduced or turned off.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d1ea6-169">보존 정책을 잠그기 전에 해당 정책의 영향을 이해하고 조직에서 규정 요구 사항을 충족하는 데 해당 정책이 필요한지 여부를 확인하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-169">Before you lock a retention policy, it's critical that you understand the impact and confirm whether it's required for your organization to meet regulatory requirements.</span></span> <span data-ttu-id="d1ea6-170">보존 잠금이 적용된 후에는 관리자가 보존 정책을 사용하지 않도록 설정하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-170">Administrators won't be able to disable or delete a retention policy after the preservation lock is applied.</span></span>

#### <a name="releasing-a-retention-policy"></a><span data-ttu-id="d1ea6-171">보존 정책 해제</span><span class="sxs-lookup"><span data-stu-id="d1ea6-171">Releasing a retention policy</span></span>

<span data-ttu-id="d1ea6-172">보존 정책에 보존 잠금이 없으면 언제든지 보존 정책을 끄거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-172">Providing your retention policy doesn't have a Preservation Lock, you can turn off or delete a retention policy at any time.</span></span> 

<span data-ttu-id="d1ea6-173">이렇게 하면 자료 보존 라이브러리에 보존되어 있는 모든 SharePoint 또는 OneDrive 콘텐츠가 바로 영구적으로 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-173">When you do so, any SharePoint or OneDrive content that's being retained in the Preservation Hold library is not immediately and permanently deleted.</span></span> <span data-ttu-id="d1ea6-174">실수로 데이터가 손실되는 것을 방지하기 위해 30일간의 유예 기간이 있습니다. 이 기간에는 자료 보존 라이브러리에서 해당 정책에 대한 콘텐츠 만료가 발생하지 않으므로 필요한 경우 콘텐츠를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-174">Instead, to help prevent inadvertent data loss, there is a 30-day grace period, during which content expiration for that policy does not happen in the Preservation Hold library, so that you can restore any content from there, if needed.</span></span> <span data-ttu-id="d1ea6-175">또한 유예 기간에 이 콘텐츠를 수동으로 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-175">Additionally, you can't manually delete this content during the grace period.</span></span>

<span data-ttu-id="d1ea6-176">유예 기간에 보존 정책을 다시 켤 수 있고 해당 정책에 대한 콘텐츠가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-176">You can turn on the retention policy again during the grace period, and no content will be deleted for that policy.</span></span>

<span data-ttu-id="d1ea6-177">SharePoint 및 OneDrive의 30일간의 유예 기간은 Exchange의 30일 지연 기간에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-177">This 30-day grace period in SharePoint and OneDrive corresponds to the 30-day delay hold in Exchange.</span></span> <span data-ttu-id="d1ea6-178">자세한 내용은 [지연되는 사서함 관리](identify-a-hold-on-an-exchange-online-mailbox.md#managing-mailboxes-on-delay-hold)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-178">For more information, see [Managing mailboxes on delay hold](identify-a-hold-on-an-exchange-online-mailbox.md#managing-mailboxes-on-delay-hold).</span></span>

### <a name="retention-labels"></a><span data-ttu-id="d1ea6-179">보존 레이블</span><span class="sxs-lookup"><span data-stu-id="d1ea6-179">Retention labels</span></span>

<span data-ttu-id="d1ea6-180">다른 보존 설정이 있어야 하는 다양한 유형의 콘텐츠에는 보존 레이블을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-180">Use retention labels for different types of content that require different retention settings.</span></span> <span data-ttu-id="d1ea6-181">예제:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-181">For example:</span></span>
  
- <span data-ttu-id="d1ea6-182">최소 기간 동안 보존해야 하는 세금 양식</span><span class="sxs-lookup"><span data-stu-id="d1ea6-182">Tax forms that need to be retained for a minimum period of time.</span></span> 
    
- <span data-ttu-id="d1ea6-183">특정 기간에 도달하면 영구적으로 삭제되어야 하는 보도 자료</span><span class="sxs-lookup"><span data-stu-id="d1ea6-183">Press materials that need to be permanently deleted when they reach a specific age.</span></span> 
    
- <span data-ttu-id="d1ea6-184">특정 기간 동안 보존되었다가 영구적으로 삭제되어야 하는 경쟁 연구 자료</span><span class="sxs-lookup"><span data-stu-id="d1ea6-184">Competitive research that needs to be retained for a specific period and then permanently deleted.</span></span> 
    
- <span data-ttu-id="d1ea6-185">편집하거나 삭제할 수 없게 레코드로 표시해야 하는 취업 비자</span><span class="sxs-lookup"><span data-stu-id="d1ea6-185">Work visas that must be marked as a record so that they can't be edited or deleted.</span></span> 
    
<span data-ttu-id="d1ea6-186">이 모든 경우 보존 레이블을 사용하여 항목 수준(문서 또는 전자 메일)에서 거버넌스 제어에 대한 보존 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-186">In all these cases, retention labels let you apply retention settings for governance control at the item level (document or email).</span></span>
  
<span data-ttu-id="d1ea6-187">보존 레이블을 사용하여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-187">With retention labels, you can:</span></span>
  
- <span data-ttu-id="d1ea6-188">Outlook, 웹용 Outlook, OneDrive, SharePoint 및 Microsoft 365 그룹의 콘텐츠에 **조직의 사용자가 수동으로 보존 레이블을 적용할 수 있도록 합니다**.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-188">**Enable people in your organization to apply a retention label manually** to content in Outlook and Outlook on the web, OneDrive, SharePoint, and Microsoft 365 groups.</span></span> <span data-ttu-id="d1ea6-189">대개 사용자가 자신이 작업 중인 콘텐츠의 유형을 가장 잘 알고 있으므로 사용자가 콘텐츠를 분류하고 적절한 보존 설정이 적용되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-189">Users often know best what type of content they're working with, so they can classify it and have the appropriate retention settings applied.</span></span> 
    
- <span data-ttu-id="d1ea6-190">콘텐츠에 다음이 포함된 경우처럼 특정 조건과 일치하는 경우 **콘텐츠에 보존 레이블을 자동으로 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-190">**Apply retention labels to content automatically** if it matches specific conditions, such as when the content contains:</span></span> 
    - <span data-ttu-id="d1ea6-191">특정 중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="d1ea6-191">Specific types of sensitive information.</span></span>
    - <span data-ttu-id="d1ea6-192">만든 쿼리와 일치하는 특정 키워드</span><span class="sxs-lookup"><span data-stu-id="d1ea6-192">Specific keywords that match a query you create.</span></span>
    - <span data-ttu-id="d1ea6-193">학습 가능한 분류자에 대한 패턴 일치</span><span class="sxs-lookup"><span data-stu-id="d1ea6-193">Pattern matches for a trainable classifier.</span></span>

- <span data-ttu-id="d1ea6-194">**콘텐츠에 레이블이 지정된 시점부터 보존 기간 시작**(SharePoint 사이트 및 OneDrive 계정의 문서, 일정 항목을 제외한 전자 메일 항목)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-194">**Start the retention period from when the content was labeled** for documents in SharePoint sites and OneDrive accounts, and to email items with the exception of calendar items.</span></span> <span data-ttu-id="d1ea6-195">이 구성과 함께 보존 레이블을 일정 항목에 적용하는 경우 해당 보존 기간은 보낸 날짜부터 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-195">If you apply a retention label with this configuration to a calendar item, the retention period starts from when it is sent.</span></span>

- <span data-ttu-id="d1ea6-196">**이벤트가 발생할 때 보존 기간 시작**(예: 직원 퇴사, 계약 만료)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-196">**Start the retention period when an event occurs**, such as employees leave the organization, or contracts expire.</span></span>

- <span data-ttu-id="d1ea6-197">SharePoint의 **문서 라이브러리, 폴더 또는 문서 집합에 기본 보존 레이블을 적용**하여 해당 위치에 저장된 모든 문서가 기본 보존 레이블을 상속하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-197">**Apply a default retention label to a document library, folder, or document set** in SharePoint, so that all documents that are stored in that location inherit the default retention label.</span></span>

<span data-ttu-id="d1ea6-198">또한, 보존 레이블은 Microsoft 365 앱과 서비스에서 전자 메일 및 문서의 [레코드 관리](records-management.md)를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-198">Additionally, retention labels support [records management](records-management.md) for email and documents across Microsoft 365 apps and services.</span></span> <span data-ttu-id="d1ea6-199">보존 레이블을 사용하여 콘텐츠를 레코드로 분류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-199">You can use a retention label to classify content as a record.</span></span> <span data-ttu-id="d1ea6-200">이런 경우 콘텐츠가 Microsoft 365에 남아 있으면 레이블을 변경하거나 제거할 수 없으며 콘텐츠를 편집하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-200">When this happens and the content remains in Microsoft 365, the label can't be changed or removed, and the content can't be edited or deleted.</span></span> 

<span data-ttu-id="d1ea6-201">보존 레이블은 [민감도 레이블](sensitivity-labels.md)과 달리 Microsoft 365 외부로 콘텐츠를 이동해도 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-201">Retention labels, unlike [sensitivity labels](sensitivity-labels.md), do not persist if the content is moved outside Microsoft 365.</span></span>

<span data-ttu-id="d1ea6-202">테넌트에 지원되는 보존 레이블 개수에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-202">There is no limit to the number of retention labels that are supported for a tenant.</span></span> <span data-ttu-id="d1ea6-203">그러나 10,000은 테넌트에 지원되는 최대 정책의 수이며, 여기에는 레이블뿐만 아니라 보존 정책이 적용되는 정책(보존 레이블 정책과 자동 적용 보존 정책)도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-203">However, 10,000 is the maximum number of policies that are supported for a tenant and these include the policies that apply the labels (retention label policies and auto-apply retention policies), as well as retention policies.</span></span>

#### <a name="classifying-content-without-applying-any-actions"></a><span data-ttu-id="d1ea6-204">작업을 적용하지 않고 콘텐츠 분류하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-204">Classifying content without applying any actions</span></span>

<span data-ttu-id="d1ea6-205">보존 레이블의 주요 용도는 콘텐츠를 보존하거나 삭제하는 것이지만, 보존 또는 기타 작업을 설정하지 않고 보존 레이블을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-205">Although the main purpose of retention labels is to retain or delete content, you can also use retention labels without turning on any retention or other actions.</span></span> <span data-ttu-id="d1ea6-206">이 경우 작업을 적용하지 않고 보존 레이블을 단순히 텍스트 레이블로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-206">In this case, you can use a retention label simply as a text label, without enforcing any actions.</span></span>
  
<span data-ttu-id="d1ea6-207">예를 들어 작업이 없는 "나중에 검토"라는 보존 레이블을 만들고 적용한 다음 해당 레이블을 사용하여 나중에 해당 콘텐츠를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-207">For example, you can create and apply a retention label named "Review later" with no actions, and then use that label to find that content later.</span></span>
  
![보존이 해제된 레이블 설정 페이지](../media/retention-label-retentionoff.png)

#### <a name="using-a-retention-label-as-a-condition-in-a-dlp-policy"></a><span data-ttu-id="d1ea6-209">보존 레이블을 DLP 정책의 조건으로 사용하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-209">Using a retention label as a condition in a DLP policy</span></span>

<span data-ttu-id="d1ea6-210">SharePoint의 문서에 대한 DLP(데이터 손실 방지) 정책에서 보존 레이블을 조건으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-210">You can specify a retention label as a condition in a data loss prevention (DLP) policy for documents in SharePoint.</span></span> <span data-ttu-id="d1ea6-211">예를 들어 문서에 지정된 보존 레이블이 적용된 경우, 문서를 조직 외부에 공유하지 못하도록 DLP 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-211">For example, configure a DLP policy to prevent documents from being shared outside the organization if they have a specified retention label applied to it.</span></span>

<span data-ttu-id="d1ea6-212">자세한 내용은 [보존 레이블을 DLP 정책의 조건으로 사용하기](data-loss-prevention-policies.md#using-a-retention-label-as-a-condition-in-a-dlp-policy)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-212">For more information, see [Using a retention label as a condition in a DLP policy](data-loss-prevention-policies.md#using-a-retention-label-as-a-condition-in-a-dlp-policy).</span></span>

#### <a name="retention-labels-and-policies-that-apply-them"></a><span data-ttu-id="d1ea6-213">보존 레이블과 보존 레이블을 적용하는 정책 </span><span class="sxs-lookup"><span data-stu-id="d1ea6-213">Retention labels and policies that apply them</span></span>

<span data-ttu-id="d1ea6-214">보존 레이블은 독립적이고, 다시 사용할 수 있는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-214">Retention labels are independent, reusable building blocks.</span></span> <span data-ttu-id="d1ea6-215">보존 레이블 정책의 기본 목적은 보존 레이블 집합을 그룹화하고 해당 레이블을 표시할 위치를 지정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-215">The primary purpose of a retention label policy is to group a set of retention labels and specify the locations where you want those labels to appear.</span></span> <span data-ttu-id="d1ea6-216">그러면 관리자와 사용자가 해당 위치에 해당 레이블을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-216">Then, admins and users can apply those labels to content in those locations.</span></span>
  
![레이블, 레이블 정책 및 위치 다이어그램](../media/eee42516-adf0-4664-b5ab-76727a9a3511.png)
  
<span data-ttu-id="d1ea6-218">보존 레이블을 게시하면 보존 레이블은 보존 레이블 정책에 포함되어 관리자와 사용자가 다음을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-218">When you publish retention labels, they're included in a retention label policy that make them available for admins and users to select:</span></span>

- <span data-ttu-id="d1ea6-219">하나의 보존 레이블이 여러 보존 레이블 정책에 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-219">A single retention label can be included in many retention label policies.</span></span>

- <span data-ttu-id="d1ea6-220">보존 레이블 정책이 보존 레이블을 게시할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-220">Retention label policies specify the locations to publish the retention labels.</span></span>

- <span data-ttu-id="d1ea6-221">하나의 위치가 여러 보존 레이블 정책에 포함될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-221">A single location can also be included in many retention label policies.</span></span>

<span data-ttu-id="d1ea6-222">보존 레이블 정책 외에도 하나의 보존 레이블을 사용하여 하나 이상의 자동 적용 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-222">In addition to retention label policies, you can also create one or more auto-apply policies, each with a single retention label.</span></span> <span data-ttu-id="d1ea6-223">이 정책을 사용하면 정책에서 지정하는 조건이 충족될 경우 보존 레이블이 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-223">With this policy, a retention label is automatically applied when conditions that you specify in the policy are met.</span></span> 

#### <a name="retention-label-policies-and-locations"></a><span data-ttu-id="d1ea6-224">보존 레이블 정책 및 위치</span><span class="sxs-lookup"><span data-stu-id="d1ea6-224">Retention label policies and locations</span></span>

<span data-ttu-id="d1ea6-225">보존 레이블이 수행하는 작업에 따라, 다양한 유형의 보존 레이블을 여러 다른 위치에 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-225">Different types of retention labels can be published to different locations, depending on what the retention label does.</span></span>
  
| <span data-ttu-id="d1ea6-226">보존 레이블이</span><span class="sxs-lookup"><span data-stu-id="d1ea6-226">If the retention label is…</span></span> | <span data-ttu-id="d1ea6-227">레이블 정책을 적용할 수 있는 위치</span><span class="sxs-lookup"><span data-stu-id="d1ea6-227">Then the label policy can be applied to…</span></span> |
|:-----|:-----|
|<span data-ttu-id="d1ea6-228">관리자 및 최종 사용자에게 게시됨</span><span class="sxs-lookup"><span data-stu-id="d1ea6-228">Published to admins and end users</span></span>  <br/> |<span data-ttu-id="d1ea6-229">Exchange, SharePoint, OneDrive, Microsoft 365 그룹</span><span class="sxs-lookup"><span data-stu-id="d1ea6-229">Exchange, SharePoint, OneDrive, Microsoft 365 Groups</span></span>  <br/> |
|<span data-ttu-id="d1ea6-230">중요한 정보 유형 또는 학습 가능한 분류자를 기반으로 자동 적용됨</span><span class="sxs-lookup"><span data-stu-id="d1ea6-230">Auto-applied based on sensitive information types or trainable classifiers</span></span>  <br/> |<span data-ttu-id="d1ea6-231">Exchange(모든 사서함만), SharePoint, OneDrive</span><span class="sxs-lookup"><span data-stu-id="d1ea6-231">Exchange (all mailboxes only), SharePoint, OneDrive</span></span>  <br/> |
|<span data-ttu-id="d1ea6-232">쿼리에 따라 자동 적용</span><span class="sxs-lookup"><span data-stu-id="d1ea6-232">Auto-applied based on a query</span></span>  <br/> |<span data-ttu-id="d1ea6-233">Exchange, SharePoint, OneDrive, Microsoft 365 그룹</span><span class="sxs-lookup"><span data-stu-id="d1ea6-233">Exchange, SharePoint, OneDrive, Microsoft 365 Groups</span></span>  <br/> |
   
<span data-ttu-id="d1ea6-234">Exchange에서 자동 적용 보존 레이블은 현재 사서함에 있는 모든 항목(미사용 데이터)이 아닌 새로 전송된 메시지(전송 중인 데이터)에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-234">In Exchange, auto-apply retention labels are applied only to messages newly sent (data in transit), not to all items currently in the mailbox (data at rest).</span></span> <span data-ttu-id="d1ea6-235">또한, 중요한 정보 유형과 학습 가능한 분류자에 대한 자동 적용 보존 레이블은 모든 사서함에만 적용되며, 특정 사서함을 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-235">Also, auto-apply retention labels for sensitive information types and trainable classifiers apply to all mailboxes; you can't select specific mailboxes.</span></span>
  
<span data-ttu-id="d1ea6-236">Exchange 공용 폴더, Skype, Teams 채널 메시지 및 채팅은 보존 레이블을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-236">Exchange public folders, Skype, and Teams channel messages and chats do not support retention labels.</span></span> <span data-ttu-id="d1ea6-237">해당 위치에서 콘텐츠를 보존하고 삭제하려면 보존 정책을 대신 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-237">To retain and delete contain from these locations, use retention policies instead.</span></span>

#### <a name="only-one-retention-label-at-a-time"></a><span data-ttu-id="d1ea6-238">한 번에 하나의 보존 레이블만</span><span class="sxs-lookup"><span data-stu-id="d1ea6-238">Only one retention label at a time</span></span>

<span data-ttu-id="d1ea6-239">전자 메일 또는 문서에는 한 번에 하나의 보존 레이블만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-239">An email or document can have only a single retention label assigned to it at a time:</span></span>
  
- <span data-ttu-id="d1ea6-240">관리자나 최종 사용자가 수동으로 할당한 보존 레이블의 경우, 할당된 보존 레이블을 제거하거나 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-240">For retention labels assigned manually by admins or end users, people can remove or change the retention label that's assigned.</span></span>
    
- <span data-ttu-id="d1ea6-241">콘텐츠에 자동 적용 레이블이 할당된 경우에는 이 레이블을 게시된 보존 레이블로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-241">If content has an auto-apply label assigned, this label can be replaced by a published retention label.</span></span>
    
- <span data-ttu-id="d1ea6-242">콘텐츠에 게시된 보존 레이블이 할당된 경우 자동 적용 레이블은 대체되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-242">If content has a published retention label assigned, an auto-apply label cannot replace it.</span></span>
    
- <span data-ttu-id="d1ea6-243">자동 적용 레이블을 할당하는 여러 규칙이 있고 콘텐츠가 여러 규칙의 조건을 충족하는 경우 가장 오래된 규칙에 대한 보존 레이블이 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-243">If there are multiple rules that assign an auto-apply label and content meets the conditions of multiple rules, the retention label for the oldest rule is assigned.</span></span>
    
<span data-ttu-id="d1ea6-244">한 보존 레이블이 적용되는 방법과 그 이유를 이해하려면 레이블을 명시적으로 할당하는 것과 암시적으로 레이블이 할당되는 것의 차이점을 이해하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-244">To understand how and why one retention label is applied rather than another, it's helpful to understand the difference between explicitly assign a label, and implicitly assigned a label:</span></span>

- <span data-ttu-id="d1ea6-245">레이블 정책에서 적용되는 보존 레이블은 명시적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-245">Retention labels applied from a label policy are explicitly assigned</span></span>
- <span data-ttu-id="d1ea6-246">자동 적용 정책에서 자동으로 적용되는 보존 레이블은 암시적으로 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-246">Retention labels applied automatically from an auto-apply policy are implicitly assigned</span></span>

<span data-ttu-id="d1ea6-247">명시적으로 할당된 보존 레이블이 암시적으로 할당된 보존 레이블에 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-247">An explicitly assigned retention label takes precedence over an implicitly assigned retention label.</span></span> <span data-ttu-id="d1ea6-248">자세한 내용은 [보존 원칙 또는 우선하는 항목](retention.md#the-principles-of-retention-or-what-takes-precedence)에 대한 이 페이지의 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-248">For more information, see the [The principles of retention, or what takes precedence?](retention.md#the-principles-of-retention-or-what-takes-precedence) section on this page.</span></span>

#### <a name="using-content-search-to-find-all-content-with-a-specific-retention-label-applied-to-it"></a><span data-ttu-id="d1ea6-249">콘텐츠 검색을 사용하여 특정 보존 레이블이 적용된 모든 콘텐츠 찾기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-249">Using Content Search to find all content with a specific retention label applied to it</span></span>

<span data-ttu-id="d1ea6-250">사용자가 콘텐츠에 보존 레이블을 할당하거나 레이블이 자동 적용된 후에 콘텐츠 검색을 사용하여 특정 보존 레이블로 분류된 모든 콘텐츠를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-250">After retention labels are assigned to content, either by users or auto-applied, you can use content search to find all content that's classified with a specific retention label.</span></span>
  
<span data-ttu-id="d1ea6-251">콘텐츠 검색을 만들 때 **규정 준수 레이블** 조건을 선택한 다음 보존 레이블 이름을 전체 또는 일부만 입력하고 와일드 카드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-251">When you create a content search, choose the **Compliance label** condition, and then enter the complete retention label name or part of the label name and use a wildcard.</span></span> <span data-ttu-id="d1ea6-252">자세한 내용은 [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-252">For more information, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
![규정 준수 레이블 조건](../media/compliance-label-condition.png)


## <a name="compare-capabilities-for-retention-policies-and-retention-labels"></a><span data-ttu-id="d1ea6-254">보존 정책 및 보존 레이블의 기능 비교하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-254">Compare capabilities for retention policies and retention labels</span></span>

<span data-ttu-id="d1ea6-255">다음 표를 사용하여 기능을 기반으로 보존 정책을 사용할지 또는 보존 레이블을 사용할지를 식별하는 데 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-255">Use the following table to help you identify whether to use a retention policy or retention label, based on capabilities.</span></span>

|<span data-ttu-id="d1ea6-256">기능</span><span class="sxs-lookup"><span data-stu-id="d1ea6-256">Capability</span></span>|<span data-ttu-id="d1ea6-257">보존 정책</span><span class="sxs-lookup"><span data-stu-id="d1ea6-257">Retention policy</span></span> |<span data-ttu-id="d1ea6-258">보존 레이블</span><span class="sxs-lookup"><span data-stu-id="d1ea6-258">Retention label</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d1ea6-259">보존 후 삭제, 보존만 또는 삭제만 할 수 있는 보존 설정</span><span class="sxs-lookup"><span data-stu-id="d1ea6-259">Retention settings that can retain and then delete, retain-only, or delete-only</span></span> |<span data-ttu-id="d1ea6-260">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-260">Yes</span></span> |<span data-ttu-id="d1ea6-261">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-261">Yes</span></span> |
|<span data-ttu-id="d1ea6-262">워크로드 지원됨: </span><span class="sxs-lookup"><span data-stu-id="d1ea6-262">Workloads supported:</span></span> <br /><span data-ttu-id="d1ea6-263">- Exchange</span><span class="sxs-lookup"><span data-stu-id="d1ea6-263">- Exchange</span></span> <br /><span data-ttu-id="d1ea6-264">- SharePoint</span><span class="sxs-lookup"><span data-stu-id="d1ea6-264">- SharePoint</span></span> <br /><span data-ttu-id="d1ea6-265">- OneDrive</span><span class="sxs-lookup"><span data-stu-id="d1ea6-265">- OneDrive</span></span> <br /><span data-ttu-id="d1ea6-266">- Microsoft 365 그룹</span><span class="sxs-lookup"><span data-stu-id="d1ea6-266">- Microsoft 365 groups</span></span> <br /><span data-ttu-id="d1ea6-267">- 비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="d1ea6-267">- Skype for Business</span></span> <br /><span data-ttu-id="d1ea6-268">- Teams</span><span class="sxs-lookup"><span data-stu-id="d1ea6-268">- Teams</span></span>|<br /> <span data-ttu-id="d1ea6-269">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-269">Yes</span></span> <br /> <span data-ttu-id="d1ea6-270">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-270">Yes</span></span> <br /> <span data-ttu-id="d1ea6-271">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-271">Yes</span></span> <br /> <span data-ttu-id="d1ea6-272">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-272">Yes</span></span> <br /> <span data-ttu-id="d1ea6-273">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-273">Yes</span></span> <br /> <span data-ttu-id="d1ea6-274">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-274">Yes</span></span> | <br /> <span data-ttu-id="d1ea6-275">예, 공용 폴더 제외</span><span class="sxs-lookup"><span data-stu-id="d1ea6-275">Yes, except public folders</span></span> <br /> <span data-ttu-id="d1ea6-276">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-276">Yes</span></span> <br /> <span data-ttu-id="d1ea6-277">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-277">Yes</span></span> <br /> <span data-ttu-id="d1ea6-278">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-278">Yes</span></span> <br /> <span data-ttu-id="d1ea6-279">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-279">No</span></span> <br /> <span data-ttu-id="d1ea6-280">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-280">No</span></span>  |
|<span data-ttu-id="d1ea6-281">자동으로 보존 적용됨</span><span class="sxs-lookup"><span data-stu-id="d1ea6-281">Retention applied automatically</span></span> | <span data-ttu-id="d1ea6-282">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-282">Yes</span></span> | <span data-ttu-id="d1ea6-283">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-283">Yes</span></span> |
|<span data-ttu-id="d1ea6-284">수동으로 보존 적용됨</span><span class="sxs-lookup"><span data-stu-id="d1ea6-284">Retention applied manually</span></span> | <span data-ttu-id="d1ea6-285">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-285">No</span></span> | <span data-ttu-id="d1ea6-286">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-286">Yes</span></span> |
|<span data-ttu-id="d1ea6-287">최종 사용자를 위한 UI 존재</span><span class="sxs-lookup"><span data-stu-id="d1ea6-287">UI presence for end users</span></span> | <span data-ttu-id="d1ea6-288">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-288">No</span></span> | <span data-ttu-id="d1ea6-289">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-289">Yes</span></span> |
|<span data-ttu-id="d1ea6-290">콘텐츠를 이동해도 유지됨</span><span class="sxs-lookup"><span data-stu-id="d1ea6-290">Persists if the content is moved</span></span> | <span data-ttu-id="d1ea6-291">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-291">No</span></span> | <span data-ttu-id="d1ea6-292">예, Microsoft 365 내</span><span class="sxs-lookup"><span data-stu-id="d1ea6-292">Yes, within Microsoft 365</span></span> |
|<span data-ttu-id="d1ea6-293">항목을 레코드로 선언</span><span class="sxs-lookup"><span data-stu-id="d1ea6-293">Declare item as a record</span></span>| <span data-ttu-id="d1ea6-294">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-294">No</span></span> | <span data-ttu-id="d1ea6-295">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-295">Yes</span></span> |
|<span data-ttu-id="d1ea6-296">레이블이 지정되거나 이벤트를 기반으로 보존 기간 시작</span><span class="sxs-lookup"><span data-stu-id="d1ea6-296">Start the retention period when labeled or based on an event</span></span> | <span data-ttu-id="d1ea6-297">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-297">No</span></span> | <span data-ttu-id="d1ea6-298">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-298">Yes</span></span> |
|<span data-ttu-id="d1ea6-299">처리 검토</span><span class="sxs-lookup"><span data-stu-id="d1ea6-299">Disposition review</span></span> | <span data-ttu-id="d1ea6-300">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-300">No</span></span>| <span data-ttu-id="d1ea6-301">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-301">Yes</span></span> |
|<span data-ttu-id="d1ea6-302">최대 7년 동안 처리 증명</span><span class="sxs-lookup"><span data-stu-id="d1ea6-302">Proof of disposition for up to 7 years</span></span> | <span data-ttu-id="d1ea6-303">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-303">No</span></span> |<span data-ttu-id="d1ea6-304">예, 항목이 레코드로 선언되는 경우</span><span class="sxs-lookup"><span data-stu-id="d1ea6-304">Yes, when item is declared a record</span></span>|
|<span data-ttu-id="d1ea6-305">보존될 항목 식별:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-305">Identify items subject to retention:</span></span> <br /> <span data-ttu-id="d1ea6-306">- 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="d1ea6-306">- Content Search</span></span> <br /> <span data-ttu-id="d1ea6-307">- 데이터 분류 페이지, 콘텐츠 탐색기, 활동 탐색기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-307">- Data classification page, content explorer, activity explorer</span></span> | <br /> <span data-ttu-id="d1ea6-308">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-308">No</span></span> <br /> <span data-ttu-id="d1ea6-309">아니요</span><span class="sxs-lookup"><span data-stu-id="d1ea6-309">No</span></span> | <br /> <span data-ttu-id="d1ea6-310">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-310">Yes</span></span> <br /> <span data-ttu-id="d1ea6-311">예</span><span class="sxs-lookup"><span data-stu-id="d1ea6-311">Yes</span></span>|

<span data-ttu-id="d1ea6-312">보존 정책과 보존 레이블을 모두 보완 보존 방법으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-312">Note that you can use both retention policies and retention labels as complementary retention methods.</span></span> <span data-ttu-id="d1ea6-313">예제:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-313">For example:</span></span>

1. <span data-ttu-id="d1ea6-314">콘텐츠를 마지막으로 수정한 후 5년이 지나면 콘텐츠를 자동으로 삭제하는 보존 정책을 만들고 구성하여, 모든 OneDrive 계정에 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-314">You create and configure a retention policy that automatically deletes content five years after it's last modified, and apply the policy to all OneDrive accounts.</span></span>

2. <span data-ttu-id="d1ea6-315">콘텐츠를 영구적으로 유지하는 보존 레이블을 만들고 구성하여, 모든 OneDrive 계정에 게시하는 레이블 정책에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-315">You create and configure a retention label that keeps content forever and add this to a label policy that you publish to all OneDrive accounts.</span></span> <span data-ttu-id="d1ea6-316">5년 후에 수정하지 않으면 자동 삭제에서 제외되어야 하는 특정 문서에 이 레이블을 수동으로 적용하는 방법을 사용자에게 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-316">You explain to users how to manually apply this label to specific documents that should be excluded from automatic deletion if not modified after five years.</span></span>

<span data-ttu-id="d1ea6-317">보존 정책과 보존 레이블이 함께 작동하는 방식과 결합된 결과를 결정하는 방법에 대한 자세한 내용은 보존 원칙과 우선하는 항목을 설명하는 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-317">For more information about how retention policies and retention labels work together and how to determine their combined outcome, see the next section that explains the principles of retention and what takes precedence.</span></span>

## <a name="the-principles-of-retention-or-what-takes-precedence"></a><span data-ttu-id="d1ea6-318">보존 원칙 또는 우선하는 항목</span><span class="sxs-lookup"><span data-stu-id="d1ea6-318">The principles of retention, or what takes precedence?</span></span>

<span data-ttu-id="d1ea6-319">콘텐츠에 작업(보존, 삭제 또는 보존 후 삭제) 및 보존 기간이 각기 다른 여러 보존 정책과 보존 레이블이 적용되어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-319">It's possible or even likely that content might have several retention policies and retention labels applied to it, each with a different action (retain, delete, or retain and then delete) and retention period.</span></span> <span data-ttu-id="d1ea6-320">우선하는 항목</span><span class="sxs-lookup"><span data-stu-id="d1ea6-320">What takes precedence?</span></span> 

<span data-ttu-id="d1ea6-321">높은 수준에서는 보존이 항상 삭제보다 우선하며 가장 긴 보존 기간이 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-321">At a high level, you can be assured that retention always takes precedence over deletion, and then the longest retention period wins.</span></span> 

<span data-ttu-id="d1ea6-322">그러나 여기에 몇 가지 요소를 더해야 하므로, 다음 흐름을 사용하여 각 수준이 위에서 아래로의 타이 브레이커 역할을 하는 결과를 이해하세요. 결과가 첫 번째 수준에 의해 결정되면 다음 수준으로 진행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-322">However, there are a few more factors to throw into the mix, so use the following flow to understand the outcome where each level acts as a tie-breaker from top to bottom: If the outcome is determined by the first level, there's no need to progress to the next level, and so on.</span></span> <span data-ttu-id="d1ea6-323">해당 수준에 대한 규칙에 따라 결과를 확인할 수 없는 경우에만 흐름이 다음 수준으로 이동하여 보존 설정의 우선순위를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-323">Only if the outcome can't be determined by the rules for the level does the flow move down to the next level to determine the outcome for which retention settings take precedence.</span></span>

![보존 원칙 다이어그램](../media/1693d6ec-b340-4805-9da3-89aa41bc6afb.png)
  
<span data-ttu-id="d1ea6-325">네 가지 수준에 대한 설명:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-325">Explanation for the four different levels:</span></span>
  
1. <span data-ttu-id="d1ea6-326">**삭제보다 보존 우선.**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-326">**Retention wins over deletion.**</span></span> <span data-ttu-id="d1ea6-327">한 보존 정책에서는 3년 후 Exchange 전자 메일을 삭제하도록 구성하지만 다른 보존 정책에서는 5년 동안 Exchange 전자 메일을 보존한 다음 삭제하도록 구성한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-327">Suppose that one retention policy is configured to delete Exchange email after three years, but another retention policy is configured to retain Exchange email for five years and then delete it.</span></span> <span data-ttu-id="d1ea6-328">3년에 도달하는 모든 콘텐츠는 삭제되고 사용자의 보기에서 숨겨지지만, 콘텐츠가 영구적으로 삭제되는 5년에 도달하기까지는 복구 가능한 항목 폴더에 여전히 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-328">Any content that reaches three years old will be deleted and hidden from the users' view, but still retained in the Recoverable Items folder until the content reaches five years old, when it is permanently deleted.</span></span> 
2. <span data-ttu-id="d1ea6-329">**가장 긴 보존 기간 우선.**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-329">**The longest retention period wins.**</span></span> <span data-ttu-id="d1ea6-330">콘텐츠가 다른 기간 동안 콘텐츠를 보존하는 여러 보존 설정의 적용을 받는 경우, 가장 긴 보존 기간이 끝날 때까지 콘텐츠는 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-330">If content is subject to multiple retention settings that retain content for different periods of time, the content will be retained until the end of the longest retention period.</span></span>
    
3. <span data-ttu-id="d1ea6-331">**암시적 포함보다 명시적 포함 우선.**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-331">**Explicit inclusion wins over implicit inclusion.**</span></span> <span data-ttu-id="d1ea6-332">의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-332">This means:</span></span> 
    
    1. <span data-ttu-id="d1ea6-333">보존 설정이 포함된 보존 레이블이 사용자에 의해 수동으로 항목(예: Exchange 전자 메일 또는 OneDrive 문서)에 할당된 경우, 해당 보존 레이블이 사이트 또는 사서함 수준에서 할당된 보존 정책이나 문서 라이브러리에 할당된 기본 보존 레이블보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-333">If a retention label with retention settings is manually assigned by a user to an item, such as an Exchange email or OneDrive document, that retention label takes precedence over both a retention policy assigned at the site or mailbox level and a default retention label assigned to the document library.</span></span> <span data-ttu-id="d1ea6-334">예를 들어 명시적 보존 레이블에서 10년 동안 콘텐츠를 보존하기로 구성하지만 사이트에 할당된 보존 정책에서 5년 동안만 콘텐츠를 보존하기로 구성한다면, 보존 레이블이 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-334">For example, if the explicit retention label is configured to retain content for ten years, but a retention policy assigned to the site is configured to retain content for only five years, the retention label takes precedence.</span></span> <span data-ttu-id="d1ea6-335">자동 적용 보존 레이블은 Microsoft 365에서 자동으로 적용하므로 명시적이 아니라 암시적으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-335">Auto-applied retention labels are considered implicit rather than explicit, because they're applied automatically by Microsoft 365.</span></span>
    
    2. <span data-ttu-id="d1ea6-336">보존 정책에 특정 사용자의 사서함 또는 OneDrive 계정과 같이 특정 위치가 포함되는 경우 해당 보존 정책이 모든 사용자의 사서함 또는 OneDrive 계정에 적용되지만 특히 해당 사용자의 사서함을 포함하지 않는 다른 보존 정책보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-336">If a retention policy includes a specific location, such as a specific user's mailbox or OneDrive account, that retention policy takes precedence over another retention policy that applies to all users' mailboxes or OneDrive accounts but doesn't specifically include that user's mailbox.</span></span>
    
4. <span data-ttu-id="d1ea6-337">**가장 짧은 삭제 기간이 우선합니다.**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-337">**The shortest deletion period wins.**</span></span> <span data-ttu-id="d1ea6-338">마찬가지로 콘텐츠에 보존 기간 없이 콘텐츠를 삭제하는 여러 보존 설정이 적용된 경우, 해당 콘텐츠는 가장 짧은 보존 기간이 끝나면 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-338">Similarly, if content is subject to multiple retention settings that delete content without a retention period, that content will be deleted at the end of the shortest retention period.</span></span> 

<span data-ttu-id="d1ea6-339">마지막으로, 보존 정책 또는 보존 레이블은 eDiscovery에 대해 보류된 모든 콘텐츠를 영구히 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-339">Finally, a retention policy or retention label cannot permanently delete any content that's on hold for eDiscovery.</span></span> <span data-ttu-id="d1ea6-340">보류가 해제되면 콘텐츠는 다시 워크로드의 보안 위치에서 정리 프로세스의 적용을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-340">When that hold is released, the content again becomes eligible for the cleanup process in the secured locations for the workload.</span></span>

## <a name="powershell-cmdlets-for-retention-policies-and-retention-labels"></a><span data-ttu-id="d1ea6-341">보존 정책 및 보존 레이블의 PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="d1ea6-341">PowerShell cmdlets for retention policies and retention labels</span></span>

<span data-ttu-id="d1ea6-342">보존 정책 cmdlet을 사용하려면 먼저 [Office 365 보안 및 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-342">To use the retention cmdlets, you must first [connect to the Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span> <span data-ttu-id="d1ea6-343">그런 다음, 다음 cmdlet 중 하나를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-343">Then, use any of the following cmdlets:</span></span>

- [<span data-ttu-id="d1ea6-344">Get-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="d1ea6-344">Get-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancetag)

- [<span data-ttu-id="d1ea6-345">New-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="d1ea6-345">New-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-compliancetag)

- [<span data-ttu-id="d1ea6-346">Remove-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="d1ea6-346">Remove-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-compliancetag)

- [<span data-ttu-id="d1ea6-347">Set-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="d1ea6-347">Set-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-compliancetag)

- [<span data-ttu-id="d1ea6-348">Enable-ComplianceTagStorage</span><span class="sxs-lookup"><span data-stu-id="d1ea6-348">Enable-ComplianceTagStorage</span></span>](https://docs.microsoft.com/powershell/module/exchange/enable-compliancetagstorage)

- [<span data-ttu-id="d1ea6-349">Get-ComplianceTagStorage</span><span class="sxs-lookup"><span data-stu-id="d1ea6-349">Get-ComplianceTagStorage</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancetagstorage)

- [<span data-ttu-id="d1ea6-350">Get-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="d1ea6-350">Get-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy)

- [<span data-ttu-id="d1ea6-351">New-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="d1ea6-351">New-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-retentioncompliancepolicy)

- [<span data-ttu-id="d1ea6-352">Remove-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="d1ea6-352">Remove-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-retentioncompliancepolicy)

- [<span data-ttu-id="d1ea6-353">Set-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="d1ea6-353">Set-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy)

- [<span data-ttu-id="d1ea6-354">Get-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="d1ea6-354">Get-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancerule)

- [<span data-ttu-id="d1ea6-355">New-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="d1ea6-355">New-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-retentioncompliancerule)

- [<span data-ttu-id="d1ea6-356">Remove-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="d1ea6-356">Remove-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-retentioncompliancerule)

- [<span data-ttu-id="d1ea6-357">Set-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="d1ea6-357">Set-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancerule)

## <a name="use-retention-policies-and-retention-labels-instead-of-older-features"></a><span data-ttu-id="d1ea6-358">이전 기능 대신 보존 정책 및 보존 레이블 사용하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-358">Use retention policies and retention labels instead of older features</span></span>

<span data-ttu-id="d1ea6-359">정보 거버넌스를 위해 Microsoft 365에서 콘텐츠를 사전에 보존하거나 삭제해야 하는 경우에는 다음과 같은 이전 기능 대신 보존 정책 및 보존 레이블을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-359">If you need to proactively retain or delete content in Microsoft 365 for information governance, we recommend that you use retention policies and retention labels instead of the following older features.</span></span> 
  
<span data-ttu-id="d1ea6-360">현재 이러한 이전 기능을 사용하는 경우 해당 기능은 보존 정책 및 레이블과 함께 계속해서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-360">If you currently use these older features, they will continue to work side-by-side with retention policies and retention labels.</span></span> <span data-ttu-id="d1ea6-361">하지만 앞으로는 보존 정책 및 보존 레이블을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-361">However, we recommend that going forward, you use retention policies and retention labels instead.</span></span> <span data-ttu-id="d1ea6-362">Microsoft 365 전체에서 콘텐츠의 보존 및 삭제를 중앙에서 관리하는 단일 메커니즘을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-362">They provide you with a single mechanism to centrally manage both retention and deletion of content across Microsoft 365.</span></span>

<span data-ttu-id="d1ea6-363">**Exchange Online의 이전 기능:**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-363">**Older features from Exchange Online:**</span></span>

- <span data-ttu-id="d1ea6-364">[원본 위치 유지 및 소송 보존](https://go.microsoft.com/fwlink/?linkid=846124)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-364">[In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/?linkid=846124) (eDiscovery hold)</span></span> 

- [<span data-ttu-id="d1ea6-365">Exchange Online 사서함의 보류 유형을 식별하는 방법</span><span class="sxs-lookup"><span data-stu-id="d1ea6-365">How to identify the type of hold placed on an Exchange Online mailbox</span></span>](identify-a-hold-on-an-exchange-online-mailbox.md)
    
- <span data-ttu-id="d1ea6-366">[보존 태그 및 보존 정책](https://go.microsoft.com/fwlink/?linkid=846125), [[MRM(메시징 레코드 관리)](https://go.microsoft.com/fwlink/?linkid=846126)라고도 함(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-366">[Retention tags and retention policies](https://go.microsoft.com/fwlink/?linkid=846125), also known as [messaging records management (MRM)](https://go.microsoft.com/fwlink/?linkid=846126) (deletion only)</span></span>
    
<span data-ttu-id="d1ea6-367">또한 [레거시 eDiscovery 도구의 사용 중지](legacy-ediscovery-retirement.md)도 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-367">See also [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md).</span></span>


<span data-ttu-id="d1ea6-368">**SharePoint 및 OneDrive의 이전 기능:**</span><span class="sxs-lookup"><span data-stu-id="d1ea6-368">**Older features from SharePoint and OneDrive:**</span></span>

- <span data-ttu-id="d1ea6-369">[eDiscovery 센터에서 사례에 콘텐츠 추가 및 원본 우 위치 유지](https://docs.microsoft.com/SharePoint/governance/add-content-to-a-case-and-place-sources-on-hold-in-the-ediscovery-center)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-369">[Add content to a case and place sources on hold in the eDiscovery Center](https://docs.microsoft.com/SharePoint/governance/add-content-to-a-case-and-place-sources-on-hold-in-the-ediscovery-center) (eDiscovery hold)</span></span> 
    
- <span data-ttu-id="d1ea6-370">[문서 삭제 정책](https://support.office.com/article/Create-a-document-deletion-policy-in-SharePoint-Server-2016-4fe26e19-4849-4eb9-a044-840ab47458ff)(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-370">[Document deletion policies](https://support.office.com/article/Create-a-document-deletion-policy-in-SharePoint-Server-2016-4fe26e19-4849-4eb9-a044-840ab47458ff) (deletion only)</span></span>
    
- <span data-ttu-id="d1ea6-371">[현재 위치 레코드 관리 구성](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (보존만 해당)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-371">[Configuring in place records management](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (retention only)</span></span> 
    
- <span data-ttu-id="d1ea6-372">[사이트 폐쇄 및 삭제에 대한 정책 사용](https://support.microsoft.com/ko-KR/office/use-policies-for-site-closure-and-deletion-a8280d82-27fd-48c5-9adf-8a5431208ba5) (삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-372">[Use policies for site closure and deletion](https://support.microsoft.com/ko-KR/office/use-policies-for-site-closure-and-deletion-a8280d82-27fd-48c5-9adf-8a5431208ba5) (deletion only)</span></span> 
    
- <span data-ttu-id="d1ea6-373">[정보 관리 정책](intro-to-info-mgmt-policies.md) (삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="d1ea6-373">[Information management policies](intro-to-info-mgmt-policies.md) (deletion only)</span></span>
     
<span data-ttu-id="d1ea6-374">이전에 정보 거버넌스 용도로 eDiscovery 보류를 사용한 적이 있는 경우 사전 규정 준수를 위해 보존 정책을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-374">If you've previously used any of the eDiscovery holds for the purpose of information governance, for proactive compliance, use a retention policy instead.</span></span> <span data-ttu-id="d1ea6-375">보류 전용으로 eDiscovery를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-375">Use eDiscovery for holds only.</span></span>
  
### <a name="retention-policies-and-sharepoint-content-type-policies-or-information-management-policies"></a><span data-ttu-id="d1ea6-376">보존 정책 및 SharePoint 콘텐츠 유형 정책 또는 정보 관리 정책</span><span class="sxs-lookup"><span data-stu-id="d1ea6-376">Retention policies and SharePoint content type policies or information management policies</span></span>

<span data-ttu-id="d1ea6-377">콘텐츠 유형 정책 또는 정보 관리 정책에 대해 SharePoint 사이트를 구성하여 목록이나 라이브러리에 대한 콘텐츠를 보존하는 경우 보존 정책이 유효하는 동안 해당 정책은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-377">If you have configured SharePoint sites for content type policies or information management policies to retain content for a list or library, those policies are ignored while a retention policy is in effect.</span></span> 

## <a name="related-information"></a><span data-ttu-id="d1ea6-378">관련 정보</span><span class="sxs-lookup"><span data-stu-id="d1ea6-378">Related information</span></span>

- [<span data-ttu-id="d1ea6-379">SharePoint Online 제한 사항</span><span class="sxs-lookup"><span data-stu-id="d1ea6-379">SharePoint Online Limits</span></span>](https://docs.microsoft.com/office365/servicedescriptions/sharepoint-online-service-description/sharepoint-online-limits)
- [<span data-ttu-id="d1ea6-380">Microsoft Teams의 제한 사항 및 사양</span><span class="sxs-lookup"><span data-stu-id="d1ea6-380">Limits and specifications for Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/limits-specifications-teams) 
- [<span data-ttu-id="d1ea6-381">SEC 규칙 17a-4 준수</span><span class="sxs-lookup"><span data-stu-id="d1ea6-381">Comply with SEC Rule 17a-4</span></span>](use-exchange-online-to-comply-with-sec-rule-17a-4.md)

## <a name="next-steps"></a><span data-ttu-id="d1ea6-382">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d1ea6-382">Next steps</span></span>

<span data-ttu-id="d1ea6-383">보존 정책을 만들 준비가 되었으면 [보존 정책 만들기 및 구성하기](create-retention-policies.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ea6-383">If you are ready to create retention policies, see [Create and configure retention policies](create-retention-policies.md).</span></span>

<span data-ttu-id="d1ea6-384">보존 레이블을 만들고 적용하려면:</span><span class="sxs-lookup"><span data-stu-id="d1ea6-384">To create and apply retention labels:</span></span>
- [<span data-ttu-id="d1ea6-385">보존 레이블을 만들고 앱에 적용하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-385">Create retention labels and apply them in apps</span></span>](create-apply-retention-labels.md)
- [<span data-ttu-id="d1ea6-386">보존 레이블을 콘텐츠에 자동으로 적용하기</span><span class="sxs-lookup"><span data-stu-id="d1ea6-386">Apply a retention label to content automatically</span></span>](apply-retention-labels-automatically.md)
