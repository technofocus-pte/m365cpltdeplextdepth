# Lab 17: Creating AI plugin actions for Microsoft Copilot (preview)

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

<img src="./media/image1.png" style="width:6.5in;height:4.76528in" />

3.  Select **Copilot for Microsoft 365** in the **Which Copilot would
    you like to extend? (preview)** dialog.

<img src="./media/image2.png" style="width:6.5in;height:4.11875in"
alt="A screenshot of a computer Description automatically generated" />

4.  Select **Prompt** in the New action menu that appears.

<img src="./media/image3.png" style="width:6.5in;height:2.16667in"
alt="A screenshot of a computer Description automatically generated" />

5.  Name it as +++**Dynamic prompt**+++. Select **Summarize text**.

<img src="./media/image4.png" style="width:6.5in;height:3.55764in"
alt="A screenshot of a chat Description automatically generated" />

6.  It will add a prompt with a dynamic value **input text**.

> <img src="./media/image5.png" style="width:6.5in;height:3.30139in"
> alt="A screenshot of a computer Description automatically generated" />

7.  Click on the **Input** under Prompt Settings add the below content
    in the Sample data.

> **Meet comfortably and confidently with customizable meeting views**
>
> **The meeting stage, or gallery, is at the core of the virtual meeting
> experience and can either hinder or enhance meeting efficiency
> depending on your needs. We’re excited to share how we’re evolving the
> default gallery experience in Teams meetings to give you a simpler,
> more predictable meeting presence—while enabling more controls that
> let you personalize the view to suit your preferences.**
>
> **First, let’s look at the new default gallery experience that will be
> applicable to all. The new gallery will place everyone in tiles of
> equal size (16:9 ratio) whether their video is turned on or off.
> Additionally, the new default gallery layout will be more consistent
> and predictable for all meetings, regardless of size and content
> shared.**
>
> **And when a Teams Room joins the meeting, the video of the room
> automatically enlarges, bridging the gap between remote and in-room
> participants. Remote attendees enjoy a clearer view and better
> connection, easily spotting who is speaking. Want a custom view?
> Simply tweak the tile size to your preference from the more options
> (...) menu by hovering on the room name. It's seamless, inclusive, and
> ensures everyone can be seen, no matter where they are.**
>
> **Next, let’s look at the controls that help you customize every
> meeting view to suit your needs.**
>
> **  
> While the default gallery size for meetings will be 16 participants,
> you can customize the number of participants visible on your screen to
> best fit your preference. You can choose from 4, 9, 16, and 49
> participants visible on the screen for gallery size.**
>
> **There are still a few default configurations that AI will optimize
> for to improve engagement and efficiency. For virtual participants,
> these are prioritizing those that have a raised hand and prioritizing
> the active speaker, enhancing their visibility so comments are not
> missed.**
>
> <img src="./media/image6.png" style="width:6.5in;height:3.60903in" />

8.  Click on **Test prompt**.

> <img src="./media/image7.png" style="width:6.5in;height:3.55347in" />

9.  Notice that the Prompt response, summarizing the text is generated.

> <img src="./media/image8.png" style="width:6.5in;height:3.64306in"
> alt="A screenshot of a computer Description automatically generated" />

10. Click on **Finalize prompt**.

<img src="./media/image9.png" style="width:6.5in;height:3.65556in"
alt="A screenshot of a computer Description automatically generated" />

11. Click on **Create prompt action**.

<img src="./media/image10.png" style="width:6.5in;height:3.5375in"
alt="A screenshot of a computer Description automatically generated" />

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

<img src="./media/image11.png" style="width:6.5in;height:2.79028in"
alt="A screenshot of a computer Description automatically generated" />

2.  The flow editor automatically opens with the **Run from
    Copilot** trigger and **Respond to Copilot** action present. Rename
    the flow as +++**Get Weather forecast for next day**+++

<img src="./media/image12.png" style="width:6.5in;height:3.11458in"
alt="A screenshot of a computer Description automatically generated" />

3.  Click on the **Run a flow from Copilot** node. The details pane
    opens up. Click on **+ Add an input**.

<img src="./media/image13.png" style="width:6.5in;height:3.21528in"
alt="A screenshot of a computer Description automatically generated" />

4.  Select Text and name it as **City**.

5.  Similarly, add another input of type **Number** and name it as
    **Zipcode**.

<img src="./media/image14.png" style="width:6.5in;height:3.25556in"
alt="A screenshot of a computer Description automatically generated" />

6.  Click on the **+** symbol between **Run a flow from Copilot** and
    the **Respond to Copilot** nodes and select **Add an action**.

> <img src="./media/image15.png" style="width:3.37529in;height:2.6919in"
> alt="A screenshot of a computer Description automatically generated" />

7.  Select **MSN Weather**.

<img src="./media/image16.png" style="width:5.15878in;height:5.32546in"
alt="A screenshot of a computer Description automatically generated" />

8.  Select **Get the forecast for tomorrow** option.

<img src="./media/image17.png" style="width:6.35055in;height:4.77541in"
alt="A screenshot of a weather forecast Description automatically generated" />

9.  Add the **City** and **Zipcode** input parameters to **Location**.

<img src="./media/image18.png" style="width:4.01701in;height:4.1837in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image19.png" style="width:6.5in;height:3.28611in"
alt="A screenshot of a computer Description automatically generated" />

10. Click on **Respond to copilot** action and select **Add an output**.

11. Add a Text output variable and name it as +++**Weather
    condition**+++. Add the output variable **Conditions**.

<img src="./media/image20.png" style="width:6.5in;height:3.56944in"
alt="A screenshot of a computer Description automatically generated" />

12. Click on **Save**.

<img src="./media/image21.png" style="width:4.20036in;height:5.37547in"
alt="A screenshot of a computer Description automatically generated" />

13. Click on **Test**.

<img src="./media/image22.png" style="width:4.75041in;height:5.36713in"
alt="A screenshot of a computer Description automatically generated" />

**Note:** This might take some time to get reflected. Wait for 5 to 10
minutes if you are not able to start the flow after clicking on
**Test**.

14. In the **Test Flow** pane, select the checkbox for **Manually** and
    then click on **Next**.

<img src="./media/image23.png" style="width:3.48364in;height:5.41714in"
alt="A screenshot of a phone Description automatically generated" />

15. In the **Run flow** panel, select **MSN Weather** and click on
    **Continue**.

<img src="./media/image24.png" style="width:3.51697in;height:5.35046in"
alt="A screenshot of a phone Description automatically generated" />

16. Enter +++**Redmond**+++ for city and +++**98004**+++ for **Zipcode**
    and select **Run flow**.

<img src="./media/image25.png" style="width:3.51697in;height:5.3588in"
alt="A screenshot of a computer Description automatically generated" />

17. Once the execution is completed, a success message is obtained.
    Click on **Done**.

<img src="./media/image26.png" style="width:3.49197in;height:5.4088in"
alt="A screenshot of a phone Description automatically generated" />

**Note:** The AI uses the title and description of the flow to determine
when to invoke the flow plugins. Ensure your flows run correctly, as
only tested flows show up as available plugins in Microsoft Copilot.

18. The created flow is listed in the **Library**.

<img src="./media/image27.png" style="width:5.0171in;height:5.26712in"
alt="A screenshot of a computer Description automatically generated" />

19. After you create your action, enable it for use in Microsoft
    Copilot.

## Summary:

In this lab, we have learnt to create **AI actions**.
