# AI-powered-EMail-Analyzer

📧 Email Assistant Chatbot

Overview

This project is an Email Assistant Chatbot built using Streamlit and Google's Gemini AI model. It allows users to generate fake emails for testing purposes and interact with an AI-powered chatbot for email-related tasks, such as querying, reading, deleting, forwarding, and replying to emails. A local NoSQL database (Shelve) is used to store and retrieve email data.

Features

Generate and store fake emails for testing.

View recent emails stored in a local NoSQL database.

Chat with an AI-powered assistant to manage email-related tasks.

Prerequisites

Before running this project, ensure you have the following installed:

Python 3.8+

Required Python libraries:

streamlit

google-generativeai

shelve

faker

You can install the required dependencies using:

pip install streamlit google-generativeai faker

Setup and Running the Project Locally

Clone the repository:

git clone <repository_url>
cd <repository_folder>

Install the required dependencies (if not already installed):

pip install -r requirements.txt

Set up your Google Gemini API key by modifying the following line in main.py:

ai.configure(api_key="YOUR_GOOGLE_GEMINI_API_KEY")

Run the Streamlit application:

streamlit run main.py

Open the browser to the URL displayed (usually http://localhost:8501).

API Endpoints and Their Usage

This application does not expose separate API endpoints but interacts within the Streamlit UI. Below is how different components work:

Generate Fake Emails: When the "Generate Fake Emails" button is clicked, 10 fake emails are stored in a local NoSQL database.

Retrieve Emails: The recent 5 emails are fetched from the database and displayed in the UI.

Chatbot Interaction: The chatbot is configured to understand various email management tasks and responds based on user queries.

Example Test Cases

1. Generating Fake Emails

Test Case: Click the "Generate Fake Emails" button.
Expected Output: A success message confirming that 10 fake emails have been stored.

2. Retrieving Emails

Test Case: View the "Recent Emails" section.
Expected Output: The UI should display a list of the 5 most recent stored emails.

3. Chatbot Response

Test Case: Enter "Show me my recent emails" in the chatbot input box and click "Send".
Expected Output: The chatbot should list the recent stored emails.

4. Invalid Chatbot Input

Test Case: Enter an unrelated question like "What is the weather today?" and click "Send".
Expected Output: The chatbot should provide a response indicating that it can only assist with email-related queries.

Future Enhancements

Implement actual email sending and receiving features.

Add user authentication for personalized email management.

Integrate with a real email provider like Gmail API.

Author
Developed by Yalamuri Yaswanth.
