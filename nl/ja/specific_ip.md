---

copyright:

  years: 2018, 2019

lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# ユーザーに特定の IP アドレスを許可
{: #ips}

デフォルトでは、すべての IP アドレスを {{site.data.keyword.cloud}} コンソールにログインするため、およびクラシック・インフラストラクチャー API にアクセスするために使用できます。 どの IP アドレスがアクセス権限を持つのかを指定することができます。そうすると、指定されたアドレスのみの使用が許可され、他のすべてのアドレスは制限されます。
{:shortdesc}

制限された IP アドレスを持っている場合は、[https://cloud.ibm.com](https://cloud.ibm.com){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") のクラシック・インフラストラクチャー・ページにアクセスできません。[https://control.softlayer.com](https://control.softlayer.com){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") に移動する必要があります。
{: important}

以下のアクセス権限が割り当てられている場合、別のユーザーの IP アドレス制限を更新できます。

  * ユーザー管理サービスに対するエディター以上の役割が設定された IAM ポリシー。
  * 当該ユーザーのクラシック・インフラストラクチャー階層内で上位にいて、かつ、「ユーザーの管理」クラシック・インフラストラクチャー許可を割り当てられている
  
「ユーザーの詳細」ページで「ユーザー管理ログイン」設定を有効にしてもらったユーザーは、自分自身でこの設定を管理できます。
{: tip}

ユーザーが特定の IP アドレスのみを使用するように制限するには、以下の手順を実行します。 

1. メニュー・バーから、**「管理」** &gt; **「アクセス (IAM)」**をクリックして、**「ユーザー」**を選択します。 
2. リストからユーザーを選択します。
3. 「ユーザーの詳細」ページで**「IP アドレス制限」**セクションに移動します。 
4. **「Cloud プラットフォーム」**で、IP アドレスを入力します。 このユーザーが {{site.data.keyword.Bluemix}} にログインできるのは、ここでリストされる IP アドレスからのみです。
5. **「クラシック・インフラストラクチャー」**で、IP アドレスを入力します。 このユーザーがクラシック・インフラストラクチャー API を呼び出せるのは、ここにリストされる IP アドレスからのみです。 
  
  クラシック・インフラストラクチャー IP アドレスを入力するには、このユーザーが作成済みのクラシック・インフラストラクチャー API キーを既に持っている必要があります。
  {: note}
 

