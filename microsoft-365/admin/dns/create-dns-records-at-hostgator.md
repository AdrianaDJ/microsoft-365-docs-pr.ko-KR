---
title: Hostgator에서 Office 365용 DNS 레코드 만들기
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
ms.assetid: 5f0c840e-4140-4571-88ed-cf235ff142d6
description: 도메인을 확인 하 고 전자 메일, 비즈니스용 Skype Online 및 기타 서비스에 대 한 DNS 레코드를 Office 365 용 Hostgator에 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: cb0b26081e5946ed2558d090c976847197ed7eb8
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42249143"
---
# <a name="create-dns-records-at-hostgator-for-office-365"></a>Hostgator에서 Office 365용 DNS 레코드 만들기

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
DNS 호스팅 공급자로 Hostgator를 사용하고 있는 경우, 이 문서에 나와 있는 단계를 따라 도메인을 확인하고 전자 메일, 비즈니스용 Skype Online 등에 대한 DNS 레코드를 설정합니다.
  
> [!IMPORTANT]
> 이 문서의 다른 절차를 사용 하 여 DNS 레코드를 추가 하기 전에 첫 번째 procedurebelow를 수행 하 여 [호스팅 계정에 대 한 도메인을 가리키도록](#point-your-domain-to-your-hosting-account)해야 합니다. 

Hostgator에서 이렇게 변경하고 나면 도메인이 Office 365 서비스에서 작동하도록 설정됩니다.
  
Office 365에서 웹 사이트의 웹 호스팅 및 DNS에 대한 자세한 내용은 [Office 365에서 공개 웹 사이트 사용](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)을 참조하세요.
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
## <a name="point-your-domain-to-your-hosting-account"></a>도메인을 호스팅 계정에 연결
<a name="BKMK_PointDomain"> </a>

> [!IMPORTANT]
> 이 문서의 다른 절차를 수행하기 전에 이 절차를 수행해야 합니다. 
  
이러한 단계에 따라 도메인 및 호스팅 계정을 연결합니다.
  
1. 시작하려면 [이 링크](https://portal.hostgator.com/)를 사용하여 Hostgator의 도메인 관리 페이지로 이동합니다. 로그인하라는 메시지가 표시됩니다.
    
2. 왼쪽에서 **도메인** 을 선택 합니다.
  
3. **도메인 관리** 페이지에서 업데이트 하려는 도메인을 선택 합니다. 
  
4. 왼쪽의 팝업 메뉴에서 **이름 서버**를 선택 합니다.
  
5. 도메인의 **이름 서버** 페이지에 있는 **이 도메인을 내 호스팅 계정으로 자동 가리키기** 드롭다운 목록에서 도메인과 연결 된 호스팅 계정을 선택 합니다. 
  
6. **이름 서버 저장**을 선택 합니다.
    
  
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가
<a name="BKMK_verify"> </a>

> [!IMPORTANT]
> 이 절차를 수행하기 전에 이 문서의 첫 번째 구역에 있는 절차, [도메인을 호스팅 계정에 연결](#point-your-domain-to-your-hosting-account)을 수행해야 합니다. 
  
Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. To get started, go to your cPanel page at Hostgator. You'll be prompted to log in first.
    
    (Each hosted account at Hostgator is assigned a unique cPanel address. cPanel 주소의 형식은 https://YourSiteAddress:secure-port-number와 같습니다. Hostgator에서 받은 등록 전자 메일에는 해당 주소가 지정 되 고, **호스팅** 페이지 에서도 cpanel 링크를 사용할 수 있습니다.
    
    > [!IMPORTANT]
    > 도메인과 연결된 cPanel을 소유하려면 Hostgator의 호스팅 계정이 필요합니다. Office 365를 시작하려면 Hostgator에서 호스팅 계정을 구입하거나 [이름 서버가 Office 365를 가리키도록 다시 위임](change-nameservers-at-hostgator.md)할 수 있습니다. 
  
2. **제어판** 페이지의 **도메인** 영역에서 **고급 영역 편집기**를 선택 합니다.
    
3. **고급 영역 편집기** 페이지의 **레코드 추가** 영역에서 새 레코드 용 상자에 다음 표의 값을 입력 하거나 복사 하 여 붙여넣습니다. 
    
    (드롭다운 목록에서 **Type(종류)** 값을 선택합니다.) 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |**이름** <br/> |**TTL** <br/> |**유형** <br/> |**TXT 데이터** <br/> |
    |*Domain_name*를 사용 합니다. (for example, fourthcoffee.com.)  <br/> **This value MUST end with a period (.)** <br/> |개  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
4. **레코드 추가**를 선택 합니다.
    
5. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
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

> [!IMPORTANT]
> 이 절차를 수행하기 전에 이 문서의 첫 번째 구역에 있는 절차, [도메인을 호스팅 계정에 연결](#point-your-domain-to-your-hosting-account)을 수행해야 합니다. 
  
1. 시작하려면 Hostgator의 cPanel 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    (Hostgator에서 호스팅되는 각 계정에는 고유 cPanel 주소가 할당되어 있습니다. cPanel 주소의 형식은 https://YourSiteAddress:secure-port-number와 같습니다. Hostgator에서 받은 등록 전자 메일에는 해당 주소가 지정 되 고, **호스팅** 페이지 에서도 cpanel 링크를 사용할 수 있습니다.
    
    > [!IMPORTANT]
    > 도메인과 연결된 cPanel을 소유하려면 Hostgator의 호스팅 계정이 필요합니다. Office 365를 시작하려면 Hostgator에서 호스팅 계정을 구입하거나 [이름 서버가 Office 365를 가리키도록 다시 위임](change-nameservers-at-hostgator.md)할 수 있습니다. 
  
2. **제어판** 페이지의 **전자 메일** 영역에서 **MX 항목**을 선택 합니다.
    
 
3. **전자 메일 라우팅** 영역에서 **원격 메일 교환기**를 선택합니다.

4. **변경을**선택 합니다.
  
5. **새 레코드 추가** 영역의 새 레코드 용 상자에 다음 표의 값을 입력 하거나 복사 하 여 붙여넣습니다. 
    
    |**우선 순위**|**대상**|
    |:-----|:-----|
    |개  <br/> 우선 순위에 대한 자세한 내용은 [MX 우선 순위란?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)을 참조하세요. <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **참고:** \< Office 365 계정에서 *도메인 키* \> 를 가져옵니다.    [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
  
6. **새 레코드 추가**를 선택 합니다.
   
 
7. **Mx 레코드** 구역에 다른 mx 레코드가 있으면 각 레코드를 제거 합니다. 

    
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>Office 365에 필요한 6개의 CNAME 레코드 추가
<a name="BKMK_add_CNAME"> </a>

> [!IMPORTANT]
> 이 절차를 수행하기 전에 이 문서의 첫 번째 구역에 있는 절차, [도메인을 호스팅 계정에 연결](#point-your-domain-to-your-hosting-account)을 수행해야 합니다. 
  
1. 시작하려면 Hostgator의 cPanel 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    (Hostgator에서 호스팅되는 각 계정에는 고유 cPanel 주소가 할당되어 있습니다. cPanel 주소의 형식은 https://YourSiteAddress:secure-port-number와 같습니다. Hostgator에서 받은 등록 전자 메일에는 해당 주소가 지정 되 고, **호스팅** 페이지 에서도 cpanel 링크를 사용할 수 있습니다.
    
    > [!IMPORTANT]
    > 도메인과 연결된 cPanel을 소유하려면 Hostgator의 호스팅 계정이 필요합니다. Office 365를 시작하려면 Hostgator에서 호스팅 계정을 구입하거나 [이름 서버가 Office 365를 가리키도록 다시 위임](change-nameservers-at-hostgator.md)할 수 있습니다. 
  
2. **제어판** 페이지의 **도메인** 영역에서 **고급 영역 편집기**를 선택 합니다.
    
3. 6개의 CNAME 레코드 중 첫 번째 레코드를 추가합니다.
    
    **고급 영역 편집기** 페이지의 **레코드 추가** 영역의 새 레코드 용 상자에 다음 표에 있는 첫 번째 행의 값을 입력 하거나 복사 하 여 붙여넣습니다. 
    
    (드롭다운 목록에서 **Type(종류)** 값을 선택합니다.) 
    
    |**이름**|**TTL**|**종류**|**CNAME**|
    |:-----|:-----|:-----|:-----|
    |autodiscover. *domain_name*합니다. (예: autodiscover.fourthcoffee.com)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |CNAME  <br/> |autodiscover.outlook.com  <br/> |
    |sip. *domain_name*합니다. (예: sip.fourthcoffee.com)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |CNAME  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover. *domain_name*합니다. (예: lyncdiscover.fourthcoffee.com)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |CNAME  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration. *domain_name*합니다. (예: enterpriseregistration.fourthcoffee.com)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |CNAME  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment. *domain_name*합니다. (예: enterpriseregistration.fourthcoffee.com)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |CNAME  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |

  
4. **레코드 추가**를 선택 합니다.

5. 나머지 5개의 CNAME 레코드를 각각 추가합니다.
    
    **레코드 추가** 구역에서 표의 다음 행 값을 사용 하 여 레코드를 만들고 다시 **레코드 추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
    6개의 CNAME 레코드를 모두 만들 때까지 이 프로세스를 반복합니다.
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>전자 메일 스팸 방지에 유용한 SPF용 TXT 레코드 추가
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a single SPF record that includes both sets of values. Need examples? 이러한 [외부 도메인 이름 시스템 레코드에서 Office 365를](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords)확인 하세요. To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md). 
  
> [!IMPORTANT]
> 이 절차를 수행하기 전에 이 문서의 첫 번째 구역에 있는 절차, [도메인을 호스팅 계정에 연결](#point-your-domain-to-your-hosting-account)을 수행해야 합니다. 
  
1. 시작하려면 Hostgator의 cPanel 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    (Hostgator에서 호스팅되는 각 계정에는 고유 cPanel 주소가 할당되어 있습니다. cPanel 주소의 형식은 https://YourSiteAddress:secure-port-number와 같습니다. Hostgator에서 받은 등록 전자 메일에는 해당 주소가 지정 되 고, **호스팅** 페이지 에서도 cpanel 링크를 사용할 수 있습니다.
    
    > [!IMPORTANT]
    > 도메인과 연결된 cPanel을 소유하려면 Hostgator의 호스팅 계정이 필요합니다. Office 365를 시작하려면 Hostgator에서 호스팅 계정을 구입하거나 [이름 서버가 Office 365를 가리키도록 다시 위임](change-nameservers-at-hostgator.md)할 수 있습니다. 
  
2. **제어판** 페이지의 **도메인** 영역에서 **고급 영역 편집기**를 선택 합니다.
    
3. On the **Advanced DNS Zone Editor** page, in the **Add a Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (드롭다운 목록에서 **Type(종류)** 값을 선택합니다.) 
    
    |**이름**|**TTL**|**유형**|**TXT 데이터**|
    |:-----|:-----|:-----|:-----|
    |*Domain_name*를 사용 합니다. (for example, fourthcoffee.com.)  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
  
4. **레코드 추가**를 선택 합니다.
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>Office 365에 필요한 2개의 SRV 레코드 추가
<a name="BKMK_add_SRV"> </a>

> [!IMPORTANT]
> 이 절차를 수행하기 전에 이 문서의 첫 번째 구역에 있는 절차, [도메인을 호스팅 계정에 연결](#point-your-domain-to-your-hosting-account)을 수행해야 합니다. 
  
1. 시작하려면 Hostgator의 cPanel 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
    (Hostgator에서 호스팅되는 각 계정에는 고유 cPanel 주소가 할당되어 있습니다. cPanel 주소의 형식은 https://YourSiteAddress:secure-port-number와 같습니다. Hostgator에서 받은 등록 전자 메일에는 해당 주소가 지정 되 고, **호스팅** 페이지 에서도 cpanel 링크를 사용할 수 있습니다.
    
    > [!IMPORTANT]
    > 도메인과 연결된 cPanel을 소유하려면 Hostgator의 호스팅 계정이 필요합니다. Office 365를 시작하려면 Hostgator에서 호스팅 계정을 구입하거나 [이름 서버가 Office 365를 가리키도록 다시 위임](change-nameservers-at-hostgator.md)할 수 있습니다. 
  
2. **제어판** 페이지의 **도메인** 영역에서 **고급 영역 편집기**를 선택 합니다.

    
3. 2개의 SRV 레코드 중 첫 번째 레코드를 추가합니다.
    
    **고급 DNS 영역 편집기** 페이지의 **레코드 추가** 영역에서 새 레코드용 상자에 다음 표의 첫 번째 행 값을 입력하거나 복사하여 붙여넣습니다. 
    
    (드롭다운 목록에서 **Type(종류)** 값을 선택합니다.) 
    
    |**이름**|**TTL**|**종류**|**우선 순위**|**가중치**|**포트**|**대상**|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |_tls을 _sip 합니다. *domain_name*합니다. 예를 들어 fourthcoffee를 _tls _sip 합니다.  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |SRV  <br/> |100  <br/> |개  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |_tcp을 _sipfederationtls 합니다. *domain_name*합니다. 예를 들어 fourthcoffee를 _tcp _sipfederationtls 합니다.  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |3600  <br/> |SRV  <br/> |100  <br/> |개  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   

4. **레코드 추가**를 선택 합니다.

  
5. 다른 SRV 레코드를 추가합니다.
    
    **레코드 추가** 구역에서 표의 다음 행 값을 사용 하 여 레코드를 만들고 다시 **레코드 추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 