# Lab 3 - Add and LLM capability with Cohere


In this lab you'll add an LLM Invoke capability through API Services in Oracle Digital Assistant

___

**Step 1: Get an Cohere account**

1. From ![Cohere Site](https://cohere.com/) get an account and create an API Key from account settings:

![](/images/lab3-coherellm-3.png)

___

**Step 2: Add an API Service**

1. Open the ODA menu button on the top left, select **Settings** > **API Services**

![](/images/lab3-coherellm-1.png)

2. Click on **Add REST Service** and fill the page with this information:

- **Name**: *Select a name for your API REST Service*
- **Endpoint**: *the Cohere API Enpoint* **https://api.cohere.ai/v1/generate** 
- **Description**: *Define any description for this service*
- **Methods**: *Select POST Method*

![](/images/lab3-coherellm-2.png)

   Click **Create**

3. On the new API REST Service created, you'll need to do some configuration:

- **Authentication Type**: Bearer Token
- **Token**: *Set the API Key get from Cohere account*
- **Request**: Use this one to test the service:
```
{
    "max_tokens": 20,
    "return_likelihoods": "NONE",
    "truncate": "END",
    "prompt": "Please explain to me how LLMs work"
}
```

![](/images/lab3-coherellm-4.png)

4. Click on **Test Request** and look the response:

![](/images/lab3-coherellm-5.png)

___

**Step 3: Modify the *Starter Skill* to use the Cohere API REST Service**


1. Open the ODA menu button on the top left, select **Development** > **Skills** > and select the **Cohere** Skill, then select the **Flows** page and select the *UnresolvedIntent*


2. Select the **callRestServiceCohere** state and then do these changes:
   
- **REST Service**: Select an REST Service previously created
- **Request Body**: Look the variable that is used from the last state
```
{
    "max_tokens": 20,
    "return_likelihoods": "NONE",
    "truncate": "END",
    "prompt": "${promptStart}"
}
```

![](/images/lab3-coherellm-6.png)


3. Click on any blank space from Flow's page, then click on **Preview**, type *Please explain to me how LLMs work* on text field and then *ENTER*. Look the response:

![](/images/lab3-coherellm-7.png)

