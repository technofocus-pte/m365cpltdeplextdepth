# ラボ 6 - Microsoft Copilot Studio を使用して構築された HR エージェントを使用して Microsoft 365 Copilot チャットを拡張する

**目的**

このラボでは、Microsoft Copilot Studio
を使用して作成された宣言型エージェントを使用して Microsoft 365 Copilot
チャットを拡張する方法を学習します。 また、作成したエージェントにカスタムアクションを追加する方法についても学習します。

所要時間 – 45分

## 演習 1: Power Platform 環境の作成

Power Platform
を使用すると、さまざまな環境を作成し、必要に応じて簡単に切り替えることができます。環境には、アプリ、フロー、データ、エージェントなどが格納され、各環境は他の環境から完全に分離されています。この演習では、残りの演習とタスクを実行する新しい専用環境を作成します。

1.  ブラウザを開き、「**Resources**」タブのログイン資格情報を使用して
    、「[https://admin.powerplatform.com](https://admin.powerplatform.com/)」に移動します。

![](./media/image1.png)

2.  **Manage**を選択し 、**Environment**で **+ Newを選択します**。

![](./media/image2.png)

3.  「Name」に「+++Dev
    env+++」と入力し、「**Type**」に**「Developer」を選択して、「Next」をクリックします**。
    **Add Dataverse** の追加 **画面で**保存 を選択します。

![](./media/image3.png)

![](./media/image4.png)

4.  新しい環境が作成され、
    **PreparingがReadyと**準備完了状態**から**準備完了状態に変わります。

![](./media/image5.png)

![](./media/image6.png)

## 演習 2 : Microsoft 365 Copilot Chat のエージェントの作成

この演習では、Microsoft Copilot Studio
を使用して宣言型エージェントを作成し、Microsoft 365 Copilot Chat
でホストします。

1.  「Resources[**」タブのログイン資格情報を使用して**
    https://copilotstudio.microsoft.com/](https://copilotstudio.microsoft.com/)**にログインし**ます。

![](./media/image7.png)

2.  前の演習で作成した **Dev env** 環境を選択します。

![](./media/image8.png)

3.  Microsoft 365 Copilot
    チャットの宣言型エージェントを作成するには、まず Copilot Studio
    でエージェントの一覧を参照し、次に **Microsoft 365 Copilot
    という名前のエージェントを選択する必要があります**。

4.  左側のナビゲーション バーから **\[Agents\]** を選択し **、一覧から**
    \[**Copilot for Microsoft 365**\] を選択します。

![](./media/image9.png)

5.  Microsoft Copilot Studio の新しいセクションが開きます。そこから、
    **\[+ Add**\] コマンドを選択して、Microsoft 365 Copilot Chat
    の新しいエージェントを作成します。

![](./media/image10.png)

6.  Copilot
    Studioは、エージェントの目的を自然言語で説明するように求めます。エージェントの要件を定義できます。これを行うには、以下のプロンプトを貼り付けます

> +++You are an agent helping employees to find information about HR
> policies and procedures, about how to improve their career, and about
> how to define learning pathways.+++

![](./media/image11.png)

7.  Copilot Studio から要求された場合は、カスタム エージェントに
    "Agentic HR" という名前を付けます。次のプロンプトを使用します。

+++Name it as Agentic HR+++

![](./media/image12.png)

8.  次に、次の指示を使用して、Copilot Studio
    に特定のタスクまたは目標を設定するように指示します。

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![](./media/image13.png)

9.  次に、エージェントのプロフェッショナルなトーンを定義し、次の入力を提供します。

> **+++It should have a professional tone+++**

![](./media/image14.png)

10. エージェントの説明が完了したら、\[**Create**\]
    コマンドを選択して実際のエージェントを作成します。

![](./media/image15.png)

![](./media/image16.png)

## 演習 3: Microsoft 365 Copilot チャットでエージェントを公開する

1.  エージェントの概要ページから **\[Publish**\] を選択します。

![](./media/image17.png)

2.  \[**Publish agent\] 画面で** \[**Publish**\] **を選択します** 。

![](./media/image18.png)

> ![](./media/image19.png)

3.  **\[Share link**\] で **\[Copy**\]
    を選択してリンクをコピーし、\[**Done\] を選択します**。

![](./media/image20.png)

4.  新しいタブを開き、コピーしたURLを貼り付けます。**Add**を選択して
    、**Agentic HR** をリスト エージェントに追加します。

![](./media/image21.png)

![](./media/image22.png)

5.  概要画面で **\[Skip**\] を選択します。

![](./media/image23.png)

6.  **Agentic HR** エージェントが追加されました。

![](./media/image24.png)

## 演習 4: SharePoint サイトを作成する

1.  新しいブラウザーで、左側のウィンドウから
    +++https://m365.cloud.microsoft/chat/+++
    \[**Apps**\]の選択に移動し、アプリが読み込まれたら
    **\[SharePoint**\] を選択します。

> ![](./media/image25.png)

2.  SharePoint ページから **\[+ Create** site\] を選択します。

![](./media/image26.png)

3.  \[**Select the site type\] ページから \[Communication** site**\]
    を選択します** 。

![](./media/image27.png)

4.  使用する**template**を選択します 。

![](./media/image28.png)

5.  \[**Use template\] を選択します**。

![](./media/image29.png)

6.  \[サイト名**\] に「+++Contoso site+++**」と入力し、\[**Next**\]
    を選択します**。**

![](./media/image30.png)

7.  次の画面で、**Create siteを選択します**。

![](./media/image31.png)

8.  作成したら、このサイトのURLをメモします 。

![](./media/image32.png)

9.  メニューバーから「**Documents」を選択します** 。\[**Upload -\>
    Files\] を選択します**

![](./media/image33.png)

10. C:\LabFiles**からアップロードするSample-list-of-candidates.xlsx**ファイル**を選択します**
    。

![](./media/image34.png)

## 演習 5: エージェントにアクションを追加する

この演習では、作成したエージェントにカスタムアクションを追加します。Microsoft
Copilot Studio では、Microsoft 365 Copilot Chat
のエージェントを作成するときに、次の 4 種類のアクションを追加できます:

- 新しいプロンプト: 自然言語で記述されたプロンプトを使用して構築された
  AI アクションを消費できます。

- 新しい Power Automate フロー: Power Automate フローを使用できます。

- 新しいカスタム コネクタ: Power Platform カスタム
  コネクタを使用できます。

- 新しい REST API: 外部 REST API の使用を許可します。

1.  新しいアクションを追加するには、 エージェントの構成パネルの
    \[**Actions\] セクションで \[+ Add action**\] を選択します。

![](./media/image35.png)

2.  \[ **List rows present in a table**(Excel
    online)\]オプションを選択し、\[**Next**\]を選択します **。**

![](./media/image36.png)

![](./media/image37.png)

3.  \[**List rows present in a table\] 画面で**
    、以下の詳細を入力し、\[**Add action\] を選択します**。

名前 - +++List HR candidates+++

説明 – +++List candidates for HR role+++

![](./media/image38.png)

![](./media/image39.png)

4.  アクションが追加されたら、それをクリックして開いて編集します。

![](./media/image40.png)

5.  \[**Input**\] **セクション**を選択します。

![](./media/image41.png)

6.  各入力引数の **\[How will the agent fill this input**\] で **\[Set
    as a value**\] を選択します。

![](./media/image42.png)

7.  入力設定ダイアログの変更で**\[Confirm**\]を選択します。

![](./media/image43.png)

![](./media/image44.png)

8.  各入力に以下の値を指定します。

**Location** – 前の演習で保存した Contoso サイトの URL。

Document Library – +++**Documents**+++

File – +++**Sample-list-of-candidates.xlsx**+++

Table – +++**Candidates_Table**+++

![](./media/image45.png)

![](./media/image46.png)

![](./media/image47.png)

9.  すべての更新が完了したら、\[**Save**\] を選択します。

![](./media/image48.png)

![](./media/image49.png)

10. \[ **Publish\]** を選択して、エージェントを発行します。

![](./media/image50.png)

11. もう一度 \[**Publish**\] **を選択します** 。

![](./media/image51.png)

12. URLを**コピ**ーして**、**ブラウザから**開きます。**

![](./media/image52.png)

13. 今回は、すでに追加されているため、**Update
    nowオプションが表示されます** 。それを選択します。

![](./media/image53.png)

14. 更新したら**、\[Open**\] を選択します。

![](./media/image54.png)

15. エージェントHRエージェント画面で、以下のメッセージを送信します。

> +++Show me a list of candidates for HR with role “HR Director” or ”HR
> Manager”+++

![](./media/image55.png)

16. 「Agent HR と共有されるデータ」メッセージで、「 **Allow once」**
    オプションを選択します。

![](./media/image56.png)

17. サインインを求められた場合は、 **\[Sign in to Agentic HR**\]
    オプションを選択し、次の画面で **\[Connect**\] を選択します。

![](./media/image57.png)

![](./media/image58.png)

18. 接続したら\[**Submit\]** を選択します。

![](./media/image59.png)

![](./media/image60.png)

19. 次に、次のメッセージをエージェントに再送信します。

> +++Show me a list of candidates for HR with role “HR Director” or ”HR
> Manager”+++

![](./media/image61.png)

20. その後、リクエストされたリストを受け取ります

![](./media/image62.png)

![](./media/image63.png)

## 概要

このラボでは、Copilot Studio でカスタム
コネクタを使用する方法を学びました。
