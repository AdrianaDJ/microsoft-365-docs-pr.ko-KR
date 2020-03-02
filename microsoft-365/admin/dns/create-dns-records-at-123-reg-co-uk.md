---
title: 123 reg.co.uk에서 Office 365용 DNS 레코드를 만들기
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
ms.assetid: 1f2d08c9-2a88-4d2f-ae1f-e39f9e358b17
description: 도메인을 확인 하 고 전자 메일, 비즈니스용 Skype Online 및 기타 서비스에 대 한 DNS 레코드를 Office 365 용 123-reg.co.uk에 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: acbc0f1c8a7eb7dcbe5f274d0f2c8b2c403e7de0
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42246882"
---
# <a name="create-dns-records-at-123-regcouk-for-office-365"></a>123 reg.co.uk에서 Office 365용 DNS 레코드를 만들기

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
DNS 호스팅 공급자로 123-reg.co.uk를 사용하고 있는 경우, 이 문서에 나와 있는 단계를 따라 도메인을 확인하고 전자 메일, 비즈니스용 Skype Online 등에 대한 DNS 레코드를 설정합니다.
  
123-reg.co.uk에서 이러한 레코드를 추가하고 나면 도메인이 Office 365 서비스에서 작동하도록 설정됩니다.
  
Office 365에서 웹 사이트의 웹 호스팅 및 DNS에 대한 자세한 내용은 [Office 365에서 공개 웹 사이트 사용](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)을 참조하세요.
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가
<a name="BKMK_verify"> </a>

Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. 시작하려면 [이 링크](https://www.123-reg.co.uk/secure/cpanel/domain/overview)를 사용하여 123-reg.co.uk의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. On the **Domain name overview** page, select the name of the domain that you want to edit. 
    
3. Choose **DNS** from the **Select action** drop-down list. 
    
4. **DNS 관리** 페이지에서 **고급 DNS** 탭을 선택 합니다. 
    
5. In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    ||||
    |:-----|:-----|:-----|
    |**호스트 이름** <br/> |**종류** <br/> |**Destination TXT/SPF** <br/> |
    |@  <br/> |TXT/SPF  <br/> |MS=ms *XXXXXXXX*  <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
6. **추가**를 선택합니다.
    
7. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 관리 센터에서 **설정** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">도메인</a> 페이지로 이동 합니다.

    
2. **도메인** 페이지에서 확인 하려는 도메인을 선택 합니다. 
    
3. **설정** 페이지에서 **설정 시작**을 선택 합니다.
    
4. **도메인 확인** 페이지에서 **확인**을 선택 합니다.
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>사용자 도메인의 전자 메일이 Office 365로 전송되도록 MX 레코드 추가
<a name="BKMK_add_MX"> </a>

1. 시작하려면 [이 링크](https://www.123-reg.co.uk/secure/cpanel/domain/overview)를 사용하여 123-reg.co.uk의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. On the **Domain name overview** page, select the name of the domain that you want to edit. 
    
3. Choose **DNS** from the **Select action** drop-down list. 
    
4. **DNS 관리** 페이지에서 **고급 DNS** 탭을 선택 합니다. 
    
5. In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**호스트 이름**|**종류**|**우선 순위**|**대상 MX**|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |MX  <br/> |개  <br/> 우선 순위에 대한 자세한 내용은 [MX 우선 순위란?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)을 참조하세요. <br/> | *\<domain-key\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> **참고:** Office 365 \<계정에서 도메인\> 키를 가져옵니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![표의 값 복사 및 붙여넣기](../media/65366165-85a6-4a39-b9a7-6c5f47fbe790.png)
  
6. **추가**를 선택합니다.
    
    ![추가를 선택 합니다.](../media/a8ae6c0c-4365-4137-af8a-6e003996e3d0.png)
  
7. 다른 MX 레코드가 있으면 해당 레코드에 대한 **삭제(휴지통)** 아이콘을 선택하여 각 레코드를 삭제합니다. 
    
    ![삭제 (휴지통 아이콘)를 선택 합니다.](../media/3be635e6-b591-49af-8430-a158272834b4.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>Office 365에 필요한 6개의 CNAME 레코드 추가
<a name="BKMK_add_CNAME"> </a>

1. 시작하려면 [이 링크](https://www.123-reg.co.uk/secure/cpanel/domain/overview)를 사용하여 123-reg.co.uk의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. On the **Domain name overview** page, select the name of the domain that you want to edit. 
    
3. Choose **DNS** from the **Select action** drop-down list. 
    
4. **DNS 관리** 페이지에서 **고급 DNS** 탭을 선택 합니다. 
    
5. 6개의 CNAME 레코드 중 첫 번째 레코드를 추가합니다.
    
    In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**호스트 이름**|**종류**|**대상 CNAME**|
    |:-----|:-----|:-----|
    |autodiscover  <br/> |CNAME  <br/> |autodiscover.outlook.com  <br/> **This value MUST end with a period (.)** <br/> |
    |sip  <br/> |CNAME  <br/> |sipdir.online.lync.com  <br/> **This value MUST end with a period (.)** <br/> |
    |lyncdiscover  <br/> |CNAME  <br/> |webdir.online.lync.com  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseregistration  <br/> |CNAME  <br/> |enterpriseregistration.windows.net  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |
    |enterpriseenrollment  <br/> |CNAME  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |
   
    ![테이블의 값을 복사 하 여 붙여넣기](../media/24bf388c-5f7f-4fc0-b4ec-4b17226b6246.png)
  
6. **추가**를 선택합니다.
    
    ![추가를 선택 합니다.](../media/825a9854-559d-4a22-90ac-5e7a0a54269a.png)
  
7. 나머지 5개의 CNAME 레코드를 추가합니다.
    
    **고급 DNS** 구역에서 표의 다음 행 값을 사용 하 여 레코드를 만들고 다시 **추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
    6개의 CNAME 레코드를 모두 만들 때까지 이 프로세스를 반복합니다.
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>전자 메일 스팸 방지에 유용한 SPF용 TXT 레코드 추가
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. Need examples? 이러한 [외부 도메인 이름 시스템 레코드에서 Office 365를](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords)확인 하세요. To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md). 
  
1. 시작하려면 [이 링크](https://www.123-reg.co.uk/secure/cpanel/domain/overview)를 사용하여 123-reg.co.uk의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. On the **Domain name overview** page, select the name of the domain that you want to edit. 
    
3. Choose **DNS** from the **Select action** drop-down list. 
    
4. **DNS 관리** 페이지에서 **고급 DNS** 탭을 선택 합니다. 
    
5. In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**호스트 이름**|**종류**|**Destination TXT/SPF**|
    |:-----|:-----|:-----|
    |@  <br/> |TXT/SPF  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
   
    ![123Reg-BP-4-1](../media/4697701c-eba0-4b03-8d75-4f7fc3bef94a.png)
  
6. **추가**를 선택합니다.
    
    ![추가를 선택 합니다.](../media/7906dd91-fd23-44c3-bb37-ef185655c6eb.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>Office 365에 필요한 2개의 SRV 레코드 추가
<a name="BKMK_add_SRV"> </a>

1. 시작하려면 [이 링크](https://www.123-reg.co.uk/secure/cpanel/domain/overview)를 사용하여 123-reg.co.uk의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. On the **Domain name overview** page, select the name of the domain that you want to edit. 
    
3. Choose **DNS** from the **Select action** drop-down list. 
    
4. **DNS 관리** 페이지에서 **고급 DNS** 탭을 선택 합니다. 
    
5. 처음 2개의 SRV 레코드를 추가합니다.
    
    In the **Advanced DNS** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    ||||||
    |:-----|:-----|:-----|:-----|:-----|
    |호스트 이름|종류|우선 순위|TTL|대상 SRV|
    |_sip _tls|SRV|100|3600|1 443 sipdir.online.lync.com. **This value MUST end with a period (.)**<br> **참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
    |_sipfederationtls _tcp|SRV|100|3600|1 5061 sipfed.online.lync.com. **This value MUST end with a period (.)** <br> **참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
   
    ![테이블의 값을 복사 하 여 붙여넣기](../media/c1786b86-52ef-4dca-8b99-b479554fa531.png)
  
6. **추가**를 선택합니다.
    
    ![추가를 선택 합니다.](../media/5fd9d3a2-a8bb-466b-829f-b3a6e54b5104.png)
  
7. 다른 SRV 레코드를 추가하려면
    
    **고급 DNS** 구역에서 표의 두 번째 행 값을 사용 하 여 레코드를 만들고 다시 **추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  