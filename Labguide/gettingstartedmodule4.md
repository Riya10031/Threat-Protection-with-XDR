# Threat Protection with XDR - Threat Hunting using Notebooks with Microsoft Sentinel - 4

### Overall Estimated Duration: 1 Hour 30 Mintues

## Overview

In this lab, you will work as a Security Operations Analyst tasked with performing a threat hunt in Microsoft Sentinel after receiving intelligence about a Command and Control technique. You will integrate data sources, enable Microsoft Defender for Cloud, and simulate various attack techniques such as persistence and privilege escalation. Through custom hunting queries and the use of Sentinel Notebooks, you will identify potential security breaches and investigate incidents. By the end of the lab, you will have practical experience in using Microsoft Sentinel to detect and respond to Command and Control techniques and other advanced attack methods, helping improve your organization’s security posture.

## Objective

Understand how to configure Microsoft Sentinel for security monitoring and threat detection through the integration of various data sources and tools. Gain skills in simulating real-world attacks, including persistence, Command and Control, and privilege escalation, to better understand threat landscapes. By the end of this lab, you will be able to :

- **Connect the Windows Security Event Connector for log collection**: Learn how to connect the Windows Security Event Connector in Microsoft Sentinel, enabling you to gather security event logs from Windows machines for comprehensive threat monitoring and analysis.
- **Enable Microsoft Defender for Cloud to secure resources**: Gain expertise in enabling Microsoft Defender for Cloud, configuring it to provide continuous security assessments and threat protection for your cloud resources, ensuring a secure and compliant environment.
- **Simulate a Persistence Attack using Registry Key Add**: Understand how to simulate a persistence attack by adding a registry key, providing insights into how attackers maintain access to compromised systems and how you can detect and mitigate these threats.
- **Simulate a Command and Control (C2) Attack using DNS queries**: Learn to simulate a Command and Control (C2) attack via DNS queries, helping you understand how attackers communicate with compromised machines and how to detect these malicious activities within your environment.
- **Simulate a Privilege Elevation Attack by adding a new user**: Develop the ability to simulate a privilege elevation attack by adding a new user account, allowing you to identify how attackers might escalate privileges and compromise sensitive systems.
- **Create a hunting query to detect suspicious PowerShell activity**: Acquire the skills to create a custom hunting query to detect suspicious PowerShell activity, enabling you to proactively hunt for potential threats and investigate malicious behavior in your environment.
- **Develop a near real-time (NRT) query rule for continuous monitoring**: Learn to build and implement a near real-time (NRT) query rule for continuous monitoring of your environment, automating the detection of security threats and responding swiftly to incidents.
- **Execute a search job to detect Command and Control (C2) activity**: Gain hands-on experience in executing search jobs within Microsoft Sentinel to detect C2 activity, improving your ability to track and mitigate threats involving external command and control communications.
- **Explore Microsoft Sentinel Notebooks for advanced threat hunting and analysis**: Master the use of Microsoft Sentinel Notebooks for advanced threat hunting and analysis, leveraging data science techniques to detect, investigate, and respond to sophisticated attacks.

## Prerequisites

Participants should have:

- **Familiarity with Microsoft Sentinel**: Understanding the core concepts and functionalities of Microsoft Sentinel, including data connectors and threat management.
- **Basic Knowledge of PowerShell**: Proficiency in using PowerShell for script execution and command-line operations.
- **Understanding of Security Events**: Familiarity with Windows security events and their significance in threat detection and investigation.
- **Experience with KQL**: Basic knowledge of Kusto Query Language (KQL) to create and run queries in Microsoft Sentinel.
- **Basic Understanding of Cybersecurity Concepts**: Awareness of common attack techniques and defense strategies, particularly regarding Command and Control communications and privilege escalation.

## Architecture

In this lab, the architecture flow encompasses essential components to enhance threat hunting capabilities. You will connect the Windows security event connector to the Microsoft Sentinel workspace, serving as the centralized hub for monitoring security incidents and executing hunting queries. Integrated with Microsoft Defender for Cloud, this architecture enables real-time threat detection across your environment. Log Analytics is used for querying security events with Kusto Query Language (KQL), allowing for custom hunting queries and alerts. PowerShell scripts simulate attacks to generate log entries, while Notebooks facilitate interactive data exploration. This comprehensive architecture empowers security analysts to proactively hunt for and effectively respond to threats within the organization.

## Architecture Diagram

![](./media/01-2.png)


## Explanation of Components

The architecture for this lab involves the following key components:

- **Microsoft Sentinel**: Microsoft Sentinel is a cloud-native security information and event management (SIEM) solution that provides intelligent security analytics and threat intelligence across the enterprise, enabling proactive threat hunting and incident response.
- **Microsoft Defender for Cloud**: This service offers advanced threat protection for cloud resources, integrating seamlessly with Microsoft Sentinel to enhance security posture through continuous monitoring and threat detection.
- **Log Analytics Workspace**: The Log Analytics workspace collects and analyzes log data, enabling users to perform powerful queries using Kusto Query Language (KQL). It serves as a central repository for security event logs.
- **Windows Security Event Connector**: This connector facilitates the ingestion of security event logs from Windows environments into Microsoft Sentinel, ensuring comprehensive visibility into potential security incidents.
- **PowerShell Scripts**: PowerShell scripts are used to simulate various attack scenarios, generating log entries that can be analyzed during the threat hunting process, helping to train and refine detection capabilities.
- **Notebooks in Microsoft Sentinel**: Notebooks provide an interactive environment for data analysis and visualization, enabling security analysts to explore and share insights derived from security data effectively.

## Getting Started with the Lab
 
Welcome to your Threat protection with XDR workshop! We've prepared a seamless environment for you familiarize yourself with the Microsoft security operations analyst, you monitor, identify, investigate, and respond to threats in multicloud environments and related Microsoft services. Let's begin by making the most of this experience:
 
## Accessing Your Lab Environment
 
Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.
 
![](./media/XDRintro1.png)

### Virtual Machine & Lab Guide
 
Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.
 
## Exploring Your Lab Resources
 
To get a better understanding of your lab resources and credentials, navigate to the **Environment Details** tab.
 
![Explore Lab Resources](./media/t10.png)
 
## Utilizing the Split Window Feature
 
For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the Top right corner.
 
![Use the Split Window Feature](./media/t9.png)
 
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
 
     ![Enter Your Password](./media/t1.png)
 
4. If you see the pop-up Action Required, click Ask Later.

   ![](./media/update04.png)

   > **NOTE**: Do not enable MFA, select Ask Later.

5. If you see the pop-up Stay Signed in?, select No.

6. If you see the pop-up **You have free Azure Advisor recommendations!**, close the window to continue the lab.

7. If a Welcome to **Microsoft Azure** popup window appears, select **Maybe Later** to skip the tour.

8. Now that you will see the Azure Portal Dashboard, click on Resource groups from the Navigate panel to see the resource groups.

   ![](./media/update05.png)  
 
In this hands-on lab, you'll leverage Microsoft Sentinel and Microsoft Defender for Cloud to simulate attacks, create custom detections using KQL, and automate incident responses to enhance your organization's security operations.

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:

 - Email Support: labs-support@spektrasystems.com
 - Live Chat Support: https://cloudlabs.ai/labs-support

Now, click on Next from the lower right corner to move on to the next page.

![Start Your Azure Journey](./media/XDRintro6.png)

## Happy Learning!!

