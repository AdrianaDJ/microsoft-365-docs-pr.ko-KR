---
title: Exchange Online 사서함에 저장 된 콘텐츠
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: Microsoft 365에서 클라우드 기반 앱에 의해 생성 된 데이터는 사용자의 Exchange Online 사서함에 저장 되거나 연결 됩니다.
ms.openlocfilehash: 121380cdaaf5d0397d082159ddf6461c0c12cbe1
ms.sourcegitcommit: 4ac96855d7c269a0055ca8943000b762a70ca4ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47321987"
---
# <a name="content-stored-in-exchange-online-mailboxes"></a>Exchange Online 사서함에 저장 된 콘텐츠

Exchange Online의 사서함은 주로 메시지, 일정 항목, 작업 및 메모와 같은 전자 메일 관련 항목을 저장 하는 데 사용 됩니다. 하지만 클라우드 기반 앱이 더 많이 변경 되 면 사용자 사서함에도 데이터가 저장 됩니다. 사서함에 데이터를 저장 하는 경우의 한 가지 이점은 콘텐츠 검색, 코어 eDiscovery, 고급 eDiscovery 및 데이터 조사에서 검색 도구를 사용 하 여 이러한 클라우드 기반 앱에서 데이터를 찾고, 보고, 내보낼 수 있다는 것입니다. 이러한 앱 중 일부의 데이터는 사서함의 비 IPM 메시지 하위 트리에 있는 숨겨진 폴더에 저장 됩니다. 다른 클라우드 기반 앱의 데이터는 사서함에 저장 되지 않을 수 있지만 사서함 _에_ _연결_ 되어 있으며 해당 데이터가 검색 쿼리와 일치 하는 경우 검색에 반환 됩니다. 클라우드 기반 데이터가 사용자 사서함에 저장 되는지 여부에 관계 없이 사용자가 사서함을 여는 경우에는 일반적으로 전자 메일 클라이언트에서 데이터가 표시 되지 않습니다.

다음 표에는 데이터를 클라우드 기반 사서함과 함께 저장 하거나 연결 하는 앱이 나와 있습니다. 이 표에서는 각 앱에서 생성 하는 콘텐츠 형식에 대해서도 설명 합니다.

|Microsoft 365 앱|설명|
|:---------|:---------|
|Forms|양식에 대 한 양식 및 응답은 전자 메일 메시지에 첨부 되 고 양식을 만든 사용자의 사서함에 있는 숨겨진 폴더에 저장 되는 파일에 저장 됩니다. 4 월 2020 이전에 만든 양식은 PDF 파일로 저장 됩니다. 2020 이후에 만든 양식은 JSON 파일로 저장 됩니다.  양식에 대 한 응답은 CSV 파일에 저장 됩니다. PST 파일의 양식에서 콘텐츠를 내보낼 때이 데이터 **는 다음과 같은**guid (globally unique identification)가 지정 된 하위 폴더의 **ApplicationDataRoot** 폴더에 있습니다.|
|Microsoft 365 그룹|전자 메일 메시지, 일정 항목, 연락처 (사용자), 메모 및 작업은 Microsoft 365 그룹과 연결 된 사서함에 저장 됩니다.|
|Outlook/Exchange Online|전자 메일 메시지, 일정 항목, 연락처 (사용자), 메모 및 작업은 사용자의 사서함에 저장 됩니다.|
|사람|사용자 앱 (Outlook에서 액세스할 수 있는 연락처와 같은 대화 상대 응용 프로그램)의 대화 상대는 user의 사서함에 저장 됩니다.|
|클래스 일정|클래스 일정에서 만든 요금제는 새 요금제를 만들 때 프로 비전 되는 해당 Microsoft 365 그룹의 사서함에 저장 됩니다. 그룹 사서함의 별칭은 계획의 이름입니다.|
|비즈니스용 Skype|비즈니스용 Skype의 대화는 사용자 사서함의 대화 내용 폴더에 저장 됩니다. Skype 모임 참가자의 사서함을 소송 보존으로 설정 하거나 보관 정책에 할당 하는 경우 모임에 첨부 된 파일이 참가자 사서함에 보존 됩니다.|
|Sway|Sway는 전자 메일 메시지에 첨부 되 고 sway를 만든 사용자의 사서함에 있는 숨겨진 폴더에 저장 되는 HTML 파일로 저장 됩니다. PST 파일의 Sway에서 콘텐츠를 내보낼 때이 데이터는 **905fcf26-4eb7-48a0-9ff0-8dcc7194b5ba**라는 하위 폴더의 **ApplicationDataRoot** 폴더에 있습니다.|
|작업|작업 앱 (Outlook에서 액세스할 수 있는 작업과 같은 작업)의 작업은 사용자의 사서함에 저장 됩니다.|
|Teams|팀 채널의 일부인 대화는 팀 사서함과 연결 됩니다. 팀에서 채팅 목록의 일부인 대화 ( *1 x N 채팅*이 라고도 함)는 채팅에 참가 하는 사용자의 사서함에 연결 됩니다. 또한 팀 채널의 모임 및 통화에 대 한 요약 정보는 모임 또는 통화에 전화를 거는 사용자의 사서함과 연결 됩니다. 따라서 팀 콘텐츠를 검색할 때 팀 사서함에서 채널 대화의 콘텐츠를 검색 하 고 사용자 사서함에서 1 x N 채팅의 콘텐츠를 검색 합니다.| 
|To-Do|할 일 앱에 있는-do 목록에 저장 되는 작업 ( *dos*로 호출 됨)은 사용자의 사서함에 저장 됩니다.|
|Yammer|Yammer 커뮤니티 내의 대화와 의견은 Microsoft 365 그룹 사서함과 연결 되 고 작성자의 사용자 사서함과 모든 명명 된 받는 사람 (@mentioned 또는 참조 users)과 연관 됩니다. Yammer 커뮤니티 외부로 전송 된 개인 메시지는 개인 메시지에 참가 하는 사용자의 사서함에 저장 됩니다.|  
||||

> [!NOTE]
> 지금은 사서함에 보류가 적용 되는 경우 (eDiscovery 및 Advanced eDiscovery 사례에 보류를 사용 하 여) 양식 및 Sway의 콘텐츠가 보류에 의해 보존 되지 않습니다. 
