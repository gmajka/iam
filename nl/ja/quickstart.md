---

copyright:

  years: 2017, 2019

lastupdated: "2019-01-28"

keywords: get started with IAM, IAM tutorial, IAM quick start

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 入門チュートリアル
{: #getstarted}

このチュートリアルの目的は、IBM Cloud ID Identity and Access Management (IAM) を稼働中にできるように支援することです。これは、ご使用のアカウントにユーザーを招待し、それらのユーザーに Cloud IAM アクセス権限を割り当てることによって行われます。
{:shortdesc}

このチュートリアルは、IAM 対応リソースを対象としています。 アクセス権限管理のための Cloud IAM ポリシーの作成をサポートしていないサービスには、[Cloud Foundry アクセス権限](/docs/iam?topic=iam-cfaccess#cfaccess)または[クラシック・インフラストラクチャー許可](/docs/iam?topic=iam-infrapermission#infrapermission)を使用できます。
{: note}


## ステップ 1. ユーザーを招待し、初期アクセス権限を割り当てる
{: #step1}

1 人または複数のユーザーを招待し、招待時にユーザーの初期アクセス・ポリシーを設定することができます。 1 回の招待で複数のユーザーを招待する場合、各ユーザーに同じアクセス権限が割り当てられます。 「ユーザーの招待」ページの「アクセス権限」セクションには、割り当てを実行するための権限があるセクションのみが表示されます。

アカウント所有者は、「サービス」セクションで、招待するユーザーの Cloud IAM 役割を割り当てることができます。 以下のようにして、リソース・グループ内のすべてのリソースへのアクセス権限、リソース・グループ内の特定のサービス用のすべてのリソースへのアクセス権限、アカウント内のすべての ID およびアクセス対応サービスへのアクセス権限、アカウント内の単一リソースへのアクセス権限、またはアカウント管理サービスへのアクセス権限を付与することができます。

1. **「管理」** &gt; **「アクセス (IAM)」**に移動して、**「ユーザー」**を選択します。
2. **「ユーザーの招待」**をクリックします。
3. 招待するユーザーの E メール・アドレスを指定します。
4. **「アクセス権限」**セクションで、**「サービス」**オプションを展開します。
5. **リソース**、**リソース・グループ** 内のリソース、または**アカウント管理サービス**へのアクセス権限の割り当てを選択します。
6. 選択内容に応じて、プロンプトに従ってアクセス権限を指定します。 リソース・グループのオプションを選択した場合、そのリソース・グループにアクセスするための役割を選択することによって、リソースへのアクセス権限の表示、編集、または管理を行うことのできる権限をユーザーに提供することもできます。
7. 許可がある場合は、招待時に Cloud Foundry アクセス権限またはインフラストラクチャー・アクセス権限を割り当てることもできます。
8. **「ユーザーの招待」**をクリックします。

詳しくは、[ユーザーの招待とアクセス権限の割り当て](/docs/iam?topic=iam-iamuserinv#iamuserinv)を参照してください。

## ステップ 2. アクセス・グループの作成
{: #step2}

アカウント内のユーザーにアクセス権限を割り当てるプロセスを簡素化するために、アクセス・グループを作成できます。 アクセス・グループは、ユーザーおよびサービス ID を編成し、グループ全体に対して単一のポリシーを定義することでアクセス権限を簡単に割り当てられるようにする方法です。

### グループのセットアップ
{: #group_setup}

アクセス・グループを作成するには、以下のステップを実行します。

1. メニュー・バーから、**「管理」** &gt; **「アクセス (IAM)」**をクリックして、**「アクセス・グループ」**を選択します。
2. **「作成」**をクリックします。
3. グループの名前と説明 (オプション) を入力します。
4. **「作成」**をクリックします。

次に、ユーザーまたはサービス ID を追加することでグループのセットアップに進みます。

1. 追加先のグループの名前を選択します。
2. **「ユーザーの追加」**をクリックします。
3. 追加するユーザーをリストから選択して、**「グループに追加 (Add to group)」**をクリックします。
4. サービス ID をグループに追加するには、**「サービス ID」**をクリックします。
5. 追加する ID をリストから選択して、**「グループに追加 (Add to group)」**をクリックします。

### グループへのアクセス権限の割り当て
{: #group_access}

グループの作成後に、単一のポリシーまたは複数のポリシーを使用して、グループ内のすべてのエンティティーにアクセス権限を割り当てることができます。

1. メニュー・バーから、**「管理」** &gt; **「アクセス (IAM)」**をクリックして、**「アクセス・グループ」**を選択します。
2. アクセス権限を割り当てる対象のグループの名前を選択します。
3. **「アクセス・ポリシー」**タブで、**「アクセス権限の割り当て」**をクリックしてアクセス・ポリシーをセットアップします。 必要に応じて操作を繰り返して、さらにアクセス権限を割り当てます。

リソース・グループ内のリソースとアクセス・グループ内のユーザーを編成することで、単一のポリシーを使用してリソースのグループへのアクセス権限をユーザーのグループに割り当てて、管理する必要があるポリシーの合計数を減らすことができます。
{: tip}


## ステップ 3. 既存ユーザーのアクセス権限の管理
{: #user_access_manage}

ユーザーを招待し、初期アクセス権限を割り当て、アクセス・グループを作成した後で、アカウント内のすべてのユーザーとグループのアクセス・レベルが必要なレベルになるように、追加のアクセス権限を割り当てたり、割り当てた初期アクセス権限を編集したりする必要が生じることがあります。

### 新規アクセス権限の割り当て
{: #new_access}

新規アクセス・ポリシーを割り当てるには、以下の手順を実行します。

1. メニュー・バーから、**「管理」** &gt; **「アクセス (IAM)」**をクリックして、**「ユーザー」**を選択します。
2. アクセス権限を割り当てるユーザーの名前を選択します。
3. **「アクセス・ポリシー」**をクリックします。
4. **「アクセス権限の割り当て (Assign access)」**をクリックします。
5. 次のようにして、アクセス権限をどのように割り当てるのかを選択します。
    * グループ内のすべてのリソースへのアクセス権限を割り当てるか、グループ内の特定のサービス用のリソースのみへのアクセス権限を割り当てる場合は、**「リソース・グループ内のアクセス権限の割り当て (Assign access within a resource group)」**を選択します。 リソース・グループにアクセスするための役割を選択することによって、リソース・グループへのアクセス権限の表示、編集、または管理を行うことのできる権限をユーザーに提供することもできます。 指定されたリソースへのアクセス権限のみをユーザーに付与し、そのリソースが編成されているグループへのアクセス権限は付与しない場合は、**「アクセス権限なし」**を選択します。
    * アカウント全体のすべての ID およびアクセス対応リソースへのアクセス権限を割り当てるか、アカウント全体の特定サービスのすべてのリソースへのアクセス権限を割り当てるか、単一インスタンスへのアクセス権限を割り当てるか、または、特定のサービス・インスタンス内の単一リソースへのアクセス権限を割り当てる場合は、**「リソースへのアクセス権限の割り当て (Assign access to resources)」**を選択します。
    * **「アカウント管理サービスへのアクセス権限の割り当て (Assign access to Account management services)」**を選択して、すべてのアカウント管理サービス、または 1 つだけのアカウント管理サービスへのアクセス権限を割り当てます。
5. アクセス有効範囲を定義する役割の組み合わせを選択します。 アクセス権限について詳しくは、[Cloud IAM 役割](/docs/iam?topic=iam-iamusermanrol#iamusermanrol)を参照してください。
6. **「割り当て」**をクリックします。


### 既存のアクセス権限の編集
{: #editing_access}

ユーザーに割り当てられた役割を編集することによって、既存のアクセス権限を更新することができます。

1. メニュー・バーから、**「管理」** &gt; **「アクセス (IAM)」**をクリックして、**「ユーザー」**を選択します。
2. アクセス権限を編集する対象のユーザーの名前を選択します。
3. **「アクセス・ポリシー」**をクリックします。
4. 編集するポリシーの行で**「アクション」** ![「アクションのリスト」アイコン](../icons/action-menu-icon.svg) メニューから**「編集」**をクリックします。
4. 割り当てられた役割を更新してポリシーを編集します。
5. **「保存」**をクリックします。

削除したいポリシーの**「アクション」** ![「アクションのリスト」アイコン](../icons/action-menu-icon.svg) メニューから**「削除」**オプションをクリックすることによって、ユーザーからアクセス権限を削除できます。

## 次のステップ
{: #next}

[Cloud IAM の機能](/docs/iam?topic=iam-features#features)リストで、Cloud IAM で他に何を行うことができるのかを検討してください。
