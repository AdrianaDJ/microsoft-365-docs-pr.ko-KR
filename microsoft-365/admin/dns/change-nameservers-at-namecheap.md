---
title: 이름 서버를 변경 하 여 Namecheap을 사용 하 여 Office 365 설정
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
ms.assetid: 84f467f6-28cf-40f0-94d0-a2a27ddfc2e7
description: 'Office 365에서 DNS 레코드를 관리 하도록 하려면 Namecheap을 사용 하 여 Office 365 사용자 지정 도메인을 설정 하는 방법을 알아봅니다. '
ms.openlocfilehash: caf0a484b82ecf10f2835ae8fd5dea98c16e61c3
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42246606"
---
# <a name="change-nameservers-to-set-up-office-365-with-namecheap"></a>이름 서버를 변경 하 여 Namecheap을 사용 하 여 Office 365 설정

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요.
  
Office 365에서 Office 365 DNS 레코드를 관리하도록 하려면 다음 지침을 따릅니다. 원하는 경우 [모든 Office 365 DNS 레코드를 Namecheap에서 관리할](create-dns-records-at-namecheap.md)수 있습니다.
  
    
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가

1. 시작 하려면 [이 링크](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f)를 사용 하 여 Namecheap의 도메인 페이지로 이동 합니다. 로그인 하 고 계속 진행 하 라는 메시지가 표시 됩니다.
    
    ![Namecheap-BP-1-1](../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. **랜딩** 페이지의 **계정**아래 드롭다운 목록에서 **도메인 목록을** 선택 합니다. 
    
    ![Namecheap-BP-1-2](../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. **도메인 목록** 페이지에서 편집 하려는 도메인의 이름을 찾은 다음 **관리**를 선택 합니다.
    
    ![Namecheap-BP-1-3](../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. **고급 DNS**를 선택 합니다.
    
    ![Namecheap-BP-1-4](../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. **호스트 레코드** 섹션에서 **새 레코드 추가**를 선택 합니다.
    
    ![Namecheap-BP-1-5](../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. **형식** 드롭다운에서 **TXT 레코드**를 선택 합니다.
    
    > [!NOTE]
    > **새 레코드 추가**를 선택 하면 **유형** 드롭다운이 자동으로 표시 됩니다.
  
    ![Namecheap-BP-Verify-1-1](../media/a5b40973-19b5-4c32-8e1b-1521aa971836.png)
  
7. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (드롭다운 목록에서 **TTL** 값을 선택 합니다.) 
    
|**유형**|**호스트**|**값**|**TTL**|
|:-----|:-----|:-----|:-----|
|TXT  <br/> |@  <br/> |MS=ms *XXXXXXXX*  <br/> **참고**:이는 예입니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다.           [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)          |30 분  <br/> |
   
   ![Namecheap-BP-Verify-1-2](../media/fe75c0fd-f85c-4bef-8068-edaf9779b7f1.png)
  
8. **변경 내용 저장** (확인 표시) 컨트롤을 선택 합니다. 
    
    ![Namecheap-BP-Verify-1-3](../media/b48d2c67-66b5-4aa4-8e59-0c764f236fac.png)
  
9. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 관리 센터에서 **설정** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">도메인</a> 페이지로 이동 합니다.

    
2. **도메인** 페이지에서 확인 하려는 도메인을 선택 합니다. 
    
    
  
3. **설정** 페이지에서 **설정 시작**을 선택 합니다.
    
    
  
4. **도메인 확인** 페이지에서 **확인**을 선택 합니다.
    
    
  
> [!NOTE]
>  일반적으로 DNS 변경 내용을 적용하는 데 15분 정도 걸립니다. 그러나 변경한 내용이 인터넷의 DNS 시스템 전체에 업데이트되는 데에는 시간이 오래 걸릴 수 있습니다. DNS 레코드를 추가한 후 메일 흐름이나 기타 문제가 있는 경우 [도메인 이름 또는 DNS 레코드 변경 후 발생한 문제 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조하세요. 
  
## <a name="change-your-domains-nameserver-ns-records"></a>도메인의 NS(이름 서버) 레코드 변경

Office 365에서 도메인 설정을 완료하려면 도메인 등록 기관에서 도메인의 NS 레코드가 Office 365 기본 및 보조 이름 서버를 가리키도록 변경합니다. 이렇게 하면 Office 365가 사용자 대신 도메인의 DNS 레코드를 업데이트하도록 설정됩니다. 전자 메일, 비즈니스용 Skype Online, 공개 웹 사이트가 사용자의 도메인을 사용하도록 모든 레코드가 자동으로 추가되고 모든 설정이 완료됩니다.
  
> [!CAUTION]
> Office 365 이름 서버를 가리키도록 도메인 NS 레코드를 변경하면 현재 도메인에 연결되는 모든 서비스가 영향을 받습니다. 예를 들어 이 변경 내용을 적용하면 사용자의 도메인(예: rob@ *사용자_도메인*  .com)으로 보낸 전자 메일이 Office 365로 수신됩니다. 
  
> [!IMPORTANT]
>  이 섹션의 단계를 완료하면 다음과 같이 네 개의 이름 서버  *만*  나열됩니다. >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com >  다음 절차에는 원치 않는 기타 이름 서버를 목록에서 삭제하는 방법과  *올바른*  이름 서버가 목록에 아직 없는 경우 이를 추가하는 방법이 설명되어 있습니다. 
  
1. 시작 하려면 [이 링크](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f)를 사용 하 여 Namecheap의 도메인 페이지로 이동 합니다. 로그인 하 고 계속 진행 하 라는 메시지가 표시 됩니다.
    
    ![Namecheap-BP-1-1](../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. **랜딩** 페이지의 **계정**아래 드롭다운 목록에서 **도메인 목록을** 선택 합니다. 
    
    ![Namecheap-BP-1-2](../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. **도메인 목록** 페이지에서 편집 하려는 도메인의 이름을 찾은 다음 **관리**를 선택 합니다.
    
    ![Namecheap-BP-1-3](../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. **도메인**을 선택 합니다.
    
    ![Namecheap-BP-Redelegate-1-1](../media/59588406-794e-4ae4-8526-35e3111b5791.png)
  
5. **이름 서버** 섹션을 찾은 다음 **Namecheap 기본** 드롭다운 목록에서 **사용자 지정** 을 선택 합니다. 
    
    ![Namecheap-BP-Redelegate-1-2](../media/7df56295-fdb3-472f-9442-13f780c2c93e.png)
  
6. 현재 표시 된 페이지에 이미 이름 서버 나열 되어 있는지 여부에 따라 다음 두 가지 절차 중 하나를 계속 합니다.
    
### <a name="if-there-are-no-nameservers-already-listed"></a>나열된 이름 서버가 없으면
<a name="BKMK_ProcedureWithOUT"> </a>

1. 이름 서버 **추가** 를 두 번 선택 하 여 두 개의 새 행을 추가 합니다.
    
    ![Namecheap-BP-Redelegate-1-3-1](../media/e8816bf5-bb59-49d5-bfca-43e502242dc3.png)
  
2. 이름 서버 **상자에서** 다음 표의 값을 입력 하거나 복사 하 여 붙여넣습니다.
    
|||
|:-----|:-----|
|**이름 서버 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**이름 서버 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**이름 서버 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**이름 서버 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
   ![Namecheap-BP-Redelegate-1-3-2](../media/21d681b7-4f96-4e96-ac27-9534c388537c.png)
  
3. **저장** (확인 표시) 컨트롤을 선택 합니다. 
    
    ![Namecheap-BP-Redelegate-1-5](../media/07aaf1e5-c24f-4c51-bfe0-f99868b3bf35.png)
  
> [!NOTE]
> 이름 서버 레코드 업데이트가 인터넷의 DNS 시스템 전체에 업데이트되기까지 몇 시간이 걸릴 수 있습니다. 그 후에는 Office 365 전자 메일 및 기타 서비스가 모두 사용자의 도메인을 사용하도록 설정됩니다. 
  
### <a name="if-there-are-nameservers-already-listed"></a>이름 서버가 나열되어 있는 경우

> [!CAUTION]
> 네 개의  *올바른*  이름 서버 외에 기존 이름 서버가 있는 경우에  *만*  다음 단계를 따릅니다(즉, 이름이 *ns1.bdm.microsoftonline.com*, *ns2.bdm.microsoftonline.com*, **ns3.bdm.microsoftonline.com** 또는 **ns4.bdm.microsoftonline.com** 이  **아닌**  현재 모든 이름 서버  **만**  삭제). 
  
1. 이름 서버 상자에 다른 이름 서버 나열 되어 있으면 하나씩 선택 하 고 키보드에서 **delete** 키를 눌러 **삭제 합니다.** 
    
    ![Namecheap-BP-Redelegate-1-4](../media/3270603a-c4f4-40b7-acad-733d56e2f53c.png)
  
2. 이름 서버 **추가** 를 두 번 선택 하 여 두 개의 새 행을 추가 합니다. 
    
    ![Namecheap-BP-Redelegate-1-3-1](../media/e8816bf5-bb59-49d5-bfca-43e502242dc3.png)
  
3. 이름 서버 **상자에서** 다음 표의 값을 입력 하거나 복사 하 여 붙여넣습니다.
 
    
|||
|:-----|:-----|
|**이름 서버 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**이름 서버 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**이름 서버 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**이름 서버 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
   ![Namecheap-BP-Redelegate-1-3-2](../media/21d681b7-4f96-4e96-ac27-9534c388537c.png)
  
4. **저장** (확인 표시) 컨트롤을 선택 합니다. 
    
    ![Namecheap-BP-Redelegate-1-5](../media/07aaf1e5-c24f-4c51-bfe0-f99868b3bf35.png)
  
> [!NOTE]
> 이름 서버 레코드 업데이트가 인터넷의 DNS 시스템 전체에 업데이트되기까지 몇 시간이 걸릴 수 있습니다. 그 후에는 Office 365 전자 메일 및 기타 서비스가 모두 사용자의 도메인을 사용하도록 설정됩니다.