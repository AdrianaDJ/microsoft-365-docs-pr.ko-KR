---
title: PowerShell을 사용 하 여 SharePoint Online 사이트 그룹 관리
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/17/2019
audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- PowerShell
- Ent_Office_Other
- SPO_Content
- seo-marvel-apr2020
ms.assetid: d0d3877a-831f-4744-96b0-d8167f06cca2
description: 이 문서에서는 Microsoft 365 용 PowerShell을 사용 하 여 SharePoint Online 사이트 그룹을 관리 하는 절차를 알아봅니다.
ms.openlocfilehash: fa9aff769ff84f8567c45b20c7b6c8a078b4a70c
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692748"
---
# <a name="manage-sharepoint-online-site-groups-with-powershell"></a>PowerShell을 사용 하 여 SharePoint Online 사이트 그룹 관리

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Microsoft 365 관리 센터를 사용할 수도 있지만 Microsoft 365 용 PowerShell을 사용 하 여 SharePoint Online 사이트 그룹을 관리할 수도 있습니다.

## <a name="before-you-begin"></a>시작하기 전에

이 문서의 절차를 수행 하려면 SharePoint Online에 연결 해야 합니다. 자세한 내용은 [SharePoint Online PowerShell에 연결을](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)참조 하세요.

## <a name="view-sharepoint-online-with-powershell-for-microsoft-365"></a>Microsoft 365 용 PowerShell을 사용 하 여 SharePoint Online 보기

SharePoint Online 관리 센터에는 사이트 그룹을 관리 하기 위한 사용 하기 쉬운 몇 가지 방법이 있습니다. 예를 들어 사이트의 그룹 및 그룹 구성원을 확인 하려는 경우를 가정해 보겠습니다 `https://litwareinc.sharepoint.com/sites/finance` . 수행 해야 하는 작업은 다음과 같습니다.

1. SharePoint 관리 센터에서 **활성 사이트**를 클릭 한 다음 사이트의 URL을 클릭 합니다.
2. 사이트 페이지에서 페이지 오른쪽 위 모서리에 있는 **설정** 아이콘을 클릭 한 다음 **사이트 사용 권한을**클릭 합니다.

확인하려는 다음 사이트에 대해 프로세스를 반복합니다.

Microsoft 365 용 PowerShell을 사용 하 여 그룹 목록을 가져오려면 다음 명령을 사용할 수 있습니다.

```powershell
$siteURL = "https://litwareinc.sharepoint.com/sites/finance"
$x = Get-SPOSiteGroup -Site $siteURL
foreach ($y in $x)
    {
        Write-Host $y.Title -ForegroundColor "Yellow"
        Get-SPOSiteGroup -Site $siteURL -Group $y.Title | Select-Object -ExpandProperty Users
        Write-Host
    }
```

SharePoint Online 관리 셸 명령 프롬프트에서이 명령 집합을 실행 하는 방법에는 두 가지가 있습니다.

- 메모장 (또는 다른 텍스트 편집기)에 명령을 복사 하 고 **$siteURL** 변수의 값을 수정한 다음 명령을 선택 하 여 SharePoint Online 관리 셸 명령 프롬프트에 붙여 넣습니다. 이렇게 하면 PowerShell이 프롬프트에서 중지 됩니다 **>>** . Enter 키를 눌러 `foreach` 명령을 실행 합니다.<br/>
- 메모장 (또는 다른 텍스트 편집기)에 명령을 복사 하 고 **$siteURL** 변수의 값을 수정한 다음이 텍스트 파일을 적절 한 폴더에 이름을 지정 하 고 ps1 확장명을 사용 하 여 저장 합니다. 다음으로, 경로와 파일 이름을 지정 하 여 SharePoint Online 관리 셸 명령 프롬프트에서 스크립트를 실행 합니다. 예제 명령은 다음과 같습니다.

```powershell
C:\Scripts\SiteGroupsAndUsers.ps1
```

두 경우 모두에 다음과 같은 내용이 표시 됩니다.

![SharePoint Online 사이트 그룹](../media/SPO-site-groups.png)

사이트에 대해 만들어진 모든 그룹 `https://litwareinc.sharepoint.com/sites/finance` 및 해당 그룹에 할당 된 모든 사용자입니다. 그룹 이름은 노란색으로 되어 그룹 이름을 해당 구성원 으로부터 구분 하는 데 도움이 됩니다.

또 다른 예로, 모든 SharePoint Online 사이트에 대 한 그룹 및 모든 그룹 구성원 자격이 나열 된 명령 집합입니다.

```powershell
$x = Get-SPOSite
foreach ($y in $x)
    {
        Write-Host $y.Url -ForegroundColor "Yellow"
        $z = Get-SPOSiteGroup -Site $y.Url
        foreach ($a in $z)
            {
                 $b = Get-SPOSiteGroup -Site $y.Url -Group $a.Title 
                 Write-Host $b.Title -ForegroundColor "Cyan"
                 $b | Select-Object -ExpandProperty Users
                 Write-Host
            }
    }
```
    
## <a name="see-also"></a>참고 항목

[SharePoint Online PowerShell에 연결](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[SharePoint Online 사이트 만들기 및 PowerShell을 사용 하 여 사용자 추가](create-sharepoint-sites-and-add-users-with-powershell.md)

[PowerShell을 사용 하 여 SharePoint Online 사용자 및 그룹 관리](manage-sharepoint-users-and-groups-with-powershell.md)

[PowerShell로 Microsoft 365 관리](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[Microsoft 365 용 PowerShell 시작](getting-started-with-microsoft-365-powershell.md)

