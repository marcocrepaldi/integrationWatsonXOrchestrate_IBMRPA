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
       




14.2- click on Skills layer.




14.3 – Click on Add Skill button.
 




14.4 – Click on From a File.
 
















14.5 – "Import the file integrating_wxo and ibmrpa-openapi.yml", wait for the green check mark and click next button.







14.6 – Select the 3 skills and click on the Add button.







14.7 – In the Project_Step01 skill, click on the edit options.




14.8 – Click on the “Enchance this skill” option.







14.9 – Click on Input layer.
 




14.10- Enter the line number and check the required option and click Publish button.




14.11- In the Project_Client_management_bot, click on the edit options.

14.12-  Click on the “Enchance this skill” option.




14.13 – Click on the publish Button







14.14 - In the Project_Services_Management_Bot, click on the edit options.










14.15 - Click on the “Enchance this skill” option.




14.16 – Click on the Publish Button










14.17 – The three skills need to be published.







14.18- In the left sidebar menu, click on Skill catalog.







14.19 - Locate your main skill that contains the three skills and click on it.




14.20 - Click on Add Skill + for the three skills and then click on Connect app.







14.21 –Please provide the username and password for the control center connection and click on the Connect app button.




14.22 – In the left sidebar menu, click on Skill and Apps.







14.23 – Click on the options of the Add Skills button and select the Create a skill flow option.




14.24 – Click on the pencil icon to name the Skill Flow.







14.25 - Enter a name for the skill flow, a description, and then click on the Save button.







14.26 – Click on the icon to add a skill.













14.27 - Select the app Integrating WxO and IBM RPA.







14.28 –Click on the 'add skill +' button for the skill Project_Step01.
















14.29- Click on the icon to add a second skill.







14.30 - Select the app Integrating WxO and IBM RPA.










14.31 - Click on the 'add skill +' button for the skill Project_Client_management_bot.




14.32 – Click on the Skill to display the configuration options.
















14.33 - For all inputs of the bot Project_client_management, it is necessary to specify the source of the data coming from the output of the script Project_management_Step001,You can manually enter each of the parameters or click the 'Generate Mapping Suggestion' button.The first input in the 'City' field will be done manually. Click on the 'City' field, then select the data source'Project_Step01'."




14.34 -Select variable city










14.35 - For the remaining parameters, let's follow the filling suggestion from Watsonx Orchestrate. Click on 'Generate mapping suggestions'. When the filling is completed, a success message will be displayed.







14.36 - Confirm if all parameters have been filled correctly. If necessary, adjust manually.







14.37 - Let's add a new skill. Click on the plus icon.







14.38 - Select the app Integrating WxO and IBM RPA.




14.39 - Click on the 'add skill +' button for the skill Project_Services_Management_bot.







14.40 - Click on the skill to perform the mapping
 
















14.41 - Click on 'Generate mapping suggestions (item 14.31)

14.42- Click on the options of the Actions button and select Enhance.

14.43 – Click on the Save an Close button

 14.44 - Now, let's publish the skill flow 'Client and Service Registration.' Click on the 'Publish' button.






















14.45 - Now, let's add the skill to the catalog, On the left-hand side menu, click on 'Skill Catalog.'.




14.46 – Find to Skill flow and click
 

14.47 – Click on the Add Skill + Button




14.48 - On the left-hand side menu, click on 'Chat.'.










14.49 - Now, your skill flow is available in the chat. Click to interact using the shortcut or engage in the chat. Click on the Client and Service Registration skill.




14.50- Fill in the input line. This input requests which line of the data.csv table will be registered. The table currently has a total of 2 lines, but you can insert more records.Click on the Apply button.




14.51 - The records will be displayed in the form. You can confirm or edit these values. To proceed to the next skill, click the 'Apply' button.




Congratulations on successfully integrating Watsonx Orchestrate with IBM RPA! Now that the integration is complete, you have the opportunity to enhance the project by integrating error-handling routines in the IBM RPA scripts, creating interaction phrases for chat communication, customizing the display fields in the chat, and more. If you have any questions, feel free to reach out for assistance.





