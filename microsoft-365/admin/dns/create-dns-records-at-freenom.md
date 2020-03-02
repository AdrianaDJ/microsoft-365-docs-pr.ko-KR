---
title: Freenom에서 Office 365에 대 한 DNS 레코드 만들기
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
ms.assetid: d8ff45a2-19e3-413d-aa64-a9982bd6633c
description: 도메인을 확인 하 고 전자 메일, 비즈니스용 Skype Online에 대 한 DNS 레코드를 설정 하 고 Office 365에 대 한 Freenom에 있는 기타 서비스를 설치 하는 방법을 알아봅니다.
ms.openlocfilehash: a1396964c7dc9c279589a6020e0c741fd0cb29d5
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42248974"
---
# <a name="create-dns-records-at-freenom-for-office-365"></a>Freenom에서 Office 365에 대 한 DNS 레코드 만들기

원하는 정보를 찾지 못한 경우 [도메인 FAQ를 확인](../setup/domains-faq.md) 합니다. 
  
> [!CAUTION]
> Freenom 웹 사이트에서는 SRV 레코드를 지원 하지 않으므로 비즈니스용 Skype 온라인 및 Outlook Web App 기능이 여러 개 작동 하지 않습니다. 사용 하는 Office 365 계획에 관계 없이 중요 한 서비스 제한이 있으며 다른 DNS 호스팅 공급자로 전환할 수 있습니다. 
  
서비스 제한 사항에도 불구 하 고 Freenom에서 자체 Office 365 DNS 레코드를 관리 하도록 선택 하 고,이 문서에 나와 있는 단계에 따라 도메인을 확인 하 고 전자 메일 및 기타 서비스에 대 한 DNS 레코드를 설정 합니다.
  
Office 365에서 웹 사이트의 웹 호스팅 및 DNS에 대한 자세한 내용은 [Office 365에서 공개 웹 사이트 사용](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx)을 참조하세요.
  
> [!NOTE]
> 일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가
<a name="bkmk_txt"> </a>

Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. 시작 하려면 [이 링크](https://my.freenom.com/)를 사용 하 여 Freenom의 도메인 페이지로 이동 합니다. You'll be prompted to log in.
    
    ![Freenom 로그인](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. **서비스**를 선택한 다음 **내 도메인**을 선택 합니다.
    
    ![Freenom 서비스 및 내 도메인 선택](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. 편집 하려는 도메인에서 **도메인 관리**를 선택 합니다.
    
    ![Freenom 관리 도메인 선택](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. **Freenom DNS 관리**를 선택 합니다.
    
    ![Freenom 관리 Freenom DNS](../media/9854a511-27e3-4658-8903-34b3d425096d.png)
  
5. **레코드 추가**의 **형식** 열에 있는 메뉴에서 **TXT** 를 선택 합니다. 
    
    ![Freenom 레코드 형식 TXT 추가](../media/7f0e85e7-844f-4962-815e-5d80d9e6efa0.png)
  
6. In the boxes for the new record, type or copy and paste the values from the following table. 
    
    |**이름**|**종류**|**TTL**|**대상**|
    |:-----|:-----|:-----|:-----|
    |(공백으로 둠)  <br/> |TXT  <br/> |3600 (초)  <br/> |MS = msXXXXXXXX  <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다.           [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![확인을 위한 freenom TXT 값](../media/650098df-b3aa-47e5-9763-7fde24e34c3f.png)
  
7. **변경 내용 저장**을 선택 합니다.
    
    ![Freenom TXT 레코드 저장 변경 내용](../media/b1a63f9a-4578-491a-9554-c40f73b37e09.png)
  
8. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 관리 센터에서 **설정** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">도메인</a> 페이지로 이동 합니다.

    
2. **도메인** 페이지에서 확인 하려는 도메인을 선택 합니다. 
    
    
  
3. **설정** 페이지에서 **설정 시작**을 선택 합니다.
    
    
  
4. **도메인 확인** 페이지에서 **확인**을 선택 합니다.
    
    
  
> [!NOTE]
>  일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a>사용자 도메인의 전자 메일이 Office 365로 전송되도록 MX 레코드 추가
<a name="bkmk_mx"> </a>

1. 시작 하려면 [이 링크](https://my.freenom.com/)를 사용 하 여 Freenom의 도메인 페이지로 이동 합니다. You'll be prompted to log in.
    
    ![Freenom 로그인](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. **서비스**를 선택한 다음 **내 도메인**을 선택 합니다.
    
    ![Freenom 서비스 및 내 도메인 선택](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. 편집 하려는 도메인에서 **도메인 관리**를 선택 합니다.
    
    ![Freenom 관리 도메인 선택](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. 도메인에 사용 되는 이름을 기본 Freenom 이름 서버로 설정 합니다. **관리 도구**를 선택 하 고 **이름 서버**를 선택 합니다.
    
    ![Freenom 이름 서버 설정](../media/a6ae877a-c248-42b9-bae9-210a80cd01e7.png)
  
5. **기본 이름 서버 사용** 이 선택 되어 있는지 확인 하 고 **이름 서버 변경을**선택 합니다.
    
    ![Freenom 변경 이름 서버](../media/0ef90d84-c0a0-4ef9-9e4c-43ef0aac3a2e.png)
  
6. **Freenom DNS 관리**를 선택 합니다.
    
    ![Freenom 관리에서 Freenom DNS를 선택 합니다.](../media/f55a8053-2411-45da-a357-776c6699f721.png)
  
7. **레코드 추가**의 **종류** 열에 있는 메뉴에서 **MX** 를 선택 합니다. 
    
    ![Freenom 레코드 유형 MX 추가](../media/c728c6ee-786c-4f6a-8ad5-1d9914a5bfcf.png)
  
8. 새 레코드의 상자에서 다음 표에 있는 첫 번째 행의 값을 입력하거나 복사하여 붙여넣습니다. 
    
    |**이름**|**종류**|**TTL**|**대상**|**우선 순위**|
    |:-----|:-----|:-----|:-----|:-----|
    |(공백으로 둠)  <br/> |MX (Mail Exchanger)(MX(메일 교환기))  <br/> |3600 (초)  <br/> |\<\>mail.protection.outlook.com  <br/> **참고:** Office 365 계정에서 * \<도메인\> 키* 를 가져옵니다.   [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |10   <br/> 우선 순위에 대한 자세한 내용은 [MX 우선 순위란?](https://support.office.com/article/17d415c1-067e-4974-84d5-aaeaf3a0c0a9)을 참조하세요. <br/> |
   
   ![Freenom MX 레코드](../media/8896c4a9-b3dd-45ed-9916-f7da2715ba8c.png)
  
9. **변경 내용 저장**을 선택 합니다.
    
    ![Freenom MX 레코드 저장 변경 내용](../media/7aa0a464-d136-417f-be40-48d3f728eeb7.png)
  
10. 다른 MX 레코드가 있으면 모두 삭제 합니다. 각 레코드에 대해 **삭제**를 선택 합니다. **이 항목을 정말로 제거 하 시겠습니까?** 라는 메시지가 나타나면 **확인**을 선택 합니다.
    
## <a name="add-the-cname-records-that-are-required-for-office-365"></a>Office 365에 필요한 CNAME 레코드 추가
<a name="bkmk_cname"> </a>

1. 시작 하려면 [이 링크](https://my.freenom.com/)를 사용 하 여 Freenom의 도메인 페이지로 이동 합니다. You'll be prompted to log in.
    
    ![Freenom 로그인](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. **서비스**를 선택한 다음 **내 도메인**을 선택 합니다.
    
    ![Freenom 서비스 및 내 도메인 선택](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. 편집 하려는 도메인에서 **도메인 관리**를 선택 합니다.
    
    ![Freenom 관리 도메인 선택](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. **Freenom DNS 관리**를 선택 합니다.
    
    ![Freenom 관리에서 Freenom DNS를 선택 합니다.](../media/5e7bc3a7-0d5e-431b-bb27-da3b0f316d01.png)
  
5. **레코드 추가**의 **종류** 열에 있는 메뉴에서 **CNAME** 을 선택 합니다. 
    
    ![Freenom 레코드 형식 CNAME 추가](../media/9b204755-ca2a-46d2-bce2-030d82fd1f9e.png)
  
6. 첫 번째 CNAME 레코드를 만듭니다. 새 레코드의 상자에서 다음 표에 있는 첫 번째 행의 값을 입력하거나 복사하여 붙여넣습니다. 
    
    |**이름**|**Record type(레코드 종류)**|**TTL**|**대상**|
    |:-----|:-----|:-----|:-----|
    |autodiscover  <br/> |CNAME  <br/> |3600 (초)  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |CNAME  <br/> |3600 (초)  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |CNAME  <br/> |3600 (초)  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |CNAME  <br/> |3600 (초)  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |CNAME  <br/> |3600 (초)  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![Freenom CNAME 값](../media/752fc682-e3f2-4b9c-9253-bf1ba2d414e9.png)
  
7. **변경 내용 저장**을 선택 합니다.
    
    ![Freenom CNAME 저장 변경 내용](../media/68103fd2-0f5f-4aac-a875-25157c6bbdd2.png)
  
8. 이전 단계를 반복 하 여 나머지 5 개의 CNAME 레코드를 만듭니다. 
    
    각 레코드에 대해 위 표에 있는 다음 행의 값을 해당 레코드의 상자에 입력 하거나 복사 하 여 붙여넣습니다.
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a>전자 메일 스팸 방지에 유용한 SPF용 TXT 레코드 추가
<a name="bkmk_spf"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 

1. 시작 하려면 [이 링크](https://my.freenom.com/)를 사용 하 여 Freenom의 도메인 페이지로 이동 합니다. You'll be prompted to log in.
    
    ![Freenom 로그인](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. **서비스**를 선택한 다음 **내 도메인**을 선택 합니다.
    
    ![Freenom 서비스 및 내 도메인 선택](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. 편집 하려는 도메인에서 **도메인 관리**를 선택 합니다.
    
    ![Freenom 관리 도메인 선택](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. **Freenom DNS 관리**를 선택 합니다.
    
    ![Freenom 관리에서 Freenom DNS를 선택 합니다.](../media/94809955-0315-409c-a15d-703a2fe4c4ed.png)
  
5. **레코드 추가**의 **형식** 열에 있는 메뉴에서 **TXT** 를 선택 합니다. 
    
    ![Freenom 레코드 형식 TXT 추가](../media/d8854285-c4ae-416c-a072-72a11ba1cd9a.png)
  
6. In the boxes for the new record, type or copy and paste the following values. 
    
    |**이름**|**Record type(레코드 종류)**|**TTL**|**대상**|
    |:-----|:-----|:-----|:-----|
    |(공백으로 둠)  <br/> |TXT  <br/> |3600 (초)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/>**참고:** 모든 공백이 올바르게 유지 되도록이 항목을 복사 하 여 붙여 넣는 것이 좋습니다.           |
   
    ![SPF의 freenom TXT 값](../media/1b3b1199-9104-4ca1-acdb-786d139c21ac.png)
  
7. **변경 내용 저장**을 선택 합니다.
    
    ![SPF 저장 변경에 대 한 freenom TXT 레코드](../media/e2fc52b1-0dcb-4595-9a4c-fca5e2ef9f97.png)
  
