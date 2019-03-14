---

copyright:

  years: 2019

lastupdated: "2019-02-11"

keywords: account management, access, access policy, account administrator

subcollection: iam


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 指派帳戶管理服務的存取權
{: #account-services}

身為帳戶管理服務的帳戶擁有者或管理者，您可以使用帳戶管理服務來授與使用者帳戶存取權，以邀請使用者加入帳戶、追蹤計費和用量，以及使用支援案例。具有存取權的使用者還可以管理服務 ID、存取原則、型錄項目，以及存取群組。

## 建立帳戶管理服務存取權的原則
{: #account-management-access}

若要指派對一個或所有帳戶管理服務的存取權，請完成下列步驟：

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**使用者**。
2. 從您要指派存取權的使用者列中，選取**動作** ![「動作清單」圖示](../icons/action-menu-icon.svg) 功能表，然後按一下**指派存取權**。
3. 選取以指派**帳戶管理服務**的存取權。
4. 選取**所有帳戶管理服務**，或選取特定的帳戶管理服務。
5. 選取任何角色組合，以指派想要的存取權。

若要將帳戶的完整存取權授與給另一位使用者，以管理使用者存取權及所有帳戶資源，您必須指派兩個原則。其中一個原則可讓使用者藉由選取**所有已啟用「身分及存取」的服務**並指派**管理者**角色來存取帳戶中的所有資源。此外，另一個原則可讓使用者藉由選取**所有帳戶管理服務**並指派**管理者**角色來存取帳戶中的所有帳戶管理服務。
{: tip}

## 帳戶管理服務的動作與角色對映
{: #account-management-actions-roles}

下表概述使用者獲指派每個帳戶管理服務的特定角色時可採取的動作。請檢閱此資訊以確保您為使用者指派了正確的存取權層次。

|角色|動作|
|:-------|----------|
|檢視者|檢視存取群組及成員|
|操作員|不適用|
|編輯者|檢視、建立、編輯及刪除群組<br><br> 從群組新增或移除使用者|
|管理者|檢視、建立、編輯及刪除群組<br><br> 新增或移除使用者<br><br> 指派群組的存取權<br><br> 管理使用存取群組的存取權|
{: caption="表 1. 「存取群組」服務的角色與範例動作" caption-side="top"}

|角色|動作|
|:-------|----------|
|檢視者|檢視帳戶中的使用者<br><br> 檢視使用者設定檔設定|
|操作員|檢視帳戶中的使用者<br><br> 檢視使用者設定檔設定|
|編輯者|檢視、邀請、移除及更新帳戶中的使用者<br><br> 檢視及更新使用者設定檔設定|
|管理者|檢視、邀請、移除及更新帳戶中的使用者<br><br> 檢視及更新使用者設定檔設定|
{: caption="表 2. 「使用者管理」服務的角色與範例動作" caption-side="top"}

|角色|動作|
|:-------|----------|
|檢視者| 檢視案例 <br><br>  搜尋案例 |
|操作員|不適用|
|編輯者| 檢視案例 <br><br>  搜尋案例 <br><br> 更新案例<br><br> 建立案例|
|管理者| 檢視案例 <br><br>  搜尋案例 <br><br> 更新案例<br><br> 建立案例|
{: caption="表 3. 「支援中心」服務的角色與範例動作" caption-side="top"}

|角色|動作|
|:-------|----------|
|檢視者|檢視帳戶特性設定<br><br> 檢視帳戶中的訂閱<br><br> 檢視帳戶名稱<br><br> 檢視資源群組|
|操作員|檢視帳戶特性設定<br><br> 檢視帳戶中的訂閱<br><br> 檢視及變更帳戶名稱<br><br> 檢視及更新資源群組|
|編輯者|檢視及更新帳戶特性設定<br><br> 檢視帳戶中的訂閱<br><br> 檢視帳戶中的供應項目<br><br> 檢視及套用特性碼<br><br> 檢視及變更帳戶名稱<br><br> 檢視及更新消費限制<br><br> 檢視、建立及更新資源群組|
|管理者|檢視及更新帳戶特性設定<br><br> 檢視帳戶中的訂閱<br><br> 檢視帳戶中的供應項目<br><br> 檢視及套用特性碼<br><br> 檢視及變更帳戶名稱<br><br> 檢視及更新消費限制<br><br> 檢視訂閱餘額及追蹤用量<br><br> 檢視、建立、更新及指派管理資源群組的存取權|
{: caption="表 4. 「計費」服務的角色與範例動作" caption-side="top"}

|角色|動作|
|:-------|----------|
|檢視者|檢視 ID|
|操作員|建立及刪除 ID 和 API 金鑰|
|編輯者|建立、更新及刪除 ID 和 API 金鑰|
|管理者|建立、更新及刪除 ID 和 API 金鑰<br><br> 將存取原則指派給 ID|
{: caption="表 5. 「IAM 身分」服務的角色與範例動作" caption-side="top"}

對於「IAM 身分服務」，這些動作會套用至帳戶中使用者未建立的服務 ID。所有使用者都可以建立服務 ID。他們是那些 ID 的管理者，而且可以建立相關聯的 API 金鑰及存取原則。不過，此帳戶管理服務會套用至對其他使用者所建立帳戶中的服務 ID 進行檢視、刪除及指派存取權的能力。
{: note}

|角色|動作|
|:-------|----------|
|檢視者|檢視專屬服務|
|操作員|不適用|
|編輯者|變更物件 meta 資料，但無法變更專用服務的可見性|
|管理者|變更專用服務的物件 meta 資料或可見性，以及限制公用服務的可見性|
{: caption="表 6. 「全球型錄」服務的角色與範例動作" caption-side="top"}

|角色|動作|
|:-------|----------|
|檢視者|帳戶管理服務的所有檢視者角色動作：|
|操作員|帳戶管理服務的所有操作員角色動作：|
|編輯者|帳戶管理服務的所有編輯者角色動作：|
|管理者|帳戶管理服務的所有管理者角色動作：|
{: caption="表 7. 所有身分及存取服務上原則的角色與範例動作" caption-side="top"}