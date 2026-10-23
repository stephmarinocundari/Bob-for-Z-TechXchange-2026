# LAB-3598: Modernizing mainframe applications with IBM Bob Premium Package for Z

**Hands-on lab guide** — IBM TechXchange 2026

## Table of Contents

1. [Introduction](#1-introduction)
   - 1.1 [About this hands-on lab](#11-about-this-hands-on-lab)
2. [Did not complete the lab?](#2-did-not-complete-the-lab)
3. [Lab overview](#3-lab-overview)
   - 3.1 [Use case 1 – Environment Setup and Familiarization](#31-use-case-1--environment-setup-and-familiarization)
   - 3.2 [Use case 2 – Technical Documentation Generation](#32-use-case-2--technical-documentation-generation)
   - 3.3 [Use Case 3 — Extract business rules](#33-use-case-3--extract-business-rules)
   - 3.4 [Use Case 4 — Run impact Analysis](#34-use-case-4--run-impact-analysis)
   - 3.5 [Use case 5 – Generate implementation plan](#35-use-case-5--generate-implementation-plan)
   - 3.6 [Use Case 6 — Implementing the Change](#36-use-case-6--implementing-the-change)
   - 3.7 [Deterministic AI Outcomes with Application Metadata](#37-deterministic-ai-outcomes-with-application-metadata)
   - 3.8 [Familiarization Walkthrough](#38-familiarization-walkthrough)
4. [Impact analysis and implementing a code change](#4-impact-analysis-and-implementing-a-code-change)
   - 4.1 [Setup environment](#41-setup-environment)
   - 4.2 [Generate technical documentation](#42-generate-technical-documentation)
   - 4.3 [Extract business rules](#43-extract-business-rules)
   - 4.4 [Run impact analysis](#44-run-impact-analysis)
   - 4.5 [Generate implementation plan](#45-generate-implementation-plan)
   - 4.6 [Implement the change](#46-implement-the-change)
5. [Getting help and troubleshooting](#5-getting-help-and-troubleshooting)
   - 5.1 [Reach out to the Lab instructor](#51-reach-out-to-the-lab-instructor)
   - 5.2 [Download and open the application code](#52-download-and-open-the-application-code)
   - 5.3 [Common troubleshooting tips](#53-common-troubleshooting-tips)
6. [Reference Materials](#6-reference-materials)
   - 6.1 [Learn more](#61-learn-more)
   - 6.2 [Product architecture](#62-product-architecture)

---

## 1 Introduction

IBM Bob Premium Package for Z is IBM's AI-powered developer assistant designed specifically for mainframe application development. IBM Bob is a partner for enterprise developers that plans, executes, validates, and governs multi-step modernization tasks across the SDLC. The Premium Package for Z adds deep mainframe expertise to accurately and efficiently modernize large, complex IBM Z applications. It brings together AI-powered capabilities with deep mainframe context awareness to understand complex programs, copybooks, Db2 schemas, CICS transactions, z/OS system conventions, and more.

Bob Premium Package for Z operates through two specialized modes:

- **Z Architect mode** enables implementation planning, impact analysis, system design documentation, and the generation of technical artifacts such as data dictionaries, architecture diagrams, and technical design documents — all grounded in the actual application code.
- **Z Code mode** allows users to explain, modify, refactor, and modernize mainframe applications through conversational prompts and prebuilt workflows. Developers can identify business rules, generate standards-aligned code, and implement changes identified using Z Architect mode.

### 1.1 About this hands-on lab

This hands-on lab provides a guided, end-to-end exploration of Bob Premium Package for Z across five key use cases that represent real-world mainframe development and modernization scenarios.

This lab uses Bank of Z, a hybrid banking application that demonstrates modern IBM Z development practices. It routes transactions through CICS or IMS depending on customer ID, with z/OS Connect as the API gateway between the browser-based UI and the z/OS transactional applications.

Download the sample code here: [GitHub demo material](https://github.com/IBM/Bank-of-Z)

By completing this lab, participants will be able to:

- Set up Bob Premium Package for Z in a local environment by scanning the workspace, initialize an AGENTS.md project context file, and generate a data dictionary that maps COBOL field names to their business meanings.
- Generate technical documentation, including a comprehensive technical design document with program inventory, code snippets, and Mermaid architecture diagrams, to provide greater visibility into the application.
- Identify and document business rules using prebuilt workflows to capture critical business logic, preserve institutional knowledge, and create a trusted foundation for application modernization, impact analysis, and future development efforts.
- Perform impact analysis by prompting Bob Premium Package for Z to trace every program and component affected by a proposed change.
- Implement the changes by switching to Z Code Mode and using the impact report to drive systematic, AI-assisted code updates across all affected COBOL programs.

## 2 Did not complete the lab?

If you did not finish all exercises during the session, you can continue working through the lab at any time using the self-paced version hosted on GitHub Pages.

Download the [sample code here](https://github.com/IBM/Bank-of-Z) and open it in the Bob IDE to pick up exactly where you left off.

If you need access to the Premium Package for Z, reach out to your lab instructors or IBM contact.

## 3 Lab overview

In this workshop scenario, participants will use Bob Premium Package for Z to add a new field "email address" to the customer information.

While the requested enhancement appears to be a simple update to a table, the change impacts application logic, dependencies, and downstream components across the system. Participants will use Bob to understand the business requirement, identify affected artifacts, assess the full impact of the change, generate an implementation plan, and safely update the application with confidence.

This lab is structured around five use cases that progress from initial environment setup through documentation, impact analysis, and implementing the code changes. Each use case builds on the previous one using the same Bank of Z banking application codebase.

### 3.1 Use case 1 – Environment Setup and Familiarization

Scan the workspace to build a local metadata database accessible by the AI model, initialize the AGENTS.md to automatically analyze your codebase and produce a concise configuration file, and generate a Data Dictionary that maps field names to their business meanings using the Generate Data Dictionary workflow. This provides a faster path to understanding application structure, data elements, and business context.

### 3.2 Use case 2 – Technical Documentation Generation

In Z Architect Mode, use the prebuilt workflow to generate a comprehensive technical design document for the application. The document includes program inventory, processing logic, and system architecture visualized with flow charts and diagrams. This accelerates knowledge transfer, reducing time spent manually documenting and analyzing the application.

### 3.3 Use Case 3 — Extract business rules

In Z Architect Mode, use the prebuilt workflow to identify and generate structured documentation for business logic in the programs, making it easier to understand application behavior and preserve critical business knowledge.

### 3.4 Use Case 4 — Run impact Analysis

In Z Architect Mode, prompt Bob to generate an impact analysis for updating the customer information with a new field for email address. Review the generated Impact-Analysis.md report to identify affected programs, copybooks, dependencies, and overall risk level. By understanding the full scope and potential impacts of a change before any code is modified, teams can reduce risk, avoid unintended consequences, and make more informed modernization and maintenance decisions.

### 3.5 Use case 5 – Generate implementation plan

In Z Architect Mode, prompt Bob to generate an implementation plan for updating the customer information with a new field for email address. Review the recommended implementation sequence, required updates, and validation considerations. By providing a structured, step-by-step approach to implementing changes, Bob helps development teams accelerate delivery, improve consistency, and execute updates with greater confidence while minimizing disruption to the application.

### 3.6 Use Case 6 — Implementing the Change

Switch to Z Code Mode and prompt Bob to implement the change. Bob will systematically update any fields, variables, and copybooks to execute the implementation plan. Review the different view for each file before approving, accelerating code changes while maintaining developer oversight and control.

### 3.7 Deterministic AI Outcomes with Application Metadata

The use cases in this lab demonstrate how AI can help teams understand, modernize, and document complex applications. While modern models are highly effective at analyzing code and generating insights, application metadata provides additional enterprise context that helps AI understand how applications, systems, data, and business processes are connected.

Most AI coding assistants rely primarily on source code and documentation, requiring them to infer application relationships, dependencies, and business context. Application metadata provides this information directly, giving AI access to trusted knowledge about application structures, dependencies, data flows, and business processes. By grounding AI in this context, models can deliver more deterministic, consistent, and accurate outputs while reducing token consumption by leveraging known relationships rather than repeatedly inferring them from code.

Application metadata enables AI to understand the broader application landscape, not just individual programs or repositories. This enterprise-wide perspective improves impact analysis, supports better decision-making, and provides insights that code-only AI tools often cannot.

While this lab focuses on a single sample application, the same principles apply to enterprise environments where applications, data, and business processes span thousands of interconnected components. As application landscapes grow in size and complexity, the value of application metadata becomes even greater.

### 3.8 Familiarization Walkthrough

1. **Open Bob** — The Bob chat window is on the right side of the IDE. The file explorer panel is on the left, where generated artifacts and source code will appear.
2. **Log into Bob** – Click "Log in to Bob". When prompted with the message "The extension 'IBM Bob' wants to sign in using Bob" click allow. Next, click "open" to open the external login website. Sign in using your IBM ID.
3. **Check your mode** — Click the mode icon at the bottom of the chat window. Confirm you can see Z Architect and Z Code modes. You will switch between these throughout the lab.
4. **Locate the sample code** — In the file explorer, expand the workspace folders. You should see the Bank of Z application and its associated programs and copybooks. If you do not see the code, refer to the trouble shooting section of this document for steps on how to download and open the code in Bob.
5. **Enable Auto Approve (optional)** — Click the Permissions dropdown near the mode selector and toggle Auto Approve on to reduce the number of manual approvals during long-running tasks.
6. **Open a chat session** — Click the **+** icon at the top of the chat window to start a fresh session. You will use this same pattern at the start of each use case.

## 4 Impact analysis and implementing a code change

For this exercise, you will use IBM Bob Premium Package for Z to add a new field to the customer information to collect email addresses.

Although the change seems straightforward, implementing it requires understanding the underlying business logic, identifying impacted application components, analyzing dependencies, and determining the safest path to make the change. Bob will help you explore the application, assess the impact, and guide the implementation from requirement to code update.

**Important notes to consider while completing the hands-on activities:**

- This hands-on lab uses an active AI model rather than pre-scripted responses. Your experience and results may vary based on prompts, context, and system behavior.
- If prompted for additional details (for example, field types or indicators), choose the responses that best match your preferences. Since this lab uses sample code, there are no wrong answers. Multiple responses may be valid, and your selections will not affect the lab outcome, generated results, or overall value demonstrated by the exercise. If you need help, raise your hand to ask a lab instructor.
- Since this is sample code on a test environment, some errors may appear, and some tasks may need to be re-run. Please re-run task or run diagnostics as needed.
- In case of any issues, re-run the task, refer to the trouble shooting section of this document, or raise your hand and a lab instructor will assist.

### 4.1 Setup environment

#### 4.1.1 AGENTS.md

AGENTS.md acts as a project context file that analyzes the codebase and provides Bob with insights into application, enabling more accurate documentation, analysis, and code recommendations.

1. To generate the AGENTS.md file, make sure you are in Z Code or Z Architect mode, and in the chat, type:

   ```
   /init
   ```

2. Click approve as prompted.
3. Review the output to gain a high-level understanding of the program, including its purpose, structure, key components, and dependencies. This context helps accelerate onboarding, improve analysis accuracy, and provides a stronger foundation for documentation, modernization, and future development activities.

#### 4.1.2 Data dictionary

A Data Dictionary documents data elements used throughout an application by mapping technical field names to their business meaning, helping developers quickly understand how data is used across the application and reducing the time required to analyze unfamiliar programs.

1. Run the **Generate data dictionary** workflow to get started. (Note: if you are viewing the AGENTS.md file, click the "IBM Bob Premium Package for Z" tab at the top of the screen.)
2. When prompted in the top search bar, hit enter to select "Run workflow in Bank-of-Z-main".
3. When prompted in the chat, click "browse files", then search and select program `BANKDATA.cbl` to create a data dictionary.
4. An editable data dictionary is generated in a Diff view. From here, we can review and edit, providing greater control and keeping the human in the loop. Once done, click **I'm done editing**.
5. In the background, the AGENTS.md file is updated to include the information from the data dictionary, enriching the application's business context and creating a more complete knowledge base for Bob. This enables more accurate analysis, documentation, impact assessments, modernization recommendations, and AI-assisted development workflows across the application lifecycle.

### 4.2 Generate technical documentation

Automatically generate technical documentation from existing source code (dependencies, processing logic, etc.), reducing the effort required to manually analyze code to gain insights into how applications operate.

1. Run the **Generate program documentation** workflow to get started.
2. When prompted in the top search bar, hit enter to select "Run workflow in Bank-of-Z-main".
3. When prompted in the chat, click "browse files", then search and select program `BANKDATA.cbl` to create a data dictionary.
4. Once the workflow completes, click the MD file link in the chat to open the documentation. You can right-click the file tab (top of screen) and click "open preview" to view the report in a formatted, readable layout.
5. Review the generated documentation to quickly understand the program's purpose, processing logic, dependencies, and key functions. This documentation helps accelerate knowledge transfer, reduce the effort required to analyze legacy code, and provides a trusted foundation for maintenance, impact analysis, modernization, and onboarding new team members.

### 4.3 Extract business rules

Extract and document business logic from your program, including a functional overview and rules inventory document. By converting embedded business logic into structured documentation, teams can more easily understand how key business process are implemented and reduce the effort required to analyze and maintain the application.

1. Run the **Extract business rules** workflow to get started.
2. When prompted in the top search bar, hit enter to select "Run workflow in Bank-of-Z-main".
3. When prompted in the chat, click "browse files", then search and select program `BANKDATA.cbl` to extra business logic.
4. Once the workflow completes, all extracted business rules will be listed in the chat. For each program containing business rules, two files have been created. The overview document helps you understand the purpose of a program, sorted by business function, sub-function, and business rule. The inventory document contains each business rule found, sorted by order of appearance in the program, and includes code snippets and variable tables.
5. To view a specific rule's information, click the MD file link in the chat. You can right-click the file tab (top of screen) and click "open preview" to view the report in a formatted, readable layout.

### 4.4 Run impact analysis

Impact analysis identifies all components that may be affected by a proposed change, helping teams understand the scope, complexity, and risk of an update before any code is modified. This reduces the likelihood of unintended downstream impacts, improves planning accuracy, and supports more confident decision-making.

1. Ensure you are in **Z Architect Mode**. In the chat, enter:

   ```
   Create an impact analysis to add a new field called email address to customer info
   ```

2. Approve each tool request as it appears.
3. If prompted for additional details (for example, field types or indicators), choose the responses that best match your preferences. Since this lab uses sample code, there are no wrong answers, and multiple responses may be valid. If you need help, raise your hand to ask a lab instructor.
4. Once Bob finishes its analysis, an `Impact-Analysis.md` file will be generated. If the file does not appear in the chat, click **Show All** next to the file count above the chat window, then select the `Impact-Analysis.md` file. For easier viewing, right-click the file tab at the top of the screen and select "open preview" to view the report in a formatted, readable layout.
5. Review the report, paying particular attention to scope (total programs and copybooks affected), risk level (High / Medium / Low), affected components, and dependency relationships. Understanding these insights helps teams assess change impact early, prioritize remediation efforts, and reduce implementation risk.

### 4.5 Generate implementation plan

Based on the impact analysis results, Bob generates a recommended implementation plan that outlines the safest and most efficient path for implementing the change. This provides development teams with a structured approach, improves coordination across affected applications, and helps reduce delivery risk while accelerating execution.

1. Ensure you are in **Z Architect Mode**. In the chat, enter:

   ```
   Turn this into an implementation plan
   ```

2. Approve each tool request as it appears.
3. If prompted for additional details (for example, field types or indicators), choose the responses that best match your preferences. Since this lab uses sample code, there are no wrong answers, and multiple responses may be valid. If you need help, raise your hand to ask a lab instructor.
4. Once complete, review the generated implementation plan, focusing on recommended implementation sequence, required code and data changes, dependencies between tasks, risk mitigation recommendations, and any validation and testing considerations.

### 4.6 Implement the change

Use Z Code Mode to execute the generated implementation plan, leveraging capabilities such as Z Code Scan to understand dependencies across the application and generate standards-aligned code updates across affected programs. By automating repetitive tasks while keeping developers in control through review and approval workflows, teams can accelerate delivery and improves consistency.

1. Switch to **Z Code Mode** by clicking the mode icon and selecting Z Code. In the chat, enter:

   ```
   Implement the changes
   ```

2. If prompted for additional details (for example, field types or indicators), choose the responses that best match your preferences. Since this lab uses sample code, there are no wrong answers, and multiple responses may be valid. If you need help, raise your hand to ask a lab instructor.
3. Bob will generate a to-do list of all changes it plans to make. It will execute tasks and updates in parallel, providing a Diff view of each change once complete. Click on an item to review the Diff view. Green lines indicate additions; red lines indicate removals. This transparent review process gives developers full visibility into proposed changes, helping validate accuracy, reduce risk, and maintain confidence in AI-assisted updates before they are applied.
4. Approve each tool request as it appears.
5. Once complete, Bob will display a summary of all changes made. This consolidated view makes it easier to understand the overall impact of the implementation, accelerate code reviews, document modifications, and ensure changes align with business requirements and development standards.

## 5 Getting help and troubleshooting

This section provides information about getting help with your lab and some common troubleshooting topics.

### 5.1 Reach out to the Lab instructor

If you need help during the hands-on lab, raise your hand and a lab instructor will assist.

If you need help after the event, please reach out to the following for any question!

Lab Instructors: Stephanie Marino-Cundari ([stephanie.marino@ibm.com](mailto:stephanie.marino@ibm.com)) and Tim McKeoun ([Timothy.McKeoun@ibm.com](mailto:Timothy.McKeoun@ibm.com))

### 5.2 Download and open the application code

In this exercise, you will use a sample application from GitHub and open it in the Bob IDE (located [here](https://github.com/IBM/Bank-of-Z)).

If the code is not already available in your lab environment, complete the download steps below. Otherwise, proceed directly to opening the code in Bob.

**Download the code:**

1. Open the GitHub repository (located [here](https://github.com/IBM/Bank-of-Z)).
2. Click **Code > Download ZIP** and save the repository to the local machine.
3. Extract the ZIP file to a convenient location.

**Open code in Bob:**

1. Launch the Bob IDE from the lab environment.
2. Select **Open Workspace**.
3. Browse to the extracted repository folder.
4. Click **Open** to load the project into the workspace.
5. Allow Bob to index the project files and display them in the Explorer view.
6. Expand the project folders and open a few source files to familiarize yourself with the application structure.

### 5.3 Common troubleshooting tips

| Issue | Solution |
|---|---|
| Modes (Z Code or Z Architect) does not appear | Ensure you are on the correct entitlement team. Verify that Z Open Editor (v6.8.0 or later) and Zowe Explorer are installed and activated. Please refresh Bob IDE. |
| Bob is not responding or analysis seems stuck | Do not close Bob. Some operations (especially workspace scans) run in the background and can take several minutes. Wait for the scan to fully complete before sending another prompt. |
| Approval dialog is not appearing | Scroll up in the chat window — approval cards sometimes appear above the visible area. If Auto Approve is on, the action may have already been processed. |
| AGENTS.md was not created after /init | Ensure you are in Z Architect Mode before running /init. If the file still does not appear, start a new chat session with the + button and try again. |
| Data Dictionary was not updated | During generation Bob will ask if you want to edit entries — select "I'm done editing" to confirm and complete the write. |
| The impact report references wrong files or shows no affected programs | Confirm the workspace scan completed successfully before running impact analysis. Re-run Scan the local workspace in Z Architect Mode if needed. |

## 6 Reference Materials

### 6.1 Learn more

Learn more with the following resources!

- [IBM Bob Premium Package for Z Product Page](https://www.ibm.com/products/ai-coding-agent/mainframe-modernization)
- [IBM Bob Premium Package for Z overview on Bob Docs](https://bob.ibm.com/docs/ide/premium-packages/bob-for-z/bob-for-z-index)
- [IBM Bob Premium Package for Z details on IBM Docs](https://www.ibm.com/docs/en/bobz/3.0.0)
- [IBM Bob YouTube](https://www.youtube.com/@ibm-bob)
- [IBM Bob Premium Package for Z Media Center Playlist](https://mediacenter.ibm.com/playlist/details/1_5fncfata/categoryId/189147203)

### 6.2 Product architecture

- Click [here](https://www.ibm.com/docs/en/bobz/3.x?topic=overview-solution-architecture-bob-premium-package-z-saas-deployment) to see the product architecture for IBM Bob Premium Package for Z SaaS.
- Click [here](https://www.ibm.com/docs/en/bobz/3.x?topic=overview-solution-architecture-premise-deployment) to see the product architecture for IBM Bob Premium Package for Z self-hosted, on-premise deployments.

---

## Notices and disclaimers

© 2026 International Business Machines Corporation. No part of this document may be reproduced or transmitted in any form without written permission from IBM.

U.S. Government Users Restricted Rights — use, duplication or disclosure restricted by GSA ADP Schedule Contract with IBM.

This document is current as of the initial date of publication and may be changed by IBM at any time. Not all offerings are available in every country in which IBM operates.

Information in these presentations (including information relating to products that have not yet been announced by IBM) has been reviewed for accuracy as of the date of initial publication and could include unintentional technical or typographical errors. IBM shall have no responsibility to update this information.

This document is distributed "as is" without any warranty, either express or implied. In no event, shall IBM be liable for any damage arising from the use of this information, including but not limited to, loss of data, business interruption, loss of profit or loss of opportunity. IBM products and services are warranted per the terms and conditions of the agreements under which they are provided. The performance data and client examples cited are presented for illustrative purposes only. Actual performance results may vary depending on specific configurations and operating conditions.

IBM products are manufactured from new parts or new and used parts. In some cases, a product may not be new and may have been previously installed. Regardless, our warranty terms apply.

Any statements regarding IBM's future direction, intent or product plans are subject to change or withdrawal without notice.

Performance data contained herein was generally obtained in a controlled, isolated environments. Customer examples are presented as illustrations of how those customers have used IBM products and the results they may have achieved. Actual performance, cost, savings or other results in other operating environments may vary.

References in this document to IBM products, programs, or services does not imply that IBM intends to make such products, programs or services available in all countries in which IBM operates or does business.

Workshops, sessions and associated materials may have been prepared by independent session speakers, and do not necessarily reflect the views of IBM. All materials and discussions are provided for informational purposes only, and are neither intended to, nor shall constitute legal or other guidance or advice to any individual participant or their specific situation.

It is the customer's responsibility to ensure its own compliance with legal requirements and to obtain advice of competent legal counsel as to the identification and interpretation of any relevant laws and regulatory requirements that may affect the customer's business and any actions the customer may need to take to comply with such laws. IBM does not provide legal advice or represent or warrant that its services or products will ensure that the customer follows any law.

Questions on the capabilities of non-IBM products should be addressed to the suppliers of those products. IBM does not warrant the quality of any third-party products, or the ability of any such third-party products to interoperate with IBM's products. IBM expressly disclaims all warranties, expressed or implied, including but not limited to, the implied warranties of merchantability and fitness for a purpose.

The provision of the information contained herein is not intended to, and does not, grant any right or license under any IBM patents, copyrights, trademarks or other intellectual property right.

IBM, the IBM logo, and ibm.com are trademarks of International Business Machines Corporation, registered in many jurisdictions worldwide. Other product and service names might be trademarks of IBM or other companies. A current list of IBM trademarks is available on the Web at "Copyright and trademark information" at: [www.ibm.com/legal/copytrade.shtml](http://www.ibm.com/legal/copytrade.shtml).
