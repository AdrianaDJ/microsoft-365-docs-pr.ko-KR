---
title: Microsoft 365의 테 넌 트 격리
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
description: 이 문서에서는 Microsoft 365와 같은 클라우드 서비스에서 테 넌 트 격리를 적용 하는 방법에 대 한 요약 정보를 포함 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c9af522c71f3b089c8f2f198f861bcac8a0011a2
ms.sourcegitcommit: 11d1044c6600b1f568b6dc8a53db9b07f2f0ad1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48384940"
---
# <a name="tenant-isolation-in-microsoft-365"></a>Microsoft 365의 테 넌 트 격리

클라우드 컴퓨팅의 주요 장점 중 하나는 다 수의 고객이 동시에 공유 공통 인프라를 확장 하는 개념입니다. 이 개념을 *다중 테 넌 시*라고 합니다. Microsoft는 클라우드 서비스의 다중 테 넌 트 아키텍처에서 엔터프라이즈 수준의 보안, 기밀성, 개인 정보, 무결성 및 가용성 표준을 지원 하는지 확인 하기 위해 지속적으로 작동 합니다.

신뢰할 수 있는 [컴퓨팅](https://www.microsoft.com/trust-center) 및 [보안 개발 수명 주기](https://www.microsoft.com/securityengineering/sdl/)로부터 수집 된 중요 한 투자 및 경험을 기반으로, Microsoft 클라우드 서비스는 모든 테 넌 트가 다른 모든 테 넌 트의 보안 또는 서비스에 영향을 주지 않도록 하거나 다른 테 넌 트의 콘텐츠에 액세스 하는 것을 방지 하기 위한 보안 조치를 구현 했습니다.

다중 테 넌 트 환경에서 테 넌 트 격리를 유지 관리 하는 두 가지 주요 목적은 다음과 같습니다.

1.    테 넌 트 간에 고객 콘텐츠 누출 또는 무단 액세스 차단 한
2.    한 테 넌 트의 작업이 다른 테 넌 트에 대 한 서비스에 악영향을 미치지 않도록 방지

고객이 Microsoft 365 서비스 또는 응용 프로그램을 손상 하거나, 다음을 비롯 하 여 다른 테 넌 트 또는 Microsoft 365 시스템 자체의 정보에 무단으로 액세스 하지 못하도록 방지 하기 위해 Microsoft 365에서 여러 가지 보호 방법을 구현 했습니다.

- Microsoft 365 서비스에 대 한 각 테 넌 트 내에서 고객 콘텐츠를 논리적으로 격리 하는 기능은 Azure Active Directory 권한 부여 및 역할 기반 액세스 제어를 통해 달성 됩니다.
- SharePoint Online은 저장소 수준에서 데이터 격리 메커니즘을 제공 합니다.
- Microsoft는 엄격한 물리적 보안, 배경 조사 및 다중 계층화 된 암호화 전략을 사용 하 여 고객 콘텐츠의 기밀성과 무결성을 보호 합니다. 모든 Microsoft 365 데이터 센터에는 생체 인식 액세스 제어가 있으며, 팜 인쇄에 필요한 대부분의 경우 실제 액세스 권한을 얻게 됩니다. 또한 미국 기반 Microsoft 직원은 고용 프로세스의 일부로 표준 배경 확인을 성공적으로 완료 하는 데 필요 합니다. Microsoft 365의 관리 액세스에 사용 되는 컨트롤에 대 한 자세한 내용은 [microsoft 365 관리 액세스 제어](microsoft-365-administrative-access-controls-overview.md)를 참조 하십시오.
- Microsoft 365에서는 BitLocker, 파일 단위 암호화, TLS (보안 계층 보안) 및 IPsec (인터넷 프로토콜 보안)을 포함 하 여 rest 및 전송 중에 고객 콘텐츠를 암호화 하는 서비스 쪽 기술을 사용 합니다. Microsoft 365의 암호화에 대 한 자세한 내용은 [microsoft 365의 데이터 암호화 기술을](../compliance/office-365-encryption-in-the-microsoft-cloud-overview.md)참조 하십시오.

위에 나열 된 보호를 함께 사용 하면 물리적 격리 만으로 제공 되는 것과 동등한 위협 방지 및 완화를 제공 하는 강력한 논리적 격리 컨트롤이 제공 됩니다.

## <a name="related-links"></a>관련 링크

- [Azure Active Directory에서 격리 및 액세스 제어](microsoft-365-isolation-in-azure-active-directory.md)
- [Office Graph 및 Delve에서 테넌트 격리](microsoft-365-isolation-in-graph-and-delve.md)
- [Microsoft 365 검색에서 테넌트 격리](microsoft-365-isolation-in-microsoft-365-search.md)
- [Office 365 비디오에서 테넌트 격리](microsoft-365-isolation-in-microsoft-365-video.md)
- [리소스 제한 사항](microsoft-365-resource-limits.md)
- [테넌트 경계 모니터링 및 테스트](microsoft-365-monitoring-and-testing.md)
- [Microsoft 365에서 격리 및 액세스 제어](microsoft-365-isolation-in-microsoft-365.md)
