---
title: 이전 버전의 메시지 암호화에 대 한 Azure 권한 관리 설정
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: 이전 버전의 Office 365 메시지 암호화는 Microsoft Azure 권한 관리 (이전에는 Windows Azure Active Directory Rights Management)에 따라 달라 집니다.
ms.openlocfilehash: 879f4ec1db8a8cfe1fe3c8d3b1dd9e1fc68dd687
ms.sourcegitcommit: 46644f9778bc70ab6d62783e0a1e60ba2eccc27f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/08/2020
ms.locfileid: "44165919"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-message-encryption"></a>이전 버전의 메시지 암호화에 대 한 Azure 권한 관리 설정

이 항목에서는 이전 버전의 Office 365 메시지 암호화 (OME)에 사용 하기 위해 RMS (Azure 권한 관리), Azure Information Protection의 일부를 설정 하기 위해 수행 해야 하는 단계에 대해 설명 합니다.

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a>이 문서는 이전 버전의 OME에만 적용 됩니다.

아직 조직을 새 OME 기능으로 이동 하지 않았지만 이미 OME을 배포한 경우이 문서의 정보가 조직에 적용 됩니다. 조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 [Office 365 메시지 암호화 기능 새로 만들기](set-up-new-message-encryption-capabilities.md)를 참조 하세요. 새 기능이 먼저 작동 하는 방식에 대해 자세히 알아보려면 [Office 365 메시지 암호화](ome.md)를 참조 하세요. 이 문서의 나머지 부분에서는 새 OME 기능이 출시 되기 전에 발생 하는 OME 동작을 나타냅니다.

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a>이전 버전의 Office 365 메시지 암호화를 사용 하기 위한 필수 구성 요소
<a name="warmprereqs"> </a>

IRM을 포함 하는 Office 365 메시지 암호화 (OME)는 azure RMS (보안 권한 관리)에 따라 달라 집니다. Azure RMS는 Azure Information Protection에서 사용 되는 보호 기술입니다. OME를 사용 하려면 조직에서 Azure 권한 관리 구독을 포함 하는 Exchange Online 또는 Exchange Online Protection 구독을 포함 해야 합니다.
  
- 구독에 포함 된 내용을 모르는 경우 Exchange Online 서비스 설명에서 [메시지 정책, 복구 및 규정 준수](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx)를 참조 하세요.

- Azure 권한 관리가 있지만 Exchange Online 또는 Exchange Online Protection에 대해 설정 되어 있지 않은 경우이 문서에서는 azure 권한 관리를 활성화 하는 방법에 대해 설명 하 고 Azure 권한 관리와 함께 작동 하도록 OME을 설정 하는 가장 효율적인 방법을 알아봅니다.

- Exchange Online 또는 Exchange Online Protection에 대해 Azure Rights Management를 사용 하도록 OME을 이미 설정한 경우이를 설정 하는 방법에 따라 OME 및 새 기능 바로 사용을 시작할 수 있습니다. 이 문서에서는 OME을 올바르게 설정 했는지 여부를 확인 하는 방법, 설치를 변경 해야 하는 경우 수행할 작업 및 설정을 변경 하지 않도록 선택한 경우 수행 되는 작업에 대해 설명 합니다. 예를 들어 새 기능을 사용 하려면 OME에서 Azure RMS를 사용 해야 합니다. 온-프레미스 Active Directory RMS에서는 새 기능을 사용할 수 없습니다.

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a>Office 365에서 이전 버전의 OME에 대 한 Azure 권한 관리를 활성화 합니다.

조직의 사용자가 보내는 메시지에 정보 보호를 적용 하 고 Azure 권한 관리 서비스를 통해 보호 된 메시지 및 파일을 여는 경우 Azure 권한 관리를 활성화 해야 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://go.microsoft.com/fwlink/p/?LinkId=525775)를 참조 하세요. 정품 인증을 완료 한 후 여기로 돌아와서이 문서의 작업을 계속 진행 합니다.
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>TPDs (트러스트 된 게시 도메인)를 가져와서 Azure RMS를 사용 하도록 OME의 이전 버전을 설정 합니다.

TPD는 조직의 권한 관리 설정에 대 한 정보가 포함 된 XML 파일입니다. 예를 들어 TPD에는 인증서 및 라이선스 서명 및 암호화에 사용 되는 SLC (서버 사용 허가자 인증서), 라이선스 및 게시에 사용 되는 Url 등이 포함 되어 있습니다. Windows PowerShell을 사용 하 여 조직으로 TPD를 가져올 수 있습니다.
  
> [!IMPORTANT]
> 이전에는 AD RMS (Active Directory Rights Management service)에서 조직으로 TPDs를 가져오도록 선택할 수 있습니다. 그러나 이렇게 하면 새 OME 기능을 사용할 수 없으며 권장 되지 않습니다. 조직이 현재이 방식으로 구성 된 경우 온-프레미스 Active Directory RMS에서 클라우드 기반 Azure 정보 보호로 마이그레이션하는 계획을 세우는 것이 좋습니다. 자세한 내용은 [AD RMS에서 Azure Information Protection으로 마이그레이션을](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)참조 하세요. Azure Information Protection으로의 마이그레이션을 완료 해야 새 OME 기능을 사용할 수 있습니다.
  
 **Azure RMS에서 TPDs를 가져오려면**
  
1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.

2. 조직의 지리적 위치에 해당 하는 키 공유 URL을 선택 합니다.

|**위치**|**키 공유 위치 URL**|
|:-----|:-----|
|북미  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|유럽 연합  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|아시아  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|남미  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 Government(정부 커뮤니티 클라우드)  <br/> 이 RMS 키 공유 위치는 정부 Sku 용 Office 365을 구입한 고객을 위해 예약 되어 있습니다.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
  
3. 다음과 같이 [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet을 실행 하 여 키 공유 위치를 구성 합니다. 

   ```powershell
   Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
   ```
  
   예를 들어 조직이 북미에 있는 경우 키 공유 위치를 구성 하려면 다음을 수행 합니다.

   ```powershell
   Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
   ```

4. -RMSOnline 스위치를 사용 하 여 [import-rmstrustedpublishingdomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet을 실행 하 여 Azure 권한 관리에서 TPD를 가져옵니다. 

   ```powershell
   Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
   ```

   여기서 *T사용자 이름은* TPD에 사용할 이름입니다. 예를 들어 "Contoso 북미 미국식 TPD"을 사용할 때 

5. Azure 권한 관리 서비스를 사용 하도록 조직을 성공적으로 구성 했는지 확인 하려면 다음과 같이-RMSOnline 스위치를 통해 [테스트-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet을 실행 합니다.

   ```powershell
   Test-IRMConfiguration -RMSOnline
   ```

   무엇 보다도이 cmdlet은 Azure 권한 관리 서비스와의 연결을 확인 하 고, TPD를 다운로드 하 고, 유효성을 검사 합니다.

6. 다음과 같이 [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet을 실행 하 여 웹 및 Outlook에서 Outlook에서 Azure 권한 관리 템플릿을 사용할 수 없도록 설정 합니다. 

   ```powershell
   Set-IRMConfiguration -ClientAccessServerEnabled $false
   ```

7. 클라우드 기반 전자 메일 조직에 대해 Azure 권한 관리를 사용 하도록 설정 하 고 Office 365 메시지 암호화에 대해 Azure 권한 관리를 사용 하도록 configure [-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet을 실행 합니다.

   ```powershell
   Set-IRMConfiguration -InternalLicensingEnabled $true
   ```

8. TPD를 올바르게 가져왔는지 Azure 권한 관리를 사용 하도록 설정 했는지 확인 하려면 IRMConfiguration cmdlet을 사용 하 여 Azure 권한 관리 기능을 테스트 합니다. 자세한 내용은 [테스트-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx)의 "예제 1"을 참조 하십시오.

## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>이전 버전의 OME가 Azure Information Protection이 아닌 Active Directory Rights Management로 설정 되어 있습니다.
<a name="importTPDs"> </a>

Active Directory Rights Management를 사용 하 여 기존 Office 365 메시지 암호화 메일 흐름 규칙을 계속 사용할 수 있지만 새 OME 기능을 구성 하거나 사용 하는 것은 불가능 합니다. 대신 Azure Information Protection로 마이그레이션해야 합니다. 마이그레이션에 대 한 자세한 내용과 조직에서 수행 하는 작업에 대 한 자세한 내용은 [AD RMS에서 Azure Information Protection로 마이그레이션을](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms)참조 하세요.
  
## <a name="next-steps"></a>다음 단계
<a name="importTPDs"> </a>

Azure 권한 관리 설치를 완료 한 후에 새 OME 기능을 사용 하도록 설정 하려면 [Azure Information Protection에 기본적으로 제공 되는 새로운 Office 365 메시지 암호화 기능 설정을](https://docs.microsoft.com/microsoft-365/compliance/set-up-new-message-encryption-capabilities) 참조 하십시오.
  
새 OME 기능을 사용 하도록 조직을 설정한 후에는 [새 OME 기능을 사용 하 여 전자 메일 메시지를 보호 하는 메일 흐름 규칙을 정의할](define-mail-flow-rules-to-encrypt-email.md)수 있습니다.
  
## <a name="related-topics"></a>관련 항목
<a name="importTPDs"> </a>

[Office 365의 암호화](encryption.md)
  
[Office 365의 암호화에 대한 기술 관련 세부 정보](technical-reference-details-about-encryption.md)
  
[Azure 권한 관리란?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
