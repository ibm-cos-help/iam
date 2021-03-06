---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-26"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# API キーの処理
{: #manapikey}

アプリケーション・プログラミング・インターフェース・キー (API キー) は、呼び出し側のアプリケーションまたはユーザーを識別するためにアプリケーション・プログラミング・インターフェース (API) に渡される固有コードです。  API キーは、API の使用方法を追跡および制御する (例えば、API の悪用または不正利用を防止する) ために使用されます。 API キーは、多くの場合、認証のための固有 ID と秘密トークンの両方として機能し、通常はそのキーに関連付けられた ID に特定の一連のアクセス権限を持ちます。

## プラットフォーム API キー

プラットフォーム API キーは、「ID およびアクセス管理」UI で作成され、以下に関連付けることができます。

* アカウントのユーザー
* アカウントに作成されたサービス ID

アカウントにリンクされている API キーを作成および使用することができます。 フェデレーテッド・ユーザーまたは非フェデレーテッド・ユーザーは、API キーを作成し、CLI で使用したり、ID としてログインするための自動化の一部として使用したりすることができます。 ユーザー ID に関連付けられた API キーの使用について詳しくは、[ユーザー API キーの管理](userid_keys.html)を参照してください。

また、作成するサービス ID に関連付けられた API キーを使用することもできます。 サービス ID は、{{site.data.keyword.Bluemix_notm}} の内部または外部のアプリケーションを {{site.data.keyword.Bluemix_notm}} サービスに接続するために使用されます。 サービス ID に関連付けられた API キーの作成について詳しくは、[サービス ID の API キーの管理](serviceid_keys.html)を参照してください。

## その他の {{site.data.keyword.Bluemix_notm}} API キー

プラットフォーム API キーに加えて、{{site.data.keyword.Bluemix_notm}} で使用する可能性があるその他のタイプの API がいくつかあります。

* インフラストラクチャー API キー
* サービス固有の API キー

インフラストラクチャー API キーは、カスタマー・ポータルで作成され、SoftLayer アカウントのユーザー ID に関連付けられ、インフラストラクチャー・サービス用の API にアクセスするときに使用されます。

{{site.data.keyword.Bluemix_notm}} 内のいくつかのサービスも、それらのサービスを操作するときに使用する API キーを提供する場合があります。 例えば、ダッシュボードから Watson サービスのサービス詳細を表示している場合、「サービス資格情報」タブでそのサービスのみに固有の資格情報 (API キーと秘密を含む) を作成することができます。

