# 实验 10：为测验生成代理的主题实施提示作

## 练习 1：使用自然语言创建代理

1.  打开浏览器并登录到
    +++<https://copilotstudio.microsoft.com/+++>，并使用 Resources
    （资源） 选项卡中的凭据登录（如果您尚未进入该页面）。

![](./media/image1.png)

2.  如果您已经在 Copilot Studio 页面上，请单击**Home** 以转到主页。

![](./media/image2.png)

3.  在主页上，在 描述您的代理 创建它的文本区域中，输入 +++I want you to
    be a question and answering assistant that can answer common
    questions from users using the content of a website+++，然后单击
    **Send**。

![](./media/image3.png)

4.  它可能会建议代理的名称。要么接受它，要么提供你自己的名字。

5.  提供有关代理功能的其他详细信息，如下所示。

> +++help answer common product and support questions using the content
> of a website, and help answer HR questions from an uploaded file+++

6.  为将用作 sknowledge 源的网站提供 +++<u>www.microsoft.com+++</u> 。

![](./media/image4.png)

7.  完成提供说明后，单击 **Create** 创建您的代理。

![](./media/image5.png)

8.  代理随即创建并打开详细信息。滚动页面以了解代理已根据您提供的说明创建。

![](./media/image6.png)

![](./media/image7.png)

9.  单击 **Test** 图标以测试代理。输入 ++What is Copilot
    Studio+++，然后按 **Enter**。

![](./media/image8.png)

10. 输入 +++What is the latest xbox model?+++

![](./media/image9.png)

对于上述两个步骤，您将从代理那里获得一个通用的答案，因为代理将使用其常识。

## 练习 2：为生成式答案的主题创建提示作

作可用于扩展代理的功能。您可以在 Microsoft Copilot Studio
中向代理添加多种类型的作：

- **预构建的连接器作，**使用 Power Platform
  连接器访问来自其他系统的数据，例如 Salesforce、Zendesk、MailChimp 和
  GitHub 等流行的企业产品。

- **预构建的连接器作，**使用 Power Platform
  连接器访问来自其他系统的数据，例如 Salesforce、Zendesk、MailChimp 和
  GitHub 等流行的企业产品。

- **Power Automate 云端流，**使用 Power Automate
  云端流来执行作、检索和处理数据。

- **AI Builder 提示，**它使用 AI Builder
  和自然语言理解来定位您业务中的特定场景和工作流。

- **Bot Framework
  技能，**它使用概述技能可以执行的作的技能清单，包括其输入和输出参数、技能的终结点以及技能的调度模型。

在本练习中，您将学习如何向主题节点添加作提示

1.  在您的代理中，选择 **Topics** 选项卡，选择 **+ Add a topic** 并选择
    **From blank**。

![](./media/image10.png)

2.  将主题的名称输入为 +++Generate questions for a quiz +++。在触发器的
    Phrases 下选择 **Edit** 超链接。至少需要输入 5 个触发短语

> 逐个添加以下短语。添加每个短语，然后选择 + 选项以添加触发器。
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
> 选择右上角的 **Save** 以保存主题。

![](./media/image11.png)

3.  单击 Trigger 节点下方的 **+** 符号。选择 **Add an action**
    选项，然后选择 **New prompt （default AI model）** 选项。

![](./media/image12.png)

![](./media/image13.png)

4.  此时将显示 Prompt （提示）
    对话框，并且您可能会看到一个浮出控件，该浮出控件将指导您如何创建提示。选择
    **Next** 浏览指南。

5.  我们将创建提示，该提示将为测验生成问题。将提示的名称输入为 +++Quiz
    Generator+++。

6.  将以下内容粘贴到 Prompt 字段中。

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++
>
> 展开 **Input** 部分，然后选择 **+ Add input**。

![](./media/image14.png)

7.  选择 **Text** 在下面 **Add input** 选项。

![](./media/image15.png)

8.  输入名称 +++number+++，然后输入示例数据，例如 +++5+++。选择 **+ Add
    input -\> Text** 以添加下一个输入。

![](./media/image16.png)

9.  将名称输入为 +++topic+++ 并输入示例数据，例如
    +++Science+++，然后选择 **+ Add input -\> Text** 以添加下一个输入。

\![\](./media/image16.png)

11. 输入名称 +++format+++ 并输入示例数据，例如 +++bullet points+++

![](./media/image17.png)

12. 现在，我们已经添加了输入名称和示例数据。接下来，需要将输入插入到提示符中。在提示符中，突出显示
    **\[number\]** 并选择 **+ Add** ，然后**在提示符下**选择
    **number**。number 的输入现已作为输入添加到提示符中。

![](./media/image18.png)

![](./media/image19.png)

13. 对其余输入重复相同的步骤。

14. 将所有输入添加到提示符后，单击 **Test
    prompt**（测试提示符）并观察提示符响应。

![](./media/image20.png)

15. 选择 **Save** 以保存提示。

![](./media/image21.png)

16. 提示作节点现在将显示在 Topic 的创作画布中。接下来，需要定义 input
    参数的值，以便代理程序填充它们。选择**\>**图标

![](./media/image22.png)

17. 选择 **System** 选项卡，然后选择 **Acivity.Text**
    作为作的输入值，以使用用户的整个响应并标识格式值。

![](./media/image23.png)

18. 对提示作的其余输入参数重复相同的作。

![](./media/image24.png)

19. 接下来，我们需要定义 prompt作的 output
    变量。这样，就可以在主题的下游引用响应。选择 **\>** 图标，然后在
    **自定义** 选项卡中，选择 **Create new** 并将变量命名为
    +++**VarQuizQuestionsResponse**+++。

![](./media/image25.png)

![](./media/image26.png)

20. 在 Prompt作下，选择 + 图标以添加新节点，然后选择 **Send a
    message**。选择 {**x**} 变量图标。

![](./media/image27.png)

21. 选择变量 **VarQuizQuestionsResponse.text**。这会将提示作响应的 text
    属性添加到 send a message 节点。选择 **Save** （保存）
    以保存您的主题。

![](./media/image28.png)

22. 接下来需要更新 Topic details （主题详细信息）
    ，当启用生成模式时，您的代理将使用该详细信息将主题与用户的意图相关联。选择
    **Details** （详细信息） 并输入以下内容。

    - 显示名称 - +++generate questions for a quiz+++

    - 描述 - +++This topic creates questions for a quiz based on the
      number of questions, the topic and format provided by the user+++

> 选择 **Save** （保存） 以保存您的主题。

![](./media/image29.png)

23. 现在，需要启用 **Generative mode** （生成模式）
    设置，代理才能使用提示作调用主题。为您的代理选择
    **Settings**（设置）。

![](./media/image30.png)

24. 选择 **Generative AI** （生成式 AI） 设置，然后选择 Generate
    （preview） （生成（预览）），然后选择 **Save** （保存）。

![](./media/image31.png)

25. 现在我们准备好测试代理。在测试窗格中，选择**refresh**
    图标。然后输入以下问题并观察输出。

+++Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

![](./media/image32.png)

![](./media/image33.png)

**总结**

在本实验中，我们学习了如何通过创建自定义提示来为主题创建提示作并对其进行测试。

