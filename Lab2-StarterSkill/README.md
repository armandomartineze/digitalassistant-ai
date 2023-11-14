# Lab 2 - Create a starter Skill

In this lab you will import the Starter Skill and open the skill by clicking on the tile, then will explore the skill.

___
**Step 1: Import the Skill**

1. Download the skill, click in this link [Starter Skill](/cohere(1.0).zip) and click on Dowload:

![](/images/lab2-importskill-0.png)

2. From the Digital Assistant main page, open the ODA menu button on the top left, select **Development** > **Skills** > **Import Skill** from top right and select the file *cohere(1.0).zip*

![](/images/lab2-importskill-1.png)
  
5. Once the skill is imported, search the skill by name in the field text "Type in filter or pick from recents" and click on skill's name

6. In skill page, select the **Flows**, then select the **UnresolvedIntent**:

![](/images/lab2-importskill-2.png)

   this is a simple flow that will allow us to show how you can incorporate other AI services in Oracle Digital Assistant

7. Select the **SetVariablePrompt** state and take a look:

![](/images/lab2-importskill-3.png)

   the *Component* tab shows the variable name **promptStart** that is used.

8. The *Transitions* tab show the next transition to *callRestServiceCohere* state:

![](/images/lab2-importskill-4.png)

Click on a blank space in the flow to close the state properties.

9. Select the *callRestServiceCohere* state and see the configuration:

- **REST Service**: *Select an REST Service previously created*
- **Authentication Type**: *Autentication used to call this REST Service"
- **Endpoint**: *The REST Service endpoint"
- **Request Body**: *Look the variable that is used from the last state*

10. Click on **Transitions** tab and see the next one is *outputCohereAPI*

![](/images/lab2-importskill-5.png)

11. Click on any blank space on Flow page, then click on **outputCohereAPI**, choose the *Component* tab and see the *Messages* field, this state just print the text gotten from the REST Service call

![](/images/lab2-importskill-6.png)


