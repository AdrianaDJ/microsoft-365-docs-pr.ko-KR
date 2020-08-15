---
title: SharePoint 사이트 콘텐츠를 지리적 위치로 제한
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.collection: Strat_SP_gtc
localization_priority: Normal
description: 이 문서에서는 여러 지리적 환경에서 SharePoint 사이트를 지정 된 지리적 위치로 제한 하는 방법을 알아봅니다.
ms.openlocfilehash: f2a09f177c68d30121c207287e053b2b25405fbc
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692354"
---
# <a name="restrict-sharepoint-site-content-to-a-geo-location"></a><span data-ttu-id="1a79f-103">SharePoint 사이트 콘텐츠를 지리적 위치로 제한</span><span class="sxs-lookup"><span data-stu-id="1a79f-103">Restrict SharePoint site content to a geo location</span></span>

<span data-ttu-id="1a79f-104">상황에 따라 사이트가 이동되지 않도록 하거나 다른 지리적 위치에 있는 사이트의 파일 콘텐츠를 캐싱하지 못하게 하여 사이트가 만들어진 위치에 남아 있도록 사이트와 파일 콘텐츠를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-104">Under some circumstances you may choose to enforce a site and its file content to remain in the geo location where the site was created, either by preventing the site from being moved or by preventing the caching of the site's file content in another geo location.</span></span>

<span data-ttu-id="1a79f-105">[Set-SPOSite](https://docs.microsoft.com/powershell/module/sharepoint-online/set-sposite) cmdlet을 **RestrictedToGeo** 매개 변수와 함께 사용하여 이 작업을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-105">You can do this by using the [Set-SPOSite](https://docs.microsoft.com/powershell/module/sharepoint-online/set-sposite) cmdlet with the **RestrictedToGeo** parameter.</span></span> <span data-ttu-id="1a79f-106">이 매개 변수의 기본값은 NULL이지만 다음 중 하나로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-106">This parameter has a default value of NULL, but you can change it to one of the following:</span></span>

|<span data-ttu-id="1a79f-107">제한</span><span class="sxs-lookup"><span data-stu-id="1a79f-107">Restriction</span></span>|<span data-ttu-id="1a79f-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a79f-108">Description</span></span>|
|:----------|:----------|
|<span data-ttu-id="1a79f-109">NoRestriction</span><span class="sxs-lookup"><span data-stu-id="1a79f-109">NoRestriction</span></span>|<span data-ttu-id="1a79f-110">사이트를 다른 지리적 위치로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-110">The site can be moved to another geo location.</span></span>|
|<span data-ttu-id="1a79f-111">BlockMoveOnly</span><span class="sxs-lookup"><span data-stu-id="1a79f-111">BlockMoveOnly</span></span>|<span data-ttu-id="1a79f-112">사이트를 다른 지리적 위치로 이동할 수는 없지만 사이트 콘텐츠는 다른 지리적 위치에 캐시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-112">Site cannot be moved to another geo location, but site content can be cached in other geo locations.</span></span>|
|<span data-ttu-id="1a79f-113">BlockFull</span><span class="sxs-lookup"><span data-stu-id="1a79f-113">BlockFull</span></span>|<span data-ttu-id="1a79f-114">사이트를 다른 지리적 위치로 이동할 수 없으며 전체 파일 콘텐츠는 다른 지리적 위치에 캐시될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-114">Site cannot be moved to another geo location, and full file content is not cached in other geo locations.</span></span> <span data-ttu-id="1a79f-115">파일의 제목(콘텐츠에서 수집), 파일 이름 및 파일의 기타 속성은 다른 지리적 위치에 계속 캐시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-115">Files' title (harvested from the content), file name, and other properties of the file can still be cached in other geo-locations.</span></span><br><span data-ttu-id="1a79f-116">BlockFull로 구성되기 전에 사이트에 저장된 콘텐츠는 다른 지역의 위치에 계속 캐시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-116">Content stored in the site before it was configured to BlockFull, may continue to be cached in other geo locations.</span></span>|

<span data-ttu-id="1a79f-117">다음 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-117">Use the following syntax:</span></span>

`Set-SPOSite -Identity <siteURL> -RestrictedToGeo <restriction>`

<span data-ttu-id="1a79f-118">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a79f-118">For example:</span></span>

`Set-SPOSite -Identity https://contoso.sharepoint.com/sites/RegionRestrictedTeamSite -RestrictedToGeo BlockFull`