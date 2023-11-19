# TechConf Registration Website

## Project Overview
The TechConf website allows attendees to register for an upcoming conference. Administrators can also view the list of attendees and notify all attendees via a personalized email message.

The application is currently working but the following pain points have triggered the need for migration to Azure:
 - The web application is not scalable to handle user load at peak
 - When the admin sends out notifications, it's currently taking a long time because it's looping through all attendees, resulting in some HTTP timeout exceptions
 - The current architecture is not cost-effective 

In this project, you are tasked to do the following:
- Migrate and deploy the pre-existing web app to an Azure App Service
- Migrate a PostgreSQL database backup to an Azure Postgres database instance
- Refactor the notification logic to an Azure Function via a service bus queue message

## Monthly Cost Analysis
Complete a month cost analysis of each Azure resource to give an estimate total cost using the table below:

| Azure Resource   | Service Tier           | Monthly Cost   |
| ---------------- | ------------           | -------------- |
| Azure PostgreSQL |   General Purpose      |   $231.69      |
| Azure Service Bus|   Basic                |   $0.05        |
| Azure App Service|   Basic (B1)           |   $19.24       |
| Azure Storage    |   Basic                |   $0.10        |

The app service includes the web app and the function app.

## Architecture Explanation
Architecture Explanation
Azure Function
• Azure Functions makes the app development process more productive, and lets you launch serverless applications on Microsoft Azure. It
helps in processing data, coordinating with different systems for IoT, integrating various processes and systems and building simple APIs
and microservices.
• It is autoscalable and allow to handle a huge peak of activity, the web app can't do this cost-effectively. This also, allows to do a division of
concerns and create a service for email sending.
Azure Web App
It is cheaper than on-premise solutions.This is one of the biggest concerns for businesses, the ultimate question — does investing in cloud
solutions make financial sense for your business? In most cases, it does and by a good margin too. With Azure, you don't have to invest in new
machines, infrastructure, or replace aging servers. You also don't need to make space for infrastructure and servers.Azure, offers flexible
expenditure, which means:
• You pay according to your needs.
• You pay more to get more.
• You save on energy, spacer and cooling costs. Not only that, you have certainty in your recurring costs as Microsoft charge per user for
their Azure cloud services.
Service Bus
Microsoft Azure Service Bus is a fully managed enterprise integration message broker:
- Service Bus can decouple applications and services.
- Service Bus offers a reliable and secure platform for asynchronous transfer of data and state.
And data is transferred between different applications and services using messages. A message is in binary format and can contain JSON, XML,
or just text.
