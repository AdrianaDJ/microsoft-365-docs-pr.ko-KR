---
title: 간결한 팝업을 사용 하 여 메일 메시지를 읽을 때 사용 되는 메모리 줄이기
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 12/3/2019
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a6d6ba01-2562-4c3d-a8f1-78748dd506cf
f1.keywords:
- NOCSH
description: 이 문서에서는 간결한 팝업을 사용 하 여 웹에서 Outlook의 메시지 다운로드 성능을 개선 하는 방법에 대해 설명 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 7bf53464ac6b2783fbbfc335fd4ff73dbe4435fb
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692778"
---
# <a name="use-lean-popouts-to-reduce-memory-used-when-reading-mail-messages"></a><span data-ttu-id="57702-103">간결한 팝업을 사용 하 여 메일 메시지를 읽을 때 사용 되는 메모리 줄이기</span><span class="sxs-lookup"><span data-stu-id="57702-103">Use lean popouts to reduce memory used when reading mail messages</span></span>

<span data-ttu-id="57702-104">이 문서에서는 웹용 Outlook에서 메시지 다운로드 성능을 개선 하기 위한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="57702-104">This article contains information for improving message download performance in Outlook on the web.</span></span> <span data-ttu-id="57702-105">이 문서는 [Office 365 프로젝트에 대 한 네트워크 계획 및 성능 조정](https://aka.ms/tune) 의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="57702-105">This article is part of the [Network planning and performance tuning for Office 365](https://aka.ms/tune) project.</span></span>
  
<span data-ttu-id="57702-106">Office 365 전역 관리자는 Microsoft Edge 또는 Internet Explorer에서 비교적 작고 메모리를 많이 사용 하는 특정 전자 메일 메시지에 대 한 _간결한 팝업_를 제공 하도록 웹에서 Outlook을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57702-106">As an Office 365 global administrator, you can configure Outlook on the web to deliver _lean popouts_, a smaller, less memory-intensive version of certain email messages in Microsoft Edge or Internet Explorer.</span></span> <span data-ttu-id="57702-107">웹에서 Outlook에 대해 간결한 팝업를 구성 하면 성능을 최적화 하는 서버 쪽 렌더링 된 구성 요소가 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57702-107">When lean popouts are configured for Outlook on the web, server-side rendered components are loaded that optimize performance.</span></span>
  
> [!NOTE]
> <span data-ttu-id="57702-108">3 월 2018 일에, IRM (정보 권한 관리)과 같은 사용 권한 제한을 지정 하는 메시지에는 팝업을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57702-108">As of March 2018, lean popouts are not available for messages that specify usage rights restrictions, such as Information Rights Management (IRM).</span></span>
  
<span data-ttu-id="57702-109">이러한 기능은 주 창에서 계속 작동 하지만 간결한 팝업에서는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57702-109">These features will continue to work in the main window but are not available in lean popouts:</span></span>
  
- <span data-ttu-id="57702-110">Outlook 추가 기능</span><span class="sxs-lookup"><span data-stu-id="57702-110">Outlook add-ins</span></span>
  
- <span data-ttu-id="57702-111">비즈니스용 Skype 현재 상태</span><span class="sxs-lookup"><span data-stu-id="57702-111">Skype for Business presence</span></span>
  
## <a name="to-configure-lean-popouts-for-all-users-within-your-office-365-organization"></a><span data-ttu-id="57702-112">Office 365 조직 내의 모든 사용자에 대해 간결한 팝업를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="57702-112">To configure lean popouts for all users within your Office 365 organization</span></span>
  
1. <span data-ttu-id="57702-113">[원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx )합니다.</span><span class="sxs-lookup"><span data-stu-id="57702-113">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx ).</span></span>
  
2. <span data-ttu-id="57702-114">다음과 같이 LeanPopoutEnabled 매개 변수를 사용 하 여 [set-organizationconfig](https://technet.microsoft.com/library/aa997443%28v=exchg.160%29.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="57702-114">Run the [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443%28v=exchg.160%29.aspx) cmdlet with the LeanPopoutEnabled parameter as follows:</span></span>

  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled <$true |$false >
  ```

  <span data-ttu-id="57702-115">예를 들어 조직의 모든 사용자에 대해 간결한 팝업을 사용 하도록 설정 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="57702-115">For example, to enable lean popouts for all users in your organization:</span></span>
  
  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled $true
  ```

  <span data-ttu-id="57702-116">조직의 모든 사용자에 대해 간결한 팝업을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="57702-116">To disable lean popouts for all users in your organization:</span></span>

  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled $false
  ```