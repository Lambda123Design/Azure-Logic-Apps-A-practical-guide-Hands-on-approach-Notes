# Azure-Logic-Apps-A-practical-guide-Hands-on-approach-Notes
This Repository contains my Notes of "Azure Logic Apps - A practical guide ( Hands-on approach )" Course from Udemy

**Table of Contents:**

**I) Setting the Stage**

**A) Course Overview**

**B) Basics of Serverless Computing**

**C) Understanding Workflows**

**D) Why Logic Apps**

**E) Connectors, Triggers & Actions**

**F) Summary**

**II) Getting Hands Dirty**

**A) Overview**

**B) Create First Logic App**

**C) Behind the Scenes**

**D) Demo: Twitter Feed Processing**

**E) Recurrent Workflows**

**F) Demo: Scheduling Weather and Traffic Data Retrieval**

**G) Request Response Logic App**

**H) Demo: Loan Application Processing App**

**I) Demo: Automated Service Ticket Management App**

**J) Exception Handling in Logic App**

**K) Demo: Exception Handling**

**L) Logic App Development using Visual Studio**

**M) Summary**



# **I) Setting the Stage**

# **A) Course Overview**

This course provides a comprehensive understanding of Azure Logic Apps, a cloud-based service used to automate workflows and integrate systems seamlessly within the Azure ecosystem. The course takes a structured approach, divided into six modules, each designed to progressively build your knowledge and hands-on experience with Logic Apps.

The first module introduces the fundamental concepts of cloud computing and explains how Logic Apps fit into the broader cloud automation and integration landscape. It lays the groundwork by covering key terminologies, architectural principles, and prerequisites necessary for building and managing Logic Apps effectively. By understanding these foundational concepts, learners will be better prepared to tackle the practical aspects of workflow automation in later modules.

Once the basic concepts are clear, the course transitions into a more practical phase. Learners begin designing and implementing Logic Apps using Azure’s intuitive graphical interface. This hands-on experience allows you to see the internal workings of Logic Apps — how triggers, actions, and connectors interact to execute complex workflows.

After mastering the basics of app creation, the focus shifts toward implementing flow control mechanisms. This includes using conditional logic (if-else statements) and loop constructs (for each, until) to manage dynamic and data-driven workflow behavior. These concepts are essential for building robust and intelligent automation processes.

The next step involves exploring nested Logic Apps, which allow developers to call one Logic App from another. This approach promotes modularity and reusability, enabling the creation of scalable and maintainable workflow architectures.

Following that, the course delves into custom connectors, a critical feature for extending Logic Apps beyond the predefined set of Azure and third-party connectors. You’ll learn how to create and configure custom connectors to integrate unique APIs or internal systems, which is especially useful for automating complex enterprise workflows.

The final module focuses on Business-to-Business (B2B) integration and Electronic Data Interchange (EDI) processing. This section demonstrates how Logic Apps can be used for enterprise-level integrations, securely exchanging structured data between organizations and automating supply chain or partner communication processes.

By the end of the course, learners will have both the theoretical knowledge and practical experience to design, implement, and optimize end-to-end workflow automation solutions using Azure Logic Apps. It’s a complete journey from understanding the fundamentals to mastering advanced integration scenarios.

**B) Basics of Serverless Computing**

When your locally built application is ready for public use, the next crucial step is deploying it on a server. Traditionally, this process requires a dedicated team to manage server-related tasks such as updating applications, applying security patches, monitoring performance, handling capacity planning, and managing load distribution. These operational complexities demand continuous effort and maintenance to ensure that the application remains stable and scalable.

Cloud computing simplifies this process significantly. By choosing a cloud service provider, you can deploy your application on hosted virtual servers that are fully managed by the cloud provider. This means you no longer need to worry about hardware management, system updates, or server downtime. Your focus can remain purely on developing and improving your application while the cloud takes care of infrastructure and operational efficiency.

Scaling your application in the cloud is also straightforward. By configuring a load balancer, you can distribute traffic evenly across multiple instances of your application to handle increased user demand. You can define rules that determine how many instances should be running at any given time, enabling auto-scaling based on real-time load conditions. You create an image of your application, and the cloud platform uses this image to spin up new servers automatically when required. This flexibility drastically reduces post-deployment effort while ensuring high performance and minimal downtime.

As cloud technology has evolved, it has gone even further with the introduction of serverless computing. Although servers still exist physically, they are completely abstracted from the user’s perspective. In a serverless model, you no longer manage or even see the servers. The cloud platform automatically provisions resources and runs your code in the right environment whenever it’s needed. It takes care of scaling, load balancing, and high availability behind the scenes. This allows developers to focus entirely on business logic and application functionality rather than infrastructure management.

In serverless computing, when your application experiences higher loads, the underlying platform automatically allocates more resources to handle the demand and releases them when the load decreases. High availability and fault tolerance are built-in, meaning your application stays responsive and resilient without any manual intervention.

To design applications that leverage serverless architecture effectively, it’s essential to follow the principle of separation of concerns. Each component of the application should be designed as an independent service that performs a specific function and remains stateless. This means the service does not store data locally; instead, data is stored and managed separately in databases or data stores. The services simply connect to these data sources to process and execute business logic.

This modular approach leads to what is known as a microservices architecture, where the application is composed of multiple small, independent services that work together to achieve overall functionality. For instance, you might have separate services for email handling, database management, analytics, and core application logic. Each service operates independently but communicates with others to deliver a cohesive and scalable system.

By combining cloud computing with serverless and microservices architectures, applications achieve high scalability, fault tolerance, and operational efficiency — allowing developers and organizations to focus on innovation and business growth rather than managing infrastructure.

**C) Understanding Workflows**

Any application is fundamentally designed to automate a business process that involves a sequence of tasks leading to a specific outcome. For instance, consider an order management system that handles product orders. The process begins when an order is placed — this serves as the system’s input. From there, a series of logical steps must be executed before the order can be confirmed and completed.

The system first checks whether the ordered product is available in inventory and whether the delivery location is serviceable. Based on predefined business rules, if the order value is below a certain threshold, it can be automatically approved, and the customer is directed to a payment gateway for transaction completion. However, if the order value exceeds that threshold, it must be queued for additional verification or approval by a concerned authority. Simultaneously, an email notification is sent to that authority to inform them of the pending approval. Once the order is reviewed, processed, and payment is confirmed, the system generates a final approval email and attaches an invoice for the customer.

This entire chain of steps — from receiving an order to confirming it and sending notifications — represents a workflow. The goal of an order management system is to automate this workflow end-to-end, ensuring accuracy, efficiency, and minimal human intervention.

Even with modern development tools, APIs, and third-party libraries, traditional implementation of such workflows still requires a considerable amount of coding to define and handle each task individually. While serverless platforms simplify deployment, scaling, and maintenance, the business logic still has to be explicitly written and maintained by developers.

The next evolution in this process is workflow automation without coding, made possible by Azure Logic Apps. With Logic Apps, developers and businesses can integrate various services, define workflow sequences, and implement business logic visually — all without writing any code. This represents a major step forward in automation technology, where the focus shifts from programming to designing workflows using a graphical interface.

Azure Logic Apps act as a powerful workflow automation engine, enabling users to connect systems, services, and data sources seamlessly. They allow you to automate complex business processes — like the order management example — through simple configurations, connectors, and triggers. This makes it possible to achieve sophisticated functionality with minimal effort, greater flexibility, and faster deployment.

With this foundation, the next step is to dive deeper into understanding Azure Logic Apps, their components, and how they can be used to build intelligent, automated workflows that integrate diverse systems effortlessly.

**D) Why Logic Apps**

Logic Apps simplify the process of designing and building scalable solutions that can run either in the cloud, on-premises, or in a hybrid setup. They allow developers and organizations to focus solely on implementing business logic, while all other aspects — such as building, hosting, scaling, managing, and monitoring — are automatically handled by the platform. Although this sounds similar to what any serverless offering does, Logic Apps stand out because of their unique capability to integrate multiple services, systems, and data sources through visual, no-code workflows, enabling powerful automation with minimal technical effort.

To understand the practical benefits of Logic Apps, consider a few real-world scenarios. Suppose you have just launched a new product, and people start posting about it on Twitter. Using Azure’s Cognitive Services API, you can analyze these tweets to determine customer sentiment — positive or negative. Based on the analysis, Logic Apps can automatically send alerts, emails, or even create support tickets in systems like Zendesk for issues that need attention. This entire workflow — from collecting tweets to analyzing sentiment and generating alerts — can be built and automated without writing any code. Moreover, you can extend this setup to connect with your application’s feedback database, allowing you to combine user feedback from multiple channels in a single automated process.

Another example involves an image moderation module, commonly required in applications where users upload profile pictures. When users upload an image, it could be stored in Dropbox for review while showing a “pending approval” status to the user. The moderator then receives a notification and can approve, reject, or escalate the image for further review. Using Logic Apps, this entire review workflow can be designed visually. Later, you can enhance it by integrating Azure Content Moderator — a cognitive service capable of automatically detecting offensive or inappropriate content in images, videos, or text. This removes the need for human moderation and ensures faster and more reliable content approval.

Logic Apps can also be applied in business process automation such as order management systems. Orders below a certain amount can be auto-approved, while larger orders can be routed for manual review. Real-time dashboards can be integrated through Power BI to visualize order processing performance. You can automatically generate invoices, send payment follow-ups, and synchronize customer data with platforms like Salesforce or Dynamics CRM to enhance customer experience. For customer support, integration with Zendesk ensures that support tickets are created and updated automatically as part of the workflow.

Beyond these, Logic Apps can be used for a wide range of automation scenarios — such as sending real-time alerts for system events, updating SQL databases automatically, moving files from an FTP server to Azure Storage, managing credit requests, or processing XML file batches from third-party systems. The processed data can even be routed into Azure Service Bus for further downstream processing. These examples illustrate how Logic Apps can connect multiple systems and automate complex business processes effortlessly. The possibilities are virtually limitless as you combine its integrations, connectors, and workflow capabilities.

To summarize, Logic Apps enable the creation of cloud-based or hybrid automation solutions that scale automatically based on workload demands. They dramatically reduce time to market by allowing faster development and integration of workflows. The Azure portal and Visual Studio extensions provide a rich, intuitive interface for building and managing Logic Apps, while built-in monitoring and logging features ensure visibility and reliability. They seamlessly connect with various Azure and third-party services, making them ideal for complex enterprise integration needs. Finally, Logic Apps follow a pay-as-you-go model — you pay only when your workflow runs — making them both cost-efficient and operationally effective.

In essence, Logic Apps empower businesses to design, automate, and integrate workflows of any complexity, with minimal effort, faster delivery, and maximum scalability.

**E) Connectors, Triggers & Actions**

When creating any Logic App, the first step is to understand and select the connectors you’ll be working with. Logic Apps function by linking multiple connectors together to automate workflows and achieve specific outcomes. Each connector is associated with triggers and actions, which form the foundation of every Logic App.

A connector can be thought of as a code-less integration interface that allows your app to communicate with external services or applications through well-defined APIs. Instead of writing custom code to call APIs over HTTP, connectors act as wrappers or proxies that handle all communication for you. You simply provide authentication details — such as a username, password, or API key — and configure what data you want to send or receive. This greatly simplifies integration, eliminating the need for manual coding or API management.

Connectors are shared components within the Microsoft ecosystem and are also used in tools like Power Automate and Power Apps, apart from Logic Apps. They provide immense flexibility and power by making complex integrations as easy as filling out a few configuration fields. For example, if your app needs to perform database operations on a remote SQL server, you can use the SQL connector instead of writing custom database code. If you need to post or read tweets, you can use the Twitter connector, sign in, and start automating immediately. Similarly, for sending emails, you can use Outlook or Gmail connectors, and for performing sentiment analysis or image recognition, you can use Cognitive Services connectors. If you want to handle event-driven workflows, connectors like Azure Event Grid or Azure Service Bus can help integrate messaging and event routing seamlessly.

In short, connectors provide an enormous range of possibilities — from integrating with third-party platforms like Dropbox, Zendesk, or Salesforce to connecting with enterprise-grade systems like BizTalk Server or SAP.

Every Logic App begins with a trigger, which is responsible for starting the workflow. A trigger is essentially a notification or signal that new data or an event has occurred. Once triggered, the Logic App executes a sequence of actions defined in its workflow. For instance, in a tweet monitoring system, a trigger could detect a new tweet containing specific keywords, and subsequent actions could analyze its sentiment and automatically create a support ticket. Similarly, a trigger could listen for new customer entries in a database and start actions such as sending a welcome email or updating a CRM system.

Triggers are of two main types — polling triggers and push triggers.

Polling triggers run at scheduled intervals, checking for updates or new data. Examples include the recurrence trigger or an HTTP trigger that runs periodically.

Push triggers wait for an event to occur and respond instantly when data arrives. For example, a webhook trigger is a common type of push trigger. In a payment integration scenario, when a payment is made on PayPal, PayPal sends a webhook call to your Logic App URL, triggering an automated workflow such as order fulfillment or shipping confirmation.

The next important concept is the type of connectors used in Logic Apps. The first category is built-in connectors, which are native to Logic Apps and provide basic operational capabilities. Built-in connectors enable scheduling, looping, conditional branching, data manipulation, and integration with other Azure services like Functions, App Service, or other Logic Apps. They also include standard programming-like constructs — such as “if-else” conditions, “for each” loops, “switch” cases, and “until” loops — allowing you to control the workflow’s logic visually. You can also manipulate data easily by filtering arrays, parsing JSON, working with timestamps, initializing and updating variables, or performing mathematical operations. These are similar to what you would typically do in a traditional programming language, but here they are available through pre-built, no-code actions.

The second major category is Managed API connectors. These are pre-built connectors that enable integration with external cloud services. They allow you to interact with resources such as Azure Storage, Service Bus, Salesforce, Twitter, or Office 365. For example, using Managed API connectors, you can manage your emails and calendar events in Office 365, handle asynchronous messages, work with Salesforce data, or consume and publish events through Azure Event Hub.

Logic Apps can also connect to on-premises systems such as BizTalk Server, IBM DB2, Oracle Database, SharePoint Server, and SQL Server. To enable this communication, you must install an on-premises data gateway, which securely connects your Logic App in Azure to resources in your internal network.

Some connectors cater to Business-to-Business (B2B) scenarios and are known as enterprise connectors. These include connectors for IBM MQ, SAP, and integration account connectors such as EDI Encode/Decode, Liquid Transform, and XML Transform. Interestingly, some connectors may belong to multiple categories — for instance, SAP is both an enterprise and on-premises connector.

Even with hundreds of available connectors, there might be scenarios where none meet your specific requirements. In such cases, Logic Apps allow you to create custom connectors, enabling you to define your own APIs and integrate them seamlessly into workflows. A separate module in the course focuses entirely on creating and configuring custom connectors.

Before using any connector, it’s mandatory to configure a connection, which includes environment-specific parameters like credentials and endpoints. For example, when using the Twitter connector, you must authorize the Logic App to access your Twitter account. Similarly, for a REST API connector, you’ll need to supply an API key, and for connecting to a remote database, you’ll provide the server address and authentication details. These connection settings are stored securely and used by the connector each time the workflow runs.

Triggers and actions also come with configurable properties to fine-tune workflow behavior, such as setting conditions, defining data transformations, or handling retries. As you progress through the course and start building Logic Apps, you’ll work hands-on with these connectors, triggers, and actions to design automated workflows that connect cloud and on-premises systems effortlessly.

**F) Summary**

We began by understanding the fundamentals of cloud computing and the concept of serverless architecture — where the focus is purely on business logic while infrastructure concerns like scaling, hosting, and monitoring are managed automatically by the cloud provider.

We then explored how applications can be represented as workflows, which are sequences of tasks that collectively produce a business outcome.

Building upon that, we discussed Azure Logic Apps, a serverless workflow automation engine that enables developers to integrate services, automate processes, and build solutions without writing code.

We learned that Logic Apps are composed of three fundamental building blocks:

Triggers – events that start the workflow,

Actions – steps executed as part of the workflow, and

Connectors – integrations with external services and systems.

Finally, we concluded by emphasizing how Logic Apps simplify integration, reduce time to market, and offer scalability, monitoring, and pay-per-use pricing out of the box.

In the next module, we’ll move from theory to practice — implementing real Logic Apps to see these concepts in action.

# **II) Getting Hands Dirty**

# **A) Overview**

In this module, you will see Logic Apps in action. We will start by developing a basic app to visualize the concepts that we have learned in the previous module.

We will create different automated workflows and explore what happens under the hood, that is, how workflows are implemented internally using the Workflow Definition Language. We will also gain an understanding of how a request-response Logic App can be built.

Additionally, we will discuss exception handling in Logic Apps. This module contains multiple demos that cover different real-world scenarios, helping you understand practical applications.

Towards the end, we will talk about how to set up a local development environment using Visual Studio and then summarize our learning from the module.

# **B) Create First Logic App**

Let us create our first automated workflow. We will build a very basic Logic App that checks a website's RSS feed for new postings and then sends an email whenever a new item is published. For this task, we will use two connectors: the RSS Connector and the Gmail Connector. The trigger for our app will be "when a new feed item is published," and the action will be to send an email.

I have signed into the Azure Portal and am currently viewing the "All Services" page. Let's navigate to the integration option, or alternatively, you could use the search bar to select Logic Apps. While there is already an existing app, we will create a new one for the purpose of this demo. Click on the "Add" button, select a resource group, or create a new one if you don’t have an existing group. I will use an existing group throughout this course. Next, give a name to your app. Hosting in the East US location is fine. Review and create the app, and you will see a notification indicating the status of deployment. Once the deployment has succeeded, we can jump to our app designer page.

The app designer is intuitive, offering predefined triggers and templates for quick start. For this demo, we will create a blank Logic App. Search for the RSS connector and select the trigger "When a feed item is published." I will reduce the polling interval to one minute so that it polls for new feed items every minute from the feed URL. You can choose from a number of freely available feed URLs from popular news websites.

In the next step, we will choose the Gmail Connector to send an email. If you are connecting for the first time, you will need to sign in and provide the necessary permissions. Fill in the email ID to which emails will be sent. Add a new parameter for the "email subject" and populate it dynamically with the feed title. Next, add another parameter for the "email body," which we will populate with the feed summary and feed link.

Once done, save the Logic App and see it in action. Your inbox will be populated with emails not immediately, but as new feed items become available. You can check the run history of your other Logic App and select one of the successful run instances. The tick marks suggest that the feed was successfully read and the email was sent. You can get more information from "Run Details."

We have effectively created a kind of "Hello World" application that is up and running. This can easily be extended to more useful scenarios. For example, if you are into blogging, popular platforms like Blogger or WordPress provide RSS feed URLs. You can use the same in this app and extend it to automatically post a blog summary and link on Twitter or LinkedIn whenever you publish new content on your blog.

# **C) Behind the Scenes**

Let us now check out what happens under the hood when you build a Logic App using the designer window. We will take the Logic App that we built just now as a reference to understand what goes on behind the scenes.

Let us start with the code view of the app that we designed. Here, we can see the JSON representation of the entire app. When we were building the app using the designer view, the code was automatically generated in the backend. Some important fields to note here are actions, triggers, and connections, which were used in our app. This file essentially defines everything needed for the Logic App to function. In other words, it is an alternative way to build a Logic App, though the designer view makes the development process much simpler. You can also view the code in parts directly within the designer view. Just go to the settings in any action, and you can view the code for that specific part.

Next, let us explore some of the other properties found under settings. One important property is the retry policy of the Logic App. This policy determines the app’s behavior during errors or exceptions. Currently, the default policy is set, but you can always select a policy of your choice from the drop-down box.

Now, let us look at the API connection objects that were created for our app. Since we used Gmail and RSS connectors, their connection objects are displayed. By clicking on properties, you can explore further details of the connection and even edit some properties if needed.

Let us also see the versions of our app. Every modification to the app generates a new version. You can always revert to an older version of your app by clicking the “promote” button. Going back to the overview of the Logic App and refreshing the run history shows multiple successful executions of the app. You can select any run instance to explore further details. Clicking on actions shows all the data that was used during the execution, which is very helpful for debugging and identifying the root cause in case something goes wrong. This data includes the inputs passed to each action and the outputs generated. More detailed information is available by clicking on “Run Details.”

By now, you would have gained a fairly good understanding of what happens under the hood when building and running Logic Apps. This knowledge will help us build more complex apps as we continue with the course.

# **D) Demo: Twitter Feed Processing**

In this demo, we will use the Azure Cognitive Services API to perform sentiment analysis on Twitter feeds. We will read tweets related to a specific subject from Twitter and pass the contents of each tweet to the Text Analytics service to obtain a sentiment score. Considering any score less than 0.7 as negative, we will configure the Logic App to send an email whenever a negative sentiment is detected.

Let us start by creating a new Logic App. Choose a resource group, give the Logic App a name, and click on Create. Once the deployment is complete, go to the resource to begin building the Logic App.

We will first choose the trigger “When a new tweet is posted.” In the designer view, we can see the Twitter connector. Sign in to Twitter, authorize the app, and establish the connection. This step needs to be done only once, as the connection information will be saved for subsequent connection requests. Click Continue, change the polling frequency to one minute, and provide the text to be searched in tweets — for example, “BMW.” Once done, save the Logic App.

Next, let us go to Azure Cognitive Services and create a new Text Analytics service for this demo. Provide a name for the service, specify the subscription, location, pricing tier, and resource group, and then click Create. This will initiate the deployment of the service. Once the deployment is complete, go to the resource. You will find the information needed to connect to the Text Analytics service, including the API key and the service endpoint URL. Copy this information and make a note of it, as we will need it to connect the Logic App to the service.

Now, go back to the Logic App we started working on. We have already established a connection to Twitter. The next step is to choose a connector for the Text Analytics service and select the “Detect Sentiment” action. Provide a name to identify the connection, enter the API key and service URL that we copied earlier, and then click Create. This establishes a connection to the Text Analytics service that we deployed for this demo.

Next, add a new parameter — the text to analyze — which will serve as the input for the “Detect Sentiment” action. Click on Dynamic Content and select the original tweet text that is available from the previous step in the Logic App.

Now, we will add a control action. In this case, we will add a Condition that checks the sentiment score from the previous step. Select Score from Dynamic Content and check if its value is less than 0.7. If the condition evaluates to true, we will add an action in the “True” block. Choose the Gmail connector and select the “Send Email” action. Provide the email address to which the email should be sent. Add a subject for the email and dynamically populate it with the tweet ID. Then, add another parameter — the body of the email — and dynamically populate it with one or more attributes of the tweet being analyzed.

For this demo, we will skip the “False” block. This means that when the sentiment analysis score is higher than 0.7, no action will be taken. Save the Logic App, and it will start polling Twitter for any new tweets related to “BMW.”

You will see a notification in the top-right corner indicating “Successfully checked the trigger.” In the designer view, the Logic App execution is shown as successful with all green tick marks. The condition states “The expression result is true,” which means an email was sent by the Logic App.

To verify, check your email inbox — you will find multiple emails sent, each with the subject as the tweet ID and the body containing other tweet attributes. Going back to the Logic App, you can analyze the data used by each action during the execution. This data provides valuable insight into how each action uses the output of the previous step and provides input to the next step.

# **E) Recurrent Workflows**

If you want to automate scenarios where a workflow needs to run regularly, you can use the Scheduled “Recurrence Trigger” action. This trigger in Logic Apps allows us to set a specific date and time for starting the workflow, as well as define a recurring schedule for performing tasks automatically.

There are several scenarios where recurrent workflows can be extremely useful. For example, they can be used to migrate data warehouses periodically, ensuring that data remains up to date across systems. They can also be used to clean records that are no longer required in a database, helping maintain data hygiene and efficiency. Another common use case is to run stored procedures in a database on a regular basis to update records automatically.

Additionally, recurrent workflows can be applied to scenarios like pulling weather or traffic data periodically from third-party services, enabling systems to stay updated with real-time information.

# **F) Demo: Scheduling Weather and Traffic Data Retrieval**

In this demo, we will illustrate a recurrent workflow that pulls the current weather and traffic information from different services and sends an email with the fetched information at regular intervals.

Let us begin by creating a new Logic App. Specify a resource group, provide a name for the app, and click Create to initiate the deployment. Once the deployment is successful, go to the resource to start building the app.

Begin by selecting the Recurrence trigger and specify the interval as one minute. In the next step, choose the MSN Weather connector and select the Get current weather action. For this demo, specify the location as New Jersey.

Next, add another step by choosing the Gmail connector and selecting the Send email action. Specify the recipient’s email address, add a subject to the email, and dynamically populate it with the weather conditions variable. Then, add another parameter for the body of the email and populate it dynamically with the information available from the previous action, such as humidity and temperature.

Save the Logic App. Once saved, it is ready to execute. The app should now poll the weather information every minute and send an email. Go to Gmail and verify whether the app is functioning properly. You should see an email with the subject “Partly Cloudy Data” and the humidity and temperature information in the body.

Next, return to the Logic App and refresh the run history. You should see a Succeeded status for the latest run instance. Let us now disable the app to add a new feature.

Add a new action and choose the Bing Maps connector. Select the Get route action. To establish a connection with the Bing Maps service, you’ll need to provide an API key. Go to the Bing Maps Service Portal, sign in, navigate to My Account → My Keys, and create a new key by providing an application name. Click Create, then Show Key, and copy the key.

Return to your Logic App, give a connection name, paste the API key, and hit Create to establish the connection. Specify the locations for which you want to get the route information. Add a parameter called Optimize and set its value to time with traffic.

Now, modify the mail subject to include another attribute obtained from the Get route action. Similarly, update the email body to include dynamic traffic information retrieved from the previous step.

Save the Logic App again. Go to the Overview section and enable it. You should now start receiving emails containing both weather and traffic information.

Verify this in Gmail — as expected, you should receive an email with the subject “Partly Cloudy Weather and Mild Traffic” and detailed information about both weather and traffic in the email body.

Finally, go back to your Logic App and disable it to prevent receiving too many emails. Refresh the run history and click on the latest run instance — all green tick marks indicate that the Logic App executed successfully.

# **G) Request Response Logic App**

With the help of the built-in Request trigger and Response action, we can create automated workflows that can receive and respond to incoming HTTPS requests.

Consider a scenario of submitting a loan application online. A user fills in the required details using a user-friendly interface provided by the banking service. When the user clicks the Submit button, the front end creates a JSON object containing the entered details and embeds it in an HTTP POST request. The backend, which acts as the HTTP endpoint, receives this request, extracts the details from the request body, and stores them in a database.

Next, the backend creates a JSON response containing the Application ID and the current status of the application, and sends it back to the front end. As a result, the user sees a message indicating that the application has been submitted for further processing. The status of that application can later be tracked using the Application ID.

We will automate this entire workflow in the upcoming demo. But before that, let us learn a few things that will help us build and test this scenario.

We will not be building any UI to test our logic. Instead, we will use an excellent tool called Postman, which allows us to send requests to an HTTP endpoint. Postman is one of the most widely used tools for testing APIs. We just need to provide the URL, craft the request body, and click the Send button. This sends the request to the HTTP service and displays the received response.

Our Logic App will need to store user data for further processing. Instead of using traditional databases, we will use Azure Table Storage as the data store for our app. This is a NoSQL database that provides key-value storage with a schema-less design.

In Azure Table Storage, a table is a collection of entities. An entity is a set of properties, and it is analogous to a row in a relational database table. Each property is a “name–value” pair, similar to a column in a table.

In our loan processing Logic App, we need to generate unique tracking IDs. For this, we can use internal functions available in Logic Apps. Internal functions act as shortcuts for working with collections, strings, logical operators, and conversions. One of these functions can generate a unique GUID, which can serve as a tracking ID once the application is submitted.

Alternatively, we can use Azure Functions for this purpose. We can write an Azure Function that is triggered by an HTTPS request and returns a unique ID in response. This function can then be integrated with our Logic App using built-in connectors.

Now, it’s time to see a Request–Response Logic App in action.

# **H) Demo: Loan Application Processing App**

In this demo, we are going to build a Loan Authorization Logic App, and in the process, we will learn a few important concepts.

Here are the objectives for this demo:

Illustrate how a Request–Response Logic App works.

Learn how to use Azure Table Storage as a data store for a Logic App.

Integrate an Azure Function with a Logic App.

Get familiar with internal functions, which are extremely useful while building Logic Apps.

Finally, use Postman for testing purposes.

Before building the Logic App, let’s first set up Azure Table Storage. Go to Storage Accounts, choose the account that you want to use, select the Table option, and add a new table. Provide a name and click OK — a new table has now been created.

Next, let’s go back to our Logic App and create a new one. Select a resource group, provide a name for the app, and click Create to initiate the deployment. Once deployment is complete, go to the resource.

We will begin by choosing the predefined HTTP Request Trigger for our app. The URL for posting the request will be generated once we save the app. Now, we need to provide a schema for the request body. This can be easily generated using a sample JSON that we plan to send in our POST request. In this example, we will send JSON data containing name, age, and salary. Click Done, and the schema will be automatically generated.

Remember to specify the Content-Type header as application/json while sending the request using Postman. Review the schema to ensure everything is correct.

In the next step, choose the Initialize Variable action. Give a name to the variable, specify its type, and set the initial value. For the initial value, click on Dynamic Content and select the internal function that generates a unique GUID.

Then, add an Azure Table Storage Connector and select the Insert Entity action. Specify the table name. The entity represents a JSON object — similar to a row in a table, with fields inside the JSON acting as columns.

Populate the entity with a Partition Key and a Row Key. Use the value of the initialized variable (the GUID) as the Row Key. Populate other fields, which will automatically capture values from the request body.

Next, choose the Response action and populate the response body with the entity that was inserted into the table.

Save the Logic App and copy the generated HTTP Request URL.

Now, let’s test it using Postman. Paste the URL, go to the Headers tab, and add Content-Type: application/json. Then, in the Body tab, select raw JSON format and provide values for name, age, and salary. Click Send.

You should see a 200 OK response, indicating that the request was successful and that the inserted entity was returned in the response body.

To verify, go to the Azure Storage Explorer, select the storage account, and open the table we created. You will see the newly inserted entity — the same one that was sent back in the response.

Back in the Logic App, open Run History and view the latest run instance. All green tick marks indicate successful execution. You can also check the GUID value, inserted entity, and response body.

Now, let’s modify the Logic App to use an Azure Function instead of the internal function for generating the GUID (which acts as the Row Key in the Azure Table).

Save the app, then search for Function App and create a new one. Select a resource group, provide a name, choose the .NET Core runtime stack, and click Create to start deployment. Once the deployment is complete, go to the resource and start building the Azure Function.

Add a new function, choose the development environment as Portal, and click Continue. Select Webhook + API trigger and hit Create. This generates boilerplate code for the function. Modify the function to generate a unique GUID, then save and run it. Test it using an HTTP GET method — it should return a GUID successfully.

Now, go back to the Logic App. Add an Azure Functions Connector, select the function app that you just created, and rename it for clarity. Then, add an Azure Table Storage Connector, choose Insert Entity, and specify the table name.

Populate the entity — this time, use the output of the Azure Function (the GUID) as the Row Key. Fill in other fields as before, and add a new field called status with the value "submitted".

Next, add a Response action and include the inserted entity in the response body. Save the Logic App.

Go back to Postman, modify the request body, ensure the content type is correct, and click Send. You should receive a successful response with the inserted entity.

Return to the Logic App, refresh Run History, and view the latest run — all green checkmarks confirm success. In the Storage Explorer, you can also validate that the data has been inserted successfully.

Now, we’ll take one of the previously inserted entities that did not have a status field. Add a new status property and mark it as "approved", then update the entity.

Back in the Logic App, modify it again. Delete all actions and change the request body schema — this time, we will take an ID as input and fetch the corresponding entity from the table to send it back as a response.

Next, choose the Azure Table Storage Connector and select Get Entity. Specify the table name, partition key, and row key (the ID from the request body). Then, add a Response action to return the fetched entity as the response body.

Save the Logic App, go to Postman, and copy the Row Key from one of the previous entities. Paste it into the request body and send the request. You will receive the corresponding entity as the response.

Now, use the Row Key of the entity we edited and marked as "approved" — send the request again. You will see that the correct entity is returned.

Finally, try sending an incorrect ID. The Logic App will respond with an error. Back in the Logic App, refresh the Run History and open the failed instance — the red mark indicates an error in the action stating that the "entity was not found," and the response action failed accordingly.

This completes the demo, where we explored Azure Table Storage and Azure Functions while learning how to build a Request–Response Logic App.

# **I) Demo: Automated Service Ticket Management App**

In this demo, we will further explore the Request–Response Logic App.

Today’s software systems are typically built using microservices architecture, where each service exposes a URL and defines the schema for the expected input in the request body. The service processes the request and sends a response back to the caller.

In this example, we’ll build a Logic App that automatically creates a service ticket based on user feedback. In a real-world scenario, users would submit feedback using the UI on a mobile or web application, and this feedback would then be posted to a cloud service responsible for managing support tickets.

For this demo, we’ll use Postman to submit feedback, and our Logic App will use Azure Cognitive Services Text Analytics to perform sentiment analysis. If the feedback is negative, the Logic App will automatically create a service ticket using a third-party ticket management tool called Freshdesk.

You can think of this Logic App as a microservice that handles customer feedback and ticket creation. It exposes an HTTP endpoint as an interface for other applications or services to consume.

Building the Logic App

Let’s begin by creating a new Logic App.
Select a resource group, give the app a name, and click Create to initiate deployment. Once the deployment completes, go to the resource and start building the Logic App.

Choose the HTTP Request Trigger as the starting point. When we save the app, a unique URL will be generated for receiving incoming HTTP POST requests.

Next, define the request body schema using a sample JSON payload — this will represent the structure of the feedback sent from users.

Adding Sentiment Analysis

In the next step, add a connector for the Text Analytics Service and select the Detect Sentiment action. We’ve already created this connection in a previous demo, so we can reuse it.

Set the text to analyze as the feedback parameter dynamically obtained from the HTTP request body.

Now, add a Condition Control Action to check if the sentiment score is less than 0.7 (on a scale of 0 to 1). If the score is below 0.7, the feedback will be considered negative, and the Logic App will proceed to create a ticket.

Creating a Ticket in Freshdesk

Inside the True Block, add a new action.
Choose the Freshdesk Connector and select the Create a Ticket action.

Now, let’s connect Freshdesk to our Logic App.
Go to your Freshdesk account, log in, and copy your Freshdesk account URL. Paste this into the Logic App connection setup, then provide your API key or email ID and password. Click Create to establish the connection.

Once connected, populate the ticket fields:

Subject → “Negative Feedback”

Description → dynamically populate with the feedback text

Email → dynamically use the user’s email ID from the feedback

Priority → set the desired priority level

At this point, the Logic App can automatically create tickets in Freshdesk whenever negative feedback is detected.

Sending Email Notifications

Next, add another action to send a notification email to the user once a ticket is created.
Use the Gmail Connector and select the Send Email action.

To → dynamically use the user’s email ID from the feedback

Subject → “Ticket Created – [Ticket ID]” (populate ticket ID dynamically from the previous action)

Body → dynamically include ticket details such as description, ID, and priority

This completes the True Block.

Handling Positive Feedback

Now, move to the False Block (when the sentiment score is ≥ 0.7).

Add an action using the Gmail connector to send a thank-you email to the user acknowledging their positive feedback.

To → dynamically use the user’s email

Subject → “Thank You for Your Feedback”

Body → include the feedback message dynamically

With this, both branches of the condition are complete.

Adding the Response

Add a Response Action to send a blank 200 OK response back to the HTTP caller (Postman). Save the Logic App and copy the generated HTTP Request URL.

Testing with Postman

Open Postman, paste the Logic App URL, and prepare a JSON body containing user feedback and email details. Click Send.

You’ll receive a 200 OK response, indicating that the Logic App executed successfully.

Check the user’s email — you should see an email stating that a ticket was created (for negative feedback).

Now, log in to Freshdesk and refresh the dashboard. A new ticket titled “Negative Feedback” should appear, created from the same user email. You can now assign or update the ticket directly in Freshdesk.

Back in the Logic App, refresh the Run History. You’ll see a successful run instance. Expand it to view detailed logs — you’ll notice that a low sentiment score triggered ticket creation and an email notification to the user.

Testing Positive Feedback

Go back to Postman and modify the feedback message to something positive. Click Send again.

You’ll receive another 200 OK response, but this time, when you check Freshdesk, no new ticket will appear. Instead, the user will receive a thank-you email acknowledging their positive feedback.

Back in the Logic App run history, you’ll see that the False Block executed this time, since the sentiment score was high.

Adding an SMS Notification (Optional Enhancement)

You can further enhance this Logic App by adding a parallel branch after ticket creation to send an SMS notification using Twilio.

To do this, create a Twilio account, choose the Send Text Message action from the Twilio connector, and fill in the required details such as phone number, message body, and account credentials. Once configured, the Logic App will be able to send both an email and SMS notification when a new ticket is created.

That’s it for this demo!
We successfully built a Request–Response Logic App that integrates Azure Cognitive Services, Freshdesk, Gmail, and optionally Twilio, to automate customer feedback handling and service ticket creation.

# **J) Exception Handling in Logic App**

Exceptions are unforeseen scenarios that can occur during the execution of applications, and not handling these exceptions can lead to undefined behavior of the application. In Logic Apps, there are two ways to handle exceptions.

The first method is Retry Policy. If an action fails to perform the task, it will automatically reattempt the operation based on the retry policy set for that action. This can be particularly useful in cases of intermittent issues, such as connectivity problems, which might be resolved by the time the app makes the next attempt.

The second method is Run After Configuration. Here, we define scopes in which actions execute. In case an exception occurs in one scope, another scope block in the app can catch it based on the defined policy. There can also be other actions in that scope designed to perform tasks specifically meant to handle exceptions.

With proper exception-handling mechanisms in place, we ensure that the application has a way to handle error scenarios gracefully, maintaining stability and predictable behavior even when things go wrong.

# **K) Demo: Exception Handling**

In this demo, we learn how exception handling can be implemented in Logic Apps using scope actions. The business logic executes within a try block, and in case an exception occurs, it is handled in the catch block. The finally block executes regardless of whether an exception happened or not. This mechanism is analogous to what you would see in traditional programming languages.

Let us move to the designer window where we will introduce exception handling to a previously designed app. We already have the HTTP request trigger added to our app. In the next step, we initialize a variable named status, specify its type as integer, and assign it a value of 200.

Next, we add a scope action and rename it as Try scope for clarity. Similarly, we add another scope action called Catch scope and a parallel scope action called Finally scope.

Expanding the Try block, we add an action using the Azure Storage Table connector and select Get Entity. We specify the partition key and dynamically populate the Row key with the id received in the HTTP request body. While the retry policy can be changed in the settings of the scope action, for this demo, we leave it as default.

In the Catch block, we add an action to set the status variable to 500, indicating an error. The critical step is to configure the "Run After" property of the catch block by selecting "has failed" and "has timed out", ensuring this scope executes whenever an error occurs in the try scope.

For the Finally block, we add a response action to return the entity retrieved from the Azure table to the caller. We configure its "Run After" property to select all options, ensuring that this block runs regardless of the try block’s outcome.

After saving the logic app, an error occurred because the table name was not specified in the try block. Once corrected, the app could be saved successfully.

To test, we use Postman with a random id in the request body to intentionally cause an exception. In the response, a "resource not found" message is returned, but the status code remains 200 OK, which would have differed without exception handling.

Finally, checking the run history of the logic app shows that the action in the try block failed and the exception was correctly handled in the catch block. This completes the demo on exception handling in Logic Apps.

# **L) Logic App Development using Visual Studio**

In this demo, we explored how to set up a local development environment for Logic Apps using Visual Studio.

First, in Visual Studio 2019, go to the Extensions menu and select Manage Extensions. Here, you can search for Logic Apps extensions. If not already installed, install it.

Next, create a new project via File → New Project. Choose Cloud as the project type and select Azure Resource Group. Give your project a name and click Create. Then, choose the Logic App template for the project.

In Solution Explorer, you’ll see the necessary files for your app. Double-click LogicApp.json to view the basic template. Right-click on it and choose Open With Designer. If this is your first time, you’ll be prompted to sign in to your Azure account. Once signed in, select a resource group and click OK.

The designer interface in Visual Studio mirrors what you see in the Azure portal, so from here, designing the Logic App is the same as in the portal. You can also view and modify existing Logic Apps by using Cloud Explorer. Right-clicking an app allows you to open it in the Logic App editor, make changes locally, and redeploy directly to your specified Azure subscription via the Deploy option.

This demo shows that Visual Studio (or Visual Studio Code) can be used to build, modify, and deploy Logic Apps locally. However, for the purposes of this course, we will continue building Logic Apps directly in the Azure portal.

# **M) Summary**

We began by building a basic Logic App and explored what happens under the hood when a Logic App runs. We then created different automated workflows, including Request-Response Logic Apps, and saw how these apps can interact with services like Azure Table Storage, Azure Functions, and third-party connectors.

Finally, we looked at how to develop Logic Apps locally using Visual Studio and deploy them to the cloud. While this course will continue using remote development in the Azure portal, you have the flexibility to choose the development approach that best suits your workflow.



