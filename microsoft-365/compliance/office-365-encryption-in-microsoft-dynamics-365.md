---
title: Microsoft Dynamics 365에서 암호화
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Microsoft는 microsoft 데이터베이스에 있고 전송 중에는 암호화 기술을 사용 하 여 microsoft Dynamics 365의 고객 데이터를 보호 하는 방법을 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: bd349890fc7fc1ae7f1f7eaf07f90c22423637cf
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44031418"
---
# <a name="encryption-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365에서 암호화

Microsoft는 Microsoft 데이터베이스에 있고 사용자 장치와 데이터 센터 간에 전송 되는 동안에도 암호화 기술을 사용 하 여 Dynamics 365의 고객 데이터를 보호 합니다. 고객과 Microsoft 데이터 센터 간에 설정 된 연결은 암호화 되며 모든 공용 끝점은 업계 표준 TLS를 사용 하 여 보호 됩니다. TLS에서는 데스크톱과 데이터 센터 간의 기밀성과 무결성을 유지 하기 위해 보안이 향상 된 브라우저 간 연결을 효과적으로 설정 합니다. 데이터 암호화가 활성화 되 면 해제할 수 없습니다. 자세한 내용은 [필드 수준 데이터 암호화](https://msdn.microsoft.com/library/dn481562.aspx)를 참조 하세요.

Dynamics 365은 사용자 이름 및 전자 메일 암호와 같은 중요 한 정보가 포함 된 기본 엔터티 특성 집합에 표준 Microsoft SQL Server 셀 수준 암호화를 사용 합니다. 이 기능은 조직에서 FIPS 140-2와 관련 된 규정 준수 요구 사항을 충족 하는 데 도움이 될 수 있습니다. 필드 수준 데이터 암호화는 특히 Dynamics 365 인스턴스와 전자 메일 서비스 간의 통합을 사용 하기 위해 사용자 이름 및 암호를 저장 해야 하는 [Microsoft DYNAMICS CRM 전자 메일 라우터](https://technet.microsoft.com/library/hh699800.aspx)를 활용 하는 시나리오에서 중요 합니다. 

Dynamics 365의 모든 인스턴스는 [MICROSOFT SQL Server tde (투명 한 데이터 암호화](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017) )를 사용 하 여 휴지 상태로 디스크에 기록 되는 실시간 데이터 암호화를 수행 합니다. TDE는 SQL Server, Azure SQL Database 및 Azure SQL Data Warehouse 데이터 파일을 암호화 합니다. 기본적으로 Microsoft는 Dynamics 365 인스턴스에 대 한 데이터베이스 암호화 키를 저장 하 고 관리 합니다. Financials에 대해 Dynamics 365에서 사용 되는 키는 .NET Framework Data Protection API에 의해 생성 됩니다. 

Dynamics 365 관리 센터의 키 관리 기능을 사용 하면 관리자가 Dynamics 365 인스턴스와 연결 된 데이터베이스 암호화 키를 자동으로 관리할 수 있습니다. 자체 관리 데이터베이스 암호화 키는 Microsoft Dynamics 365의 1 월 2017 업데이트 에서만 사용할 수 있으며 이후 버전에서는 사용 하지 못할 수 있습니다. 자세한 내용은 [Manage the encryption key for The Dynamics 365 (online) 인스턴스](https://docs.microsoft.com/dynamics365/customer-engagement/admin/manage-encryption-keys-instance)를 참조 하세요.) 키 관리 기능은 HSM에 저장 된 것과 같은 PFX 및 BYOK 암호화 키 파일을 모두 지원 합니다. 인터넷을 통해 HSM으로 보호 된 키를 생성 하 고 전송 하는 방법에 대 한 자세한 내용은 [Azure Key Vault에 대해 hsm 보호 키를 생성 하 고 전송 하는 방법을](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)참조 하세요. 

암호화 키 업로드 옵션을 사용 하려면 공개 및 개인 암호화 키가 모두 필요 합니다.

키 관리 기능은 Azure 키 자격 증명 모음을 사용 하 여 암호화 키를 안전 하 게 저장 하는 방식으로 암호화 키 관리를 단순화 합니다. Azure 키 자격 증명 모음을 통해 클라우드 응용 프로그램 및 서비스에서 사용 되는 암호화 키 및 비밀을 보호할 수 있습니다. 키 관리 기능을 사용 하는 경우에는 Azure 키 자격 증명 모음을 사용할 필요가 없으며, 대부분의 경우 자격 증명 모음 내에서 Dynamics 365에 사용할 암호화 키에 액세스할 필요가 없습니다.
