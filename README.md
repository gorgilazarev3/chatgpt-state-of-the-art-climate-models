
# ChatGPT and State-of-The-Art Climate Models

This repository contains the Notebooks (code) and Datasets that were used for the research paper ChatGPT and State-of-The-Art Climate Models.
\
This study explores how 
ChatGPT, as a general-purpose model, performs in the context of a real-world challenge such as climate change 
compared to ClimateBert, a state-of-the-art language model specifically trained on climate-related data from various 
sources, including texts, news, and papers. ClimateBert is fine-tuned on five different NLP classification tasks, making 
it a valuable benchmark for comparison with the ChatGPT on a variety of NLP tasks. The main results show that for 
climate-specific NLP tasks, ClimateBert outperforms ChatGPT.




## Experiments

In order to evaluate how ChatGPT performs compared to ClimateBert, the current state-of-the-art model for climate-related NLP tasks, we performed multiple experiments that allowed us to evaluate the performance of ChatGPT on classification tasks. For the evaluation of the ClimateBert models, the appropriate fine-tuned model was loaded, the predictions were received and then compared to the actual labels in order to get the results. As for ChatGPT, we used a few approaches, including our own prompts, used techniques for better prompt engineering and using a third-party library [Scikit LLM](https://github.com/iryna-kondr/scikit-llm)
\
Summarized, the ChatGPT experiments were grouped in the following approaches:
- Simple single-stage prompts - in which we utilize manually designed prompts
- Complex multi-stage prompts - in which we explored the use of multiple prompt engineering techniques to assess the extent of performance improvement compared to the simple single-stage prompts
- Classification using off-the-shelf Scikit-LLM library - in which we used the Scikit-LLM library that provides the ability to use ChatGPT as a Zero Shot Classifier
 





## Structure of the repository

The repository is structured in such a way that each of the approaches has its own subfolder and in each of the approaches folders, there are Notebooks with the required scripts for running each of the Classification tasks using each of the approaches.
\
Each task is in its own Notebook and contains descriptions on what kind of task they are, the prerequisites that need to be performed in order to be able to run the task and explanations of parts of the code, such that it is understandable for everyone.
## Running the experiments

In this repository, via the structure described in the section above we have provided Notebooks that contain the code for running the experiments.
\
The experiments can be performed by running the appropriate cells in the Notebooks, either all at once, by running the collapsed section in the Notebook or running the cells one by one.

### Setup

The only setup that is required in order to run the ChatGPT experiments is that you need to get your OpenAI keys and set them in the Notebooks. The procedure for setting up the keys is described in the Notebooks that require it.
\
You need to create an account on OpenAI platform in order to be able to get your API key.
\
After creating your account, you can find your API key by following either of these articles: [Article 1 - OpenAI.com](https://help.openai.com/en/articles/4936850-where-do-i-find-my-secret-api-key)
 or [Article 2 - Medium.com](https://tfthacker.medium.com/how-to-get-your-own-api-key-for-using-openai-chatgpt-in-obsidian-41b7dd71f8d3) 
 \
The organization key can be found by following this tutorial: [Tutorial to get OpenAI API Key and Organization ID](https://docs.texti.ai/how-to-get-an-openai-api-key-and-organization-id)
\
\
The approaches for storing these keys and using these keys is explained in each of the Notebooks for utilization of ChatGPT for climate-related classificaton tasks.
\
The easiest approach is to store the keys in separate files and upload them to your Google Drive. Then your Google Drive can be mounted as a folder to the Notebook and the paths to the keys need to be placed where it is noted in the Notebooks, in these places: `Here put the path to your OpenAI API key` or `Here put the path to your OpenAI organization key`.
\
\
Additionally, in some of the notebooks the results are being saved into a file on Google Drive, with a path like this: `/content/drive/MyDrive/DS-Environment-Project/ChatGPT Results/scikit-llm/chatgpt_climate_sentiment.csv`. This step is optional and can be ommitted. If you choose to run these cells and save the results on your Drive, you need to change the path to one that represents some location on your Drive.
\
\
This setup is only required for running the Notebooks that utilize ChatGPT, it is not required for running the ClimateBert models.

### Execution of the Notebooks

First, if the Notebook requires the setup for OpenAI, it needs to be performed.
\
\
Once the setup is done, the appropriate Notebook can be opened in Google Colab or any alternative Jupyter Notebook environment and the cells need to be run. You can either run all cells at once, by collapsing the section and then running the whole section, or by running the cells one by one and optionally ommitting the execution of those cells that is noted that can be skipped.
\
\
After running the Notebook, at the end, the results will be displayed.