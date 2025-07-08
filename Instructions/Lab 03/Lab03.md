# ラボ03 - 事前構築済みのエージェントで従業員の生産性を向上**

**目的**

あなたは、消費財流通のグローバル リーダーである Contoso Shoppee
で働くコミュニケーション ストラテジストです。同社は、デジタル
トランスフォーメーションの目標に対するチームの足並みを揃え、生産性ツールの採用を改善し、顧客エンゲージメント
イニシアチブの新しいアイデアを生み出すことを目的とした、社内のイノベーション準備ワークショップを準備しています。Microsoft
365 Copilot チャットで事前構築済みのエージェント (Prompt Coach、Writing
Coach、Idea Coach)
をワークショップの参加者に紹介して、ライティング、アイデア出し、プロンプト開発タスクの生産性を向上させるよう求められます。

このラボでは、Microsoft 365 Copilot Chat を使用して次のことを行います:

- Prompt Coach を使用して高品質のプロンプトを作成および改良する

- ライティングコーチから詳細なライティングフィードバックと強化のヒントを受け取る

- Idea Coachで創造的なアイデアを生み出し、整理

- さまざまなビジネスユースケースの迅速な有効性を向上

- Copilot
  Chatと連携して、洗練されたドラフトと構造化されたコンテンツを作成します

**演習 1: Copilot Chat を使用した事前構築済みエージェントの探索と対話**

この演習では、Microsoft 365 Copilot チャットを使用して事前構築済みの
Copilot エージェント (Prompt Coach、Writing Coach、Idea Coach)
にアクセスして対話する方法を示し、生産性を向上させるための独自の機能を理解します。

1.  Microsoft Edge ブラウザーを開き、次の URL を入力します:
    +++[https://m365.cloud.microsoft+++](https://m365.cloud.microsoft+++/)
    Microsoft **365 Copilot App** (以前のオフィス) ホーム
    ページに移動します。

**注**: サインインを求められた場合は、右側の \[リソース**\]
タブにある**資格情報**を使用してサインインする必要があります** 。

2.  **Copilot のチャット** ページが開きます。

3.  何らかの理由で「**Something went
    wrong」という**メッセージが表示された場合は、\[**Try
    again**\](2回)をクリックしてCopilot Chatを開きます。

![](./media/image1.png)

**注**: このラボを実行している場合、Copilot Chat のユーザー
インターフェイスは (手順 \#4 のように) 異なって表示される場合があります
(Microsoft は Microsoft Build-2025
イベントの一部として新機能と更新された機能、UI
の変更を公開しているため)。

4.  ケースのランディングページに応じて、ナビゲーションペインで**\[Create
    Agent**\]をクリックします。

![](./media/image2.png)

![](./media/image3.png)

5.  Copilot Studio Agent Builder
    が開きます。事前構築済みのエージェントリストが読み込まれるまでしばらく待ちます。\[**View
    all templates\] をクリックします**。

![](./media/image4.png)

![](./media/image5.png)

6.  リストをスクロールして、プロンプト品質の向上とライティングの改良に使用する宣言型エージェント(プロンプトコーチとライティングコーチ)を見つけます。

7.  「Prompt Coach」を選択します。

![](./media/image6.png)

**注**:
これらの宣言型エージェントは、テンプレートとして使用し、ニーズに合わせてカスタマイズできます。

8.  このラボでは、Prompt Coach
    をそのまま使用し、カスタマイズは行いません。
    右上の「Create」をクリックして、Prompt Coach
    エージェントを作成します。

![](./media/image7.png)

![](./media/image8.png)

これで、Prompt Coach **の作成が完了しました**。「**Go to
agent」**をクリックして、「Prompt Coach エージェント」を開きます。

![](./media/image9.png)

次に、プロンプトコーチを使用して、プロンプトの品質を向上させます。

**演習 2: Copilot Chat の Prompt Coach を使用したプロンプト品質の向上**

この演習では、市場調査レポートに対して、よりターゲットを絞った Copilot
プロンプトを生成します。

1.  次に、ドラフト プロンプトを入力します:  
    ++@Prompt Coach, review this prompt: “Give me insights on European
    retail industry.”++

![](./media/image10.png)

2.  開始するために、Copilot では次の詳細を提供する必要があります。

- **目標**: Copilot で達成したい望ましい結果は何ですか?

- **コンテキスト**: プロンプトに関連する背景情報または特定の詳細。

- **出典**: 含めたい具体的な情報源や例はありますか?

- **期待**事項: プロンプトの形式や構造について、何か好みはありますか?

![](./media/image11.png)

3.  Copilotに質問できます:このプロンプトをより具体的で実用的なものにするにはどうすればよいですか?

![](./media/image12.png)

4.  Copilot
    は、プロンプトをより具体的で実行可能なものにする方法のサンプルで応答します。

![](./media/image13.png)

5.  無視して別の単刀直入なプロンプトで試してみると、Copilotは詳細を明確にするように主張します。次のプロンプトで
    Copilot の出力を確認し、\[**Submit\] をクリックします**。

++I am trying to generate a more targeted Copilot prompt for a market
research report.++

![](./media/image14.png)

![](./media/image15.png)

6.  次に、提案を使用してプロンプトを修正し、

@Promptコーチ、この改訂されたプロンプトを評価してください。Copilot
が洞察に満ちた出力を返すのに十分な強度がありますか?

++“Summarize Q1 2024 retail trends in Germany and France, including
consumer behavior shifts and top-performing product categories.”
@Promptコーチ、この改訂されたプロンプトを評価してください。Copilotが洞察に満ちた出力を返すのに十分な強度がありますか?++

![](./media/image16.png)

7.  Copilot
    は評価コメントで応答し、提案を提供します。応答は、次のスクリーンショットに表示されるものとは少し異なる場合があります。

![](./media/image17.png)

![](./media/image18.png)

8.  次に、次のプロンプトで試して、\[Submit\]をクリックします。

++この分析には他にどのようなデータソースを使用できますか?++

![](./media/image19.png)

9.  Copilot は、一般的なデータソースに関する詳細で応答します。

![](./media/image20.png)

10. 次のプロンプトで試し、「Submit」をクリックします。

++これらのレポートにアクセスするにはどうすればよいですか?++

![](./media/image21.png)

11. 評価のコメントとデータ
    ソースの提案に基づいて、プロンプトを言い換えます。

次のプロンプトで試し、出力を確認してください:

++Provide a detailed analysis of Q1 2024 retail trends in Germany and
France, including consumer behavior shifts and top-performing product
categories, using data from German Retail Federation (HDE) and the
French Federation of Retailers (FCD).++

![](./media/image22.png)

12. Copilot で生成された応答を確認します。

次に、次のプロンプトで試して、出力を確認します。

++Provide a detailed analysis of Q1 2024 retail trends in Germany and
France, including consumer behavior shifts and top-performing product
categories, using data
from [https://www.nielson.com++](https://www.nielson.com++/)

![](./media/image23.png)

![](./media/image24.png)

これで、Prompt Coach の \>
の助けを借りて、プロンプトを作成および改良し、市場動向に関するレポートの生成が完了しました。

**試してみてください:**

**演習 2: Copilot Chat で Writing Coach
を使用してライティングを洗練する**

この演習では、Microsoft 365 Copilot
チャットを使用して次のことを行います。

- Wring Coachをテンプレートとして使用してエージェントを作成します。

- 社内コミュニケーションのトーン、明瞭さ、インパクトを洗練させる

- 特定のオーディエンス(例:経営幹部、現場の従業員)向けの主要なメッセージを言い換える

- ライティングコーチの提案を適用して、コンテンツをよりインスピレーションを与え、プロフェッショナルで、簡潔にします

**タスク \#1: Writing coach
をテンプレートとして使用してエージェントを作成します。**

**タスク#2:エージェントに以下のサンプル文を提供し、キャッチフレーズを言い換えるように依頼します**

- サンプル: 「The new employee wellness program starts next week. It’s
  really cool and we hope everyone enjoys it.”」

- Ask:@Writing
  Coach、このメッセージをトーン、明瞭さ、エグゼクティブオーディエンスに改善してください。

- 次に、以下を試して:

- @Writing Coachをインスピレーションを与えるように言い換え、concise.  
  @Writing Coach で、文をどのように改善したかを説明してください。

**タスク#3:自分の下書き(メールまたはLinkedInの投稿)を提供し、エージェントを使用して記事を微調整します。**

- 頼む：

@Writingコーチ、どうすればこの音をより自信を持ってプロフェッショナルにすることができますか?

- Writing
  Coachのエージェントに、改訂版をフォーマットされたメッセージに変換するように依頼します(例:ヘッダー、要約、召喚状の追加)。
