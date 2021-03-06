---
title: 보유자 데이터의 고급 인덱싱
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
description: 고급 eDiscovery 사례에 custodian을 추가 하면 부분적으로 인덱싱된 콘텐츠가 완벽 하 게 검색할 수 있도록 다시 처리 됩니다.
ms.openlocfilehash: 95e087884b65628565e596dc8ae9f33aadc4cd9f
ms.sourcegitcommit: 6501e01a9ab131205a3eef910e6cea7f65b3f010
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46527558"
---
# <a name="advanced-indexing-of-custodian-data"></a>보유자 데이터의 고급 인덱싱

고급 eDiscovery 사례에 custodian을 추가 하면 부분적으로 인덱싱된 콘텐츠가 완벽 하 게 검색할 수 있도록 다시 처리 됩니다.  이 프로세스를 *고급 인덱싱*이라고 합니다. 이미지의 존재 여부, 지원 되지 않는 파일 형식 또는 파일 크기 제한에 도달 하는 경우에는 여러 가지 이유로 인해 콘텐츠를 부분적으로 인덱싱할 수 있습니다.

처리 지원 및 부분적으로 인덱싱된 항목에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [고급 eDiscovery에서 지원 되는 파일 형식](supported-filetypes-ediscovery20.md)

- [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)

- [Exchange 검색에서 인덱싱하는 파일 형식](https://docs.microsoft.com/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [SharePoint Server의 크롤링되는 기본 파일 이름 확장명 및 구문 분석되는 파일 형식](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>고급 인덱싱 결과 보기

고급 인덱싱 프로세스가 완료 되 면 다시 처리 효율성을 파악할 수 있습니다.  사례에 대 한 **처리** 탭의 고급 인덱싱 결과 보기에서 그래프에는 *하이브리드 인덱스*에 추가 된 항목 수가 나열 됩니다.  하이브리드 인덱스는 고급 eDiscovery가 다시 처리 된 콘텐츠를 저장 하는 위치입니다.

이 보기에는 수정 해야 하는 항목 수와 파일 형식별로 또 다른 오류 그래프가 포함 되어 있습니다. 자세한 내용은 다음을 참조하세요.

- [데이터를 처리할 때 오류 수정](error-remediation.md)

- [단일 항목 오류 수정](single-item-error-remediation.md)

## <a name="updating-the-advanced-index-for-custodians"></a>Custodians에 대 한 고급 인덱스 업데이트

고급 eDiscovery 사례에 custodian을 추가 하면 부분적으로 인덱싱된 모든 항목이 다시 처리 됩니다. 그러나 시간 경과에 따라 보다 부분적으로 인덱싱된 항목이 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.  필요한 경우 특정 custodian에 대 한 인덱스를 업데이트할 수 있습니다. 자세한 내용은 [Advanced eDiscovery 사례에서 Custodians 관리](manage-new-custodians.md#re-index-custodian-data)를 참조 하세요. **처리** 탭에서 **업데이트 인덱스** 를 클릭 하 여 모든 custodians에 대 한 인덱스를 업데이트할 수도 있습니다.

> [!NOTE]
> Custodian 인덱스를 업데이트 하는 과정은 장기 실행 프로세스입니다. 인덱스를 하루에 두 번 이상 업데이트 하지 않는 것이 좋습니다.
