
## Project Title Ideas

Choose a title that is clear, concise, and highlights the agent's purpose:

* **AI-Powered Personalized Job Application Email Generator (n8n Agent)**
* **Smart Job Application Assistant with SMYKM Methodology (n8n Workflow)**
* **Automated "Show Me You Know Me" Email Agent for Job Seekers**
* **n8n AI Career Advancement Assistant**

---

## GitHub Repository Description

This will be the main `README.md` file in your GitHub repository. It should explain what the project is, how it works, and its benefits.

### Project Name: AI-Powered Personalized Job Application Email Generator

### Overview

This project features an n8n workflow designed to automate and personalize job application emails using an AI agent. Leveraging the "Show Me You Know Me" (SMYKM) methodology, this agent researches target companies, job roles, and hiring managers to craft highly customized and impactful emails that stand out to recruiters. The workflow integrates with Telegram for user input and output, Google Sheets for data management, and Gmail for email drafting and sending.

### Features

* **Personalized Email Generation:** Utilizes an AI agent (powered by Google Gemini) to create unique job application emails based on specific job descriptions, company details, and information about the hiring manager.
* **"Show Me You Know Me" Methodology:** The AI is meticulously prompted to research and synthesize authentic details about the human (hiring manager), the company, and the job role, ensuring genuine connection and relevance in the email.
* **No Placeholders:** A crucial rule enforced within the AI's instructions ensures that no generic placeholders are used in the final email, guaranteeing fully personalized content.
* **Automated Workflow:** Built on n8n, an open-source workflow automation platform, enabling seamless integration between various services.
* **Telegram Integration:** Users can interact with the AI agent directly via Telegram to initiate email generation and receive the drafted emails.
* **Google Sheets Integration:** The agent can interact with Google Sheets to retrieve or append data, such as target company lists or application statuses.
* **Gmail Integration:** Capable of sending personalized emails or creating drafts directly within Gmail.
* **Conversation Memory:** Maintains context through a buffered memory, allowing for more coherent and effective interactions.

### How It Works (Technical Flow)

The n8n workflow operates as follows:

1.  **Telegram Trigger:** The workflow is initiated when a user sends a message to the Telegram bot with job application details (e.g., job description, company name, hiring manager info).
2.  **AI Agent (Langchain Integration):** The core of the system, this node uses a Google Gemini Chat Model with a comprehensive system message outlining the SMYKM framework. It processes the user's input and leverages defined tools.
    * **Tools:**
        * **Google Sheets Tools:** `Get row(s) in sheet`, `Create sheet`, `Append row in sheet` for managing application data.
        * **Gmail Tools:** `Send a message`, `Create a label`, `Create a draft`, `Reply to a message`, `Get a thread` for email operations.
        * **Think Tool:** Guides the AI's reasoning process.
    * **Memory:** A `Simple Memory` (Buffer Window Memory) node stores conversational context, enabling the AI to refer to previous inputs and outputs.
3.  **Code Node (Output Formatting):** A JavaScript code node processes the AI's output, escaping special characters to ensure proper formatting when sent back to Telegram.
4.  **Telegram Send Message:** The final personalized email (or a request for more information) is sent back to the user via Telegram.

### Technologies Used

* **n8n:** Workflow Automation Platform
* **Google Gemini (via n8n's Langchain Integration):** AI Language Model
* **Telegram API:** Messaging Platform Integration
* **Google Sheets API:** Data Management
* **Gmail API:** Email Service Integration
* **JavaScript:** For custom logic within the Code node

### Setup and Installation

*(Here, you would detail the steps for someone to set up and run your n8n workflow. This typically includes:)*

1.  **Cloning the Repository:** `git clone [your-repo-link]`
2.  **n8n Setup:**
    * Instructions on how to import the `.json` workflow into n8n.
    * Guidance on setting up **credentials** for:
        * Telegram API (Bot Token)
        * Google Gemini API (API Key)
        * Google Sheets (OAuth2 credentials and sharing access to your sheet)
        * Gmail (OAuth2 credentials)
3.  **Telegram Bot Configuration:** Steps to create a new Telegram bot via BotFather and link it to n8n.
4.  **Google Sheet Preparation:** Details on the expected structure of the Google Sheet for `Get row(s)` and `Append row` operations (e.g., column headers).

### Usage

Provide clear instructions on how to interact with your Telegram bot to generate the emails.

* "To generate a job application email, send a message to the bot in the following format: `[Job Title] at [Company Name]. Hiring Manager: [Hiring Manager Name/Title]. Job Description: [Paste Job Description Here]. My relevant experience: [Briefly describe your experience relevant to the role].`"
* Provide examples of inputs and expected outputs.

### Contribution

* Mention if you are open to contributions and how others can contribute (e.g., bug reports, feature requests, pull requests).

---

## Resume Bullet Points

Here are some concise bullet points you can add to your resume under a "Projects" or "Technical Projects" section:

* **Developed an AI-Powered Job Application Assistant** using n8n and Google Gemini, automating the creation of highly personalized outreach emails based on the "Show Me You Know Me" (SMYKM) methodology.
* **Engineered an n8n workflow** integrating Telegram, Google Sheets, and Gmail APIs to streamline job application processes, significantly reducing manual effort in email drafting.
* **Designed a robust AI prompt engineering framework** enforcing strict "no placeholder" rules for email generation, ensuring authentic and unique communication.
* **Implemented conversational memory** within the AI agent to maintain context and enhance the quality of generated job application emails.
* **Demonstrated proficiency in workflow automation (n8n), AI integration (Langchain/Gemini), and API utilization (Telegram, Google Sheets, Gmail)** through a practical career advancement tool.

