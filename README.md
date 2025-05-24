
# ExpenseInsight AI

ExpenseInsight AI is a web application designed to help you gain valuable insights into your spending habits and receive personalized financial advice. By inputting or uploading your expense data, you can leverage the power of generative AI to analyze your finances and chat about the findings.

## Core Features

1.  **Expense Input**:
    *   **Manual Entry**: Type or paste your expense data directly into a text area.
    *   **File Upload**: Upload your expenses from common file formats:
        *   CSV (`.csv`)
        *   Text files (`.txt`, `.c`)
        *   Excel Spreadsheets (`.xlsx`, `.xls`)
    The content from uploaded files is loaded into the input area for analysis.

2.  **AI-Powered Insights**:
    *   Click "Get Insights" to have an AI model analyze your provided expense data.
    *   The AI provides a detailed breakdown focusing on:
        *   **Spending Habits**: Identifies categories with significant spending and noteworthy patterns.
        *   **Potential Impulsive Purchases**: Flags expenses that might indicate impulsive buying behavior with reasoning.
        *   **Personal Health & Wellness**: Analyzes spending related to health (gym, healthy food) versus potentially unhealthy habits (fast food, alcohol).
        *   **Expense Management Advice**: Offers practical, personalized tips for better expense management based on the analysis.
        *   **Overall Financial Picture**: Gives a brief overview of what the expenses suggest about financial priorities or lifestyle.
    *   Insights are presented in a readable Markdown format.

3.  **Configurable AI Backends**:
    *   Access AI model settings via the **Settings icon** (cogwheel) in the header.
    *   Choose from various AI models and providers, all accessed through the **OpenRouter API**:
        *   `meta-llama/llama-3.3-70b-instruct` (Provider: Cerebras)
        *   `qwen/qwen3-32b` (Provider: Cerebras - using parameters from a typical direct Cerebras usage snippet)
        *   `qwen/qwen3-30b-a3b:free` (Provider: Chutes)
    *   The selected backend is used for both initial insights generation and chat responses.

4.  **API Key Management (UI)**:
    *   In the settings popover, you can enter your **OpenRouter API Key**. This key is stored in your browser's local storage and takes precedence over environment variables. It's required for all AI functionalities.
    *   A field for a **Cerebras API Key** is also available for potential future direct Cerebras SDK integrations (currently not used by the OpenRouter-based flows).

5.  **Interactive Chat Window**:
    *   After insights are generated, a chat window appears on the right (on desktop) or below the main content (on mobile).
    *   Ask follow-up questions about your original expenses or the AI-generated insights.
    *   The chat AI uses the same selected backend and is aware of the original expense data and the initial insights provided.
    *   Chat responses are also formatted using Markdown.

6.  **User Experience**:
    *   **Toast Notifications**: Receive notifications for successful operations (e.g., insights generated, chat response received, file loaded) and errors. These also display the time taken for AI processing.
    *   **Clear Input**: Easily clear all expense input, generated insights, and chat history.
    *   **Responsive Design**: The application is designed to work on both desktop and mobile devices.

## Technology Stack

*   **Frontend**: Next.js, React, TypeScript
*   **UI Components**: ShadCN UI
*   **Styling**: Tailwind CSS
*   **Generative AI Orchestration**: Genkit
*   **AI Model Access**: OpenRouter API (connecting to various models/providers like Cerebras, Chutes)

## How to Use

1.  Navigate to the application.
2.  (Optional) Click the **Settings icon** (cogwheel) to configure your OpenRouter API key and select your preferred AI backend. An OpenRouter API key is required.
3.  Enter your expenses by:
    *   Typing or pasting them into the text area.
    *   Clicking "Upload File" and selecting a `.csv`, `.txt`, `.c`, `.xlsx`, or `.xls` file.
4.  Click the "**Get Insights**" button.
5.  Review the generated insights in the main panel.
6.  Use the chat window that appears to ask follow-up questions.
7.  Click "Clear" to reset the application state.

This application aims to provide a user-friendly way to leverage advanced AI for personal financial understanding and improvement.
