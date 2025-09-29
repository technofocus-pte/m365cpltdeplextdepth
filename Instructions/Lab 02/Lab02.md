# Lab 02 - Create and configure an agent in Microsoft 365 Copilot chat

**Objective**

In this lab you will create and configure a Copilot agent using the
Describe and Configure tabs.

You will use Copilot Studio Agent Builder:

- Create an agent using the Describe and Configure tabs in Copilot
  Studio Agent Builder

    **Note**: The availability of the **Describe** tab is based
    on [**geographic availability and language
    support**](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build).
    If the **Describe** tab isn't supported in your region or preferred
    language, you can manually build your agent through
    the **Configure** tab.

- Customize agent instructions, knowledge source and starter prompts.

- Test and edit your agent.

- Manage and share your agent within your organization.

## Exercise 1: Create a Copilot Agent Using the Describe Tab

In this exercise you will use the Describe tab in Copilot Studio to
create a basic agent.

1.  Open a Microsoft Edge browser and enter the following URL:
    ++https://m365.cloud.microsoft++ to
    go to the **Microsoft 365 Copilot app** (formerly office) home page.

    **Note**: You need to sign-in (if prompted) using
    the **Credentials** provided under the **Resources** tab on the right.

2.  **Copilot Chat** page will open.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image1.png)

3.  If, for some reason, “**Something went wrong”** message appears,
    click **Try again** (twice) to open Copilot app.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image2.png)

    **Note**: Copilot Chat user interface may appear different when you
    are executing this lab (since Microsoft has rolled out new and updated
    features along with UI changes as part of Microsoft Build-2025
    event). 

4.  From the left side of the screen, click on **Create an agent**.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image3.png)

5.  Copilot Studio Agent Builder will open.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image4.png)

6.  In the **Describe tab**, enter the description of the agent's
    purpose in natural language description and then press **Enter**
    button

    ++**An agent that assists users in finding popular learning paths and
    modules from Microsoft**++.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image5.png)

7.  A draft agent with initial configurations set will get auto saved.
    Review the auto-generated fields and make necessary adjustments. In
    this exercise you will use the auto-generated fields as-is.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image6.png)

8.  You will be prompted to confirm or suggest a name for the agent.
    Enter ++assign the name as LearnAssist Buddy++ and then click on
    the **Enter** button.

    ![A screenshot of a chat AI-generated content may be
    incorrect.](./media/image7.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image8.png)

9.  You have now created an agent with basic details. You will be
    prompted to refine the instructions for the agent and make necessary
    adjustments. In this exercise you will use the default settings to
    expedite the creation process.

    ![Screens screenshot of a chat AI-generated content may be
    incorrect.](./media/image9.png)

## Exercise 2: Configure Agent Details Using the Configure Tab

In this exercise you will configure agent settings to fine-tune its
behavior.

**Note**: If you are creating an agent from Configure Tab directly, then
you need to define the agent's name, description, and purpose.

1.  Switch to the **Configure** tab in the Agent Builder.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image10.png)

2.  You can configure the agent's behavior settings, including response
    tone and interaction style. In this exercise you will proceed with
    the default instructions.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image11.png)

3.  You will now set up the knowledge sources the agent will use, such
    as specific SharePoint sites, document libraries, and web sites. In
    this exercise you will use a website as knowledge source to ground
    the agent responses.

    Populate ++<https://learn.microsoft.com/en-us/training++> and hit
    enter.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image12.png)

    **Note**: The website URL can’t be more than two levels deep. Also,
    the agent will search public websites if you don’t add a URL, and you
    turn web search on.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image13.png)

4.  The configuration changes will be auto saved.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image14.png)

5.  You have now completed configuring agent with customized settings
    tailored to your organization's needs. You will now ensure the agent
    functions as intended and make necessary adjustments.

## Exercise 3: Testing and Editing the Agent

You will now test whether the agent responds based on the configuration
settings.

1.  You will now input the following prompt to assess the agent's
    response.

    ++**List the popular learning paths and modules offered by
    Microsoft**++.

    ![Screens screenshot of a computer AI-generated content may be
    incorrect.](./media/image15.png)

2.  You can check the response by comparing it with the information
    available in the URL entered used as knowledge source.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image16.png)

3.  You can also test the response by entering some irrelevant prompt.

    ++**Help me with instructions for baking cakes**++

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image17.png)

    The agent avoided providing answer based on the instruction “Avoid
    discussing topics unrelated to Microsoft learning paths and modules”.

    **Note**: The default instruction set in your case may be different.
    Please ensure that the instructions are properly configured to make
    the agent avoid providing the answer.

4.  Return to the **Configure tab** to edit the agent's settings,
    instructions, or knowledge sources as needed.

5.  Once you are satisfied, click **Create** on the top right to publish
    the agent.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image18.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image19.png)

6.  Your LearnAssist Buddy agent is successfully created.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image20.png)

## Exercise 4: Managing and Sharing the Agent

You will now deploy the agent within your organization and manage its
accessibility.

1.  Share the agent with specific users or groups by setting appropriate
    permissions.

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image21.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image22.png)

2.  Make iterative improvements based on user feedback and performance
    metrics.

**Try yourself:**

- Create an agent “Product Buddy” to get product details.

- Map the knowledge source to document library that you created in “Lab
  0 - Preparing for lab execution”

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image23.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image24.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image25.png)

    ![A screenshot of a computer AI-generated content may be
    incorrect.](./media/image26.png)

- Test the agent by asking relevant product related prompts to check its
  functioning.

**Summary:**

You have now completed creating agents mapped with different knowledge
sources and instruction sets to get the expected responses from the
agents.
