---
title: 비즈니스용 Microsoft 365에서 Office 클라이언트 배포 준비
f1.keywords:
- CSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.date: 10/31/2017
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: M365-subscription-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: ed34fff3-2881-4ed4-9906-1ba6bb8dd804
description: Windows 10 컴퓨터에 32 비트 Office 앱을 자동으로 설치 하 고 업데이트 된 상태로 유지 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 2de492914edbde2afe593aac290c4a634b801443
ms.sourcegitcommit: 2d664a95b9875f0775f0da44aca73b16a816e1c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/01/2020
ms.locfileid: "44470950"
---
# <a name="prepare-for-office-client-deployment-by-microsoft-365-for-business"></a>비즈니스용 Microsoft 365에서 Office 클라이언트 배포 준비

이 문서는 Microsoft 365 Business Premium에 적용 됩니다.

## <a name="prepare-to-automatically-install-office-apps-to-client-computers"></a>클라이언트 컴퓨터에 Office 앱 자동 설치 준비

Microsoft 365 Business Premium을 사용 하 여 Windows 10 컴퓨터에 32 비트 Office 앱을 자동으로 설치 하 고 업데이트를 최신 상태로 유지할 수 있습니다.
  
최종 사용자의 컴퓨터가 Windows 10 Business에 있고 다음을 수행 하는 경우 자동 설치가 가장 효율적으로 작동 합니다.
  
- 기존 Office 데스크톱 앱(Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access, 및 OneDrive)이 없는 경우
    
    또는
    
- 기존 간편 실행 버전의 Office가 설치된 경우
    
간편 실행 버전의 Office가 있는지 확인하려는 경우 Office 앱에서 **파일** \> **계정**(Outlook에서는 **Office 계정**)으로 이동합니다. 다음 그림에 표시 된 것 처럼 **Office 업데이트가** 표시 되 면 간편 실행을 사용 하 여 설치를 완료 한 것입니다. 
  
![Screenshot of Office updates in Office app Account](../media/e3439380-fa43-4ed6-ae5d-64851c297df5.png)
  
 **이 기능이 제공 되는 사용자의 혜택**
  
다음과 같은 PC 환경을 사용하는 최종 사용자에게 유용합니다.
  
- Windows 10 Business 사용자 라이선스, 비즈니스 라이선스에 대 한 활성 Microsoft 365, Windows 10 크리에이터 업데이트 및 Azure Active Directory에 가입 **되어 있습니다.** 
    
- 64 비트 Office 앱 (예: Word, Excel, PowerPoint)이 **없는** 경우 64 비트 Office 앱이 필요한 경우 365 Microsoft for business 관리 콘솔에서 64 비트 2016 간편 실행 버전의 Office를 트리거하는 것은 지원 되지 않으므로이 기능은 적합 하지 않습니다. 
    
- 2016 Windows Installer(MSI) 독립 실행형 앱(예: Visio 또는 Project)을 **보유하지 않은** 경우. 비즈니스용 마이크로소프트 365 office 2016의 간편 실행 버전으로 Office를 업그레이드 하며 Office 2016 MSI 독립 실행형 앱에서는 작동 하지 않습니다. 
    
다음 표에는 Microsoft 365 for business 관리 콘솔에서 Office 배포의 성공적인 32 비트 간편 실행 버전을 구현 하기 위해 최종 사용자/관리자가 시작 상태에 따라 수행 해야 할 수 있는 작업이 나와 있습니다.
  
|**Office 설치 시작 상태**|**Microsoft 365 for business Office 설치 전 수행 해야 하는 작업**|**종료 상태**|
|:-----|:-----|:-----|
|설치된 Office 제품군이 없는 경우  <br/> |없음  <br/> |간편 실행을 사용 하 여 Office 2016 32-비트를 설치 합니다.  <br/> |
|간편 실행 32비트 버전의 Office(2016 이하)가 있고 독립 실행형 앱이 없는 경우  <br/> |없음  <br/> |Upgraded to the latest 32-bit Click-to-Run version of Office 2016, as needed **\*** <br/> |
|기존 간편 실행 32 비트 버전의 Office 및 간편 실행 32 비트 또는 64 비트 독립 실행형 Office 앱 (예: Visio, Project)  <br/> |없음  <br/> |독립 실행형 앱은 영향을 받지 않습니다. 제품군이 간편 실행 32비트 버전의 Office 2016으로 업그레이드됩니다.  <br/> |
|간편 실행 32비트 버전의 Office 및 32비트 또는 64비트(2016 제외) MSI 독립 실행형 Office 앱이 있는 경우  <br/> |없음  <br/> |독립 실행형 앱은 영향을 받지 않습니다. 제품군이 간편 실행 32비트 버전의 Office 2016으로 업그레이드됩니다.  <br/> ||||
|간편 실행 64비트 버전의 Office가 있는 경우  <br/> |32 비트 Office 앱으로 교체 하는 것이 확인 된 경우 64 비트 Office 앱을 제거 합니다.  <br/> |Office 64비트 앱이 제거된 경우 간편 실행 32비트 버전의 Office 2016이 설치됩니다.  <br/> |
|독립 실행형 앱 유무와 상관없이 Office 2016의 MSI 설치가 있는 경우  <br/> |MSI Office 2016을 제거합니다.  <br/> |간편 실행 32비트 버전의 Office 2016이 설치됩니다. 독립 실행형 앱은 변경되지 않습니다.  <br/> |
|Office 2013(또는 이전 버전)의 MSI 설치 및/또는 독립 실행형 Office 앱이 있는 경우  <br/> |없음  <br/> |기존 MSI Office 설치가 포함된 간편 실행 32비트 버전의 Office 2016과 독립 실행형 앱이 함께 존재합니다.  <br/> |
||||
   
 **(\*) 참고:** 알려진 버그로 인해 간편 실행 32비트 버전의 Office 2016으로 업그레이드되지 않습니다. 수정이 진행 중입니다. 
  
