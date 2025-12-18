# Threat Protection with XDR - Mitigate threats using Microsoft 365 Defender - 5
### Overall Estimated Duration: 60 minutes
## Overview

In this lab, you will act as a Security Operations Analyst at a company that has implemented Microsoft Defender XDR solutions. Your task is to view alerts within incidents to assess their impact, conduct root cause investigations, and mitigate these alerts using Microsoft 365 Defender tools. You will perform key tasks, including onboarding devices, managing incidents, and investigating alerts in the M365 Defender portal.

## Objective

Understand how to utilize Microsoft 365 Defender to enhance security operations and effectively manage incidents. Gain skills in onboarding devices, managing incidents, and investigating alerts. By the end of this lab, you will be able to:

- **Onboard a Device**: Learn how to onboard devices to Microsoft Defender for Endpoint, ensuring they are monitored for security threats and visible in the Defender portal.
- **Manage Incidents**: Understand how to navigate the M365 Defender portal to manage incidents, including editing incident details, classifying incidents, and assigning them to users or groups.
- **Investigate Alerts**: Gain practical skills in investigating security alerts, including analyzing suspicious behavior, running advanced queries, and utilizing deep analysis for thorough investigations.

## Prerequisites

Participants should have:

- **Basic Understanding of Microsoft 365 Defender**: Familiarity with Microsoft 365 Defender functionalities and interface.
- **Knowledge of Security Concepts**: Basic knowledge of cybersecurity concepts and incident response procedures.
- **Access to Microsoft 365 Defender**: A valid Microsoft 365 Defender account with necessary permissions.


## Architecture

In this lab, the architecture leverages Microsoft 365 Defender to manage security incidents effectively. You will onboard devices to Microsoft Defender for Endpoint, enabling continuous threat detection. The Microsoft 365 Defender portal serves as the central management interface, where analysts can view alerts, manage incidents, and perform investigations. The incident management system aggregates alerts from various sources, providing context for security events. Additionally, advanced hunting allows for custom queries to investigate incidents further, while automation features streamline response actions to enhance incident management and threat mitigation.

## Architecture Diagram

![](./media/01-3.png)

## Explanation of Components

The architecture for this lab involves the following key components:

- **Microsoft 365 Defender Portal**: This is the primary interface for security operations analysts. It provides a centralized view of alerts, incidents, and investigation tools, enabling efficient management of security threats across the organization.

- **Microsoft Defender for Endpoint**: This component offers advanced endpoint protection and detection capabilities. It continuously monitors devices for potential threats, allowing for real-time identification and response to security incidents.

- **Incident Management System**: This system aggregates alerts generated from various sources, helping analysts manage and investigate incidents. It provides context by linking related alerts and identifying affected devices and users.

- **Alert System**: The alert system collects and categorizes security alerts from Microsoft Defender products and other integrated services. This component is critical for identifying potential security threats and prioritizing responses.

- **Advanced Hunting**: This feature allows analysts to perform custom queries on the data collected by Microsoft Defender. It enables deeper investigations into specific incidents and patterns, helping analysts uncover hidden threats.

- **Automation and Response Capabilities**: Microsoft 365 Defender includes tools for automating response actions based on predefined rules. This helps streamline incident management and enhances the efficiency of threat mitigation efforts.

## Getting Started with the Lab
 
Welcome to your Threat protection with XDR workshop! We've prepared a seamless environment for you familiarize yourself with the Microsoft security operations analyst, you monitor, identify, investigate, and respond to threats in multicloud environments and related Microsoft services. Let's begin by making the most of this experience:
 
## Accessing Your Lab Environment
 
Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.
 
![](./media/XDRintro1.png)

### Virtual Machine & Lab Guide
 
Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.
 
## Exploring Your Lab Resources
 
To get a better understanding of your lab resources and credentials, navigate to the **Environment Details** tab.
 
![Explore Lab Resources](./media/XDRintro2.png)
 
## Utilizing the Split Window Feature
 
For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the Top right corner.
 
![Use the Split Window Feature](./media/XDRintro3.png)
 
## Managing Your Virtual Machine
 
Feel free to start, stop, or restart your virtual machine as needed from the **Resources** tab. Your experience is in your hands!
 
![Manage Your Virtual Machine](./media/XDRintro4.png)

## Lab validation

1. After completing the task, hit the Validate button under Validation tab integrated within your lab guide. If you receive a success message, you can proceed to the next task, if not, carefully read the error message and retry the step, following the instructions in the lab guide.

   ![](./media/update03.png)

2. You can also validate the task by navigating to the Lab Validation tab, from the upper right corner in the lab guide section.

   ![](./media/update002.png)

3. If you need any assistance, please contact us at labs-support@spektrasystems.com.

## Login to the Azure Portal
 
1. In the JumpVM, click on the Azure portal shortcut of the Microsoft Edge browser, which is created on the desktop.
 
    ![Launch Azure Portal](./media/XDRintro5.png)

2. On the Sign in to Microsoft Azure tab, you will see the login screen. Enter the following email or username, and click on Next.
 
   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
 
     ![Enter Your Username](./media/sc900-image-1.png)
 
3. Next, provide your password:
 
   - **Password:** <inject key="AzureAdUserPassword"></inject>
 
     ![Enter Your Password](./media/azurepwlogin.png)
 
4. If you see the pop-up Action Required, click Ask Later.

   ![](./media/update04.png)

   > **NOTE**: Do not enable MFA, select Ask Later.

5. If you see the pop-up Stay Signed in?, select No.

6. If you see the pop-up **You have free Azure Advisor recommendations!**, close the window to continue the lab.

7. If a Welcome to **Microsoft Azure** popup window appears, select **Maybe Later** to skip the tour.

8. Now that you will see the Azure Portal Dashboard, click on Resource groups from the Navigate panel to see the resource groups.

   ![](./media/update05.png)  
 
In this hands-on lab, you'll utilize Microsoft 365 Defender to onboard devices, manage incidents, and investigate alerts, enabling you to effectively mitigate security threats and enhance your organization's overall security posture.

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:

 - Email Support: labs-support@spektrasystems.com
 - Live Chat Support: https://cloudlabs.ai/labs-support

Now, click on Next from the lower right corner to move on to the next page.

![Start Your Azure Journey](./media/XDRintro6.png)

## Happy Learning!!

