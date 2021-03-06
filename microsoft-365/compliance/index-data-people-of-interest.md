---
title: 조사를 위한 데이터의 고급 인덱싱
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 고급 인덱싱을 사용 하 여 검색에서 조사 하려는 모든 데이터를 캡처 하는지 확인 하는 방법을 알아봅니다.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 7b0bb1a757ac70466fb43f2385485ce6da1dc741
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285964"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a>조사를 위한 데이터의 고급 인덱싱

라이브 시스템의 콘텐츠는 이미지의 존재, 지원 되지 않는 파일 형식 또는 파일 크기 제한에 도달 하는 경우를 비롯 하 여 몇 가지 이유로 인해 부분적으로 인덱싱될 수 있습니다. 높은 위험 수준 데이터 분산을 처리 하는 경우 검색에서 조사 하려는 모든 데이터를 캡처 했는지 확인 해야 합니다. 관심 있는 사용자가 데이터 조사에 추가 되 면 부분적으로 인덱싱된 콘텐츠가 완벽 하 게 검색 가능 하도록 다시 처리 됩니다. 이 프로세스를 *고급 인덱싱*이라고 합니다. 

처리 지원 및 부분적으로 인덱싱된 항목에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [데이터 조사에서 지원 되는 파일 형식](supported-filetypes-datainvestigations.md)

- [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)

- [Exchange 검색에서 인덱싱하는 파일 형식](https://docs.microsoft.com/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [SharePoint Server의 크롤링되는 기본 파일 이름 확장명 및 구문 분석되는 파일 형식](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>고급 인덱싱 결과 보기

고급 인덱싱 프로세스가 완료 되 면 다시 처리 효율성을 파악할 수 있습니다.  관심 있는 사용자 보기에서 그래프에는 *하이브리드 인덱스*에 추가 된 모든 항목이 나열 됩니다.  하이브리드 인덱스는 데이터 조사 (미리 보기)가 다시 처리 된 콘텐츠를 저장 합니다.

또한 그래프에는 수정이 필요한 항목 수와 파일 형식별로 다른 오류 그래프가 포함 되어 있습니다. 자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오.

## <a name="updating-advanced-indexes-for-people-of-interest"></a>관심 있는 사용자를 위해 고급 인덱스 업데이트

관심 있는 사용자가 데이터 조사에 추가 되 면 부분적으로 인덱싱된 모든 항목이 다시 처리 됩니다. 그러나 시간 경과에 따라 보다 부분적으로 인덱싱된 항목이 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.  필요한 경우 인덱스를 업데이트할 수 있습니다.

> [!NOTE]
> 관심 있는 인덱스 사용자를 업데이트 하는 것은 장기 실행 프로세스입니다. 조사에서 하루에 한 번 이상 인덱스를 업데이트 하지 않는 것이 좋습니다.
