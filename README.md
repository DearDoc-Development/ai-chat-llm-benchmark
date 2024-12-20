# Introduction to the Experiment

In the ever-evolving landscape of artificial intelligence and natural language processing, evaluating the performance of Large Language Models (LLMs) is crucial for optimizing chatbot platforms. This experiment aims to assess how different LLMs handle conversation management and data extraction tasks, which are essential components for delivering efficient and user-friendly chatbot experiences.

Following the development of an LLM based Chatbot Platform, we wanted to test a conversation, with a happy path using a real Chatbot, [Austin Podiatry](https://staging.hub.getdeardoc.com/c/chatbots/D3T5gTaFM139WhXNzmkF).

## Objective

The primary objective of this experiment is to evaluate the capabilities of various LLMs in:

- **Conversation Management**: The ability to maintain coherent, contextually appropriate, and engaging dialogues with users.
- **Data Management**: The effectiveness in accurately extracting and handling data provided during conversations.

By analyzing the performance of these models on both tasks, we seek to identify strengths and weaknesses, ultimately guiding the selection or improvement of models for specific applications within chatbot platforms.

## Methodology

### Conversation Selection

A real-world conversation comprising **12 interaction steps** was selected to simulate typical user engagements with a chatbot. This conversation includes a variety of user inputs, ranging from inquiries about services to scheduling appointments and providing personal information.

### Models Tested

The conversation was processed using different LLMs, including but not limited to:

- GPT 4 Turbo
- GPT 4o
- Gemini 1.5 Pro
- Gemini 1.5 Flash
- Claude 3.5 Sonnet

Other models have been tested as well, but not evaluated:
- GPT 4o Mini

### Data Collection

For each interaction step, the following data were collected:

- **Input**: The user's message to the chatbot.
- **Output**: The chatbot's response generated by the LLM.
- **Suggestion Chips**: Predefined suggestions provided by the chatbot to guide the conversation.
- **Extracted Data**: Information extracted from the conversation, such as appointment requests, personal details, and preferences.
- **Fulfilled Properties**: Specific data points successfully captured during the interaction (e.g., name, phone number, appointment date).
- **Performance Metrics**: Evaluations based on the following criteria:
  - **Response Relevance and Accuracy**: How relevant and accurate the chatbot's response is to the user's input.
  - **Contextual Consistency Across Turns**: The chatbot's ability to maintain context throughout the conversation.
  - **Appropriateness of Suggestions**: The relevance and helpfulness of the suggestion chips offered.
  - **Natural Language Quality**: The fluency and coherence of the chatbot's language.
  - **Hallucination Detection**: Monitoring instances where the chatbot provides incorrect or fabricated information.
- **Technical Metrics**:
  - **Input Tokens**: The number of tokens in the user's input.
  - **Output Tokens**: The number of tokens in the chatbot's response.
  - **Execution Time**: Time taken by the model to generate a response.
 
The raw files are available here: [Raw files](./raw_files)

### Manual Analysis

A manual analysis was performed for each interaction step to assess the performance metrics comprehensively. This involved reviewing the chatbot's responses and the extracted data against the expected outcomes based on the user's inputs.

The evaluated metrics are available here: [Evaluation Metrics](./metrics.md)

The results of the evaluation is available in Google Sheets: [LLM Benchmark Analysis](https://docs.google.com/spreadsheets/d/1jHPdlUuSo6NuTzmqVu0GO5Q4CYqO-RV01-IJ3LbIqsc/edit?usp=sharing)

## Sample Data Overview

Here's an example of how data was collected and analyzed for a single conversation processed by **GPT-4o**:

### Interaction Steps and Analysis

The conversation followed can be checked here: [Conversation Happy Path](./conversation.md)

Sample of an interaction step

1. **User Input**: *"What insurances do you accept?"*
   - **Chatbot Response**: Provided detailed information about accepted insurances and offered assistance.
   - **Suggestion Chips**: Included options like "Can I schedule an appointment?" and "What are your office hours?"
   - **Extracted Data**: No specific data extracted at this step.
   - **Performance Metrics**:
     - **Response Relevance and Accuracy**: 5 (Highly relevant and accurate)
     - **Contextual Consistency**: 5 (Maintained context effectively)
     - **Appropriateness of Suggestions**: 5 (Suggestions were relevant)
     - **Natural Language Quality**: 5 (Response was well-articulated)
     - **Hallucination Detection**: 5 (No incorrect information provided)
   - **Technical Metrics**:
     - **Input Tokens**: 2,263
     - **Output Tokens**: 94
     - **Execution Time**: 2,129 milliseconds

## Significance of the Experiment

By conducting this experiment and analyzing the collected data, we aim to:

- Understand how effectively LLMs can handle complex conversational flows.
- Identify potential areas of improvement in conversation management and data extraction.
- Provide insights into the selection of appropriate LLMs for specific chatbot functionalities.
- Enhance the overall user experience by optimizing response relevance, accuracy, and efficiency.

## Results

The main results are available here: [Experiment Results](./results.md)
We also created an analysis of the suggestions offered by AI since is a pure create task: [Suggesion Results](./suggestions.md)
