# ラボ 10: クイズ生成エージェントのトピックに対する迅速なアクションを実装する

**目的：**

迅速なアクションは、Microsoft Copilots を拡張する方法の 1
つです。これは、ビジネス固有の自然言語アクションを作成することによって行われます。アクションはGPTモデルによって解釈され、指示どおりに必要なアクションを実行します。これらのアクションはAIプラグイン定義にラップされており、副操縦士は一致するインテントまたは発話が検出されたときに実行時に呼び出すことができます。

このラボでは、特定のトピックに基づいてクイズの質問を生成するクイズ生成トピックのプロンプト
アクションを作成する方法を学習します。

## **演習 1: 自然言語を使用してエージェントを作成する**

1.  ブラウザを開いて +++<https://copilotstudio.microsoft.com/+++>
    にログインし、\[リソース\] タブの資格情報でログインします
    (まだそのページが表示されていない場合)。

![](./media/image1.png)

2.  すでにCopilot
    Studioページを表示している場合は、\[**Home**\]をクリックして
    ホームページに移動します。

![](./media/image2.png)

3.  ホームページの「エージェントの説明」の下のテキスト領域に、「+++I
    want you to be a question and answering assistant that can answer
    common questions from users using the content of a
    website+++」と入力し、「**Send**」をクリックします。

![](./media/image3.png)

4.  エージェントの名前が提案される場合があります。それを受け入れるか、自分の名前を入力してください。

5.  エージェントの機能に関するその他の詳細を以下のように提供してください。+++help
    answer common product and support questions using the content of a
    website, and help answer HR questions from an uploaded file+++

6.  ナレッジ ソースとして使用される Web
    サイトに+++[www.microsoft.com+++](http://www.microsoft.com+++/)を指定します。

![](./media/image4.png)

7.  指示の入力が完了したら、\[Create\]をクリックして
    エージェントを作成します。

![](./media/image5.png)

8.  エージェントが作成され、詳細が表示されます。ページをスクロールして、エージェントが指定した指示で作成されていることを確認します。

![](./media/image6.png)

![](./media/image7.png)

9.  \[**Test\]**
    アイコンをクリックして、エージェントをテストします。「+++Copilot
    Studioとは+++」と入力し、**Enter**キーを押します。

![](./media/image8.png)

10. +++What is the latest xbox model?+++と入力します。

![](./media/image9.png)

> 上記の両方の手順で、エージェントが一般的な知識を使用するため、エージェントから一般的な回答が得られます。

## **演習 2: 生成的な回答のためのトピックのプロンプト アクションを作成する**

アクションを使用して、エージェントの機能を拡張できます。Microsoft
Copilot Studio
では、エージェントに複数の種類のアクションを追加できます。

- **Power Platform
  コネクタを使用して、Salesforce、Zendesk、MailChimp、GitHub**
  などの一般的なエンタープライズ製品などの他のシステムからデータにアクセスする事前構築済みコネクタ
  アクション。

- **カスタム コネクタ アクション**: パブリック API またはプライベート
  API からデータにアクセスするようにコネクタを構築できます。

- **Power Automate クラウド フロー**: Power Automate クラウド
  フローを使用して、アクションを実行し、データを取得して操作します。

- **AI Builder プロンプト**は、AI Builder
  と自然言語理解を使用して、ビジネス内の特定のシナリオとワークフローをターゲットにします。

- **Bot Framework スキル**は、スキルが実行できるアクション
  (入力パラメーターと出力パラメーター、スキルのエンドポイント、スキルのディスパッチ
  モデルなど) の概要を示すスキル マニフェストを使用します。

この演習では、トピックノードにアクションへのプロンプトを追加する方法を学習します

1.  エージェントで **トピック** タブを選択し、**+ Add a
    topic**を選択して、**From blank**を選択します。

![](./media/image10.png)

2.  トピックの名前を+++Generate questions for a
    quiz+++として入力します。 トリガーのフレーズの下にある \[**Edit**\]
    ハイパーリンクを選択します。最低5つのトリガーフレーズを入力する必要があります

> 以下のフレーズを1つずつ追加します。各フレーズを追加し、 \[+\]
> オプションを選択してトリガーを追加します。
>
> +++create a number of questions for a quiz based on a topic and format
> the quiz based on the instruction provided+++
>
> +++creates a quiz with a number of questions based on the topic
> provided and formats the quiz+++
>
> +++generate a quiz with a number of questions using the topic provide
> and format the questions+++
>
> +++creates questions for a quiz on a specific topic and format+++
>
> +++format a quiz by a number of questions based on the topic
> provided+++
>
> 右上の **Save**を選択して 、トピックを保存します。

![](./media/image11.png)

3.  トリガーノードの下にある+記号をクリックします。**Add an
    action**オプションを選択し、その下で **New prompt (default AI
    model)**オプションを選択します。

![](./media/image12.png)

![](./media/image13.png)

4.  \[プロンプト\]
    ダイアログが表示され、プロンプトの作成方法をガイドするポップアップが表示される場合があります。\[**Next**\]
    を選択して、ガイドを進めます。

5.  クイズの質問を生成するプロンプトを作成します。プロンプトの名前を
    +++Quiz Generator+++ として入力します。

6.  以下の内容を\[プロンプト\]フィールドに貼り付けます。

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++  
>   
> **\[Input**\] セクションを展開し、\[**+ Add input\]** を選択します。

![](./media/image14.png)

7.  **\[Add input**\] オプションで **\[Text**\] を選択します。

![](./media/image15.png)

8.  名前を +++number+++ として入力し、+++5+++ などのサンプル
    データを入力します。\[ **+ Add
    input** -\> **Text** \]を選択して、次の入力を追加します。

![](./media/image16.png)

9.  名前を +++topic+++ として入力し、+++Science+++ などのサンプル
    データを入力してから、 **\[+ Add input** -\> **Text** \]
    を選択して次の入力を追加します。

> \![\](./media/image16.png)

10. 名前を+++format+++として入力し、+++bullet
    points+++などのサンプルデータを入力します。

![](./media/image17.png)

11. これで、入力名とサンプルデータが追加されました。次に、入力をプロンプトに挿入する必要があります。プロンプトで
    **\[number\]** を強調表示し、\[**+ Add**\] を選択し、\[**In your
    prompt**\] で **\[number**\] を選択します。これで、number
    の入力が入力としてプロンプトに追加されました。

![](./media/image18.png)

![](./media/image19.png)

12. 残りの入力についても同じ手順を繰り返します。

13. すべての入力がプロンプトに追加されたら、\[**Test prompt**\]
    をクリックし、プロンプトの応答を確認します。

![](./media/image20.png)

14. \[**Save\] を選択して**プロンプトを保存します。

![](./media/image21.png)

15. プロンプトアクションノードがトピックのオーサリングキャンバスに表示されます。次に、エージェントが入力するために、入力パラメータの値を定義する必要があります。**\>**アイコンを選択します。

![](./media/image22.png)

16. \[**システム**\] タブを選択し、アクションの入力値として
    **\[Acivity.Text**\]
    を選択して、ユーザーの応答全体を使用し、形式値を識別します。

![](./media/image23.png)

17. プロンプト・アクションの残りの入力パラメータについても同じことを繰り返します。

![](./media/image24.png)

18. 次に、プロンプトアクションの出力変数を定義する必要があります。これは、応答をトピックの下流で参照できるようにするためです。**\>**
    アイコンを選択し、**カスタム**タブで **Create new**を選択し、変数に
    「+++**VarQuizQuestionsResponse**+++」という名前を付けます。

![](./media/image25.png)

![](./media/image26.png)

19. プロンプト アクションの下にある **+**
    アイコンを選択して新しいノードを追加し、**Send a
    message**を選択します。**{x}** 変数アイコンを選択します。

![](./media/image27.png)

20. 変数 **VarQuizQuestionsResponse.text**
    を選択します。これにより、プロンプト・アクション応答のテキスト・プロパティーがメッセージ送信ノードに追加されます。**\[Save**\]を選択してトピックを保存します。

![](./media/image28.png)

21. 次に、ジェネレーティブモードが有効になっているときに、エージェントがトピックをユーザーのインテントに関連付けるために使用するトピックの詳細を更新する必要があります。\[**Details**\]
    を選択し、次のように入力します。

    - 表示名 - +++generate questions for a quiz+++

    - 説明 - +++This topic creates questions for a quiz based on the
      number of questions, the topic and format provided by the user+++

\[**Save\]** を選択して トピックを保存します。

![](./media/image29.png)

22. 次に、 エージェントがプロンプト
    アクションでトピックを呼び出すには、ジェネレーティブ
    モード設定を有効にする必要があります。エージェントの
    \[**Settings**\]を選択します。

![](./media/image30.png)

23. \[ジェネレーティブ AI**\]** 設定を選択し、\[**Generate (preview)\]**
    を選択してから \[**Save**\] を選択します。

![](./media/image31.png)

24. これで、エージェントをテストする準備が整いました。テスト
    ウィンドウで、**更新**アイコンを選択します。次に、次の質問を入力し、出力を観察します。

> +++Create 5 questions for a quiz based on geography and format the
> quiz as multi choice+++
>
> ![](./media/image32.png)
>
> ![](./media/image33.png)

**概要**

このラボでは、カスタム
プロンプトを作成してテストすることで、トピックのプロンプト
アクションを作成する方法を学習しました。

m365cpltdeplextdepth/Instructions/Lab 10/Lab10.md at
m365cpltdeplextdepth-Dec2K24 · technofocus-pte/m365cpltdeplextdepth

 
