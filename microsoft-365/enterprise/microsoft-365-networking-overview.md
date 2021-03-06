---
title: Microsoft 365 네트워크 연결 개요
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 6/23/2020
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- m365initiative-coredeploy
f1.keywords:
- NOCSH
description: SaaS 서비스에 대 한 네트워크 최적화가 중요 한 이유, Microsoft 365 네트워킹의 목표 및 각 SaaS가 다른 작업을 수행 하는 다른 네트워킹을 필요로 하는 이유에 대해 설명 합니다.
ms.openlocfilehash: 50137e507021a6b6d26468a8a299c35a613a065a
ms.sourcegitcommit: d76a4c07f0be2938372bdfae50e0e4d523bd8e9f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/14/2020
ms.locfileid: "48456402"
---
# <a name="microsoft-365-network-connectivity-overview"></a>Microsoft 365 네트워크 연결 개요

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Microsoft 365은 다양 한 마이크로 서비스 및 응용 프로그램 집합을 통해 생산성 및 공동 작업 시나리오를 제공 하는 분산 소프트웨어 (온-서비스) 클라우드입니다. Outlook, Word, PowerPoint 등의 Microsoft 365의 클라이언트 구성 요소는 사용자 컴퓨터에서 실행 되며 Microsoft 데이터 센터에서 실행 되는 Microsoft 365의 다른 구성 요소에 연결 합니다. Microsoft 365 최종 사용자 환경의 품질을 결정 하는 가장 중요 한 요인은 Microsoft 365 클라이언트와 Microsoft 365 서비스 전면 도어 간의 네트워크 안정성 및 낮은 대기 시간입니다.

이 문서에서는 Microsoft 365 네트워킹의 목표와 Microsoft 365 네트워킹에 일반적인 인터넷 트래픽 보다 다른 최적화 된 접근 방식이 필요한 이유를 알아봅니다.

## <a name="microsoft-365-networking-goals"></a>Microsoft 365 네트워킹 목표

Microsoft 365 네트워킹의 궁극적인 목표는 클라이언트와 가장 가까운 Microsoft 365 끝점 간에 최소의 제한적인 액세스를 사용 하 여 최종 사용자 환경을 최적화 하는 것입니다. 최종 사용자 환경의 품질은 사용자가 사용 하는 응용 프로그램의 성능 및 응답성과 직접적으로 관련 됩니다. 예를 들어 Microsoft 팀은 사용자 전화 통화, 회의 및 공유 화면 공동 작업을 통해 결함 없는 기능을 사용할 수 있도록 낮은 대기 시간을 사용 하며, Outlook에서는 서버 쪽 인덱싱 및 인공 지능 기능을 활용 하는 빠른 검색 기능이 제공 됩니다.

네트워크 설계의 기본 목표는 클라이언트 컴퓨터에서 Microsoft 글로벌 네트워크로의 RTT (왕복 시간)를 줄이고 전 세계의 모든 Microsoft 데이터 센터를 낮은 대기 시간, 고가용성 클라우드 응용 프로그램 진입점과 상호 연결 하는 Microsoft의 공용 네트워크 백본으로 시간을 최소화 하는 것입니다. [Microsoft가 빠르고 안정적인 글로벌 네트워크를 구축하는 방법](https://azure.microsoft.com/blog/how-microsoft-builds-its-fast-and-reliable-global-network/)에서 Microsoft 글로벌 네트워크에 대해 자세히 알아볼 수 있습니다.

Microsoft 365을 최적화 하면 네트워크 성능이 복잡할 필요는 없습니다. 다음과 같은 몇 가지 주요 원칙에 따라 가능한 최상의 성능을 얻을 수 있습니다.

- Microsoft 365 네트워크 트래픽 식별
- 사용자가 Microsoft 365에 연결 하는 각 위치에서 인터넷으로의 Microsoft 365 네트워크 트래픽 로컬 분기 송신 허용
- Microsoft 365 트래픽이 프록시 및 패킷 검사 장치를 우회 하도록 허용

Microsoft 365 네트워크 연결 원칙에 대 한 자세한 내용은 [microsoft 365 네트워크 연결 원리](microsoft-365-network-connectivity-principles.md)를 참조 하세요.

## <a name="traditional-network-architectures-and-saas"></a>전통적인 네트워크 아키텍처 및 SaaS

클라이언트/서버 워크 로드에 대 한 전통적인 네트워크 아키텍처 원칙은 클라이언트와 끝점 간의 트래픽이 회사 네트워크 경계를 벗어나 확장 되지 않는 가정을 중심으로 설계 되었습니다. 또한 대부분의 엔터프라이즈 네트워크에서 모든 아웃 바운드 인터넷 연결은 회사 네트워크를 통과 하 고 중앙 위치에서 송신 합니다.

전통적인 네트워크 아키텍처에서는 일반적인 인터넷 트래픽에 대 한 대기 시간이 높을수록 네트워크 경계 보안을 유지 관리 하기 위해 필요한 장단점이 되며, 인터넷 트래픽에 대 한 성능 최적화는 일반적으로 네트워크 송신 지점에서 장비를 업그레이드 하거나 수평 확장 하는 작업을 수행 하는 데 필요 합니다. 그러나이 방법은 Microsoft 365와 같은 SaaS 서비스의 최적의 네트워크 성능에 대 한 요구 사항을 해결 하지 않습니다.

## <a name="identifying-microsoft-365-network-traffic"></a>Microsoft 365 네트워크 트래픽 식별

Microsoft 365 네트워크 트래픽을 보다 쉽게 식별 하 고 네트워크 식별을 보다 간단 하 게 관리할 수 있도록 합니다.

- 인터넷 대기 시간으로 영향을 받지 않는 네트워크 트래픽과의 중요 한 네트워크 트래픽을 구분 하기 위한 새로운 네트워크 끝점 범주 가장 중요 한 "최적화" 범주에는 Url이 몇 개 뿐 이며 IP 주소도 지원 합니다.
- 스크립트 사용 또는 직접 장치 구성과 Microsoft 365 네트워크 식별의 변경 관리에 대 한 웹 서비스입니다. 변경 내용은 웹 서비스 또는 RSS 형식에서 또는 Microsoft Flow 서식 파일을 사용 하 여 전자 메일에서 사용할 수 있습니다.
- [Office 365 네트워크 파트너 프로그램](https://aka.ms/Office365NPP) 은 microsoft 365 네트워크 연결 원칙을 준수 하 고 간단한 구성을 사용 하는 장치 또는 서비스를 제공 하는 microsoft 파트너를 대상으로 합니다.

## <a name="securing-microsoft-365-connections"></a>Microsoft 365 연결 보안

기존 네트워크 보안의 목표는 침입과 악의적인 악용으로부터 회사 네트워크 경계를 강화하는 것입니다. 대부분의 엔터프라이즈 네트워크에서는 프록시 서버, 방화벽, SSL 중단 및 검사, 딥 패킷 검사 및 데이터 손실 방지 시스템과 같은 기술을 사용 하 여 인터넷 트래픽에 대 한 네트워크 보안을 적용 합니다. 이러한 기술은 일반적인 인터넷 요청에 대한 중요한 위험을 완화하지만, Microsoft 365 엔드포인트에 적용되는 경우 성능, 확장성 및 최종 사용자 환경의 질을 크게 저하시킬 수 있습니다.

Microsoft 365는 Microsoft 365 기능 및 작업을 위해 특별히 설계 된 기본 제공 보안 및 관리 기능을 사용 하 여 조직의 콘텐츠 보안 및 데이터 사용 준수에 대 한 요구를 충족 하는 데 도움이 됩니다. Microsoft 365 보안 및 규정 준수에 대 한 자세한 내용은 [Office 365 보안 로드맵](https://docs.microsoft.com/office365/securitycompliance/security-roadmap)를 참조 하세요. Microsoft 365 트래픽에 고급 수준 처리를 수행 하는 고급 네트워크 솔루션에서 Microsoft의 권장 사항 및 지원 위치에 대 한 자세한 내용은 [Office 365 트래픽에 타사 네트워크 장치 또는 솔루션 사용](https://support.microsoft.com/help/2690045)을 참조 하십시오.

## <a name="why-is-microsoft-365-networking-different"></a>Microsoft 365 네트워킹이 서로 다른 이유는 무엇 인가요?

Microsoft 365는 끝점 보안 및 암호화 된 네트워크 연결을 사용 하 여 최적의 성능을 유지 하 고 경계 보안을 적용 해야 하는 필요성을 줄여줍니다. Microsoft 365 데이터 센터는 전 세계에 있으며 서비스는 다양 한 방법을 사용 하 여 클라이언트를 최상의 서비스 끝점에 연결할 수 있도록 설계 되었습니다. 사용자 데이터와 처리는 많은 Microsoft 데이터 센터에 분산 되므로 클라이언트 컴퓨터에서 연결할 수 있는 단일 네트워크 끝점이 없습니다. 실제로 최종 사용자가 액세스할 수 있는 지리적 위치에 적응 하기 위해 Microsoft 365 테 넌 트의 데이터와 서비스는 Microsoft 글로벌 네트워크에 의해 동적으로 최적화 됩니다.

Microsoft 365 트래픽이 패킷 검사 및 중앙 송신에 따라 발생 하는 경우 특정 일반적인 성능 문제가 발생 합니다.

- 대기 시간이 높으면 비디오 및 오디오 스트림의 성능이 크게 저하 될 수 있으며, 데이터 검색, 검색, 실시간 공동 작업, 일정 약속 있음/없음 정보, 제품 내 콘텐츠 및 기타 서비스에 대 한 응답 속도가 느려집니다.
- 중앙 위치 로부터의 모든 연결이 Microsoft 365 글로벌 네트워크의 동적 라우팅 기능을 무효화 하 고 대기 시간 및 왕복 횟수를 추가 합니다.
- 암호화 해독 SSL 보안 Microsoft 365 네트워크 트래픽 및 다시 암호화를 통해 프로토콜 오류가 발생 하 고 보안 위험이 있을 수 있음

네트워크 경로를 Microsoft 365 진입점으로 단축 (클라이언트 트래픽이 지리적 위치까지 가장 가까이) 하 여 Microsoft 365의 최종 사용자 환경 및 연결 성능을 향상 시킬 수 있습니다. 또한 Microsoft 365 성능 및 안정성에 대 한 향후 네트워크 아키텍처 변경이 미치는 영향을 줄이는 데도 도움이 될 수 있습니다. 최적의 연결 모델은 회사 네트워크에 있든, 홈, 호텔, 커피숍 및 공항 등의 원격 위치에 관계 없이 사용자의 위치에서 네트워크 egress를 항상 제공 하는 것입니다. 일반 인터넷 트래픽 및 WAN 기반 회사 네트워크 트래픽은 개별적으로 라우팅되고 로컬 직접 egress 모델을 사용 하지 않습니다. 이 로컬 직접 송신 모델은 아래 다이어그램에 표시되어 있습니다.

![로컬 송신 네트워크 아키텍처](../media/6bc636b0-1234-4ceb-a45a-aadd1044b39c.png)

로컬 egress 아키텍처는 기존 모델을 통해 Microsoft 365 네트워크 트래픽에 대해 다음과 같은 이점을 제공 합니다.
  
- 경로 길이를 최적화하여 최적의 Microsoft 365 성능을 제공합니다. 최종 사용자 연결은 Microsoft 전역 네트워크의 _분산 서비스 전면 도어_ 인프라에 의해 가장 가까운 microsoft 365 진입점으로 동적으로 라우팅되고, 트래픽은 microsoft의 초소형 대기 시간 고가용성 파이버를 통해 데이터 및 서비스 끝점에 내부적으로 라우팅됩니다.
- 프록시 및 트래픽 검사 장치를 무시 하 고 Microsoft 365 트래픽에 대해 로컬 송신을 허용 하 여 회사 네트워크 인프라에 대 한 부하를 줄입니다.
- 중복 네트워크 보안 기술에 대 한 응용 프로그램을 방지 하 여 클라이언트 끝점 보안 및 클라우드 보안 기능을 활용 하 여 양쪽 끝 간의 연결을 보호 합니다.

> [!NOTE]
> _분산 서비스 전면 도어_ 인프라는 지리적으로 분산 된 위치에 대 한 Microsoft 글로벌 네트워크의 가용성이 높고 확장 가능한 네트워크에 지입니다. 최종 사용자 연결을 종료 하 고 Microsoft 글로벌 네트워크 내에서이를 효율적으로 라우팅합니다. [Microsoft가 빠르고 안정적인 글로벌 네트워크를 구축하는 방법](https://azure.microsoft.com/blog/how-microsoft-builds-its-fast-and-reliable-global-network/)에서 Microsoft 글로벌 네트워크에 대해 자세히 알아볼 수 있습니다.

Microsoft 365 네트워크 연결 원칙을 이해 하 고 적용 하는 방법에 대 한 자세한 내용은 [microsoft 365 네트워크 연결 원리](microsoft-365-network-connectivity-principles.md)를 참조 하세요.

## <a name="conclusion"></a>결론

Microsoft 365 네트워크 성능 최적화는 실제로 불필요 한 장애를 제거 하는 것입니다. Microsoft 365 연결을 신뢰할 수 있는 트래픽으로 처리 하면 패킷 검사 및 프록시 대역폭 경쟁에 따라 대기 시간이 지연 되는 것을 방지할 수 있습니다. 클라이언트 컴퓨터와 Office 365 끝점 간에 로컬 연결을 허용 하면 트래픽을 Microsoft 글로벌 네트워크를 통해 동적으로 라우팅할 수 있습니다.

## <a name="related-topics"></a>관련 항목

[Microsoft 365 네트워크 연결 원칙](microsoft-365-network-connectivity-principles.md)

[Office 365 엔드포인트 관리](managing-office-365-endpoints.md)

[Office 365 URL 및 IP 주소 범위](urls-and-ip-address-ranges.md)

[Office 365 IP 주소 및 URL 웹 서비스](microsoft-365-ip-web-service.md)

[Microsoft 365 네트워크 연결 평가](assessing-network-connectivity.md)

[Microsoft 365의 네트워크 계획 및 성능 조정](network-planning-and-performance.md)

[초기 계획 및 성능 기록을 사용하여 Office 365 성능 조정](performance-tuning-using-baselines-and-history.md)

[Office 365 성능 문제 해결 계획](performance-troubleshooting-plan.md)

[콘텐츠 배달 네트워크](content-delivery-networks.md)

[Microsoft 365 연결 테스트](https://aka.ms/netonboard)

[Microsoft가 빠르고 안정적인 글로벌 네트워크를 구축하는 방법](https://azure.microsoft.com/blog/how-microsoft-builds-its-fast-and-reliable-global-network/)

[Office 365 네트워킹 블로그](https://techcommunity.microsoft.com/t5/Office-365-Networking/bd-p/Office365Networking)
