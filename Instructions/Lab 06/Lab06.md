# 实验室 6 - 使用使用 Microsoft Copilot Studio 构建的 HR 代理扩展 Microsoft 365 Copilot 聊天

**目的**

在本实验中，您将学习如何使用使用 Microsoft Copilot Studio
制作的声明性代理扩展 Microsoft 365 Copilot Chat。
您还将学习如何将自定义作添加到您所做的代理。

预计持续时间 – 45 分钟

## 练习 1：创建 Power Platform 环境

使用 Power
Platform，您可以创建不同的环境，并根据您的需要轻松地在它们之间切换。环境存储应用程序、流、数据、代理等，每个环境都与任何其他环境完全隔离。在本练习中，您将创建一个新的专用环境，您将在其中执行其余的练习和任务。

1.  打开浏览器，然后使用 **Resources** （资源）
    选项卡中的登录凭证转到[https://admin.powerplatform.com](https://admin.powerplatform.com/)。

![](./media/image1.png)

2.  选择 **Manage** ，然后在 **Environments** 下选择 + **New**。

![](./media/image2.png)

3.  将 名称 提供为 +++**Dev env**+++，选择 **Type** 作为 **Developer**
    ，然后单击 **Next**。在 **Add Dataverse** 屏幕中选择 **Save** 。

![](./media/image3.png)

![](./media/image4.png)

4.  新环境将创建，并在准备就绪后从 **Preparing** （正在准备） 更改为
    **Ready** （就绪） 状态。

![](./media/image5.png)

![](./media/image6.png)

## 练习 2：为 Microsoft 365 Copilot Chat 创建代理

在本练习中，你将使用 Microsoft Copilot Studio
创建声明性代理，并将其托管在 Microsoft 365 Copilot Chat 中。

1.  使用 **Resources** （资源）
    选项卡中的登录凭证登录到<https://copilotstudio.microsoft.com/>。

![](./media/image7.png)

2.  选择我们在上一个练习中创建的 **Dev env** 环境。

![](./media/image8.png)

3.  要为 Microsoft 365 Copilot Chat 创建声明性代理，您需要先浏览 Copilot
    Studio 中的代理列表，然后选择名为 **Microsoft 365 Copilot** 的代理。

4.  从左侧导航栏中选择 **Agents** ，然后从列表中选择 **Copilot for
    Microsoft 365**。

![](./media/image9.png)

5.  将打开 Microsoft Copilot Studio 的新部分。从那里，选择 **+ Add**
    命令为 Microsoft 365 Copilot Chat 创建新代理。

![](./media/image10.png)

6.  Copilot Studio
    要求您用自然语言描述代理的目的是什么。您可以定义代理程序要求。粘贴下面的提示以执行此作

> **+++You are an agent helping employees to find information about HR
> policies and procedures, about how to improve their career, and about
> how to define learning pathways.+++**

![](./media/image11.png)

7.  当 Copilot Studio 请求时，为您的自定义代理指定名称 “Agentic
    HR”。使用以下提示。

+++Name it as Agentic HR+++

![](./media/image12.png)

8.  然后，按照以下说明指示 Copilot Studio 执行特定任务或目标：

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![](./media/image13.png)

9.  然后，为您的座席定义专业语气，提供以下输入：

**+++It should have a professional tone+++**

![](./media/image14.png)

10. 描述完代理后，选择 **Create** 命令以创建实际代理。 

![](./media/image15.png)

![](./media/image16.png)

## 练习 3：在 Microsoft 365 Copilot Chat 中发布代理

1.  从代理概述页面中选择 **Publish**。

![](./media/image17.png)

2.  在 **Publish agent** 屏幕中选择 **Publish**。

![](./media/image18.png)

> ![](./media/image19.png)

3.  选择 **Share link** （共享链接） 下的 **Copy** （复制）
    以复制链接，然后选择 **Done** （完成）。

![](./media/image20.png)

4.  打开一个新选项卡并粘贴复制的 URL。选择 **Add** 将 **Agentic HR**
    添加到您的列表代理。

![](./media/image21.png)

![](./media/image22.png)

5.  在简介屏幕中选择 **Skip**。

![](./media/image23.png)

6.  现已添加 **Agentic HR** 代理。

![](./media/image24.png)

## 练习 4：创建 SharePoint 站点

1.  在新浏览器中，导航到 +++https://m365.cloud.microsoft/chat/+++
    从左侧窗格中选择 **Apps** ，然后在加载应用程序后选择
    **SharePoint**。

> ![](./media/image25.png)

2.  从 SharePoint 页面中选择 **+ Create** 站点。

![](./media/image26.png)

3.  从 **Select the site type** （选择站点类型） 页中选择
    **Communication site** （通信站点）。

![](./media/image27.png)

4.  选择要使用的**模板**。

![](./media/image28.png)

5.  选择 **Use template**（使用模板）。

![](./media/image29.png)

6.  输入 +++**Contoso site**+++ 作为 **Site name**
    （站点名称），然后选择 **Next** （下一步）。

![](./media/image30.png)

7.  在下一个屏幕中，选择 **Create site** （创建站点）。

![](./media/image31.png)

8.  创建后，记下此站点的 **url**。

![](./media/image32.png)

9.  从菜单栏中选择 **Documents**。选择 **Upload -\> Files**

![](./media/image33.png)

10. 从 **C：\LabFiles** 中选择要上传
    **Sample-list-of-candidates.xlsx**文件。

![](./media/image34.png)

## 练习 5：向代理添加作

在本练习中，您将向您创建的代理添加自定义作。在 Microsoft Copilot Studio
中，为 Microsoft 365 Copilot Chat
创建代理时，您可以添加四种不同类型的作：

- 新建提示：允许使用通过自然语言编写的提示构建的 AI 作。

- 新的 Power Automate 流：允许使用 Power Automate 流。

- 新建自定义连接器：允许使用 Power Platform 自定义连接器。

- 新的 REST API：允许使用外部 REST API...

1.  要添加新作，请在代理配置面板的 **Actions** （作） 部分中选择 **+ Add
    action** （添加作）。

![](./media/image35.png)

2.  选择 **List rows present in a table**（Excel online） 选项，然后选择
    **Next**。

![](./media/image36.png)

![](./media/image37.png)

3.  在 **List rows in a table** （列出表中存在的行）
    屏幕中，提供以下详细信息，然后选择 **Add action** （添加作）。

姓名- +++List HR candidates+++

描述 – +++List candidates for HR role+++

![](./media/image38.png)

![](./media/image39.png)

4.  添加作后，单击它以打开并编辑它。

![](./media/image40.png)

5.  选择 **Inputs** 部分。

![](./media/image41.png)

6.  在 **How will the agent for each of the input
    argument**（代理将如何为每个输入参数填充此输入）下选择 **Set as a
    value**（设置为值）。

![](./media/image42.png)

7.  在更改输入设置对话框中选择 **Confirm**。

![](./media/image43.png)

![](./media/image44.png)

8.  为每个输入提供以下值。

**Location （位置） –** 您在前面的练习中保存的 Contoso 站点 URL。

文档库 – +++**Documents**+++

文件 – +++**Sample-list-of-candidates.xlsx**+++

牌桌 – +++**Candidates_Table**+++

![](./media/image45.png)

![](./media/image46.png)

![](./media/image47.png)

9.  完成所有更新后，选择 **Save** （保存）。

![](./media/image48.png)

![](./media/image49.png)

10. 选择 **Publish** （发布） 以发布代理。

![](./media/image50.png)

11. 再次选择 **Publish** （发布）。

![](./media/image51.png)

12. **复制** URL 并从浏览器中**打开**它。

![](./media/image52.png)

13. 这一次，它将提供一个选项 **Update now** 因为它已经添加。选择它。

![](./media/image53.png)

14. 选择 **Open** 更新后。

![](./media/image54.png)

15. 在 Agentic HR 代理屏幕中，发送以下消息。

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image55.png)

16. 在 Data to be shared with Agentic HR 消息中，选择 **Allow once**
    选项。

![](./media/image56.png)

17. 如果系统要求您登录，请选择 “**Sign in to Agentic HR**”
    选项，然后在下一个屏幕中选择 “**Connect**” 。

![](./media/image57.png)

![](./media/image58.png)

18. 连接后选择 **Submit** （提交）。

![](./media/image59.png)

![](./media/image60.png)

19. 现在，将以下消息重新发送给代理。

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image61.png)

20. 然后，您将收到请求的列表

![](./media/image62.png)

![](./media/image63.png)

## 总结

在本实验中，您已成功学习了如何在 Copilot Studio 中使用自定义连接器。
