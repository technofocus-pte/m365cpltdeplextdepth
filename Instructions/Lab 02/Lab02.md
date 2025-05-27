# Lab 02 - Create and configure an agent in Microsoft 365 Copilot chat

## Objective

In this lab you will create and configure a Copilot agent using the
Describe and Configure tabs.

You will use Copilot Studio Agent Builder:

- Create an agent using the Describe and Configure tabs in Copilot
  Studio Agent Builder

**Note**: The availability of the **Describe** tab is based on [**geographic availability and language
support**] (https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build).
If the **Describe** tab isn't supported in your region or preferred language, you can manually build your agent through the **Configure** tab.

- Customize agent instructions, knowledge source and starter prompts.

- Test and edit your agent.

- Manage and share your agent within your organization.

## Exercise 1: Create a Copilot Agent Using the Describe Tab

In this exercise you will use the Describe tab in Copilot Studio to
create a basic agent.

1.  Open a Microsoft Edge browser and enter the following URL: +++https://www.office.com+++ to go to the **Microsoft 365 Copilot app** (formerly office) home page.

    **Note**: You need to sign-in (if prompted) using the **Credentials** provided under the **Resources** tab on the right.

2.  Select **Copilot Chat** in the left-hand navigation pane.

    **Note**: Sometimes the **Copilot chat** page will open by default. In that case go to step #4.

    ![](./media/image1.png)

3.  If, for some reason, “**Something went wrong”** message appears,
    click **Refresh** to open Copilot app.

    ![](./media/image2.png)

    ![](./media/image3.png)

4.  Click on **Create an agent**.

    ![](./media/image4.png)

5.  Copilot Studio Agent Builder will open.

    ![](./media/image5.png)

6.  In the **Describe tab**, enter the description of the agent's
    purpose in natural language description.

    In this exercise you will enter ++**An agent that assists users in finding popular learning paths and modules from Microsoft**++.

    ![](./media/image6.png)

7.  Click Submit to preview the draft agent.

8.  A draft agent with initial configurations set will get auto saved.
    Review the auto-generated fields and make necessary adjustments. In
    this exercise you will use the auto-generated fields as-is.

    ![](./media/image7.png)

9.  You will be prompted to confirm or suggest a name for the agent. In
    this exercise, assign the name as **LearnAssist Buddy.**

    ![](./media/image8.png)

    ![](./media/image9.png)

10. You have now created an agent with basic details. You will be
    prompted to refine the instructions for the agent and make necessary
    adjustments. In this exercise you will use the default settings to
    expedite the creation process.

    ![](./media/image10.png)

## Exercise 2: Configure Agent Details Using the Configure Tab

In this exercise you will configure agent settings to fine-tune its
behavior.

**Note**: If you are creating an agent from Configure Tab directly, then
you need to define the agent's name, description, and purpose.

1.  Switch to the Configure tab in the Agent Builder.

    ![](./media/image11.png)

2.  You can configure the agent's behavior settings, including response
    tone and interaction style. In this exercise you will proceed with
    the default instructions.

    ![](./media/image12.png)

3.  You will now set up the knowledge sources the agent will use, such
    as specific SharePoint sites, document libraries, and web sites. In
    this exercise you will use a website as knowledge source to ground
    the agent responses.

    Populate +++**https://learn.microsoft.com/en-us/training**+++ and hit enter.

    ![](./media/image13.png)

    ![](./media/image14.png)

    **Note**: The website URL can’t be more than two levels deep. Also, the agent will search public websites if you don’t add a URL, and you turn web search on.

    ![](./media/image15.png)

4.  The configuration changes will be auto saved.

    ![](./media/image16.png)

5.  You have now completed configuring agent with customized settings
    tailored to your organization's needs. You will now ensure the agent
    functions as intended and make necessary adjustments.

## Exercise 3: Testing and Editing the Agent

You will now test whether the agent responds based on the configuration
settings.

1.  You will now input the following prompt to assess the agent's response.

    ++**List the popular learning paths and modules offered by Microsoft**++.

    ![](./media/image17.png)

2.  You can check the response by comparing it with the information
    available in the URL entered used as knowledge source.

    ![](./media/image18.png)

3.  You can also test the response by entering some irrelevant prompt.

    ++**Help me with instructions for baking cakes**++

    ![](./media/image19.png)

    The agent avoided providing answer based on the instruction “Avoid discussing topics unrelated to Microsoft learning paths and modules”.

    **Note**: The default instruction set in your case may be different. Please ensure that the instructions are properly configured to make the agent avoid providing the answer.

4.  Return to the **Configure tab** to edit the agent's settings, instructions, or knowledge sources as needed.

5.  Once you are satisfied, click **Create** on the top right to publish the agent.

    ![](./media/image20.png)

    ![](./media/image21.png)

6.  Your LearnAssist Buddy agent is successfully created.

    ![](./media/image22.png)

## Exercise 4: Managing and Sharing the Agent

You will now deploy the agent within your organization and manage its
accessibility.

1.  Share the agent with specific users or groups by setting appropriate permissions.

    ![](./media/image23.png)

    ![](./media/image24.png)

2.  Make iterative improvements based on user feedback and performance metrics.


## Try yourself:

- Create an agent “Product Buddy” to get product details.

- Map the knowledge source to document library that you created in “Lab
  0 - Preparing for lab execution”

  ![](./media/image25.png)

  ![](./media/image26.png)

  ![](./media/image27.png)

  ![](./media/image28.png)

- Test the agent by asking relevant product related prompts to check its
  functioning.

## Summary:

You have now completed creating agents mapped with different knowledge
sources and instruction sets to get the expected responses from the
agents.
