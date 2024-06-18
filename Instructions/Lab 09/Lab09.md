# Lab 09: Create AI plugin actions for Microsoft Copilot (Preview)

## Objective:

AI Plugins can be used to extend Microsoft Copilot, or used within a
custom copilot as a plugin action. In this lab, we will learn about
creating different types of AI Plugins.

The Plugins will be available in the Microsoft Copilot in production, if
the organization has valid license for the same.

## Exercise #1: Generate content or extract insights with AI Builder dynamic prompts

1.  Login to +++**https://copilotstudio.microsoft.com/**+++ using your
    tenant credentials if not already logged in.

2.  Select **Library** on the side navigation pane. Select **+ Add an
    item**.

![](./media/image1.png)

3.  Select **Copilot for Microsoft 365** in the **Which Copilot would
    you like to extend? (preview)** dialog.

![](./media/image2.png)

4.  Select **Prompt** in the New action menu that appears.

![](./media/image3.png)

5.  Name it as +++**Dynamic prompt**+++. Select **Summarize text**.

![](./media/image4.png)

6.  It will add a prompt with a dynamic value **input text**.

![](./media/image5.png)

7.  Click on the **Input** under Prompt Settings add the below content
    in the Sample data.
```
Meet comfortably and confidently with customizable meeting views

The meeting stage, or gallery, is at the core of the virtual meeting
experience and can either hinder or enhance meeting efficiency
depending on your needs. We’re excited to share how we’re evolving the
default gallery experience in Teams meetings to give you a simpler,
more predictable meeting presence—while enabling more controls that
let you personalize the view to suit your preferences.

First, let’s look at the new default gallery experience that will be
applicable to all. The new gallery will place everyone in tiles of
equal size (16:9 ratio) whether their video is turned on or off.
Additionally, the new default gallery layout will be more consistent
and predictable for all meetings, regardless of size and content
shared.

And when a Teams Room joins the meeting, the video of the room
automatically enlarges, bridging the gap between remote and in-room
participants. Remote attendees enjoy a clearer view and better
connection, easily spotting who is speaking. Want a custom view?
Simply tweak the tile size to your preference from the more options
(...) menu by hovering on the room name. It's seamless, inclusive, and
ensures everyone can be seen, no matter where they are.

Next, let’s look at the controls that help you customize every
meeting view to suit your needs.

While the default gallery size for meetings will be 16 participants,
you can customize the number of participants visible on your screen to
best fit your preference. You can choose from 4, 9, 16, and 49
participants visible on the screen for gallery size.

There are still a few default configurations that AI will optimize
for to improve engagement and efficiency. For virtual participants,
these are prioritizing those that have a raised hand and prioritizing
the active speaker, enhancing their visibility so comments are not
missed.
```
![](./media/image6.png)

8.  Click on **Test prompt**.

> ![](./media/image7.png)

9.  Notice that the Prompt response, summarizing the text is generated.

> ![](./media/image8.png)

10. Click on **Finalize prompt**.

![](./media/image9.png)

11. Click on **Create prompt action**.

![](./media/image10.png)

12. It gets listed in the **Library.**

13. After you create your action, enable it for use in Microsoft
    Copilot.

## Exercise \#2: Create Custom automation with Power Automate flows

Power Automate flow plugins let you define flows that can be called from
AI surfaces in Power Platform. Flow plugins use the new **Run from
Copilot** trigger and **Respond to Copilot** action to define custom
processes that can be invoked with natural language.

**To create automation plugins:**

1.  Select **+ Add action**. Select **Flow** in the New action menu that
    open up.

![](./media/image11.png)

2.  The flow editor automatically opens with the **Run from
    Copilot** trigger and **Respond to Copilot** action present. Rename
    the flow as +++**Get Weather forecast for next day**+++

![](./media/image12.png)

3.  Click on the **Run a flow from Copilot** node. The details pane
    opens up. Click on **+ Add an input**.

![](./media/image13.png)

4.  Select Text and name it as **City**.

5.  Similarly, add another input of type **Number** and name it as
    **Zipcode**.

![](./media/image14.png)

6.  Click on the **+** symbol between **Run a flow from Copilot** and
    the **Respond to Copilot** nodes and select **Add an action**.

![](./media/image15.png)
7.  Select **MSN Weather**.

![](./media/image16.png)

8.  Select **Get the forecast for tomorrow** option.

![](./media/image17.png)

9.  Add the **City** and **Zipcode** input parameters to **Location**.

![](./media/image18.png)

![](./media/image19.png)

10. Click on **Respond to copilot** action and select **Add an output**.

11. Add a Text output variable and name it as +++**Weather
    condition**+++. Add the output variable **Conditions**.

![](./media/image20.png)

12. Click on **Save**.

![](./media/image21.png)

13. Click on **Test**.

![](./media/image22.png)

**Note:** This might take some time to get reflected. Wait for 5 to 10
minutes if you are not able to start the flow after clicking on
**Test**.

14. In the **Test Flow** pane, select the checkbox for **Manually** and
    then click on **Next**.

![](./media/image23.png)

15. In the **Run flow** panel, select **MSN Weather** and click on
    **Continue**.

![](./media/image24.png)

16. Enter +++**Redmond**+++ for city and +++**98004**+++ for **Zipcode**
    and select **Run flow**.

![](./media/image25.png)

17. Once the execution is completed, a success message is obtained.
    Click on **Done**.

![](./media/image26.png)

**Note:** The AI uses the title and description of the flow to determine
when to invoke the flow plugins. Ensure your flows run correctly, as
only tested flows show up as available plugins in Microsoft Copilot.

18. The created flow is listed in the **Library**.

![](./media/image27.png)

19. After you create your action, enable it for use in Microsoft
    Copilot.

## Summary:

In this lab, we have learnt to create **AI actions**.
