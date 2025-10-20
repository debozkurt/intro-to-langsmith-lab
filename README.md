# Intro to LangSmith

Welcome to Intro to LangSmith!

## Introduction
In this course we will walk through the fundamentals of LangSmith - exploring observability, prompt engineering, evaluations, feedback mechanisms, and production monitoring. Take a look at the setup instructions below so you can follow along with any of our notebook examples.

---

## Setup
Follow these instructions to make sure you have all the resources necessary for this course!

### Clone the repo: 
```bash
git clone https://github.com/debozkurt/intro-to-langsmith-lab.git
```
### Create your .env file: 
```
$ cd intro-to-langsmith-lab/
$ mv .env.example .env
```

### Sign up for LangSmith
* Sign up [here](https://smith.langchain.com/) 
* Navigate to the Tracing Projects page, and create a new project (upper right hand corner)
* Select "Generate API Key"
* This generates all environment variables necessary
* Copy environment configuration that LangSmith prepopulates

### Set OpenAI API key
* If you don't have an OpenAI API key, you can sign up [here](https://openai.com/index/openai-api/).
* Your OpenAI API keys are managed [here](https://platform.openai.com/api-keys)
* Create your key (upper right hand corner of [API key manager](https://platform.openai.com/api-keys))
* Set `OPENAI_API_KEY` in the .env file.

When you are done, your .env should be configured likeso: 
```
export LANGSMITH_TRACING=true
export LANGSMITH_ENDPOINT=https://api.smith.langchain.com
export LANGSMITH_API_KEY=<your_langsmith_key>
export LANGSMITH_PROJECT=<your_tracing_project_title>
export OPENAI_API_KEY=<your-openai-api-key>
```

### Create an environment and install dependencies (do this only once)
```
$ cd intro-to-langsmith-lab/
$ python3 -m venv intro-to-ls
$ source intro-to-ls/bin/activate
$ pip install -r requirements.txt
```
For subsequent usage, activate your python environment from intro-to-langsmith-lab/: 
```
source intro-to-ls/bin/activate
```
. . and select it for use with your notebooks.

#### Open **intro-to-langsmith-lab/notebooks/module_1/1_tracing_basics.ipynb** up in your IDE or Jupyter Notebook manager of choice

### Self-Hosted LangSmith
Note: If you are using a self-hosted version of LangSmith, you'll need to set this environment variable in addition to the others - see this [guide](https://docs.smith.langchain.com/self_hosting/usage) for more info
```
LANGSMITH_ENDPOINT = "<your-self-hosted-url>/api/v1"
```
