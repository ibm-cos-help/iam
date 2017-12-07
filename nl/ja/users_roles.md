---

copyright:

  years: 2015, 2016
lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# ユーザーの役割と許可
{: #userroles}

アカウントの**「ユーザー」**ページから、{{site.data.keyword.Bluemix_notm}} プラットフォーム・サービスとインフラストラクチャー・サービスにまたがってユーザーを管理できます。「ユーザー」ページにアクセスするには、{{site.data.keyword.Bluemix_notm}} メニューで、**「管理」** &gt; **「アカウント」** &gt; **「ユーザー」**をクリックします。アカウント所有者は、ユーザー、許可、組織、およびスペースを管理するためのすべての操作を実行できます。Cloud Foundry の組織管理者とスペース管理者も、管理する各組織および各スペースに追加されたユーザーの許可を管理するためのアクセス権限を持っています。
{:shortdesc}

別の人のアカウントに追加されたユーザーが自身に割り当てられた役割と許可を確認する場合は、**「管理」** &gt; **「セキュリティー」** &gt; **「ID およびアクセス権限 (Identity & Access)」** &gt; **「ユーザー」**に移動し、自分の名前をクリックします。

## アカウントの役割
{: #userrolesinfo}

アカウント・レベルでは、各種アカウント管理機能にアクセスできるようにする以下の 2 つの役割があります。

| アカウントの役割| 許可|
|----------------|---------|
|所有者| アカウントの所有者は、プロファイル、ユーザー、請求先情報、消費量の通知、および使用状況ダッシュボードにアクセスできます。所有者は、「ユーザー」ページから、新しいユーザーの招待および役割の調整を行うことができます。また、所有者は、プロモーション・クレジットの追加、請求制限の設定または変更、サービス・アクセスの設定、および組織とスペースの管理を行うこともできます。|
|メンバー| メンバーは、{{site.data.keyword.Bluemix_notm}} ヘッダーで、プロファイル、アカウント内のアクティブ・ユーザーを表示する「ユーザー」ページ、およびアカウント・クレジットと請求の制限にアクセスできます。|
{:caption="表 1. アカウントの役割と許可" caption-side="top"}

すべての新規ユーザーは、アカウントのメンバーとして追加されます。組織とスペースの役割を被招待者に割り当てて、{{site.data.keyword.Bluemix_notm}} で特定のビューおよび許可を有効にすることができます。被招待者が招待を受け入れ、{{site.data.keyword.Bluemix_notm}} に参加した後は、「ユーザー」ページで役割を編集できます。

## Cloud Foundry の役割
{: #cfroles}

Cloud Foundry の役割には、アカウント内で定義された組織およびスペースに対するアクセス許可が含まれます。Cloud Foundry の役割は、サービスのコンテキスト内でアクションを完了するためにユーザー許可を使用可能にしません。組織レベルでは、以下の役割を割り当てることができます。

| 組織の役割| 許可|
|-------------------|-------------|
|管理者| 組織管理者は、組織内のスペースの作成、表示、編集、または削除、組織の使用量と割り当て量の表示、組織へのユーザーの招待、組織へのアクセス権限を持つユーザーの管理とそれらのユーザーの組織内での役割の管理、および組織のカスタム・ドメインの管理を行うことができます。|
|請求管理者| 請求管理者は、「使用状況ダッシュボード」ページで組織のランタイムとサービス使用量の情報を表示できます。|
|監査員| 組織監査員は、組織のアプリケーションおよびサービス・コンテンツを表示できます。監査員は、組織のユーザー、その割り当てられている役割、および組織の割り当て量を表示することもできます。|
{:caption="表 2. 組織の役割と許可" caption-side="top"}

スペース・レベルでは、以下の役割を割り当てることができます。

| スペースの役割| 許可|
|------------|-------------|
|管理者| スペース管理者は、スペース内での既存のユーザーの追加、および役割の管理を行うことができます。スペース管理者は、スペースでの各アプリケーションのインスタンスの数、サービス・バインディング、およびリソースの使用を表示することもできます。|
|開発者| スペース開発者は、スペース内でアプリケーションおよびサービスを作成、削除、および管理できます。管理タスクには、アプリのデプロイ、アプリの開始または停止、アプリの名前変更、アプリの削除、スペースの名前変更、アプリケーションへのサービスのバインドまたはアンバインド、およびスペース内の各アプリケーションのインスタンスの数、サービス・バインディング、リソース使用の表示が含まれます。また、スペース開発者は、内部または外部 URL をスペース内のアプリケーションに関連付けることもできます。|
|監査員| スペース監査員は、スペース内の各アプリケーションのインスタンスの数、サービス・バインディング、およびリソース使用に関する情報など、スペースに関するすべての情報に対する読み取り専用権限を備えています。|
{:caption="表 3. スペースの役割と許可" caption-side="top"}

**注**: 管理者または開発者のスペース役割が割り当てられたユーザーは、VCAP_SERVICES 環境変数にアクセスできます。しかし、監査員の役割が割り当てられたユーザーは、VCAP_SERVICES にアクセスできません。

## ID およびアクセス管理のポリシーおよび役割
{: #iamusermanpol}

アカウント所有者には ID およびアクセス管理 (IAM) 用のアカウント管理者役割が自動的に割り当てられ、サービス・ポリシーの割り当ておよび管理が行えるようになります。サービス・ポリシーは、個々のユーザーまたはサービス ID に割り当てることができ、割り当てられたポリシーは、サービス全体のアクセス権限、または個々のインスタンス・レベルでのアクセス権限を定義することができます。

### サービス・ポリシー

ポリシーは、属性の組み合わせを使用して適用可能なリソース・セットを定義することにより、リソース・セットに対する 1 つまたは複数の役割をユーザーまたはサービス ID に割り当てます。ポリシーを割り当てる場合、最初にサービスを指定します。次に、割り当てる 1 つ以上の役割を選択できます。選択するサービスに応じて、追加の構成オプションが使用可能な場合があります。

適切な役割を持っている場合、ポリシーを割り当て、管理することができます。以下の表は、ポリシー管理タスクと、各タスクに必要な役割を示しています。

| アクション| 必要な役割|
|----------|---------|
| アカウントでの、すべてのサービスおよびインスタンスについてのポリシーの作成| アカウント管理者|
| アカウント内の 1 つのサービスに関するポリシーの作成| アカウント管理者またはアカウント内のサービスの管理者 |
| サービス・インスタンスの作成| アカウント管理者、またはアカウント内のサービスの管理者またはエディター |
| 1 つのサービス・インスタンスに関するポリシーの作成| アカウント管理者、アカウント内のサービスの管理者、またはサービス・インスタンスの管理者 |
{: caption="表 4. IAM が有効になったサービスのポリシーを管理するための管理用タスク" caption-side="top"}

### サービス・ポリシーの役割
{: #iamusermanrol}

IAM により、アカウント内のユーザーとリソースのアクセスを管理および定義することができます。使用するサービスの管理を、ユーザー・アクセス制御用の IAM を使用して行える場合、アカウント内での異なるアクションを可能にする 2 つのタイプの役割、すなわちプラットフォーム管理の役割とサービス・アクセスの役割があります。

<dl>
<dt>プラットフォーム管理の役割</dt>
<dd>ユーザー・アクセス制御用の IAM を使用して管理できるすべてのサービスで使用可能な役割。これには、管理者、エディター、オペレーター、ビューアー、および請求処理管理者が含まれます。これらの役割は、プラットフォーム・レベルで {{site.data.keyword.Bluemix_notm}} リソースに対して実行できるユーザー・アクションにマップされます。例えば、これらのアクションとしては、インスタンスの作成、アプリケーションへのインスタンスの接続、サービス ID の管理、ユーザーとアクセス権の管理、およびアカウントの請求処理と割り当て量の管理などの能力があります。</dd>
<dt>サービス・アクセスの役割</dt>
<dd>これらの役割はサービスに固有です。マネージャー、ライター、およびリーダーの役割は、サービスを使用し、サービス API 呼び出しを実行するユーザーの能力を定義します。各サービスは、指定された役割を持つユーザーが実行できるアクションを定義しているので、この資料に記載されている使用可能なすべての役割がサービスで使用されない場合があります。</dd>
</dl>

**注**: UI でポリシーを割り当てる時に、すべての役割がオプションとしてリストされない可能性があります。この理由は、表示されるのは、ポリシーで選択したサービスで利用可能な役割のみだからです。それぞれのサービスでの有効な役割および各アクセス役割で許可されるアクションに関する具体的な情報については、そのサービスの資料を参照してください。


#### プラットフォーム管理の役割

プラットフォーム管理の役割は、プラットフォーム・アクションを実行するためのさまざまなレベルのアクセス権をユーザーに割り当てることを可能にします。コンソールで提供されている役割の説明に加え、以下の表に、各役割を割り当てられたユーザーが実行できる可能性があるいくつかのプラットフォーム管理アクションの例を示します。

| プラットフォーム管理の役割 | アカウント内のサービスに対してユーザーが実行できるアクション | サービス ID に対するアクション |
|:-----------------|:--------------|:---------------|
| ビューアー| インスタンスの表示 | ID および API キーの表示 |
| オペレーター|  サービス・インスタンスの表示およびバインド | 適用外|
| エディター|  サービス・インスタンスの作成、削除、編集、一時停止、再開、表示、バインド | ID の削除および API キーの作成と削除 |
| 管理者|  サービスに対するすべての管理アクション | ID および API キーの作成と削除、ID へのポリシーの割り当て |
{: caption="表 5. プラットフォーム管理の役割とアクションの例" caption-side="top"}

サービスの中には、特定のアクションを、サービスのアクセスではなくサービスの管理に関連したプラットフォーム管理の役割にマップするものがあります。例として、それらの役割にマップされている {{site.data.keyword.containershort_notm}} サービス・アクションの詳細を示す以下の表を参照してください。


| プラットフォーム管理の役割 | アクションの説明| {{site.data.keyword.containershort_notm}} サービスのアクションの例 |
|:-----------------|:-----------------|:-----------------|
| ビューアー| サービス・インスタンスの表示はできるが、変更はできない  | <ul><li>クラスターのリスト</li><li>クラスターの詳細を表示する</li></ul>|
| エディター| アカウントの管理とアクセス・ポリシーの割り当てを除き、すべてのプラットフォーム・アクションを実行する |<ul><li>クラスターへのサービスのバインド</li><li>Web フックの作成</li></ul> |
| オペレーター| サービスのダッシュボードの表示など、サービス・インスタンスの構成および操作に必要なプラットフォーム・アクションを実行する。 | <ul><li>ワーカー・ノードの追加または削除</li><li>ワーカー・ノードのリブートまたは再ロード</li><li>クラスターへのサービスのバインド</li></ul> |
| 管理者| 他のユーザーへのアクセス・ポリシーの割り当てを含め、この役割が割り当てられているリソースに基づいてすべてのプラットフォーム・アクションを実行する。|<ul><li>クラスターの削除</li><li>クラスターの作成</li><li>ユーザー・アクセス・ポリシーの更新</li><li>ビューアー、エディター、およびオペレーターが実行できるすべてのアクション</li></ul>|
{: caption="表 6. プラットフォーム管理の役割とアクションの例" caption-side="top"}


#### サービス・アクセスの役割

サービス・アクセスの役割は、サービスの API を呼び出すためのさまざまなレベルのアクセス権をユーザーに割り当てることを可能にします。以下の表は、{{site.data.keyword.objectstorageshort}} サービスの使用に基づいて割り当てられるサービス・アクセスの役割に応じて実行できるアクションの例を示しています。

**注**: 割り当てられた各役割で実行できるアクションは、ポリシーに対して選択したサービスに基づいて異なります。

| サービス・アクセスの役割 | アクションの説明| {{site.data.keyword.objectstorageshort}} サービスのアクションの例 |
|:-----------------|:-----------------|:-----------------|
|  リーダー | サービス固有のリソースの表示など、サービス内で読み取り専用アクションを実行する | オブジェクトのリストおよびダウンロード |
| ライター | ライターは、サービス固有のリソースの作成および編集など、リーダー役割を超えるアクセス権を持つ。| バケットおよびオブジェクトの作成と破棄 |
| 管理者| 管理者は、サービスによって定義された特権付きアクションを実行する、ライター役割を超えるアクセス権を持つ。それに加え、サービス固有のリソースを作成および編集できます。| データ・ストレージのすべての側面の管理、バケットおよびオブジェクトの作成と破棄 |
{: caption="表 7. サービス・アクセス・ユーザーの役割とアクションの例" caption-side="top"}


## インフラストラクチャーの許可
{: #infrapermissions}

ユーザーを招待する時に、以下の初期許可を設定できます。

| 許可セット | アクションの説明|
|---------------------------|------------------------|
|表示のみ| この許可があるユーザーは、システム内の項目の表示のみが可能です。|
|基本ユーザー| この許可があるユーザーは、チケットの追加やデバイスの管理など、システム内の基本的なアクションを実行できます。|
|スーパーユーザー| この許可があるユーザーは、システム内で使用可能なすべてのアクションを実行できます。|
{:caption="表 8. インフラストラクチャーの許可" caption-side="top"}

ユーザーが招待を受け入れた後、追加の許可を設定できます。招待時の初期許可セットは、デバイスへのアクセス権限を付与しません。したがって、ユーザーが招待を受け入れた後に、コントロール・ポータルでデバイスへのアクセス権限を付与する必要があります。