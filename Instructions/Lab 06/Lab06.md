# 실습 6 - Microsoft Copilot Studio를 사용하여 구축된 HR 에이전트로 Microsoft 365 Copilot Chat 확장함

**목표**

이 실습에서는 Microsoft Copilot Studio를 사용하여 만든 선언적 에이전트를
통해 Microsoft 365 Copilot Chat을 확장하는 방법을 알아봅니다. 또한, 만든
에이전트에 사용자 지정 작업을 추가하는 방법도 알아봅니다.

예상 소요 시간 - 45분

## 연습 1: Power Platform 환경 만들기

Power Platform을 사용하면 다양한 환경을 만들고 필요에 따라 쉽게 전환할
수 있습니다. 환경은 앱, 흐름, 데이터, 에이전트 등을 저장하며, 각 환경은
다른 환경과 완전히 분리됩니다. 이 연습에서는 나머지 연습과 작업을 수행할
새로운 전용 환경을 만듭니다.

1.  브라우저를 열고 **Resources** 탭의 로그인 정보를 사용하여
    [https://admin.powerplatform.com](https://admin.powerplatform.com/)으로
    이동합니다.

![](./media/image1.png)

2.  **Manage**를 선택한 다음 **Environments**에서 **+ New**를
    선택합니다.

![](./media/image2.png)

3.  이름을 +++ **Dev env** +++로 입력하고, **Type**을 **Developer**로
    선택한 후 **Next**를 클릭합니다. **Add Dataverse**화면에서
    **Save**를 선택합니다.

![](./media/image3.png)

![](./media/image4.png)

4.  새로운 환경이 생성되고 준비가 되면 **Preparing** 상태에서 **Ready**
    상태로 변경됩니다.

![](./media/image5.png)

![](./media/image6.png)

## 연습 2: Microsoft 365 Copilot Chat용 에이전트 만들기

이 연습에서는 Microsoft Copilot Studio를 사용하여 선언적 에이전트를
만들고 Microsoft 365 Copilot Chat에서 호스팅해 보겠습니다.

1.  **Resources**탭의 로그인 자격 증명을 사용하여
    <https://copilotstudio.microsoft.com/>에 로그인합니다.

![](./media/image7.png)

2.  이전 연습에서 만든 **Dev env** 환경을 선택합니다.

<img src="./media/image8.png" style="width:6.26806in;height:2.30625in" />

3.  Microsoft 365 Copilot Chat용 선언적 에이전트를 만들려면 먼저 Copilot
    Studio에서 에이전트 목록을 탐색한 다음 이름이 **Microsoft 365
    Copilot**인 에이전트를 선택해야 합니다.

4.  왼쪽 탐색 모음에서 **Agents**를 선택하고 목록에서 **Copilot for
    Microsoft 365**를 선택합니다.

![](./media/image9.png)

5.  Microsoft Copilot Studio의 새 섹션이 열립니다. 여기에서
    **Add**명령을 선택하여 Microsoft 365 Copilot Chat용 새 에이전트를
    만듭니다.

![](./media/image10.png)

6.  Copilot Studio에서는 에이전트의 목적을 자연어로 설명하도록
    요청합니다. 에이전트 요구 사항을 직접 정의할 수 있습니다. 아래
    프롬프트를 붙여넣어 입력하세요

> **+++You are an agent helping employees to find information about HR
> policies and procedures, about how to improve their career, and about
> how to define learning pathways.+++**

![](./media/image11.png)

7.  Copilot Studio에서 요청하면 사용자 지정 에이전트의 이름을 "Agentic
    HR"로 지정하세요. 다음 프롬프트를 사용하세요.

+++Name it as Agentic HR+++

![](./media/image12.png)

8.  그런 다음 Copilot Studio에 다음 지침을 사용하여 특정 작업이나 목표를
    지정하도록 지시합니다:

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![](./media/image13.png)

9.  그런 다음 에이전트에 대한 전문적인 톤을 정의하고 다음 입력을
    제공하십시오:

**+++It should have a professional tone+++**

![](./media/image14.png)

10. 에이전트에 대한 설명이 끝나면 **Create** 명령을 선택하여 실제
    에이전트를 만듭니다.

![](./media/image15.png)

![](./media/image16.png)

## 연습 3: Microsoft 365 Copilot Chat에 에이전트 게시하기

1.  에이전트 개요 페이지에서 **Publish**를 선택합니다.

![](./media/image17.png)

2.  **Publish agent**화면에서 **Publish**를 선택합니다.

![](./media/image18.png)

> ![](./media/image19.png)

3.  Select **Copy** under **Share link** to copy the link and then
    select **Done**.

![](./media/image20.png)

4.  Open a new tab and paste the copied url. Select **Add** to add the
    **Agentic HR** to your list agents.

![](./media/image21.png)

![](./media/image22.png)

5.  Select **Skip** in the introduction screen.

![](./media/image23.png)

6.  The **Agentic HR** agent is now added.

![](./media/image24.png)

## Exercise 4: Create SharePoint site

1.  In a new browser, navigate to
    +++https://m365.cloud.microsoft/chat/+++ Select **Apps** from the
    left pane and then select **SharePoint** once the Apps are loaded.

> ![](./media/image25.png)

2.  Select **+ Create** site from the SharePoint page.

![](./media/image26.png)

3.  Select **Communication** site from the **Select the site type**
    page.

![](./media/image27.png)

4.  Select a **template** to be used.

![](./media/image28.png)

5.  Select **Use template**.

![](./media/image29.png)

6.  Enter +++**Contoso site+++** as the **Site name** and select
    **Next.**

![](./media/image30.png)

7.  In the next screen, select **Create site**.

![](./media/image31.png)

8.  Once created, note down the **url** of this site.

![](./media/image32.png)

9.  Select **Documents** from the menu bar. Select **Upload -\> Files**

![](./media/image33.png)

10. Select **Sample-list-of-candidates.xlsx** file from **C:\LabFiles**
    to be uploaded.

![](./media/image34.png)

## Exercise 5: Adding an action to the agent

In this exercise you are going to add a custom action to the agent that
you made. In Microsoft Copilot Studio, when making agents for Microsoft
365 Copilot Chat, you can add four different types of actions:

- New prompt: allows consuming an AI action built using a prompt written
  in natural language.

- New Power Automate flow: allows consuming a Power Automate flow.

- New custom connector: allows consuming a Power Platform custom
  connector.

- New REST API: allows consuming an external REST API..

1.  To add a new action, select **+ Add action** in
    the **Actions** section of the agent's configuration panel.

![](./media/image35.png)

2.  Select **List rows present in a table**(Excel online) option and
    select **Next.**

![](./media/image36.png)

![](./media/image37.png)

3.  In the **List rows present in a table** screen, provide the below
    details and select **Add action**.

Name - +++List HR candidates+++

Description – +++List candidates for HR role+++

![](./media/image38.png)

![](./media/image39.png)

4.  Once the action is added, click on it to open and edit it.

![](./media/image40.png)

5.  Select the **Inputs** section.

![](./media/image41.png)

6.  Select **Set as a value** under **How will the agent fill this
    input** for each of the input argument.

![](./media/image42.png)

7.  Select **Confirm** in changing the input settings dialog.

![](./media/image43.png)

![](./media/image44.png)

8.  Provide the below values for each input.

**Location** – The Contoso site url that you saved in the earlier
exercise.

Document Library – +++**Documents**+++

File – +++**Sample-list-of-candidates.xlsx**+++

Table – +++**Candidates_Table**+++

![](./media/image45.png)

![](./media/image46.png)

![](./media/image47.png)

9.  Once all the updates are done, select **Save**.

![](./media/image48.png)

![](./media/image49.png)

10. Select **Publish** to publish the agent.

![](./media/image50.png)

11. Select **Publish** again.

![](./media/image51.png)

12. **Copy** the url and **open** it from a browser.

![](./media/image52.png)

13. This time, it will give an option to **Update now** since it is
    already added. Select it.

![](./media/image53.png)

14. Select **Open** once it is updated.

![](./media/image54.png)

15. In the Agentic HR agent screen, send the below message.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image55.png)

16. In the Data to be shared with Agentic HR message, select **Allow
    once** option.

![](./media/image56.png)

17. If it asks you to sign in, select the **Sign in to Agentic HR**
    option and then select **Connect** in the next screen.

![](./media/image57.png)

![](./media/image58.png)

18. Select **Submit** once connected.

![](./media/image59.png)

![](./media/image60.png)

19. Now, resend the below message to the agent.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image61.png)

20. You will then receive the requested list

![](./media/image62.png)

![](./media/image63.png)

## Summary

In this lab, you have successfully learnt, how to use custom connectors
in Copilot Studio.
