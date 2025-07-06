# 实验 02 - 在 Microsoft 365 Copilot 聊天中创建和配置代理

**目的**

在本实验中，您将使用描述和配置选项卡创建和配置 Copilot 代理。

您将使用 Copilot Studio Agent Builder：

- 使用 Copilot Studio Agent Builder 中的 “描述” 和 “配置” 选项卡创建代理

- **注： Describe** （描述） 选项卡的可用性取决于 [**geographic
  availability and language
  support**](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build)
  （地理可用性和语言支持）。 如果您所在的区域或首选语言不支持
  **Describe** （描述） 选项卡，您可以通过 **Configure** （配置）
  选项卡手动构建代理。

<!-- -->

- 自定义代理说明、知识源和启动提示。

- 测试和编辑您的代理。

- 在组织内管理和共享您的代理。

**练习 1：使用 Describe 选项卡创建 Copilot 代理**

在本练习中，您将使用 Copilot Studio 中的 Describe 选项卡创建基本代理。

1.  打开 Microsoft Edge 浏览器并输入以下 URL：
    +++[https://m365.cloud.microsoft+++](https://m365.cloud.microsoft+++/) 转到
    **Microsoft 365 Copilot 应用程序**（以前称为 Office）主页。

**注意：**您需要使用右侧 **Resources （**资源） 选项卡下提供的
**Credentials** （凭据） 登录（如果出现提示）。

2.  **Copilot 聊天**页面将打开。

3.  如果出于某种原因出现 **“Something went wrong”** 消息，请单击 **Try
    again（**两次）以打开 Copilot 应用程序。

![](./media/image1.png)

**注意：**当您执行此实验室时，Copilot Chat 用户界面可能会有所不同（因为
Microsoft 已推出新功能和更新功能以及 UI 更改，作为 Microsoft Build-2025
活动的一部分）。

![](./media/image2.png)

![](./media/image3.png)

4.  单击 **Create an agent**（创建代理）。

![](./media/image4.png)

5.  Copilot Studio Agent Builder 将打开。

![](./media/image5.png)

6.  在 **Describe 选项卡**中，在 Natural language
    描述中输入代理用途的描述。

在本练习中，您将输入 ++**An agent that assists users in finding popular
learning paths and modules from Microsoft**++。

![](./media/image6.png)

7.  单击 Submit 以预览草稿代理。

8.  设置了初始配置的草稿代理将自动保存。查看自动生成的字段并进行必要的调整。在本练习中，您将按原样使用自动生成的字段。

![](./media/image7.png)

9.  系统将提示您确认或建议代理的名称。在本练习中，将名称指定为
    **LearnAssist Buddy**。

![](./media/image8.png)

![](./media/image9.png)

10. 您现在已经创建了一个包含基本详细信息的代理。系统将提示您完善代理的说明并进行必要的调整。在本练习中，您将使用默认设置来加快创建过程。

![](./media/image10.png)

**练习 2：使用 Configure 选项卡配置代理详细信息**

在本练习中，您将配置代理设置以微调其行为。

**注意：**如果您直接从 Configure
选项卡创建代理，则需要定义代理的名称、描述和用途。

1.  切换到 Agent Builder 中的 Configure 选项卡。

![](./media/image11.png)

2.  您可以配置座席的行为设置，包括响应语气和交互样式。在本练习中，您将按照默认说明继续作。

![](./media/image12.png)

3.  现在，您将设置代理将使用的知识源，例如特定的 SharePoint
    站点、文档库和网站。在本练习中，您将使用网站作为知识源来为代理响应提供基础。

填充 +++<https://learn.microsoft.com/en-us/training+++> 并按 Enter。

![](./media/image13.png)

![](./media/image14.png)

**注意：**网站 URL 的深度不能超过两层。此外，如果您不添加
URL，代理将搜索公共 Web 站点，并打开 Web 搜索。

![](./media/image15.png)

4.  配置更改将自动保存。

![](./media/image16.png)

5.  您现在已经完成了使用根据组织需求定制的自定义设置配置代理。现在，您将确保代理按预期运行并进行必要的调整。

**练习 3：测试和编辑代理**

现在，您将测试代理是否根据配置设置进行响应。

1.  现在，您将输入以下提示来评估代理的响应。

++**List the popular learning paths and modules offered by
Microsoft**++.

![](./media/image17.png)

2.  您可以通过将响应与输入的用作知识源的 URL
    中的可用信息进行比较来检查响应。

![](./media/image18.png)

3.  您还可以通过输入一些不相关的提示来测试响应。

++**Help me with instructions for baking cakes**++

![](./media/image19.png)

代理根据“避免讨论与 Microsoft
学习路径和模块无关的主题”的说明避免提供答案。

**注意：**您的情况中的默认指令集可能有所不同。请确保正确配置说明，以使代理避免提供答案。

4.  返回到 **Configure** （配置）
    **选项卡**，根据需要编辑代理的设置、说明或知识源。

5.  满意后，单击右上角的 **Create** 以发布代理。

![](./media/image20.png)

![](./media/image21.png)

6.  您的 LearnAssist Buddy 代理已成功创建。

![](./media/image22.png)

**练习 4：管理和共享代理**

现在，您将在组织内部署代理并管理其辅助功能。

1.  通过设置适当的权限，与特定用户或组共享代理。

![](./media/image23.png)

![](./media/image24.png)

2.  根据用户反馈和性能指标进行迭代改进。

**试一试：**

- 创建代理 “Product Buddy” 以获取产品详细信息。

- 将数据源映射到您在“实验室 0 - 准备实验室执行”中创建的文档库

![](./media/image25.png)

![](./media/image26.png)

![](./media/image27.png)

![](./media/image28.png)

- 通过询问相关产品相关提示来测试代理，以检查其功能。

**总结：**

您现在已经完成了创建与不同知识源和指令集映射的代理，以从代理获得预期的响应。
