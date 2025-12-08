# Analysing a contract and generating results for key terms
In this tutorial we will learn how to create a ChatGPT agent that can extract key terms.

## Pre-requisites
1. ChatGPT subscription

### Now lets move on to creating the Agent itself.

Lets go through this step by step.

1. Click on this [link](https://chat.openai.com/g/g-POb5UhhJ6-autogpt-agent) and it will take you to the Agent creation page of ChatGPT
2. After logging in/signing up, you will be prompted to buy subscription. This is what it looks like.
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/aeaaac7a-6355-4b34-a856-b1154c2b3dd9)

   Buy the Plus plan if you want to use it for individual learning, else if you want to share you models with you team/work you need to buy the Team plan.
3. Click on the Explore GPT option
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/70e348c1-d34c-4240-acaa-dbf483d66315)
4. This is the page you will land in
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/2b18876e-dd6c-4919-98c6-810642ca5dec)

   Click on the Create button to create a new Agent.
5. You will be brought here.
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/9a3b9920-8d8d-4158-bdb8-60ac2b2fa99e)

   This is where the real stuff will happen.
6. If you notice you have two tabs as Create and Configuration.
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/730d1efb-83f2-4563-b989-1a81e52f2cab)

   Create tab can be used to set up the agents using prompting. For example: This is the prompt we will use "you are an professional lawyer who's job is to analyse uploaded contracts and generate answers to key terms also use actions to store the answers in a CRM."
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/a09ccdaa-afbf-4cd5-a2c5-7b433dc1f35c)

   You will see that the Agents has been auto configured and is set for minimal use
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/81853f3b-8370-4863-9b3c-f0bc5611c3b0)

  Also if you switch to the configuration tab the fields have been populated without the need to perform manual configuration
  ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/acb919a0-e6f9-468f-bb45-f915b586cc79)

7. So, in our case we did the entire process manually, using the configuration tab. Here's how we did it.
```
  Name: Workshop101
  Description : This agent analyzes contracts, extracts key terms, and stores them to a CRM.
  ```
  The Instructions we procvided was large and needs to be very detailed for the agent to funciton properly.
  ```
You are a legal agent whose job is to analyze a contract and get answers to the key terms mentioned below in square brackets:
Also remember that the Contract Name is the file name itself.
[Contract Name
Service Provider Name
Customer Name
Contract start date
Contract end date]

After getting the results for these key terms, display them in a tabular format with column names as key terms and the rows containing the value for each of these key terms.
 Once the table is generated, call the appropriate action created to save these results to a CRM.
```
You can also add Conversation starters that the users can use.

We have our conversation starters as:
![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/f88241f7-dcc0-44f3-af9b-7e6c691b3402)

This is what the initial setup looks like:
![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/9a64cdc5-a06c-46d8-aff9-285a8f69c81d)


8. Now, go back to the Configuration page. As all the set up is now complete, we will test our agent.

## Testing/Output
### You can try our document to test your Agent: [Click here](https://drive.google.com/file/d/112lxc2jOhz4PMdkk0AoLRuS5ek3FAzHh/view?usp=sharing) to get the document and click on this button
![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/fef2ef17-a820-42a8-afec-072fc237e6a4)

1. First we will upload a contract that we want to analyse. Click on the button circled in red.
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/9686e740-f76a-4e59-95a4-81f08bac34a1)


2. We have uploaded a Master Service Agreement and given it a simple instruction on what to do.
   #### Input Prompt that we will provide
   ```
   Analyse the document and find the
   Contract Name,
   Service Provider Name,
   Customer Name,
   Contract start date,
   Contract end date
   ```
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/c6405e7e-1017-4f0d-9c6c-26bd7b959cba)

   Hit Enter

   The Contract will be analysed and the answer to the key terms will be generated in a tabular format as we have explicitly mentioned it in the instruction while configuring the agent.
   ![image](https://github.com/initmahesh/MLAI-community-labs/assets/72710483/19f9e346-ee41-4d22-bfab-cd452f642e1c)





