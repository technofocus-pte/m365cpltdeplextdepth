# 使用 Microsoft 365 Agents Toolkit 构建诗意的声明性代理

**目的**

声明性代理是 Microsoft 365 Copilot
的自定义版本，允许用户通过声明特定说明、作和知识来创建个性化体验。本指南提供了有关如何使用
Microsoft 365 Agents Toolkit （Teams Toolkit）
的演变来构建声明性代理的信息。

在本实验中，您将构建一个诗意的声明式代理。

## 练习 1：创建声明性代理

在本练习中，您将从从 Visual Studio Code 创建基本的声明性代理开始。

1.  在 VM 中，打开 **Visual Studio Code**。

2.  从左窗格中选择 **Extensions** ，然后键入 +++Microsoft 365 Agents
    Toolkit+++

![](./media/image1.png)

3.  选择 **Microsoft 365 Agents Toolkit**，然后选择 **Install** 安装
    以安装扩展。

![](./media/image2.png)

4.  选择 **Declarative Agent** （声明式代理）。

![](./media/image3.png)

5.  选择 **No Action** （无作） 以创建基本的声明性代理。

![](./media/image4.png)

6.  选择 **Default folder** （默认文件夹）
    以将项目根文件夹存储在默认位置。

![](./media/image5.png)

7.  输入 +++My Agent+++ 作为 **Application Name** ，然后按 **Enter**。

![](./media/image6.png)

8.  在打开的新 Visual Studio Code 窗口中，选择 **Microsoft 365 Agents
    Toolkit**。

![](./media/image7.png)

9.  在 **Provision** 窗格中选择 **Lifecycle**
    ，然后在出现的弹出窗口中选择 **Sign in** 以登录到 Microsoft 365
    帐户。

![](./media/image8.png)

10. 使用 Resources （资源） 选项卡中的凭证 **Sign in**
    ，并在完成后关闭窗口。

![](./media/image9.png)

11. 现在，基本的声明性代理创建已完成。

### 任务 1：测试代理

在此任务中，我们将测试我们创建的声明式代理。

1.  导航到 <https://m365.cloud.microsoft/chat> 的 Copilot 应用程序。

2.  在左上角，**选择对话抽屉图标。**

> ![](./media/image10.png)

3.  选择声明式代理 **My Agent** （我的代理）。

> ![](./media/image11.png)

4.  输入问题 +++Hello! How can you help me?+++
    您的声明性代理，并确保它回复“Thanks for using Microsoft 365 Agents
    Toolkit to create your declarative agent!“

> ![](./media/image12.png)
>
> 在本练习中，我们创建了一个基本的声明性代理并测试了其功能。

## 练习 2：添加说明

在本练习中，我们将开始向在上一个练习中创建的声明式代理添加指令，并对其进行增强

1.  在 Visual Studio Code 中，打开 **appPackage/instructions.txt**
    文件并将其内容替换为以下文本。

> <span class="mark">You are a declarative agent and were created with
> Microsoft 365 Agents Toolkit. You are an expert at creating
> poems.</span>
>
> <span class="mark">Every time a user asks a question, you **must**
> turn the answer into a poem. The poem **must** not use the quote
> markdown and use regular text.</span>
>
> ![](./media/image13.png)

在置备期间，此文件的内容将插入到代理清单的指示 属性中。

2.  在 Agents Toolkit 的 **Lifecycle** （生命周期） 窗格中选择
    **Provision**（配置）。

![](./media/image14.png)

3.  检查**预置**是否已**成功完成**。您可以在 Visual Studio Code
    的右下角看到一条消息。

> ![](./media/image15.png)

4.  在您重新加载页面后，声明式代理将使用您更新的说明。

5.  刷新聊天页面，选择 **My Agent** 并输入 +++Do we have chocolate in
    our food catalog? +++

![](./media/image16.png)

6.  观察代理给出一个诗意的答案。

![](./media/image17.png)

7.  现在，将对话启动器添加到代理。

8.  打开 **appPackage/declarativeAgent.json** 文件，在
    指示节点后添加**逗号**，按 Enter，然后粘贴以下代码。

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

9.  在 **Microsoft 365 代理工具包**的 生命周期 窗格中选择
    “**Provision**” ，并确保预配成功完成。

10. **刷新**页面后，更新的对话启动器将在您的声明式代理中可用。

11. **刷新**聊天页面以检查相同的内容。

![](./media/image19.png)

## 练习 3：添加 Web 内容

在本练习中，您将向代理添加搜索 Web 内容的功能。

1.  打开 **appPackage/declarativeAgent.json** 文件并添加包含以下内容的
    能力 数组。

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

2.  在 **Microsoft 365 代理工具包**的 生命周期 窗格中选择
    “**Provision**” ，并确保预配成功完成。

> ![](./media/image21.png)
>
> 声明式代理将有权访问 Web 内容，以便在您重新加载页面后生成其答案。

3.  询问代理，+++ How can I build a declarative agent? +++
    并观察代理是否从 Web 进行回复。

> ![](./media/image22.png)

## 总结

你已了解如何为 Microsoft 365 Copilot
创建声明性代理。您还学习了如何使用说明和 Web
内容来增强创建的代理，并在每个阶段对其进行测试。
