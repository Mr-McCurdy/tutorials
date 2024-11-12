# Creating Quizzes on Canvas with Google Colab and ChatGPT

Welcome to this step-by-step tutorial on how to create quizzes on Canvas using a Google Colab notebook and ChatGPT. This guide will walk you through the entire process, from setting up your environment to uploading your first quiz to Canvas.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setting Up the Google Colab Notebook](#setting-up-the-google-colab-notebook)
3. [Configuring Your Canvas Credentials](#configuring-your-canvas-credentials)
4. [Generating Quiz Questions with ChatGPT](#generating-quiz-questions-with-chatgpt)
5. [Uploading the Quiz to Canvas](#uploading-the-quiz-to-canvas)
6. [Conclusion](#conclusion)

---

## Prerequisites

Before we begin, ensure you have the following:

- A [Google](https://www.google.com/) account to access [Google Colab](https://colab.research.google.com/).
- A [Canvas](https://www.instructure.com/canvas/) account with API access.
- A Canvas API key and Course ID.
- Access to [ChatGPT](https://chat.openai.com/) for generating quiz questions.
- Basic knowledge of Python (optional but helpful).

---

## Setting Up the Google Colab Notebook

1. **Access the Google Colab Notebook:**

   Open your web browser and navigate to the Google Colab notebook template provided [here](https://colab.research.google.com/). Alternatively, you can use your own Colab notebook.

2. **Copy the Notebook (If Using a Template):**

   If you’re using a shared template, make a copy to your Google Drive by clicking on `File` > `Save a copy in Drive`.

3. **Familiarize Yourself with the Notebook:**

   Review the cells in the notebook to understand where you'll be inputting your Canvas credentials and quiz questions.

---

## Configuring Your Canvas Credentials

To interact with Canvas’s API, you need to provide your Canvas API key and Course ID in the Colab notebook.

1. **Locate Your Canvas API Key and Course ID:**

   - **Canvas API Key:** 
     - Log in to your Canvas account.
     - Navigate to `Account` > `Settings`.
     - Scroll down to `Approved Integrations` and click on `+ New Access Token`.
     - Generate a new API key and copy it.
   
   - **Course ID:** 
     - Navigate to the specific course on Canvas.
     - Look at the URL in your browser. It will look something like `https://yourinstitution.instructure.com/courses/12345`.
     - The number at the end (`12345` in this example) is your Course ID.

2. **Amend the Colab Notebook with Your Credentials:**

   In the Colab notebook, locate the section where you need to input your Canvas API key and Course ID. Replace the placeholder text with your actual credentials.

   ```python
   # Canvas API Configuration
   CANVAS_API_KEY = "YOUR_CANVAS_API_KEY"
   COURSE_ID = "YOUR_COURSE_ID"
   ```

## Generating Quiz Questions with ChatGPT

To create a `quiz_questions` object, you'll interact with ChatGPT using a specific prompt. Follow these steps:

1. **Open ChatGPT:**

   Navigate to <a href="https://www.chatgpt.com" target="_blank">ChatGPT</a> and ensure you're logged in.

2. **Copy and Paste the Following Prompt into ChatGPT:**

    ```plaintext
    I am creating a multiple-choice quiz for my Canvas course. Please generate a `quiz_questions` python object with 5 questions. Each question should have the following structure:

    quiz_questions = [
        {
            "question": "Question text here",
            "options": ["Option A", "Option B", "Option C", "Option D"],
            "answer": "Correct Option Letter"
        }
    ]
    ```
   <!-- Centered and resized image using HTML tags -->
   <p align="center">
     <img src="../assets/test.gif" alt="test" width="600">
   </p>

3. **Execute the Prompt:**

    Press "Enter" to send the prompt to ChatGPT. Wait for the AI to generate the quiz_questions object.

4. **Copy and Paste the Generated `quiz_questions` Object into Colab Template**

    Once ChatGPT provides the python `quiz_questions` object, copy and paste in to replace the `quiz_questions` object in the Colab template.
