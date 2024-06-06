Introduction

Automating System Registrations with WatsonX Orchestrate and IBM RPA

In the modern corporate environment, process automation is essential for increasing efficiency and reducing human errors. A practical example is the integration between WatsonX Orchestrate and IBM Robotic Process Automation (RPA), which facilitates the registration of employees, products, invoices, among others. In this article, we will explore a detailed scenario of this integration and how it can benefit companies.

Imagine a company with an extensive list of employees in a table. This table may include registration information, products, issued invoices, etc. The manual task of entering this data into various administrative systems is tedious and prone to errors. This is where WatsonX Orchestrate and IBM RPA come into play.

Scenario


Automatic Employee Registration


1. Process Initiation by the User

   - The user initiates WatsonX Orchestrate and communicates via the integrated chat, indicating the intention to register a new employee.

   - The system displays a dialogue asking the user to specify which row of the table they want to register. In this example, the row can be identified by a number from 1 to 3, representing the employee's ID or a process number.


2. Chat Interaction

   - The user responds to the chat request, providing the row number they want to register.


3. Action by WatsonX Orchestrate

   - WatsonX Orchestrate triggers a specific Skill to execute an automation BOT from IBM RPA.

   - This BOT is a published script that performs the registration task automatically, regardless of the administrative platform used by the company.

4. Workflow Execution

   - For this scenario, two different systems need to be updated with the employee's information.

   - A Workflow Skill was created to organize the execution of multiple Skills in WatsonX Orchestrate. This allows different IBM RPA bots to be triggered in sequence, where the execution of one bot depends on the successful completion of the previous one.


Integration Benefits


- Error Reduction:Automation minimizes common errors in manual processes, ensuring greater accuracy in information registration.

- Efficiency: With automation, processes that would take hours can be completed in minutes, freeing up employees for more strategic tasks.

- Scalability: The integration between WatsonX Orchestrate and IBM RPA allows the company to easily scale its operations by adding new bots and processes as needed.

- Flexibility: The Workflow Skill offers a flexible solution to organize and manage the execution of multiple automated tasks, adapting to different business needs.


Conclusion

Process automation using WatsonX Orchestrate and IBM RPA is a powerful solution for companies looking to increase operational efficiency and reduce errors. This employee registration scenario exemplifies how the integration of these tools can transform routine tasks into fast and precise processes. As technology advances, automation will become increasingly essential for business success.


Requirements

Access to Watson Orchestrate and IBM RPA environments

Repository


In this implementation, we will work with assets. You can download this example from the link below:

https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA

This repository contains all the scripts and files, as well as a detailed step-by-step guide.

Let's get started.

1       Download OpenAPI


13.1 - "Now, you should download the integration API, click on the blue button 'Download OpenAPI' on the top right of the screen.".

To integrate with WatsonX Orchestrate, you need to download the project's OpenAPI. In the detailed step-by-step guide, you will find all the instructions. If you are an advanced user, below are the steps for integration. If you are a beginner, I suggest following the detailed step-by-step guide.

![Screenshot 2024-06-06 at 09 55 23](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/d569903b-83a1-4a26-a153-f42bb9dfb1f1)



2       Creating the integration in WatsonX Orchestrate.


14.1- Login to Watsonx Orchestrate, enter the username and click on the Continue button.
       
![Screenshot 2024-06-06 at 09 56 30](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/7ca69feb-7d6e-44d6-a40f-d8c6ccf924c3)


14.2- click on Skills layer.
![Screenshot 2024-06-06 at 09 57 33](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/b5b23991-fc0d-47f9-a98c-49a55c46b059)



14.3 – Click on Add Skill button.
 ![Screenshot 2024-06-06 at 09 57 51](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/7a2de381-73f6-4266-a577-0b5278555965)



14.4 – Click on From a File.
 ![Screenshot 2024-06-06 at 09 58 06](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/8a2cadfb-d61e-4482-af31-5ce97ed06aa0)


14.5 – "Import the file integrating_wxo and ibmrpa-openapi.yml", wait for the green check mark and click next button.

![Screenshot 2024-06-06 at 09 58 39](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/c4d4f86f-2a72-45bb-884d-c3f19d9eb9cf)


14.6 – Select the 3 skills and click on the Add button.

![Screenshot 2024-06-06 at 09 59 02](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/dccc24e3-522a-4bd2-a39e-35b0c29b350c)



14.7 – In the Project_Step01 skill, click on the edit options.
![Screenshot 2024-06-06 at 09 59 21](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/3a68f2ea-6619-4e1e-a18c-b9378a7c33a9)


14.8 – Click on the “Enchance this skill” option.

![Screenshot 2024-06-06 at 09 59 50](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/142ec877-4ea4-46bd-890c-c94c86ae08d2)



14.9 – Click on Input layer.
 
![Screenshot 2024-06-06 at 10 00 08](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/bb5f4302-ce63-4c8a-9cd0-22fc56139809)


14.10- Enter the line number and check the required option and click Publish button.
![Screenshot 2024-06-06 at 10 00 29](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/e7037ff8-5b09-49c6-8216-bbc1057c6321)




14.11- In the Project_Client_management_bot, click on the edit options.
![Screenshot 2024-06-06 at 10 00 49](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/e536b823-bc49-485e-a32c-3d9f1a6a2a15)

14.12-  Click on the “Enchance this skill” option.
![Screenshot 2024-06-06 at 10 01 07](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/5ff08333-6b7d-49d5-9094-d15dbcefa56d)


14.13 – Click on the publish Button

![Screenshot 2024-06-06 at 10 01 20](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/700a6e7d-c683-4932-bdc2-f6ceedd573fb)



14.14 - In the Project_Services_Management_Bot, click on the edit options.
![Screenshot 2024-06-06 at 10 01 41](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/f5ad26f4-ef0e-43e3-8b33-4aa5d01c6158)



14.15 - Click on the “Enchance this skill” option.

![Screenshot 2024-06-06 at 10 02 05](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/1e3fe41b-9eb7-4bab-874a-f3c0edb9c4ae)



14.16 – Click on the Publish Button

![Screenshot 2024-06-06 at 10 02 25](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/2673cfa0-fdb2-4a1b-be2c-7b223a3634fa)


14.17 – The three skills need to be published.
![Screenshot 2024-06-06 at 10 02 40](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/15f076f7-35b3-45f2-8f31-66ed4dfd5e85)


14.18- In the left sidebar menu, click on Skill catalog.

![Screenshot 2024-06-06 at 10 03 06](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/7967ac19-5da2-4b7e-aba7-aadab59ca149)


14.19 - Locate your main skill that contains the three skills and click on it.
![Screenshot 2024-06-06 at 10 03 32](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/1a5e145a-36ef-41e4-b4e0-df1c83503355)


14.20 - Click on Add Skill + for the three skills and then click on Connect app.

![Screenshot 2024-06-06 at 10 03 54](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/d6b791e4-7293-4e30-b68f-66a8232a22e5)


14.21 –Please provide the username and password for the control center connection and click on the Connect app button.
![Screenshot 2024-06-06 at 10 04 20](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/97c7a550-0bb7-46a6-9ae0-c7562a5bf3f9)


14.22 – In the left sidebar menu, click on Skill and Apps.

![Screenshot 2024-06-06 at 10 04 37](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/01893998-3a86-4ecc-869d-00f0268bd4e7)



14.23 – Click on the options of the Add Skills button and select the Create a skill flow option.
![Screenshot 2024-06-06 at 10 05 00](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/f5b88c4e-7a24-4cd9-bd23-45a047c59a61)


14.24 – Click on the pencil icon to name the Skill Flow.
![Screenshot 2024-06-06 at 10 05 17](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/18bdcf43-0a26-45e4-8a67-dbbd474056ce)


14.25 - Enter a name for the skill flow, a description, and then click on the Save button.
![Screenshot 2024-06-06 at 10 05 47](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/82f51616-e1d2-4e17-bdc2-aef2ddbe1a2a)



14.26 – Click on the icon to add a skill.

![Screenshot 2024-06-06 at 10 06 04](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/a65aa79a-c99d-4e97-bf16-a7c2e65cf680)


14.27 - Select the app Integrating WxO and IBM RPA.
![Screenshot 2024-06-06 at 10 06 26](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/1a66028e-96ad-4e45-9a83-14a4f2fb919c)


14.28 –Click on the 'add skill +' button for the skill Project_Step01.
![Screenshot 2024-06-06 at 10 06 40](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/1924c39f-78f2-45f6-981e-3e976102b30a)


14.29- Click on the icon to add a second skill.
![Screenshot 2024-06-06 at 10 07 52](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/5a945ec1-0570-40ea-9f83-e4c03a3b54db)


14.30 - Select the app Integrating WxO and IBM RPA.
![Screenshot 2024-06-06 at 10 08 08](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/fa3b63b9-9888-4770-93bb-4c433f5f5604)


14.31 - Click on the 'add skill +' button for the skill Project_Client_management_bot.
![Screenshot 2024-06-06 at 10 08 32](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/91d02c87-fe38-4959-8f5d-c18e2ba8f9d5)



14.32 – Click on the Skill to display the configuration options.
![Screenshot 2024-06-06 at 10 08 44](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/32fb66b7-56d4-49e0-b4a3-92739d44292d)



14.33 - For all inputs of the bot Project_client_management, it is necessary to specify the source of the data coming from the output of the script Project_management_Step001,You can manually enter each of the parameters or click the 'Generate Mapping Suggestion' button.The first input in the 'City' field will be done manually. Click on the 'City' field, then select the data source'Project_Step01'."

![Screenshot 2024-06-06 at 10 09 01](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/70e4678a-9498-413e-8f8a-b0efe6426b07)



14.34 -Select variable city
![Screenshot 2024-06-06 at 10 09 18](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/570104aa-b2c2-4a07-b49d-2d338670528f)



14.35 - For the remaining parameters, let's follow the filling suggestion from Watsonx Orchestrate. Click on 'Generate mapping suggestions'. When the filling is completed, a success message will be displayed.
![Screenshot 2024-06-06 at 10 09 33](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/c388118e-1ef1-4e2d-9933-aac59687e400)



14.36 - Confirm if all parameters have been filled correctly. If necessary, adjust manually.
![Screenshot 2024-06-06 at 10 09 47](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/e1827ba7-6c56-4339-a162-ea6f911f00f2)


14.37 - Let's a![Uploading Screenshot 2024-06-06 at 10.10.02.png…]()
dd a new skill. Click on the plus icon.
![Screenshot 2024-06-06 at 10 10 19](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/a759adb3-ec7b-4549-8d44-e3038d8f5a5c)



14.38 - Select the app Integrating WxO and IBM RPA.
![Screenshot 2024-06-06 at 10 10 38](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/5737078b-5a0a-4068-bfd0-d591390a7b32)


14.39 - Click on the 'add skill +' button for the skill Project_Services_Management_bot.
![Screenshot 2024-06-06 at 10 10 55](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/909cab2f-bd32-4ae4-8408-749a61e20d36)



14.40 - Click on the skill to perform the mapping

![Screenshot 2024-06-06 at 10 11 10](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/953312d5-d705-41cf-836e-32f8a246aa0c)
 
 

14.41 - Click on 'Generate mapping suggestions (item 14.31)
![Screenshot 2024-06-06 at 10 11 56](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/8f135632-8820-433b-b167-25225fd788b5)

14.42- Click on the options of the Actions button and select Enhance.
![Screenshot 2024-06-06 at 10 12 15](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/db7e54a8-9af5-4f6f-a2f9-15d5bda7fd28)

14.43 – Click on the Save an Close button
![Screenshot 2024-06-06 at 10 12 29](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/978aa439-d5db-4d06-b1da-e7c31b76e6a2)

 14.44 - Now, let's publish the skill flow 'Client and Service Registration.' Click on the 'Publish' button.
![Screenshot 2024-06-06 at 10 12 43](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/b1939684-a64f-40d2-94f3-70f01c71c529)


14.45 - Now, let's add the skill to the catalog, On the left-hand side menu, click on 'Skill Catalog.'.
![Screenshot 2024-06-06 at 10 13 01](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/0b869e18-a820-4231-a459-3bb7491b8b42)


14.46 – Find to Skill flow and click
 ![Screenshot 2024-06-06 at 10 13 24](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/23351557-7eab-474d-a6ee-c3cc4764e2ff)


14.47 – Click on the Add Skill + Button
![Screenshot 2024-06-06 at 10 13 43](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/8cd0f079-de4f-4685-acab-5a4fe273e60e)


14.48 - On the left-hand side menu, click on 'Chat.'.
![Screenshot 2024-06-06 at 10 13 58](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/0dc04265-a8f2-4126-b970-ce12c17ff2dd)


14.49 - Now, your skill flow is available in the chat. Click to interact using the shortcut or engage in the chat. Click on the Client and Service Registration skill.
![Screenshot 2024-06-06 at 10 14 12](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/d248c4f8-9dbe-406e-8c41-0c0df73216dc)


14.50- Fill in the input line. This input requests which line of the data.csv table will be registered. The table currently has a total of 2 lines, but you can insert more records.Click on the Apply button.
![Screenshot 2024-06-06 at 10 14 34](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/87822d1d-58f2-4231-a1ab-aef3cd9c8d7d)


14.51 - The records will be displayed in the form. You can confirm or edit these values. To proceed to the next skill, click the 'Apply' button.
![Screenshot 2024-06-06 at 10 15 11](https://github.com/marcocrepaldi/integrationWatsonXOrchestrate_IBMRPA/assets/9463175/c31485d4-d382-4950-97e8-b70470719c9e)


Congratulations on successfully integrating Watsonx Orchestrate with IBM RPA! Now that the integration is complete, you have the opportunity to enhance the project by integrating error-handling routines in the IBM RPA scripts, creating interaction phrases for chat communication, customizing the display fields in the chat, and more. If you have any questions, feel free to reach out for assistance.





