# Google ADK

Google's ADK is an open source is an open-source framework for building AI agents in a modular, code-first way. AI Agents are Python Scripts that you pre-define to either regurgitate specific answers depending on a user's request, to call other LLM calls based on the user's request, or to perform actions.

## Purpose

An agent's ability to understand user requests and generate responses is powered by a Large Language Model (LLM). An agent needs to make secure calls to this external LLM service, which requires authentication credentials. Without valid authentication, the LLM service will deny the agent's requests, and the agent will be unable to function.

An example of a use case is in customer service, to restrict a live chatbot from answering questions incorrectly:
1. User asks a question about a particular service.
2. Agent receives request and processes query via LLM.
3. Agent can diversify request to different LLMs to process via tools like LiteLLM (in cases of LLM processing failure like hitting restrictions on ChatGPT, switching over to Claude to process request).
4. Once our user request is processed via LLM, Google ADK allows us to funnel request to most relevant pre-defined agent. For example: If a user asks for the weather or the current time, the request will be sent to the more relevant agent python script.
5. Agent returns the response to the user.

Details of this process are displayed in the following diagram.

[Google ADK Walkthrough](https://google.github.io/adk-docs/get-started/quickstart/)

![Google ADK Diagram](public/googleadk.png "Google ADK Diagram")

## Installation

#### Mac / Linux
source .venv/bin/activate

#### Windows CMD:
.venv\Scripts\activate.bat

#### Windows PowerShell:
.venv\Scripts\Activate.ps1

### Install ADK Python Package
pip install google-adk

