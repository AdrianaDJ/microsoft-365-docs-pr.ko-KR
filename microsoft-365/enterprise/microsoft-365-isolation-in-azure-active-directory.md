---
title: Azure Active Directory의 Microsoft 365 격리 및 액세스 제어
ms.author: josephd
author: JoeDavies-MSFT
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
description: 이 문서에서는 격리 및 액세스 제어를 사용 하 여 Azure Active Directory 내에서 서로 격리 된 여러 테 넌 트에 대 한 데이터를 유지 하는 방법을 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 79cfa23b788342ec533ce4f8a2f9c63ee0836c20
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692769"
---
# <a name="microsoft-365-isolation-and-access-control-in-azure-active-directory"></a><span data-ttu-id="a4475-103">Azure Active Directory의 Microsoft 365 격리 및 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="a4475-103">Microsoft 365 Isolation and Access Control in Azure Active Directory</span></span>

<span data-ttu-id="a4475-104">Azure AD (Active Directory)는 논리적 데이터 격리를 통해 고도로 안전한 방식으로 여러 테 넌 트를 호스트 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-104">Azure Active Directory (Azure AD) was designed to host multiple tenants in a highly secure way through logical data isolation.</span></span> <span data-ttu-id="a4475-105">Azure AD에 대 한 액세스는 인증 계층에 의해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-105">Access to Azure AD is gated by an authorization layer.</span></span> <span data-ttu-id="a4475-106">Azure AD는 사용자의 콘텐츠를 보호 하기 위해 테 넌 트 컨테이너를 보안 경계로 사용 하는 고객을 격리 시켜 동료에 게 콘텐츠를 액세스 하거나이를 손상 시킬 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-106">Azure AD isolates customers using tenant containers as security boundaries to safeguard a customer's content so that the content cannot be accessed or compromised by co-tenants.</span></span> <span data-ttu-id="a4475-107">Azure AD의 인증 계층에서 다음 세 가지 검사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-107">Three checks are performed by Azure AD's authorization layer:</span></span>

- <span data-ttu-id="a4475-108">주체가 Azure AD 테 넌 트에 액세스할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="a4475-108">Is the principal enabled for access to Azure AD tenant?</span></span>
- <span data-ttu-id="a4475-109">이 테 넌 트에서 데이터 액세스에 대 한 보안 주체를 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="a4475-109">Is the principal enabled for access to data in this tenant?</span></span>
- <span data-ttu-id="a4475-110">이 테 넌 트의 사용자 역할이 요청 된 데이터 액세스 유형에 대해 승인 되었습니까?</span><span class="sxs-lookup"><span data-stu-id="a4475-110">Is the principal's role in this tenant authorized for the type of data access requested?</span></span>

<span data-ttu-id="a4475-111">응용 프로그램, 사용자, 서버 또는 서비스가 적절 한 인증 및 토큰 또는 인증서 없이 Azure AD에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-111">No application, user, server, or service can access Azure AD without the proper authentication and token or certificate.</span></span> <span data-ttu-id="a4475-112">적절 한 자격 증명이 없으면 요청이 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-112">Requests are rejected if they are not accompanied by proper credentials.</span></span>

<span data-ttu-id="a4475-113">실제로 Azure AD에서는 각 테 넌 트를 자체 보호 된 컨테이너로 호스트 하며, 해당 컨테이너에 대 한 정책 및 사용 권한을 테 넌 트에서 단독으로 소유 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-113">Effectively, Azure AD hosts each tenant in its own protected container, with policies and permissions to and within the container solely owned and managed by the tenant.</span></span>
 
![Azure 컨테이너](../media/office-365-isolation-azure-container.png)

<span data-ttu-id="a4475-115">테 넌 트 컨테이너의 개념은 모든 계층의 디렉터리 서비스에서 포털부터 영구 저장소까지 깊이 있는 방식으로 세분화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-115">The concept of tenant containers is deeply ingrained in the directory service at all layers, from portals all the way to persistent storage.</span></span> <span data-ttu-id="a4475-116">여러 Azure AD 테 넌 트 메타 데이터가 동일한 실제 디스크에 저장 되어 있더라도 디렉터리 서비스에서 정의 하는 것 외의 컨테이너 간에는 아무런 관계도 없으며이는 차례로 테 넌 트 관리자에 게 지시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-116">Even when multiple Azure AD tenant metadata is stored on the same physical disk, there is no relationship between the containers other than what is defined by the directory service, which in turn is dictated by the tenant administrator.</span></span> <span data-ttu-id="a4475-117">먼저 인증 계층을 거치지 않고는 요청 하는 응용 프로그램이 나 서비스에서 Azure AD 저장소에 직접 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-117">There can be no direct connections to Azure AD storage from any requesting application or service without first going through the authorization layer.</span></span>

<span data-ttu-id="a4475-118">아래 예에서 Contoso와 Fabrikam은 모두 별도의 전용 컨테이너를 가지 지만, 이러한 컨테이너는 서버 및 저장소와 같은 동일한 기본 인프라를 공유 하 고, 서로 격리 된 상태로 유지 하며, 권한 부여 및 액세스 제어 계층으로 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-118">In the example below, Contoso and Fabrikam both have separate, dedicated containers, and even though those containers may share some of the same underlying infrastructure, such as servers and storage, they remain separate and isolated from each other, and gated by layers of authorization and access control.</span></span>
 
![Azure 전용 컨테이너](../media/office-365-isolation-azure-dedicated-containers.png)

<span data-ttu-id="a4475-120">또한 Azure AD 내에서 실행할 수 있는 응용 프로그램 구성 요소는 없으며, 한 테 넌 트에서 다른 테 넌 트의 무결성을 강제로 침해 하거나, 다른 테 넌 트의 암호화 키에 액세스 하거나, 서버에서 원시 데이터를 읽을 수도 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-120">In addition, there are no application components that can execute from within Azure AD, and it is not possible for one tenant to forcibly breach the integrity of another tenant, access encryption keys of another tenant, or read raw data from the server.</span></span>

<span data-ttu-id="a4475-121">기본적으로 Azure AD에서는 다른 테 넌 트의 id에서 실행 되는 모든 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-121">By default, Azure AD disallows all operations issued by identities in other tenants.</span></span> <span data-ttu-id="a4475-122">각 테 넌 트는 클레임 기반 액세스 제어를 통해 Azure AD 내에서 논리적으로 격리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-122">Each tenant is logically isolated within Azure AD through claims-based access controls.</span></span> <span data-ttu-id="a4475-123">디렉터리 데이터의 읽기 및 쓰기는 테 넌 트 컨테이너로 범위가 지정 되 고, 내부 추상화 계층 및 RBAC (역할 기반 액세스 제어) 계층으로 제어 되며,이를 통해 테 넌 트가 보안 경계로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-123">Reads and writes of directory data are scoped to tenant containers, and gated by an internal abstraction layer and a role-based access control (RBAC) layer, which together enforce the tenant as the security boundary.</span></span> <span data-ttu-id="a4475-124">이러한 계층은 모든 디렉터리 데이터 액세스 요청을 처리 하며, Microsoft 365의 모든 액세스 요청은 위의 논리에 의해 policed입니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-124">Every directory data access request is processed by these layers and every access request in Microsoft 365 is policed by the logic above.</span></span>

<span data-ttu-id="a4475-125">Azure AD에는 북미, 미국 정부, 유럽 연합, 독일 및 World Wide partitions가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-125">Azure AD has North America, U.S. Government, European Union, Germany, and World Wide partitions.</span></span> <span data-ttu-id="a4475-126">테 넌 트가 단일 파티션에 있고, 파티션에 여러 테 넌 트가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-126">A tenant exists in a single partition, and partitions can contain multiple tenants.</span></span> <span data-ttu-id="a4475-127">파티션 정보가 사용자 로부터 벗어나게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-127">Partition information is abstracted away from users.</span></span> <span data-ttu-id="a4475-128">지정 된 파티션 (it 내의 모든 테 넌 트 포함)은 여러 데이터 센터로 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-128">A given partition (including all the tenants within it) is replicated to multiple datacenters.</span></span> <span data-ttu-id="a4475-129">테 넌 트의 파티션은 테 넌 트의 속성 (예: 국가 코드)을 기준으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-129">The partition for a tenant is chosen based on properties of the tenant (e.g., the country code).</span></span> <span data-ttu-id="a4475-130">각 파티션의 비밀 및 기타 중요 한 정보는 전용 키로 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-130">Secrets and other sensitive information in each partition is encrypted with a dedicated key.</span></span> <span data-ttu-id="a4475-131">새 파티션을 만들 때 키가 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-131">The keys are generated automatically when a new partition is created.</span></span>

<span data-ttu-id="a4475-132">Azure AD 시스템 기능은 각 사용자 세션에 대 한 고유한 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-132">Azure AD system functionalities are a unique instance to each user session.</span></span> <span data-ttu-id="a4475-133">또한 Azure AD는 암호화 기술을 사용 하 여 무단이 고 원치 않는 정보 전송을 방지 하기 위해 네트워크 수준에서 공유 시스템 리소스의 격리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4475-133">In addition, Azure AD uses encryption technologies to provide isolation of shared system resources at the network level to prevent unauthorized and unintended transfer of information.</span></span>