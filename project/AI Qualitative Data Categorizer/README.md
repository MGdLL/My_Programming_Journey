# 🤖 Automated Comment Classifier with Gemini and Google Sheets

This project provides a **Sentiment Analysis and Comment Classification** solution integrated directly into **Google Sheets** using **Google Apps Script**. It utilizes the **Google Gemini API** to automatically analyze large volumes of text data (such as user comments, reviews, or support tickets) and classify them into predefined User Experience (UX/UI) categories.

The goal is to automate the manual labeling process and quickly obtain actionable insights into the issues reported by users.

---

## 🎯 Key Objectives and Features

* **AI Classification:** Uses the `gemini-pro` model to accurately categorize comments into specific categories like "User Experience (UI/UX)," "Performance and Stability," "Transfer Process," etc.
* **Batch Processing:** Implements a batch processing strategy (batches of 200 comments) to efficiently handle large datasets, respecting API quotas and limits.
* **Native Integration:** Runs directly from Google Sheets via a custom menu (`Gemini Tools`), eliminating the need for external tools.
* **Rapid Analysis:** Automatically transforms raw text data (Column A) into structured categories (Column B).

---

## 🚀 Requirements

1.  A **Google Account** (for Google Sheets and Google Apps Script).
2.  A valid **Gemini API Key**. You can obtain a key from Google AI Studio.

---

## 🛠️ Implementation Steps (Quick Guide)

Follow these steps to deploy and run the classifier in your own spreadsheet:

### 1. Initial Setup

1.  Open a new **Google Sheet**.
2.  Go to **Extensions > Apps Script**.
3.  Copy the content of the `Code.gs` file provided below and paste it into the Apps Script editor, replacing any existing content.

### 2. Insert the API Key

1.  Copy your **Gemini API Key**.
2.  In the Apps Script code, replace the value of the `API_KEY` variable with your key:

    ```javascript
    const API_KEY = 'YOUR_API_KEY_HERE'; 
    ```

3.  **Save the Project** (floppy disk icon).

### 3. Prepare Data and Run

1.  Go back to your Google Sheet and **paste the comments** you want to analyze into **Column A**, starting from **Row 2** (Row 1 is assumed to be the header).
2.  **Reload the Spreadsheet** (F5). A new menu called **"Gemini Tools"** will appear in the top bar.
3.  Click on **Gemini Tools** and select **"Process Comments"**.

### 4. Authorization (First time only)

* The first time you run the script, you will be prompted to review and **authorize** the necessary permissions for the script to connect to the external API. Follow Google's instructions to grant authorization.

