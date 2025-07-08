# **Microsoft 365 Agents Toolkit を使用して詩的な宣言型エージェントを構築する**

**目的**

宣言型エージェントは、Microsoft 365 Copilot のカスタマイズ
バージョンであり、ユーザーは特定の指示、アクション、知識を宣言することでパーソナライズされたエクスペリエンスを作成できます。このガイドでは、Microsoft
365 Agents Toolkit (Teams Toolkit の進化版)
を使用して宣言型エージェントを構築する方法について説明します。

このラボでは、詩的な宣言型エージェントを作成します。

## **演習 1: 宣言型エージェントを作成する**

この演習では、まず Visual Studio Code
から基本的な宣言型エージェントを作成します。

1.  VM から **Visual Studio Code** を開きます。

2.  左側のウィンドウから \[**拡張機能**\] を選択し、「+++Microsoft 365
    Agents Toolkit+++」と入力します

![](./media/image1.png)

3.  **Microsoft 365 Agents Toolkit** を選択し、**\[Install\]**
    を選択して拡張機能をインストールします。

![](./media/image2.png)

4.  「**Declarative Agent」**を選択します。

![](./media/image3.png)

5.  \[**No Action**\]
    を選択して、基本的な宣言型エージェントを作成します。

![](./media/image4.png)

6.  \[**Default folder**\] を選択して、プロジェクトのルート
    フォルダーを既定の場所に保存します。

![](./media/image5.png)

7.  \[**Application Name\] に「+++My Agent+++」と入力し** 、**Enter
    キーを押します**。

![](./media/image6.png)

8.  開いた新しい Visual Studio Code ウィンドウで、\[**Microsoft 365
    Agents Toolkit\]** を選択します。

![](./media/image7.png)

9.  **\[Lifecycle\]** ウィンドウで **\[Provision**\]
    を選択し、表示されるポップアップで \[**Sign in**\]
    を選択して、Microsoft 365 アカウントにサインインします。

![](./media/image8.png)

10. \[リソース\]
    タブの資格情報を使用して**サインイン**し、完了したらウィンドウを閉じます。

![](./media/image9.png)

11. これで、基本的な宣言型エージェントの作成が完了しました。

### **タスク 1: エージェントのテスト**

このタスクでは、作成した宣言型エージェントをテストします。

1.  URL <https://m365.cloud.microsoft/chat>で Copilot
    アプリケーションに移動します。

2.  左上の **conversation drawer iconを選択します**。

> ![](./media/image10.png)

3.  宣言型エージェント \[**My Agent\] を選択します**。

> ![](./media/image11.png)

4.  質問を入力してください +++Hello! How can you help me?+++、「Thanks
    for using Microsoft 365 Agents Toolkit to create your declarative
    agent!」と返信することを確認します。

> ![](./media/image12.png)
>
> この演習では、基本的な宣言型エージェントを作成し、その機能をテストしました。

## **演習 2: 指示を追加する**

この演習では、前の演習で作成した宣言型エージェントに指示を追加し、拡張します

1.  Visual Studio Code から **appPackage/instructions.txt**
    ファイルを開き、その内容を次のテキストに置き換えます。

> <span class="mark">宣言型エージェントであり、Microsoft 365 Agents
> Toolkit を使用して作成されました。あなたは詩を作る専門家です。</span>
>
> <span class="mark">ユーザーが質問するたびに、その
> 答えを詩に変える必要があります。詩は
> 引用符を使用し、通常のテキストを使用して**はなりません**。</span>
>
> ![](./media/image13.png)

このファイルの内容は、プロビジョニング中にエージェントのマニフェストの
instructions プロパティに挿入されます。

2.  Agents Toolkit の **\[Lifecycle**\] ペインで \[**Provision**\]
    を選択します。

![](./media/image14.png)

3.  プロビジョニングが正常に完了したことを確認します。Visual Studio Code
    の右下にメッセージが表示されます。

> ![](./media/image15.png)

4.  宣言型エージェントは、ページを再読み込みした後、更新された指示を使用します。

5.  チャットページを更新し、「**My Agent**」を選択して、「+++Do we have
    chocolate in our food catalog?+++」と入力します。

![](./media/image16.png)

6.  エージェントが詩的な答えを出すのを観察します。

![](./media/image17.png)

7.  次に、エージェントに会話のスターターを追加します。

8.  **appPackage/declarativeAgent.json** ファイルを開き、instructions
    ノードの直後に**コンマ**を追加して Enter
    キーを押し、コードの下に貼り付けます。

"conversation_starters": \[

        {

            "title": "Getting Started",

            "text": "How can I get started with Agents Toolkit?"

        },

        {

            "title": "Getting Help",

            "text": "How can I get help with Agents Toolkit?"

        }

    \]

![](./media/image18.png)

9.  Microsoft 365 Agents Toolkit **の \[ライフサイクル\] ウィンドウで**
    \[**Provision\] を選択し**
    、プロビジョニングが正常に完了したことを確認します。

10. 更新された会話のスターターは、ページを更新した後、宣言型エージェントで使用できるようになります
    。

11. チャットページを更新して同じことを確認してください。

![](./media/image19.png)

## **演習 3: Web コンテンツを追加する**

この演習では、エージェントが Web コンテンツを検索する機能を追加します。

1.  **appPackage/declarativeAgent.json** ファイルを開き、次の内容を含む
    capabilities 配列を追加します。

> "capabilities": \[
>
> {
>
> "name": "WebSearch"
>
> }
>
> \]
>
> ![](./media/image20.png)

2.  **Microsoft 365 Agents Toolkit の \[ライフサイクル\] ウィンドウで**
    \[**Provision\]**
    を選択し、プロビジョニングが正常に完了したことを確認します。

> ![](./media/image21.png)
>
> 宣言型エージェントは、ページを再読み込みした後、Webコンテンツにアクセスして回答を生成できます。

3.  エージェントに +++How can I build a declarative
    agent?+++と尋ね、エージェントが Web から応答することを確認します。

> ![](./media/image22.png)

## **概要**

Microsoft 365 Copilot
の宣言型エージェントを作成する方法を学習しました。また、作成したエージェントを指示とWebコンテンツで強化し、各ステージでテストする方法も学びました。
