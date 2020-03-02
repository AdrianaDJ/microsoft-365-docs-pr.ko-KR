---
title: Crazy Domains에서 Office 365용 DNS 레코드 만들기
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 6386d63e-b78f-4736-90e7-b99a2c116a9f
description: 도메인을 확인 하 고 전자 메일, 비즈니스용 Skype Online 및 Office 365의 기타 서비스에 대 한 DNS 레코드를 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: 5b344ebdc4a4608c27c0a84299ea171391c09ba0
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42248159"
---
# <a name="create-dns-records-at-crazy-domains-for-office-365"></a>Crazy Domains에서 Office 365용 DNS 레코드 만들기

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
DNS 호스팅 공급자로 Crazy Domains를 사용하고 있는 경우, 이 문서에 나와 있는 단계를 따라 도메인을 확인하고 전자 메일, 비즈니스용 Skype Online 등에 대한 DNS 레코드를 설정합니다.
  
Crazy Domains에서 이러한 레코드를 추가하고 나면 도메인이 Office 365 서비스에서 작동하도록 설정됩니다.
  
Office 365에서 웹 사이트의 웹 호스팅 및 DNS에 대한 자세한 내용은 [Office 365에서 공개 웹 사이트 사용](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)을 참조하세요.
  
> [!NOTE]
> 일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가
<a name="BKMK_verify"> </a>

Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. 시작하려면 [이 링크](https://manage.crazydomains.com/members/domains/)를 사용하여 Crazy Domains의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    ![CrazyDomains-BP-구성-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. **내 계정** 섹션에서 **도메인**을 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. **도메인 이름** 페이지의 **도메인** 섹션에서 업데이트 하려는 도메인의 이름을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. **DNS 설정** 섹션에서 드롭다운 목록 아이콘을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. **Add Record(레코드 추가)** 드롭다운 목록에서 **TXT Record(TXT 레코드)** 를 선택합니다. 
    
    ![CrazyDomains-BP-Verify-1-1](../media/f0ffdefb-d7a5-47df-bb5e-bf8a3bcc9b01.png)
  
7. **추가**를 선택합니다.
    
    ![CrazyDomains-BP-Verify-1-2](../media/b0cd623a-67f7-4bae-a5b5-507f5a106123.png)
  
8. 새 레코드의 상자에서 다음 표의 값을 입력하거나 복사하여 붙여넣습니다.
    
    |**Sub Domain(하위 도메인)**|**Text Record(텍스트 레코드)**|
    |:-----|:-----|
    |(Leave this field empty.)  <br/> |MS=ms *XXXXXXXX*  <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다.           [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![CrazyDomains-BP-Verify-1-3](../media/3867de97-6a98-4475-9bda-470bac75d483.png)
  
9. **업데이트**를 선택 합니다.
    
    ![CrazyDomains-BP-Verify-1-4](../media/0e416df6-b7a2-4dd7-971c-f1cc31df30da.png)
  
10. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 관리 센터에서 **설정** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">도메인</a> 페이지로 이동 합니다.

    
2. **도메인** 페이지에서 확인 하려는 도메인을 선택 합니다. 
    
    
  
3. **설정** 페이지에서 **설정 시작**을 선택 합니다.
    
    
  
4. **도메인 확인** 페이지에서 **확인**을 선택 합니다.
    
    
  
> [!NOTE]
>  일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>사용자 도메인의 전자 메일이 Office 365로 전송되도록 MX 레코드 추가
<a name="BKMK_add_MX"> </a>

1. 시작하려면 [이 링크](https://manage.crazydomains.com/members/domains/)를 사용하여 Crazy Domains의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    ![CrazyDomains-BP-구성-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. **내 계정** 섹션에서 **도메인**을 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. **도메인 이름** 페이지의 **도메인** 섹션에서 업데이트 하려는 도메인의 이름을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. **DNS 설정** 섹션에서 드롭다운 목록 아이콘을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. **레코드 추가:** 드롭다운 목록에서 **MX 레코드**를 선택합니다. 
    
    ![CrazyDomains-BP-구성-2-1](../media/63f7ab77-e686-4e7b-a3a2-1ac28a02d5f3.png)
  
7. **추가**를 선택합니다.
    
    ![CrazyDomains-BP-구성-2-2](../media/a60680a1-2513-498c-b42f-8ffa575ee48e.png)
  
8. 새 레코드의 상자에서 다음 표의 값을 입력하거나 복사하여 붙여 넣습니다.
    
    (드롭다운 목록에서 **Priority (우선 순위** ) 값을 선택 합니다.) 
    
    |**영역용 메일**|**우선 순위**|**서버에 할당**|
    |:-----|:-----|:-----|
    |(이 필드는 비워 둡니다.)  <br/> |개  <br/> 우선 순위에 대한 자세한 내용은 [MX 우선 순위란?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)을 참조하세요. <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **참고:** Office 365 계정에서 * \<도메인\> 키* 를 가져옵니다.           [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![CrazyDomains-BP-구성-2-3](../media/e27df6a6-19a6-4e58-9716-a74be1c3f8da.png)
  
9. **업데이트**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-2-4](../media/ba25cdef-a436-48bf-b0e9-5dffd03234a4.png)
  
10. **Mx 레코드** 구역에 다른 mx 레코드가 나열 되어 있으면 해당 레코드 중 하나에 대해 **수정을** 선택 합니다. 
    
    ![CrazyDomains-BP-구성-2-5](../media/9acdda39-33ec-4b24-ad83-91c26f9c599b.png)
  
11. **삭제**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-2-6](../media/50b0e263-6f21-41b3-8fa0-7dd55dbe6c2e.png)
  
12. **업데이트** 를 선택 하 여 삭제를 확인 합니다. 
    
    ![CrazyDomains-BP-구성-2-7](../media/db751bfe-31c2-4632-a491-6893eda38a51.png)
  
13. 이 절차의 앞에서 추가한 MX 레코드만 남을 때까지 목록에 있는 다른 MX 레코드를 동일한 방법으로 제거합니다.
    
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>Office 365에 필요한 6개의 CNAME 레코드 추가
<a name="BKMK_add_CNAME"> </a>

1. 시작하려면 [이 링크](https://manage.crazydomains.com/members/domains/)를 사용하여 Crazy Domains의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    ![CrazyDomains-BP-구성-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. **내 계정** 섹션에서 **도메인**을 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. **도메인 이름** 페이지의 **도메인** 섹션에서 업데이트 하려는 도메인의 이름을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. **DNS 설정** 섹션에서 드롭다운 목록 아이콘을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. **레코드 추가:** 드롭다운 목록에서 **CNAME 레코드**를 선택합니다. 
    
    ![CrazyDomains-BP-구성-3-1](../media/2f02538b-fc79-46d2-a2b7-1022eaf0fb08.png)
  
7. **추가**를 선택합니다.
    
    ![CrazyDomains-BP-구성-3-2](../media/4c5929cf-1c21-4af9-899b-e36091f0f14d.png)
  
8. 6개의 CNAME 레코드 중 첫 번째 레코드를 추가합니다.
    
    새 레코드의 상자에서 다음 표에 있는 첫 번째 행의 값을 입력하거나 복사하여 붙여넣습니다.
    
    |**Sub Domain(하위 도메인)**|**별칭**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![CrazyDomains-BP-구성-3-3](../media/81a7b837-3f4d-4565-89a9-380e4d318acf.png)
  
9. **CNAME 레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-3-4](../media/9bcba729-7085-4ebc-8183-ecde82f5c364.png)
  
10. 두 번째 CNAME 레코드를 추가합니다.
    
    새 레코드의 상자에서 표에 있는 다음 행의 값을 사용한 다음 **CNAME 레코드 추가**를 다시 선택 합니다.
    
    6개의 CNAME 레코드를 모두 만들 때까지 이 프로세스를 반복합니다.
    
11. **업데이트** 를 선택 하 여 변경 내용을 저장 합니다. 
    
    ![CrazyDomains-BP-구성-3-5](../media/dbe578f6-359c-428c-b296-ca624cecfc3c.png)
  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>전자 메일 스팸 방지에 유용한 SPF용 TXT 레코드 추가
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 
  
1. 시작하려면 [이 링크](https://manage.crazydomains.com/members/domains/)를 사용하여 Crazy Domains의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    ![CrazyDomains-BP-구성-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. **내 계정** 섹션에서 **도메인**을 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. **도메인 이름** 페이지의 **도메인** 섹션에서 업데이트 하려는 도메인의 이름을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. **DNS 설정** 섹션에서 드롭다운 목록 아이콘을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. **레코드 추가:** 드롭다운 목록에서 **TXT 레코드**를 선택합니다. 
    
    ![CrazyDomains-BP-구성-4-1](../media/7f2461e2-0468-49bd-9eb0-981e9b2f72d6.png)
  
7. **추가**를 선택합니다.
    
    ![CrazyDomains-BP-구성-4-2](../media/64ef9e1f-676d-46e2-9253-a83d9bcd1c4e.png)
  
8. 새 레코드의 상자에서 다음 표의 값을 입력하거나 붙여넣습니다.
    
    |**Sub Domain(하위 도메인)**|**Text Record(텍스트 레코드)**|
    |:-----|:-----|
    |(이 필드는 비워 둡니다.)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
   
    ![CrazyDomains-BP-구성-4-3](../media/e7fd524a-c94b-4cdd-b264-67abb532a71b.png)
  
9. **업데이트**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-4-4](../media/d4f378ee-0f14-46ae-ba32-1596660ecf91.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>Office 365에 필요한 2개의 SRV 레코드 추가
<a name="BKMK_add_SRV"> </a>

1. 시작하려면 [이 링크](https://manage.crazydomains.com/members/domains/)를 사용하여 Crazy Domains의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    ![CrazyDomains-BP-구성-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. **내 계정** 섹션에서 **도메인**을 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. **도메인 이름** 페이지의 **도메인** 섹션에서 업데이트 하려는 도메인의 이름을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. **DNS 설정** 섹션에서 드롭다운 목록 아이콘을 선택 합니다. 
    
    ![CrazyDomains-BP-구성-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. **레코드 추가:** 드롭다운 목록에서 **SRV 레코드**를 선택합니다. 
    
    ![CrazyDomains-BP-구성-5-1](../media/156acebc-7f6d-4b5e-8493-6bc62ca0ee27.png)
  
7. **추가**를 선택합니다.
    
    ![CrazyDomains-BP-구성-5-2](../media/6a711df7-4215-49b2-b58f-1cf1a242b383.png)
  
8. 처음 2개의 SRV 레코드를 추가합니다.
    
    새 레코드의 상자에서 다음 표에 있는 첫 번째 행의 값을 입력하거나 복사하여 붙여넣습니다.
    
    |**Record Type(레코드 종류)**|**Sub Domain(하위 도메인)**|**우선 순위**|**가중치**|**포트**|**대상**|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV 레코드  <br/> |_sip _tls  <br/> |100  <br/> |개  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |SRV 레코드  <br/> |_sipfederationtls _tcp  <br/> |100  <br/> |개  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
    ![CrazyDomains-BP-구성-5-3](../media/cc0ea6eb-7358-434e-bd1a-2737725c6d41.png)
  
9. **SRV 레코드 추가**를 선택 합니다.
    
    ![CrazyDomains-BP-구성-5-4](../media/de4ec312-6833-469a-b23a-f376140a35ca.png)
  
10. 다른 SRV 레코드를 추가합니다.
    
    새 레코드의 상자에서 표에 있는 두 번째 행의 값을 사용합니다.
    
11. **업데이트** 를 선택 하 여 변경 내용을 저장 합니다. 
    
    ![CrazyDomains-BP-구성-5-5](../media/f0bb1dd6-3772-4293-bf74-710f635e0658.png)
  
> [!NOTE]
> 일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  