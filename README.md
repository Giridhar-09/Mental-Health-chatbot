# Mental-Health-chatbot
 This chatbot is designed to provide initial mental health support and conduct standardized assessments (PHQ-9, GAD-7, PCL-5).
 
# AI-Powered Mental Health Assessment Chatbot

This project is an advanced, multi-language chatbot designed to conduct preliminary mental health screenings using standard clinical questionnaires. It features a conversational interface for users and a secure, separate interface for doctors to review results. The chatbot is built with powerful language models to understand user input in natural language.

## Overview

The notebook creates a complete, interactive mental health support tool that can be run in a Google Colab or Jupyter environment. It guides users through well-established assessments for depression, anxiety, and PTSD. The system is designed with a dual-user approach: a welcoming, supportive interface for the user seeking help, and a password-protected dashboard for a clinician or doctor to view, analyze, and follow up on the assessment results [2].

## Features

*   **Standard Clinical Assessments**: The chatbot administers three widely-used mental health screening tools [2]:
    *   **PHQ-9**: For screening, monitoring, and measuring the severity of depression.
    *   **GAD-7**: For screening and measuring the severity of generalized anxiety disorder.
    *   **PCL-5**: For assessing symptoms of Post-Traumatic Stress Disorder (PTSD).
*   **Multi-Language Support**: The chatbot is fully operational in **five languages**: English, Hindi, Telugu, Malayalam, and Kannada. Users can switch languages at any point during the conversation [2].
*   **Natural Language Understanding (NLU)**: Powered by a `bert-base-uncased` model, the chatbot can interpret both numeric scores (e.g., "2") and descriptive, natural language responses (e.g., "I feel down most days") [2].
*   **Dual-Interface System**:
    *   **User Chat Interface**: An interactive and user-friendly chat window for taking the assessments [2].
    *   **Doctor Dashboard**: A separate, password-protected tab where a doctor can log in to view a summary of all patient results, examine detailed responses, and write an analysis [2].
*   **Crisis Detection**: The system automatically scans user messages for keywords indicating a potential crisis (e.g., self-harm) and provides an immediate supportive message [2].
*   **Email Integration**: A doctor can send their analysis and the assessment summary directly to the user's email from the dashboard. (Requires SMTP server configuration) [2].

## Tools and Architecture

The chatbot is built using a modern stack of Python libraries for machine learning and web interfaces [2]:
*   **Core Framework**: PyTorch for the deep learning backend.
*   **Language Models**: The Hugging Face `transformers` library is used to load and run the `bert-base-uncased` model for text classification and embedding.
*   **Data Handling**: `pandas` and `numpy` are used for managing and processing patient data.
*   **Web Interface**: `Gradio` creates the interactive, user-friendly chat interface and the doctor's dashboard.

## Installation and Setup

To run the chatbot, first install the necessary Python packages using the command included in the notebook [2]:


pip install torch transformers scikit-learn pandas numpy matplotlib seaborn gradio


Before launching the application, you may need to configure the following in the notebook:
1.  **Doctor's Password**: Change the default password in the `DoctorInterface` class instance for security.
2.  **Email SMTP Server**: To enable the "Send Email" feature, update the `send_email` function with your own SMTP server address, port, and login credentials [2].

## How to Use

The notebook is organized for a straightforward workflow.

1.  **Launch the Interface**: Run all cells in the Jupyter notebook. This will start the Gradio web server and display the chat interface.
2.  **User Interaction**:
    *   The user is greeted by the chatbot and asked for their name and email.
    *   The user selects which assessment they want to take (PHQ-9, GAD-7, or PCL-5).
    *   The chatbot asks questions one by one. The user can reply with a number or describe how they feel.
    *   After the final question, the results are saved for the doctor.
3.  **Doctor Interaction**:
    *   Navigate to the "Doctor Interface" tab.
    *   Enter the password to unlock the dashboard.
    *   View all completed assessments in a table. Click a row to see detailed answers for a specific user.
    *   Write an analysis in the text box and click "Send Analysis to User via Email" to send the feedback [2].

## Customization Guide

The chatbot is highly customizable:

*   **Add More Languages**: You can add a new language by updating the `translations` dictionary in the `MultiLanguageSupport` class. You will need to provide translations for all UI elements, questions, and response options [2].
*   **Add New Questionnaires**: You can add a new clinical assessment by creating a new function in the `MentalHealthQuestionnaires` class and adding it to the main questionnaire dictionary. This includes defining its name, description, questions, options, and scoring scale [2].
*   **Change the Language Model**: The `BERTProcessor` class can be modified to use a different pre-trained model from Hugging Face by changing the model name in its initializer.
```

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/76397965/60b47cfe-824c-4ce4-ba3f-0c7056f004ad/MentalHealthChatbotBertFalcon7_B.ipynb)
