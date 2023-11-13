# Lab 1 - Resource PRovisioning

In this lab, you'll create an OCI Digital Assistant and other OCI AI services, then you'll craete an skill, with this skill and the other AI Services you'll be able to detect languages from the user input, and validate discount vouchers uploaded by customers by performing mage and text recognition.

These services are provided by Oracle Cloud Infrastructure (OCI) Language and Oracle Cloud Infrastructure (OCI) Vision AI services, respectively. While these services have SDKs for a number of different languages, including Java, Python, JavaScript, and .NET, the easiest way to integrate these services into the conversation is through their REST Service APIs.

To enable the pizzeria skill to access the endpoints for these services within the OCI environment, you need to apply for the appropriate security policy within your OCI Tenancy.

Once you gain access to these services, you'll incorporate them into the REST connector capability in Oracle Digital Assistant.
___

**Step 1: Granting Access to OCI AI services**
1. Open the OCI Console and navigate to **Analytics & AI** > **AI Services** > **Digital Assistant**

![](/images/lab1-resourceprovisioning-1.png)

2. In the Compartment Dropdown list, select the compartment where you want to create the resources.

![](/images/lab1-resourceprovisioning-2.png)

3. Click on **Create digital assistant instance** and fill the form with and click on **Create**:

- **Compartment**: *Your compartment name*
- **Name**: *Your OCI Digital Assistant instance name*
- **Description**: *(Optional) Any description*
- **Shape**: *¨For this lap, you can use a Development instance*

![](/images/lab1-resourceprovisioning-3.png)

5. 
