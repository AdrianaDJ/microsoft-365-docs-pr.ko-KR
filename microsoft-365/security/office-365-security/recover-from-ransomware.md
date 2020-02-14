---
title: 랜 섬 웨어 공격에서 복구
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Office 365 관리자는 랜 섬 웨어 공격 으로부터 복구 하는 방법에 대해 알아볼 수 있습니다.
ms.openlocfilehash: 04cfd2f2417b0c2e084a88f9ee156521339b18c4
ms.sourcegitcommit: e47694dedf7e213167d3d979a44c07c668bba543
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2020
ms.locfileid: "41932377"
---
# <a name="recover-from-a-ransomware-attack-in-office-365"></a><span data-ttu-id="2fc13-103">Office 365에서 랜 섬 웨어 공격 으로부터 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-103">Recover from a ransomware attack in Office 365</span></span>

<span data-ttu-id="2fc13-104">Office 365 조 직을 보호 하기 위해 모든 예방책을 사용 하는 경우에도 여전히 [랜 섬 웨어](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) 공격을 막을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-104">Even if you take every precaution to protect your Office 365 organization, you can still fall victim to a [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) attack.</span></span> <span data-ttu-id="2fc13-105">랜 섬 웨어는 대규모 기업 이며, 공격은 정교 하 게 확인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-105">Ransomware is big business, and the attacks are verify sophisticated.</span></span>

<span data-ttu-id="2fc13-106">이 항목의 단계에서는 랜 섬 웨어로 암호화 된 데이터를 복구할 수 있는 최상의 기회를 제공 하며, Office 365 조직에서 감염의 확산을 중지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-106">The steps in this topic will give you the best chance to recover data that was encrypted by the ransomware, and will help stop the spread of the infection in your Office 365 organization.</span></span> <span data-ttu-id="2fc13-107">시작하기 전에 다음 항목을 고려하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-107">Before you get started, consider the following items:</span></span>

- <span data-ttu-id="2fc13-108">Ransom의 비용을 지불 하면 파일에 대 한 액세스 권한이 반환 된다는 보장이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-108">There's no guarantee that paying the ransom will return access to your files.</span></span> <span data-ttu-id="2fc13-109">실제로 ransom를 지불할 경우 더 많은 랜 섬 웨어를 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-109">In fact, paying the ransom can make you a target for more ransomware.</span></span> <span data-ttu-id="2fc13-110">이미 지불 되었지만 공격자의 확인을 사용 하지 않고 파일을 성공적으로 복구할 수 있는 경우에는 뱅크를 호출 하 여 트랜잭션을 차단할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-110">If you've already paid, but you were able to successfully recover your files without having to use the attacker's resolution, you should call your bank to see if they can block the transaction.</span></span> <span data-ttu-id="2fc13-111">또한이 항목의 뒷부분에 설명 된 대로, 섬 웨어 공격을 법 집행, 사기 보고 웹 사이트 및 Microsoft에 보고 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-111">We also recommend that you report the ransomware attack to law enforcement, scam reporting websites and Microsoft as described later in this topic.</span></span>

- <span data-ttu-id="2fc13-112">공격에 빠르게 응답 하 고 그 결과를 처리 하는 것이 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-112">It's very important that you respond quickly to the attack and its consequences.</span></span> <span data-ttu-id="2fc13-113">기다리는 시간이 길수록 영향을 받는 데이터를 복구할 수 있다는 것을 덜 가능성이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-113">The longer you wait, the less likely it is that you can recover the affected data.</span></span>

## <a name="step-1-verify-your-backups"></a><span data-ttu-id="2fc13-114">1 단계: 백업 확인</span><span class="sxs-lookup"><span data-stu-id="2fc13-114">Step 1: Verify your backups</span></span>

<span data-ttu-id="2fc13-115">오프 라인 백업이 있는 경우 환경에서 맬웨어 (랜 섬 웨어 페이로드)를 제거한 **후** 에 암호화 된 데이터를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-115">If you have offline backups, you can probably restore the encrypted data **after** you've removed the ransomware payload (malware) from your environment.</span></span>

<span data-ttu-id="2fc13-116">백업이 없거나 해당 백업이 랜 섬 웨어의 영향을 받는 경우에는이 단계를 건너뛰어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-116">If you don't have backups, or if your backups were also affected by the ransomware, you can skip this step.</span></span>

## <a name="step-2-disable-activesync-and-onedrive-sync"></a><span data-ttu-id="2fc13-117">2 단계: ActiveSync 및 OneDrive 동기화를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="2fc13-117">Step 2: Disable ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="2fc13-118">여기서 중요 한 점은 랜 섬 웨어에의 한 데이터 암호화 확산을 중지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-118">The key point here is to stop the spread of data encryption by the ransomware.</span></span>

<span data-ttu-id="2fc13-119">전자 메일이 대상이 되는 것으로 의심 되는 경우 사서함에 대 한 사용자 액세스를 일시적으로 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-119">If you suspect that email is a target, you should temporarily disable user access to mailboxes.</span></span> <span data-ttu-id="2fc13-120">Exchange ActiveSync는 모바일 장치에서 장치와 Exchange Online 사서함 간에 데이터를 동기화 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-120">Exchange ActiveSync is used by mobile devices to synchronize data between the device and the Exchange Online mailbox.</span></span>

<span data-ttu-id="2fc13-121">사서함에 대해 ActiveSync를 사용 하지 않도록 설정 하려면 [Office 365에서 사용자에 대해 Exchange ActiveSync를 사용 하지 않도록 설정 하는 방법을](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-121">To disable ActiveSync for a mailbox, see [How to disable Exchange ActiveSync for users in Office 365](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365).</span></span>

<span data-ttu-id="2fc13-122">사서함에 대 한 다른 유형의 액세스를 사용 하지 않도록 설정 하려면 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-122">To disable other types of access to a mailbox, see:</span></span>

- <span data-ttu-id="2fc13-123">[사서함에 대해 MAPI를 사용 하거나 사용 하지 않도록](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi)설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-123">[Enable or disable MAPI for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span></span>

- [<span data-ttu-id="2fc13-124">사용자에 대해 POP3 또는 IMAP4 액세스를 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="2fc13-124">Enable or Disable POP3 or IMAP4 access for a user</span></span>](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)

<span data-ttu-id="2fc13-125">OneDrive 동기화를 일시 중지 하면 잠재적으로 감염 된 장치에 의해 클라우드 데이터가 업데이트 되는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-125">Pausing OneDrive sync will help protect your cloud data from being updated by potentially infected devices.</span></span> <span data-ttu-id="2fc13-126">자세한 내용은 [OneDrive에서 동기화 일시 중지 및 다시 시작 하는 방법을](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-126">For more information, see [How to Pause and Resume sync in OneDrive](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span></span>

## <a name="step-3-remove-the-malware-from-the-affected-devices"></a><span data-ttu-id="2fc13-127">3 단계: 영향을 받는 장치에서 맬웨어 제거</span><span class="sxs-lookup"><span data-stu-id="2fc13-127">Step 3: Remove the malware from the affected devices</span></span>

<span data-ttu-id="2fc13-128">의심 되는 모든 컴퓨터 및 장치에 대 한 최신 업데이트를 사용 하 여 전체 바이러스 검사를 실행 하 여 랜 섬 웨어에 연결 된 페이로드를 검색 하 고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-128">Run a full antivirus scan with the latest updates on all suspected computers and devices to detect and remove the payload that's associated with the ransomware.</span></span> <span data-ttu-id="2fc13-129">데이터를 동기화 하는 장치 또는 매핑된 네트워크 드라이브의 대상 (즉, 검색 해야 하는 컴퓨터와 장치)을 잊지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="2fc13-129">Don't forget devices that are synchronizing data, or the target of mapped network drives (those computers and devices need to be scanned, too).</span></span>

<span data-ttu-id="2fc13-130">[Windows Defender](https://www.microsoft.com/windows/comprehensive-security) 또는 (이전 클라이언트용) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-130">You can use [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) or (for older clients) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span></span>

<span data-ttu-id="2fc13-131">랜 섬 웨어 또는 맬웨어를 제거 하는 데 도움이 되는 또 다른 방법은 [악성 소프트웨어 제거 도구 (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905)입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-131">An alternative that will also help you remove ransomware or malware is the [Malicious Software Removal Tool (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905).</span></span>

<span data-ttu-id="2fc13-132">이러한 옵션이 작동 하지 않으면 [Windows Defender offline](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc) 을 시도 하거나 [맬웨어 검색 및 제거 문제를 해결할](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-132">If these options don't work, you can try [Windows Defender Offline](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc) or [Troubleshoot problems with detecting and removing malware](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware).</span></span>

## <a name="step-4-recover-files-on-a-cleaned-computer-or-device"></a><span data-ttu-id="2fc13-133">4 단계: 치료 된 컴퓨터 또는 장치에서 파일 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-133">Step 4: Recover files on a cleaned computer or device</span></span>

<span data-ttu-id="2fc13-134">이전 단계를 완료 하 여 환경에서 랜 섬 웨어 페이로드를 제거한 후 (섬 웨어 파일을 암호화 하거나 제거 하지 못하게 함) windows 10 및 Windows 8.1의 [파일 기록을](https://support.microsoft.com/help/17128/windows-8-file-history) 사용 하 여 로컬 파일 및 폴더 복구를 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-134">After you've completed the previous step to remove the ransomware payload from your environment (which will prevent the ransomware from encrypting or removing your files), you can use [File History](https://support.microsoft.com/help/17128/windows-8-file-history) in Windows 10 and Windows 8.1 or System Protection in Windows 7 to attempt to recover your local files and folders.</span></span>

<span data-ttu-id="2fc13-135">**참고**:</span><span class="sxs-lookup"><span data-stu-id="2fc13-135">**Notes**:</span></span>

- <span data-ttu-id="2fc13-136">일부 랜 섬 웨어도 백업 버전을 암호화 하거나 삭제 하므로 파일 기록 또는 시스템 보호를 사용 하 여 파일을 복원할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-136">Some ransomware will also encrypt or delete the backup versions, so you can't use File History or System Protection to restore files.</span></span> <span data-ttu-id="2fc13-137">이 경우 다음 섹션에 설명 된 대로 랜 섬 웨어 또는 OneDrive의 영향을 받지 않았던 외부 드라이브 또는 장치에서 백업을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-137">If that happens, you need use backups on external drives or devices that were not affected by the ransomware or OneDrive as described in the next section.</span></span>

- <span data-ttu-id="2fc13-138">폴더가 OneDrive에 동기화 되 고 최신 버전의 Windows를 사용 하지 않는 경우 파일 히스토리를 사용 하 여 몇 가지 제한이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-138">If a folder is synchronized to OneDrive and you aren't using the latest version of Windows, there might be some limitations using File History.</span></span>

## <a name="step-5-recover-your-files-in-your-onedrive-for-business"></a><span data-ttu-id="2fc13-139">5 단계: 비즈니스용 OneDrive에서 파일 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-139">Step 5: Recover your files in your OneDrive for Business</span></span>

<span data-ttu-id="2fc13-140">비즈니스용 OneDrive를 사용 하면 저장 한 파일을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-140">OneDrive for Business will allow you to recover any files you have stored in it.</span></span> <span data-ttu-id="2fc13-141">두 가지 옵션 가운데 선택하십시오.</span><span class="sxs-lookup"><span data-stu-id="2fc13-141">You have two options:</span></span>

- <span data-ttu-id="2fc13-142">[OneDrive 웹 사이트](https://support.office.com/article/159cad6d-d76e-4981-88ef-de6e96c93893)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-142">Use the [OneDrive website](https://support.office.com/article/159cad6d-d76e-4981-88ef-de6e96c93893).</span></span>

- <span data-ttu-id="2fc13-143">많은 수의 파일이 영향을 받는 경우 "사이트 모음 복원"에 대 한 지원 요청을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-143">If a large number of files were affected, you can create a support request for a "Site Collection Restore".</span></span> <span data-ttu-id="2fc13-144">이 요청은 이전에 최대 14 일 동안 파일을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-144">This request can restore files from up to 14 days in the past.</span></span>

## <a name="step-6-recover-deleted-email"></a><span data-ttu-id="2fc13-145">6 단계: 삭제 된 전자 메일 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-145">Step 6: Recover deleted email</span></span>

<span data-ttu-id="2fc13-146">드물지만 랜 섬 웨어가 모든 전자 메일을 삭제 한 경우에는 삭제 된 항목을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-146">In the rare case that the ransomware deleted all your email, you can probably recover the deleted items.</span></span> <span data-ttu-id="2fc13-147">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-147">For more information, see:</span></span>

- [<span data-ttu-id="2fc13-148">사용자의 사서함에서 삭제된 메시지 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-148">Recover deleted messages in a user's mailbox</span></span>](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- [<span data-ttu-id="2fc13-149">Windows용 Outlook에서 삭제된 항목 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-149">Recover deleted items in Outlook for Windows</span></span>](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce)

## <a name="step-7-re-enable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="2fc13-150">7 단계: Exchange ActiveSync 및 OneDrive 동기화 다시 사용</span><span class="sxs-lookup"><span data-stu-id="2fc13-150">Step 7: Re-enable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="2fc13-151">컴퓨터 및 장치를 청소 하 고 데이터를 복구한 후에는 [2 단계](#step-2-disable-activesync-and-onedrive-sync)에서 이전에 사용 하지 않도록 설정한 ActiveSync 및 OneDrive 동기화를 다시 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-151">After you've cleaned your computers and devices and recovered your data, you can re-enable ActiveSync and OneDrive sync that you previously disabled in [Step 2](#step-2-disable-activesync-and-onedrive-sync).</span></span>

## <a name="step-8-optional-block-onedrive-sync-for-specific-file-extensions"></a><span data-ttu-id="2fc13-152">8 단계 (선택 사항): 특정 파일 확장명에 대 한 OneDrive 동기화 차단</span><span class="sxs-lookup"><span data-stu-id="2fc13-152">Step 8 (Optional): Block OneDrive sync for specific file extensions</span></span>

<span data-ttu-id="2fc13-153">복구한 후에는 비즈니스용 OneDrive 클라이언트에서이 랜 섬에 영향을 받은 파일 형식을 동기화 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-153">After you've recovered, you can prevent OneDrive for Business clients from synchronizing the file types that were affected by this ransomware.</span></span> <span data-ttu-id="2fc13-154">자세한 내용은 [get-spotenantsyncclientrestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-154">For more information, see [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span></span>

## <a name="report-the-attack"></a><span data-ttu-id="2fc13-155">공격 보고</span><span class="sxs-lookup"><span data-stu-id="2fc13-155">Report the attack</span></span>

### <a name="contact-law-enforcement"></a><span data-ttu-id="2fc13-156">담당자 법률 집행</span><span class="sxs-lookup"><span data-stu-id="2fc13-156">Contact law enforcement</span></span>

<span data-ttu-id="2fc13-157">지역 또는 연방 법 집행 기관에 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-157">You should contact your local or federal law enforcement agencies.</span></span> <span data-ttu-id="2fc13-158">예를 들어 미국에 있는 경우 [FBI 로컬 필드인 office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) 또는 [Secret Service](http://www.secretservice.gov/)에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-158">For example, if you are in the United States you can contact the [FBI local field office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) or [Secret Service](http://www.secretservice.gov/).</span></span>

### <a name="submit-a-report-to-your-countrys-scam-reporting-website"></a><span data-ttu-id="2fc13-159">해당 국가의 사기 보고 웹 사이트로 보고서 제출</span><span class="sxs-lookup"><span data-stu-id="2fc13-159">Submit a report to your country's scam reporting website</span></span>

<span data-ttu-id="2fc13-160">사기 보고 웹 사이트는 사기를 방지 하 고 방지 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-160">Scam reporting websites provide information about how to prevent and avoid scams.</span></span> <span data-ttu-id="2fc13-161">또한 사기가 피해자 인지 여부를 보고 하는 메커니즘도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-161">They also provide mechanisms to report if you were victim of scam.</span></span>

- <span data-ttu-id="2fc13-162">오스트레일리아: [Scamwatch](http://www.scamwatch.gov.au/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-162">Australia: [SCAMwatch](http://www.scamwatch.gov.au/)</span></span>

- <span data-ttu-id="2fc13-163">캐나다: [캐나다 사기 방지 센터](http://www.antifraudcentre-centreantifraude.ca/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-163">Canada: [Canadian Anti-Fraud Centre](http://www.antifraudcentre-centreantifraude.ca/)</span></span>

- <span data-ttu-id="2fc13-164">프랑스: [agence de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-164">France: [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span></span>

- <span data-ttu-id="2fc13-165">독일: [Bundesamt Für Sicherheit in Der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span><span class="sxs-lookup"><span data-stu-id="2fc13-165">Germany: [Bundesamt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span></span>

- <span data-ttu-id="2fc13-166">아일랜드: [Garda Síochána](http://www.garda.ie/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-166">Ireland: [An Garda Síochána](http://www.garda.ie/)</span></span>

- <span data-ttu-id="2fc13-167">뉴질랜드: 소비자에 게 [사기](http://www.consumeraffairs.govt.nz/scams)</span><span class="sxs-lookup"><span data-stu-id="2fc13-167">New Zealand: [Consumer Affairs Scams](http://www.consumeraffairs.govt.nz/scams)</span></span>

- <span data-ttu-id="2fc13-168">영국: [작업 사기](http://www.actionfraud.police.uk/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-168">United Kingdom: [Action Fraud](http://www.actionfraud.police.uk/)</span></span>

- <span data-ttu-id="2fc13-169">미국: [온라인 보호 설정](http://www.onguardonline.gov/)</span><span class="sxs-lookup"><span data-stu-id="2fc13-169">United States: [On Guard Online](http://www.onguardonline.gov/)</span></span>

<span data-ttu-id="2fc13-170">해당 국가가 나열 되지 않으면 지역 또는 연방 법 집행 기관에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc13-170">If your country isn't listed, ask your local or federal law enforcement agencies.</span></span>

### <a name="submit-email-messages-to-microsoft"></a><span data-ttu-id="2fc13-171">Microsoft로 전자 메일 메시지 제출</span><span class="sxs-lookup"><span data-stu-id="2fc13-171">Submit email messages to Microsoft</span></span>

<span data-ttu-id="2fc13-172">[분석을 위해 Microsoft에 스팸, 스팸이 아닌 피싱 사기 메시지를 제출](https://docs.microsoft.com/microsoft-365/security/office-365-security/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis)하는 지침에 따라 랜 섬 웨어가 포함 된 피싱 메시지를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-172">You can report phishing message that contain ransomware by following the instructions in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](https://docs.microsoft.com/microsoft-365/security/office-365-security/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis).</span></span>

## <a name="see-also"></a><span data-ttu-id="2fc13-173">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2fc13-173">See also</span></span>

- [<span data-ttu-id="2fc13-174">랜</span><span class="sxs-lookup"><span data-stu-id="2fc13-174">Ransomware</span></span>](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)

- [<span data-ttu-id="2fc13-175">랜 섬 웨어 응답-비용 청구 또는 결제 안 하나요?</span><span class="sxs-lookup"><span data-stu-id="2fc13-175">Ransomware response—to pay or not to pay?</span></span>](https://www.microsoft.com/security/blog/2019/12/16/ransomware-response-to-pay-or-not-to-pay/)

- [<span data-ttu-id="2fc13-176">Norsk Hydro 투명도를 사용한 랜 섬 웨어 공격에 응답</span><span class="sxs-lookup"><span data-stu-id="2fc13-176">Norsk Hydro responds to ransomware attack with transparency</span></span>](https://www.microsoft.com/security/blog/2019/12/17/norsk-hydro-ransomware-attack-transparency/)

- [<span data-ttu-id="2fc13-177">랜 섬 웨어 검색 및 OneDrive에서 파일 복구</span><span class="sxs-lookup"><span data-stu-id="2fc13-177">Ransomware detection and recovering your files in OneDrive</span></span>](https://support.office.com/article/0d90ec50-6bfd-40f4-acc7-b8c12c73637f)

- [<span data-ttu-id="2fc13-178">Microsoft 보안 인텔리전스 보고서</span><span class="sxs-lookup"><span data-stu-id="2fc13-178">Microsoft Security Intelligence Report</span></span>](https://www.microsoft.com/securityinsights/)

- [<span data-ttu-id="2fc13-179">Office 파일에서 매크로를 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="2fc13-179">Enable or disable macros in Office files</span></span>](https://support.office.com/article/12b036fd-d140-4e74-b45e-16fed1a7e5c6)

- [<span data-ttu-id="2fc13-180">EOP 및 Office 365 ATP 보안에 대 한 권장 설정</span><span class="sxs-lookup"><span data-stu-id="2fc13-180">Recommended settings for EOP and Office 365 ATP security</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp)

- [<span data-ttu-id="2fc13-181">훌륭한 업그레이드: Windows 10의 차세대 보안은 2017에서 랜 섬 웨어에 대 한 복원성을 입증 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-181">A worthy upgrade: Next-gen security on Windows 10 proves resilient against ransomware outbreaks in 2017</span></span>](https://www.microsoft.com/security/blog/2018/01/10/a-worthy-upgrade-next-gen-security-on-windows-10-proves-resilient-against-ransomware-outbreaks-in-2017/)

- [<span data-ttu-id="2fc13-182">Ma 없음, Samas:이 랜 섬 웨어의 modus 기능 andi</span><span class="sxs-lookup"><span data-stu-id="2fc13-182">No mas, Samas: What's in this ransomware's modus operandi?</span></span>](https://www.microsoft.com/security/blog/2016/03/17/no-mas-samas-whats-in-this-ransomwares-modus-operandi/)

- [<span data-ttu-id="2fc13-183">Locky 맬웨어, 피하는 운이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc13-183">Locky malware, lucky to avoid it</span></span>](https://www.microsoft.com/security/blog/2016/02/24/locky-malware-lucky-to-avoid-it/)

- [<span data-ttu-id="2fc13-184">MSRT 7 월 2016 일: (으)</span><span class="sxs-lookup"><span data-stu-id="2fc13-184">MSRT July 2016: Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/07/12/msrt-july-2016-cerber-ransomware/)

- [<span data-ttu-id="2fc13-185">Cerberus의 세 가지 헤드</span><span class="sxs-lookup"><span data-stu-id="2fc13-185">The three heads of the Cerberus-like Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/03/09/the-three-heads-of-the-cerberus-like-cerber-ransomware/)

- [<span data-ttu-id="2fc13-186">Da 다빈치 코드의 영향을 받은 Troldesh 랜 섬 웨어</span><span class="sxs-lookup"><span data-stu-id="2fc13-186">Troldesh ransomware influenced by (the) Da Vinci code</span></span>](https://www.microsoft.com/security/blog/2016/07/13/troldesh-ransomware-influenced-by-the-da-vinci-code/)