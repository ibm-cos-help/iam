---

copyright:

  years: 2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 多因子鑑別的類型
{: #types}

多因子鑑別 (MFA) 會要求所有使用者使用 ID 及密碼以外的其他鑑別方法來進行鑑別，為您的帳戶新增額外的安全層。這通常也稱為雙因子鑑別 (2FA)。
{:shortdesc}

您的帳戶可能會啟用下列兩種類型的 MFA 選項：

<dl>
<dt>ID 型 MFA</dt>
<dd>在您所屬的其中一個帳戶中，由帳戶擁有者啟用的選項。這類型的 MFA 與您的 IBM ID 相關聯，並跨您所屬的所有帳戶來鑑別您，因此您只需要鑑別一次。</dd>
<dt>帳戶型選項</dt>
<dd>使用時間型一次性密碼這類安全問題的選項，以及 Symantec 及電話型鑑別這類外部鑑別選項。這些類型的 MFA 是每個帳戶特有的，這表示如果您針對所屬的每個帳戶設定不同的類型，則每次切換帳戶時都必須以不同的方式進行鑑別。這些舊式 MFA 選項只能與之前的標準基礎架構帳戶搭配使用。</dd>
</dl>

IBM ID MFA 可滿足鑑別需求，因此系統不會提示您輸入任何其他類型的 MFA，即使已啟用它們。因此，如果您所屬帳戶的任何擁有者開啟此選項，則這是登入時提示您輸入的唯一 MFA 類型。如果您是新使用者，請使用 ID 型 IBM ID MFA 選項，確保您的登入簡單且安全。
{: tip}

## ID 型 MFA 選項
{: #id-based}

在登入期間，除了標準 IBM ID 及密碼之外，帳戶的 IBM ID MFA 還需要時間型一次性密碼。這類型的 MFA 是由帳戶擁有者在帳戶層次上啟用。啟用此特性時，您需要在登入時使用額外安全標準，也需要新增至您帳戶的所有使用者。這類型的 MFA 適用於所有帳戶資源。只有在您是帳戶擁有者時，才能在 {{site.data.keyword.Bluemix}} 主控台中，從**管理** > **存取 (IAM)** > **設定**頁面，將它開啟或關閉。

IBM ID MFA 的其中一個好處是它是免費的，而且關聯至您的 ID，而不只是您所在的特定帳戶。如果您屬於多個帳戶，則在登入主控台時，您只需要鑑別一次。如需 IBM ID MFA、需要您帳戶之 IBM ID MFA 前必須檢閱的考量，以及如何設定您自己之 IBM ID MFA 的相關資訊，請參閱[針對帳戶中的使用者要求 MFA](/docs/iam/mfa.html#setting-up-ibmid-mfa)。

## 帳戶型 MFA 選項
{: #id-based}

帳戶管理者必須啟用下列任何 MFA 選項，才能供帳戶中的使用者配置及使用。這類型的 MFA 關聯至使用者的現行帳戶。如果管理者對使用者所屬的每一個帳戶啟用其中一個不同的 MFA 選項，則每次使用者切換帳戶時，都會提示使用不同的方式鑑別。

如果帳戶擁有者需要帳戶中所有使用者的 IBM ID MFA，則該 IBM ID MFA 方法會置換使用者帳戶中所啟用及設定的任何其他 MFA 選項。因此，即使使用者具有其他 MFA 選項（例如已設定下列項目），在登入時還是不會提示使用者輸入它們。

下列舊式 MFA 選項只能與之前的標準基礎架構帳戶搭配使用。

<dl>
<dt>時間型一次性密碼鑑別 (TOTP)</dt>
<dd>使用鑑別應用程式，即可設定 TOTP。只有在使用者於設定檔「登入設定」頁面上設定鑑別時，帳戶擁有者或管理者才能在「使用者詳細資料」頁面上啟用使用者的這項設定。如果啟用使用者的這項設定，則在登入期間會提示他們輸入密碼。如果使用者具有從「使用者詳細資料」頁面開啟「使用者管理的登入設定」來管理其專屬登入設定的存取權，則可以將它開啟或關閉。</dd>
<dt>安全問題</dt>
<dd>使用者可以對設定檔「登入設定」頁面上提供的安全問題設定回答。使用者必須先設定安全問題和回答，帳戶擁有者或管理者才能在「使用者詳細資料」頁面上啟用此設定。如果使用者具有從「使用者詳細資料」頁面開啟「使用者管理的登入設定」來管理其專屬登入設定的存取權，則可以將它開啟或關閉。</dd>
<dt>外部鑑別</dt>
<dd>有兩個可訂購並計入每月成本的外部協力廠商鑑別選項：Symantec 及電話型鑑別。帳戶擁有者或管理者必須針對使用者訂購這些選項，並從使用者的「使用者詳細資料」頁面使用它們。對於 Symantec，管理者必須與使用者一起工作，才能取得該使用者的認證 ID 來完成訂單。而且，若要設定電話型鑑別，管理者必須訂購它，然後，使用者必須在其「使用者詳細資料」頁面上設定它，讓管理者能夠啟用它。如果使用者具有從「使用者詳細資料」頁面開啟「使用者管理的登入設定」來管理其專屬登入設定的存取權，則可以將它開啟或關閉。</dd>
</dl>

如需設定 MFA 選項的相關資訊，請參閱[設定登入安全](/docs/account/login_settings.html#login-settings)。而且，如果您是管理其他使用者登入設定的帳戶擁有者或管理者，或您可以管理自己的登入設定，請參閱[管理使用者的登入設定](/docs/iam/user_login.html#loginsettings)。
