# Awesome Human Preference Datasets for LLM 🧑❤️🤖
A curated list of open source **Human Preference** datasets for LLM instruction-tuning, RLHF and evaluation.

For general NLP datasets and text corpora, check out [this](https://github.com/niderhoff/nlp-datasets) awesome list.


## Datasets
[**OpenAI WebGPT Comparisons**](https://huggingface.co/datasets/openai/webgpt_comparisons)
- 20k comparisons where each example comprises a question, a pair of model answers, and human-rated preference scores for each answer. 
- RLHF dataset used to train the [OpenAI WebGPT](https://arxiv.org/abs/2112.09332) reward model.

[**OpenAI Summarization**](https://huggingface.co/datasets/openai/summarize_from_feedback)
- 64k text summarization examples including human-written responses and human-rated model responses. 
- RLHF dataset used in the [OpenAI Learning to Summarize from Human Feedback](https://arxiv.org/abs/2009.01325) paper.
- Explore sample data [here](https://openaipublic.blob.core.windows.net/summarize-from-feedback/website/index.html#/tldr_comparisons).

[**Anthropic Helpfulness and Harmlessness Dataset (HH-RLHF)**](https://huggingface.co/datasets/Anthropic/hh-rlhf) 
- In total 170k human preference comparisons, including human preference data collected for [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/pdf/2204.05862.pdf) and human-generated red teaming data from [Red Teaming Language Models to Reduce Harms](https://arxiv.org/abs/2209.07858), divided into 3 sub-datasets:
    - A **base** dataset using a context-distilled 52B model, with 44k helpfulness comparisons and 42k red-teaming (harmlessness) comparisons.
    - A **RS** dataset of 52k helpfulness comparisons and 2k red-teaming comparisons using rejection sampling models, where rejection sampling used a preference model trained on the base dataset.
    - An iterated **online** dataset including data from RLHF models, updated weekly over five weeks, with 22k helpfulness comparisons.

[**OpenAssistant Conversations Dataset (OASST1)**](https://huggingface.co/datasets/OpenAssistant/oasst1)
- A human-generated, human-annotated assistant-style conversation corpus consisting of 161k messages in 35 languages, annotated with 461k quality ratings, resulting in 10k+ fully annotated conversation trees. 

[**Stanford Human Preferences Dataset (SHP)**](https://huggingface.co/datasets/stanfordnlp/SHP) 
- 385K collective human preferences over responses to questions/instructions in 18 domains for training RLHF reward models and NLG evaluation models. Datasets collected from Reddit.

[**Reddit ELI5**](https://huggingface.co/datasets/eli5)
- 270k examples of questions, answers and scores collected from 3 Q&A subreddits.

[**Human ChatGPT Comparison Corpus (HC3)**](https://huggingface.co/datasets/Hello-SimpleAI/HC3)
- 60k human answers and 27K ChatGPT answers for around 24K questions.
- Sibling dataset available for [Chinese](https://huggingface.co/datasets/Hello-SimpleAI/HC3-Chinese).

[**HuggingFace H4 StackExchange Preference Dataset**](https://huggingface.co/datasets/HuggingFaceH4/stack-exchange-preferences)
- 10 million questions (with >= 2 answers) and answers (scored based on vote count) from Stackoverflow. 

[**ShareGPT.com**](https://sharegpt.com/)
- 90k (as of April 2023) user-uploaded ChatGPT interactions.
- ~~To access the data using ShareGPT's API, see documentation [here](https://github.com/domeccleston/sharegpt#rest-api)~~ The ShareGPT API is currently disabled ("due to excess traffic"). 
- [Precompliled datasets](https://huggingface.co/datasets?sort=downloads&search=sharegpt) on HuggingFace.

[**Alpaca**](https://huggingface.co/datasets/tatsu-lab/alpaca)
- 52k instructions and demonstrations generated by OpenAI's text-davinci-003 engine for _self-instruct_ training.

[**GPT4All**](https://huggingface.co/datasets/nomic-ai/gpt4all_prompt_generations)
- 1M prompt-response pairs colleced using GPT-3.5-Turbo API in March 2023. [GitHub repo](https://github.com/nomic-ai/gpt4all).

[**Databricks Dolly Dataset**](https://huggingface.co/datasets/databricks/databricks-dolly-15k)
- 15k instruction-following records generated [by Databricks employees](https://www.databricks.com/blog/2023/04/12/dolly-first-open-commercially-viable-instruction-tuned-llm) in categories including brainstorming, classification, closed QA, generation, information extraction, open QA, and summarization.

[**HH_golden**](https://huggingface.co/datasets/Unified-Language-Model-Alignment/Anthropic_HH_Golden)
- 42k harmless data, same prompts and "rejected" responses as the Harmless dataset in [Anthropic HH datasets](https://huggingface.co/datasets/Anthropic/hh-rlhf), but the responses in the "chosen" responses are re-writtened using GPT4 to yield more harmless answers. The comparison before and after re-written can be found [here](https://huggingface.co/datasets/Unified-Language-Model-Alignment/Anthropic_HH_Golden). Empirically, compared with the original Harmless dataset, training on this dataset improves the harmless metrics for various alignment methods such as RLHF and DPO.
