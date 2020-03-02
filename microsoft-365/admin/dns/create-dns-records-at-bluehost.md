---
title: Bluehost에서 Office 365용 DNS 레코드 만들기
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
ms.assetid: 657934ff-d9d2-4563-9ccf-ef4832a03a99
description: 도메인을 확인 하 고 전자 메일, 비즈니스용 Skype Online 및 기타 서비스에 대 한 DNS 레코드를 Office 365 용 Bluehost에 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: 9a5cad6778cb66958539a324befee43ddb2dd8b9
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42247215"
---
# <a name="create-dns-records-at-bluehost-for-office-365"></a>Bluehost에서 Office 365용 DNS 레코드 만들기

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
DNS 호스팅 공급자로 Bluehost를 사용하고 있는 경우, 이 문서에 나와 있는 단계를 따라 도메인을 확인하고 전자 메일, 비즈니스용 Skype Online 등에 대한 DNS 레코드를 설정합니다.
  
Bluehost에서 이러한 레코드를 추가하고 나면 도메인이 Office 365 서비스에서 작동하도록 설정됩니다.
  
Office 365에서 웹 사이트의 웹 호스팅 및 DNS에 대한 자세한 내용은 [Office 365에서 공개 웹 사이트 사용](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9)을 참조하세요.
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가
<a name="BKMK_verify"> </a>

Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. 시작하려면 [이 링크](https://my.bluehost.com/cgi/dm)를 사용하여 Bluehost의 도메인 페이지로 이동합니다. You'll be prompted to log in first.
    
2. **domains(도메인)** 페이지의 **domain(도메인)** 영역에서 변경 중인 도메인의 행을 찾아 해당 도메인의 확인란을 선택합니다. 
    
    (아래로 스크롤해야 할 수 있습니다.)
    
3. ***Domain_name*** 영역의 **dns 영역 편집기** 행에서 **dns 레코드 관리**를 선택 합니다.
    
4. * * DNS 영역 편집기 * * 페이지의 **Dns 레코드 추가** 영역의 새 레코드 용 상자에 다음 표의 값을 입력 하거나 복사 하 여 붙여넣습니다. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |**Host Record** <br/> |**TTL** <br/> |**종류** <br/> |**TXT Value** <br/> |
    |@  <br/> |14400  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
5. **레코드 추가**를 선택 합니다.
    
6. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
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

1. 시작하려면 [이 링크](https://my.bluehost.com/cgi/dm)를 사용하여 Bluehost의 도메인 페이지로 이동합니다. You'll be prompted to log in first.
    
2. **domains(도메인)** 페이지의 **domain(도메인)** 영역에서 변경 중인 도메인의 행을 찾아 해당 도메인의 확인란을 선택합니다. 
    
    (아래로 스크롤해야 할 수 있습니다.)
    
3. ***Domain_name*** 영역의 **dns 영역 편집기** 행에서 **dns 레코드 관리**를 선택 합니다.
    
4. On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**Host Record**|**TTL**|**유형**|**연결 대상**|**우선 순위**|
    |:-----|:-----|:-----|:-----|:-----|
    |@  <br/> |14400  <br/> |MX  <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/>**참고:** \<Office 365 계정에서 *도메인 키* \> 를 가져옵니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |개  <br/> 우선 순위에 대한 자세한 내용은 [MX 우선 순위란?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)을 참조하세요. <br/> |
   
   ![드롭다운 목록에서 유형을 선택 합니다.](../media/70791420-d83c-4a5d-a46c-5cc3bc67f565.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![레코드 추가 선택](../media/c7ef9733-1665-4dbf-accc-caadf1574abc.png)
  
6. **MX(메일 교환기)** 구역에 다른 MX 레코드가 있으면 하나씩 삭제합니다. 
    
    다른 MX 레코드 중 하나에 대해 삭제를 선택 **합니다.**
    
    ![각 추가 MX 레코드에 대해 삭제를 선택 합니다.](../media/6be17f54-3f33-47af-a9db-4689141530c2.png)
  
7. 확인 대화 상자에서 **확인**을 선택 합니다.
    
    ![확인을 선택 합니다.](../media/a50df7a3-2906-4cc0-87d4-1231ab234230.png)
  
8. 같은 프로세스를 사용하여 이미 나열된 다른 MX 레코드를 삭제합니다.
    
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a>Office 365에 필요한 6개의 CNAME 레코드 추가
<a name="BKMK_add_CNAME"> </a>

1. 시작하려면 [이 링크](https://my.bluehost.com/cgi/dm)를 사용하여 Bluehost의 도메인 페이지로 이동합니다. You'll be prompted to log in first.
    
2. **domains(도메인)** 페이지의 **domain(도메인)** 영역에서 변경 중인 도메인의 행을 찾아 해당 도메인의 확인란을 선택합니다. 
    
    (아래로 스크롤해야 할 수 있습니다.)
    
3. ***Domain_name*** 영역의 **dns 영역 편집기** 행에서 **dns 레코드 관리**를 선택 합니다.
    
4. **A (호스트)** 레코드 구역에서 **자동 검색** 레코드의 행을 찾은 다음 해당 행에 대해 **삭제** 를 선택 합니다. 
    
    > [!IMPORTANT]
    > Office 365에 필요한 기존 **autodiscover** 레코드를 추가하기  *전에*  기존 **autodiscover** 레코드를 삭제해야 합니다. Bluehost에서는 두 개의 **autodiscover** 레코드를 동시에 유지할 수 없습니다. 
  
    ![삭제 선택](../media/416a447e-3710-4ae7-8bf1-459381af4f6e.png)
  
5. **확인**을 선택합니다.
    
    ![확인을 선택 합니다.](../media/0c8f409d-c39f-4ed2-9c95-9af3e61c2411.png)
  
6. 6개의 CNAME 레코드 중 첫 번째 레코드를 만듭니다.
    
    **DNS 영역 편집기** 페이지의 **DNS 레코드 추가** 영역에서 새 레코드용 상자에 다음 표의 첫 번째 행 값을 입력하거나 복사하여 붙여넣습니다. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**Host Record**|**TTL**|**유형**|**연결 대상**|
    |:-----|:-----|:-----|:-----|
    |autodiscover  <br/> |14400  <br/> |CNAME  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |14400  <br/> |CNAME  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |14400  <br/> |CNAME  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |14400  <br/> |CNAME  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |14400  <br/> |CNAME  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![첫 번째 CNAME 레코드 만들기](../media/4f12e9b1-9dec-4bc2-aa15-8bffa71fe131.png)
  
7. **레코드 추가**를 선택 합니다.
    
    ![레코드 추가 선택](../media/c2782250-a9a6-4aee-bb15-f57cb0008587.png)
  
8. 나머지 5개의 CNAME 레코드를 각각 추가합니다.
    
    여전히 **DNS 레코드 추가** 구역에서 표의 다음 행 값을 사용 하 여 레코드를 만들고 다시 **레코드 추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
    6개의 CNAME 레코드를 모두 만들 때까지 이 프로세스를 반복합니다.
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>전자 메일 스팸 방지에 유용한 SPF용 TXT 레코드 추가
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. Need examples? 이러한 [외부 도메인 이름 시스템 레코드에서 Office 365를](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0)확인 하세요. SPF 레코드의 유효성을 검사 하기 위해 이러한[spf 유효성 검사 도구](../setup/domains-faq.md)중 하나를 사용할 수 있습니다. 
  
1. 시작하려면 [이 링크](https://my.bluehost.com/cgi/dm)를 사용하여 Bluehost의 도메인 페이지로 이동합니다. You'll be prompted to log in first.
    
2. **domains(도메인)** 페이지의 **domain(도메인)** 영역에서 변경 중인 도메인의 행을 찾아 해당 도메인의 확인란을 선택합니다. 
    
    (아래로 스크롤해야 할 수 있습니다.)
    
3. ***Domain_name*** 영역의 **dns 영역 편집기** 행에서 **dns 레코드 관리**를 선택 합니다.
    
4. On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
        
    |**Host Record**|**TTL**|**종류**|**TXT Value**|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |14400  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/>**참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
   
    ![TXT 값 복사](../media/b2dabd7a-ee3d-4209-aa1e-0233eb8cf3b9.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![레코드 추가 선택](../media/c050e9a2-2274-4640-8f0f-6752d382df5d.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a>Office 365에 필요한 2개의 SRV 레코드 추가
<a name="BKMK_add_SRV"> </a>

1. 시작하려면 [이 링크](https://my.bluehost.com/cgi/dm)를 사용하여 Bluehost의 도메인 페이지로 이동합니다. You'll be prompted to log in first.
    
2. **domains(도메인)** 페이지의 **domain(도메인)** 영역에서 변경 중인 도메인의 행을 찾아 해당 도메인의 확인란을 선택합니다. 
    
    (아래로 스크롤해야 할 수 있습니다.)
    
3. ***Domain_name*** 영역의 **dns 영역 편집기** 행에서 **dns 레코드 관리**를 선택 합니다.
    
4. 2개의 SRV 레코드 중 첫 번째 레코드를 만듭니다.
    
    **DNS 영역 편집기** 페이지의 **DNS 레코드 추가** 영역에서 새 레코드용 상자에 다음 표의 첫 번째 행 값을 입력하거나 복사하여 붙여넣습니다. 
    
    (Choose the **Type** value from the drop-down list.) 
    
    |**서비스**|**프로토콜**|**호스트**|**TTL**|**유형**|**우선 순위**|**가중치**|**포트**|**연결 대상**|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |_sip  <br/> |_tls  <br/> |@  <br/> |14400  <br/> |SRV  <br/> |100  <br/> |개  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |_sipfederationtls  <br/> |_tcp  <br/> |@  <br/> |14400  <br/> |SRV  <br/> |100  <br/> |개  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
    ![새 레코드의 값을 복사 합니다.](../media/e2911bca-c00b-4b8a-837f-f1d438c474c4.png)
  
5. **레코드 추가**를 선택 합니다.
    
    ![레코드 추가 선택](../media/0fd6a587-03fd-4bce-8321-b14e6ad21f5c.png)
  
6. 다른 SRV 레코드를 추가합니다.
    
    여전히 **DNS 레코드 추가** 구역에서 표에 있는 다른 행의 값을 사용 하 여 레코드를 만들고 다시 **레코드 추가** 를 선택 하 여 해당 레코드를 완료 합니다. 
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
