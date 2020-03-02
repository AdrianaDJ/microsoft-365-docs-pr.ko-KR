---
title: Windows 장치에서 Office 2013에 대해 최신 인증 사용
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
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7dc1c01a-090f-4971-9677-f1b192d6c910
description: Microsoft Office 2013이 설치 된 장치에 대해 최신 인증을 사용 하도록 레지스트리 키를 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: f1264affa5be93b19e564a0edea00bfb78f452f1
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42248006"
---
# <a name="enable-modern-authentication-for-office-2013-on-windows-devices"></a>Windows 장치에서 Office 2013에 대해 최신 인증 사용

Office 2013이 설치되어 있는 Windows 장치에 대해 최신 인증을 사용하려면 특정 레지스트리 키를 설정해야 합니다.
  
## <a name="enable-modern-authentication-for-office-2013-clients"></a>Office 2013 클라이언트에 대해 최신 인증 사용

> [!NOTE]
> Office 2016 클라이언트에 대해 이미 최신 인증이 사용되고 있는 경우 Office 2016에 대해 레지스트리 키를 설정할 필요가 없습니다. 
  
Microsoft Office 2013이 설치되었고 Windows를 실행 중인 장치(예: 노트북 및 태블릿)에 대해 최신 인증을 사용하려면 다음 레지스트리 키를 설정해야 합니다. 최신 인증을 사용할 각 장치에서 키를 설정해야 합니다.
  
|**레지스트리 키**|**유형**|**값** |
|:-------|:------:|--------:|
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL  |REG_DWORD  |개  |
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\Version |REG_DWORD |개 |
   
레지스트리 키를 설정했으면 Office 365와 함께 [MFA(다단계 인증)](set-up-multi-factor-authentication.md)를 사용하도록 Office 2013 장치 앱을 설정할 수 있습니다. 
  
현재 클라이언트 앱에 로그인한 경우 변경 내용을 적용하려면 로그아웃 후 다시 로그인해야 합니다. 그러지 않으면 ADAL ID가 설정될 때까지 MRU 및 로밍 설정을 사용할 수 없습니다.
  
## <a name="disable-modern-authentication-on-devices"></a>장치에서 최신 인증을 사용하지 않음

장치에서 최신 인증을 사용하지 않으려면 장치의 다음 레지스트리 키를 설정합니다.
  
|**레지스트리 키**|**유형**|**값**|
|:-------|:------:|--------:|
|HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL |REG_DWORD|개|
   
## <a name="related-articles"></a>관련 문서
[두 번째 확인 방법으로 Office 2013에 로그인](https://support.office.com/article/2b856342-170a-438e-9a4f-3c092394d3cb.aspx)

  
