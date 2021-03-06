---
title: 핵심 eDiscovery 사례의 제한
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: 이 문서에서는 Microsoft 365의 핵심 eDiscovery 사례에 대 한 제한 사항에 대해 설명 합니다.
ms.openlocfilehash: 6224ce5ecb8fc0439e43ab5e1362f8a618194202
ms.sourcegitcommit: 9ce9001aa41172152458da27c1c52825355f426d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2020
ms.locfileid: "47358516"
---
# <a name="limits-in-core-ediscovery"></a>핵심 eDiscovery의 제한 사항

다음 표에서는 핵심 ediscovery 사례와 관련 된 핵심 eDiscovery 사례 및 보류에 대 한 제한을 보여 줍니다. 핵심 eDiscovery에 대 한 자세한 내용은 [Core Ediscovery 개요](ediscovery-cases.md)를 참조 하세요.
    
  |**제한 설명**|**제한 유형**|
  |:-----|:-----|
  |조직의 최대 사례 수  <br/> |제한 없음  <br/> |
  |조직에 대 한 최대 사례 보존 수  <br/> |10,000  <br/> |
  |단일 케이스 보류의 최대 사서함 수  <br/> |1,000  <br/> |
  |단일 케이스 보류에서의 최대 SharePoint 및 비즈니스용 OneDrive 사이트 수  <br/> |100  <br/> |
  |핵심 eDiscovery 홈 페이지에 표시 되는 최대 사례 수 및 사례 내의 보류, 검색 및 내보내기 탭에 표시 되는 최대 항목 수입니다. <sup>1</sup> |1,000|
  |||

   > [!NOTE]
   > <sup>1</sup> 1000 개 보다 많은 사례, 보류 중, 검색 또는 내보내기의 목록을 보려면 해당 Office 365 Security & 준수 PowerShell cmdlet을 사용할 수 있습니다.<br/> [Remove-compliancecase](https://docs.microsoft.com/powershell/module/exchange/get-compliancecase) <br/> [New-caseholdpolicy](https://docs.microsoft.com/powershell/module/exchange/get-caseholdpolicy)<br/> [Get-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/get-compliancesearch)<br/> [New-compliancesearchaction](https://docs.microsoft.com/powershell/module/exchange/get-compliancesearchaction)
