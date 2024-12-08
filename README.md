# p4-Implementation-of-chatbot-Using-NLP

# Banking Chatbot

This project implements a simple banking chatbot using **Streamlit**, **scikit-learn**, and **Natural Language Processing (NLP)**. The chatbot is designed to help users with common banking tasks, such as checking account balances, viewing transaction history, transferring funds, and more. The chatbot uses a machine learning model (Naive Bayes classifier) trained on sample intents and responses.

## Features
- **Check Account Balance**: Get the current balance of the user's account.
- **Transaction History**: Retrieve recent transactions of the user.
- **Fund Transfers**: Transfer money between accounts or to other users.
- **Account Details**: Check account holder details and type.
- **Bill Payments**: Assist with utility bill payments.
- **Loan Information**: Retrieve loan status, payments, and other loan-related details.
- **Account Management**: Manage activities like account opening, closure, contact updates, password changes, and security alerts.
  
## Technologies Used
- **Streamlit**: For building the interactive web app interface.
- **scikit-learn**: For text classification using machine learning models.
- **Naive Bayes Classifier**: A classification algorithm used to predict intents based on user input.
- **CountVectorizer**: A method from `scikit-learn` to convert text data into numerical vectors.

## Installation Instructions

### Requirements:
1. Python 3.7 or later
2. Pip for installing nltk,punkt,sklearn

### Steps:
1. Clone the repository:
    ```bash
    git clone https://github.com/Kavana89/p4-Implementation-of-chatbot-Using-NLP.git
    cd p4-Implementation-of-chatbot-Using-NLP
    ```

2. Install the required dependencies:
    ```bash
    pip install nltk
    pip install sklearn
    ```

3.Ensure the dataset (CSV file) is present in the specified directory (`"C:\\Users\\kavan\\Downloads\\banking instent.csv"`). 

4. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

5. The app will open in your default web browser. You can start interacting with the chatbot right away.

## How it Works
- The chatbot uses a simple machine learning pipeline with a `CountVectorizer` to convert user input into a numeric form. Then, the `MultinomialNB` model predicts the intent behind the input.
- Based on the predicted intent, a random response from predefined sets of responses is chosen and displayed to the user.
  
### Key Functions
- **preprocess_data(intents)**: Processes the input data (intents, patterns, and responses) and prepares them for training.
- **get_response(user_input)**: Cleans the user input, predicts the intent using the trained model, and returns a corresponding response.

## Sample Intents and Responses
Here are some examples of the available intents:

- **check_balance**:
    - Patterns: "What's my account balance?", "How much money do I have?", etc.
    - Responses: "Your current account balance is $1,500."

- **transaction_history**:
    - Patterns: "Show me my transaction history.", "What are my recent transactions?", etc.
    - Responses: "Here are your last 5 transactions: \n1. $100 - Grocery Store\n2. $50 - Gas Station..."

- **transfer_funds**:
    - Patterns: "Transfer money to my friend.", "Send $500 to my savings account.", etc.
    - Responses: "Please provide the account number and amount to transfer."

- **loan_payment**:
    - Patterns: "I want to make a loan payment.", "Pay my loan installment.", etc.
    - Responses: "Please provide the payment amount and method to proceed with the loan payment."

