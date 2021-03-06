---
title: 콘텐츠 검색을 사용 하 여 타사 가져온 데이터 검색
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: 콘텐츠 검색 eDiscovery 도구를 사용 하면 쿼리를 만들어 타사 데이터 원본에서 Microsoft 365의 사서함으로 가져온 항목을 검색할 수 있습니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 24ca63cf78b85f7b8b5181d5babd16058b641128
ms.sourcegitcommit: 25afc0c34edc7f8a5eb389d8c701175256c58ec8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47324574"
---
# <a name="use-content-search-to-search-third-party-data-imported-by-a-custom-partner-connector"></a>콘텐츠 검색을 사용 하 여 사용자 지정 파트너 커넥터로 가져온 타사 데이터 검색

보안 & 준수 센터에서 [콘텐츠 검색 eDiscovery 도구](content-search.md) 를 사용 하 여 타사 데이터 원본에서 Microsoft 365의 사서함으로 가져온 항목을 검색할 수 있습니다. 가져온 모든 타사 데이터 항목을 검색 하는 쿼리를 만들 수도 있고, 특정 타사 데이터 항목을 검색 하는 쿼리를 만들 수도 있습니다. 또한 타사 데이터를 보존 하기 위해 쿼리 기반 보존 정책 또는 쿼리 기반 eDiscovery 유지를 만들 수도 있습니다.
  
타사 데이터를 가져오는 파트너와 Microsoft 365로 가져올 수 있는 타사 데이터 형식 목록을 사용 하는 방법에 대 한 자세한 내용은 [Office 365에서 파트너와 협력 하](work-with-partner-to-archive-third-party-data.md)여 타사 데이터 보관을 참조 하십시오.

> [!IMPORTANT]
> 이 문서의 지침은 사용자 지정 파트너 커넥터로 가져온 타사 데이터에만 적용 됩니다. 이 문서는 Microsoft 준수 센터에서 타사 [데이터 커넥터](archiving-third-party-data.md#third-party-data-connectors) 를 사용 하 여 가져온 타사 데이터에는 적용 되지 않습니다.
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>모든 타사 데이터를 검색 하기 위한 쿼리 만들기

Office 365로 가져온 모든 타사 데이터 형식을 검색 하거나 보류 하려면  `kind:externaldata` 콘텐츠 검색의 키워드 상자에 메시지 속성-값 쌍을 사용 하거나 쿼리 기반 보존을 만들 때 사용할 수 있습니다. 예를 들어 모든 타사 데이터 원본에서 가져온 항목을 검색 하 고 가져온 항목의 Subject 속성에 "contoso" 라는 단어를 포함 하려면 다음 쿼리를 사용 합니다. 
  
```powershell
kind:externaldata AND subject:contoso
```

이전 keyword 쿼리 예제에는 subject 속성이 포함 되어 있습니다. 키워드 쿼리에 포함할 수 있는 타사 데이터 항목의 기타 속성 목록은 [Office 365에서 타사 데이터를 보관 하기 위한 파트너와 작업](work-with-partner-to-archive-third-party-data.md#more-information)의 "추가 정보" 섹션을 참조 하십시오.
  
타사 데이터를 검색 하 고 유지 하기 위한 쿼리를 만들 때 조건을 사용 하 여 검색 결과의 범위를 좁힐 수도 있습니다. 콘텐츠 검색 쿼리를 만드는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>특정 유형의 타사 데이터를 검색 하기 위한 쿼리 만들기

모든 유형의 타사 데이터를 검색 하는 대신 콘텐츠 검색의 키워드 상자에 있는 다음 메시지 *속성* 을 사용 하 여 타사 데이터의 지정만 검색 하는 쿼리를 만들 수 있습니다.
  
```powershell
itemclass:ipm.externaldata.<third-party data type>* 
```

예를 들어 Subject 속성에서 "contoso" 라는 단어가 포함 된 Facebook 데이터를 검색 하려면 다음 쿼리를 사용 합니다.
  
```powershell
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

다음 표에서는 검색할 수 있는 타사 데이터 형식 및  `itemclass:` 해당 유형의 타사 데이터를 특별히 검색 하기 위해 message 속성에 사용할 값을 보여 줍니다. 쿼리 구문은 대/소문자를 구분 하지 않습니다. 
  
|**타사 데이터 형식**|**속성 값 `itemclass:`**|
|:-----|:-----|
|AIM  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL with Pivot Client   <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Axs 자리 표시자  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|Bearshare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|Blackberry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|BlackBerry 통화 로그  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry PIN  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|블룸버그 메시지  <br/> | `ipm.externaldata.conversation.Bloomberg Message*` <br/> |
|Bloomberg 메시징  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box  <br/> | `ipm.externaldata.Box*` <br/> |
|Cisco IM &amp; 현재 상태 서버  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google +  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google 대화  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|IBM 연결  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|ICE 채팅  <br/> | `ipm.externaldata.conversation.Ice Chat*` <br/> |
|Indii Messenger  <br/> | `ipm.externaldata.Indii*` <br/> |
|명령이 있는 agram  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Microsoft UC  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|마인드 맞춤  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|수신  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|유 이율  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Pivot  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|비즈니스용 Skype  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|Squawker  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|한자  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
