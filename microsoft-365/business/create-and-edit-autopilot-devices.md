---
title: AutoPilot 장치 만들기 및 편집
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0f7b1d7c-4086-4331-8534-45d7886f9f34
description: Microsoft 365 Business Premium에서 AutoPilot을 사용 하 여 장치를 업로드 하는 방법을 알아봅니다. 장치 또는 장치 그룹에 프로필을 할당할 수 있습니다.
ms.openlocfilehash: 8c3d029d682ae30444bdc7d30a4790a8f982e0e0
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400997"
---
# <a name="create-and-edit-autopilot-devices"></a>AutoPilot 장치 만들기 및 편집

## <a name="upload-a-list-of-devices"></a>장치 목록 업로드

단계별 [가이드](add-autopilot-devices-and-profile.md) 를 사용 하 여 장치를 업로드할 수 있지만 **장치 탭에서** 장치를 업로드할 수도 있습니다. 
  
장치는 다음 요구 사항을 충족 해야 합니다.
  
- Windows 10, 버전 1703 이상
    
- Windows 기본 경험을 거치지 않은 새로운 장치

1. Microsoft 365 관리 센터에서 **장치** \> **AutoPilot**을 선택 합니다.
  
2. **AutoPilot** 페이지에서 **장치** 탭 \> **장치 추가**를 선택 합니다.
    
    ![In the Devices tab, choose Add devices.](../media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. **장치 추가** 패널에서 닫기 저장을 준비한 [장치 목록 CSV 파일](https://docs.microsoft.com/microsoft-365/admin/misc/device-list) 을 찾습니다 \> **Save** \> **Close**.
    
    하드웨어 공급 업체에서이 정보를 가져오거나 [Get-windowsautopilotinfo PowerShell 스크립트](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) 를 사용 하 여 CSV 파일을 생성할 수 있습니다. 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a>장치 또는 장치 그룹에 프로필 할당

1. **Windows 준비** 페이지에서 **장치** 탭을 선택 하 고 하나 이상의 장치 옆에 있는 확인란을 선택 합니다. 
    
2. **장치** 패널의 **할당된 프로필** 드롭다운에서 프로필을 선택합니다. 
    
    아직 프로필이 없는 경우 지침은 [AutoPilot 프로필 만들기 및 편집](create-and-edit-autopilot-profiles.md)을 참조하세요. 
    
