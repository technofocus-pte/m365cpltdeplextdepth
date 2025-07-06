# 实验 8 - 创建职业指导 SharePoint 代理

**介绍：**

每天，大约有 20 亿个文档被添加到 Microsoft 365
中。随着工作场所内容数量的快速增长，您需要一种快速准确的方法来筛选它并获取所需的信息。Microsoft
SharePoint
增强了存储、组织和共享组织内容的安全性和效率。但它提供的远不止于此。您可以使用
AI 驱动的 SharePoint
代理来简化工作流程并促进适合您的团队或组织的协作。SharePoint
代理可以回答有关提问者对其具有权限的任何 SharePoint
网站或文档库上的内容的问题。如果您对 SharePoint
站点具有编辑权限，您甚至可以为特定任务创建代理并与您的团队共享。

SharePoint 代理

**现成的代理**

每个 SharePoint
站点都附带一个“现成的代理”，该代理的作用域自动限定为该站点上的内容。这些代理的范围限定为
SharePoint
网站，不需要网站管理员或网站所有者进行构建。默认情况下，将显示现成的代理。 

**定制代理**

对现成代理的结果不满意？使用站点编辑权限，您可以通过更改内容范围、身份和行为来轻松创建代理。

**目的：**

在本实验中，您将创建一个职业指导 SharePoint 代理，该代理使用 SharePoint
站点中上传的文档。

## 练习 1：从 SharePoint 主页创建代理

您在前面的实验室中创建了一个 SharePoint
站点。在本练习中，您将从中创建一个代理。

提醒：如果您从 Lab 6 开始连续进行实验，这将正常工作。否则，请重做实验 6
的**练习 4 - 创建 SharePoint 网站**，并继续下面本实验指南中的步骤。

1.  打开 SharePoint 站点（使用您在前面的实验中记下的 URL）。

2.  选择 **Home**（主页）。

![](./media/image1.png)

3.  选择 **New -\> Agent** 以创建新代理。

![](./media/image2.png)

4.  将创建一个新代理，现在选择 **Open agent**。

![](./media/image3.png)

5.  创建的代理将显示在站点中。

![](./media/image4.png)

## 练习 2：从文档创建代理

在本练习中，您会将文档上传到 SharePoint 站点并从中创建代理。

1.  选择 **Documents** （文档）。

![](./media/image5.png)

2.  选择旁边的下拉列表 **Upload** 并选择 **Files**。

![](./media/image6.png)

3.  在 **C：\LabFiles** 的 **Career Path Options in the USA.pdf** 和
    **Career Path Options.docx** 中选择 ，然后选择 **Open**。

![](./media/image7.png)

![](./media/image8.png)

4.  选择上传的文档，然后右键单击它，然后选择 **Create an agent**。

![](./media/image9.png)

5.  在 New agent （新建代理） 窗口中选择 **Edit** （编辑）
    以编辑代理的名称。

![](./media/image10.png)

6.  将代理命名为 +++Career Guidance Agent+++。选择 **Save and
    close**（保存并关闭）。

**注意：**可以通过选择左下角的 “从 Copilot Studio 添加高级自定义”
选项，从 Copilot Studio 自定义代理。

![](./media/image11.png)

7.  创建的代理将列在 **Documents**。选择它以将其打开。

![](./media/image12.png)

8.  通过输入 +++What are the Management career path available in the US?
    +++

![](./media/image13.png)

9.  观察输出和引用。

![](./media/image14.png)

> ![](./media/image15.png)

10. 选择 **Share -\> Copy link**

![](./media/image16.png)

11. 在弹出窗口中选择 允许。

![](./media/image17.png)

![](./media/image18.png)

12. 在 “复制” 窗格的 “设置” 中，您可以选择可以与之共享代理的人员。

![](./media/image19.png)

13. 使用复制的链接从浏览器访问代理。

## 总结

在本实验中，您学习了如何从网站主页和网站中上传的文档创建 SharePoint
代理。
