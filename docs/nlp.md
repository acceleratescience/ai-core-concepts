# Natural Language Processing


## Learning Objectives
This section will help you understand:

- What falls under the umbrella of Natural Language Processing (NLP)
- Some common NLP tasks
- Examples of NLP applied to scientific research


## What is NLP?

Natural Language Processing (NLP) is the umbrella term for techniques that involve processing text data. NLP is a large domain, and there are many opportunities to use NLP across a wide range of scientific disciplines. NLP techniques that are used in one domain are very easily transferred to another with just a change in the data being processed. A technique which works well on legal texts, for example, is likely to work well on medical text data. Or a model that has been trained on general text data can be tuned to work with scientific papers. Hence, if you anticipate processing text data in your research, it can be valuable to look to the NLP literature to understand what has been done in similar domains.

The field of NLP has been transformed by AI and machine learning. Supervised and unsupervised learning techniques have been applied across a range of text processing tasks in many different disciplines. The NLP field has had a key influence in transformer-based foundation models and generative AI.


## NLP Tasks

If you want to work with text data in your field, the chances are good that you'll want to use some kind of NLP technology. Many common NLP tasks exist, which have a long line of research into them, including:


- **Language Modelling** is the task of predicting the next word, like an autocomplete. It's the basis of recent progress in NLP relating to generative AI.
-  **Machine Translation** automatically translates text from a source language to a target language.
-  **Summarisation** is when a model is used to summarise a long piece of text into a shorter one.
-  **Question Answering** answering questions where the answer can be found in a text that has been provided. E.g. answering questions from a given textbook.
-  **Sentiment Analysis** analysing whether a piece of text is positive or negative in its sentiment.
-  **Named Entity Recognition** picking out certain key entities from a phrase. For example, picking out names of molecules, drugs or diseases from text.
-  **Text classification** assigns predefined categories to text documents such as genre of a paper.
-  **Coreference resolution** identifies which references to people or objects in a text are referring to the same entity, such as when “it” and “the paper” are referring to the same item
-  **Semantic similarity** is identifying whether two pieces of text have similar meanings
-  **Relation extraction** identifies relations between two entities in text, like “Paris is a city” or “the apple is green”.
-  **Word sense disambiguation** identifies which sense, or definition, of a word is being used, e.g. whether “bank” refers to a river bank or the financial institution.

Many of these tasks have well established benchmark datasets, which researchers use to evaluate the performance of these models in different domains.



## Examples of NLP in Scientific Research

NLP models are typically trained using text data from the internet. This data is often selected to have a broad coverage of general topics. Researchers wanting to use NLP techniques in a specific domain or field may need to collect text from that domain for their models, to capture the kinds of vocabulary and phrases that are used.

There are many sources of text data available to researchers. Examples of NLP work on data sources that researchers might be interested in include:

- NLP techniques help researchers search through scientific literature, provide summaries, answer questions about papers and find new papers that are similar to existing papers. 
- Language models can be built using electronic health records, which can then be used for tasks like extracting medical concepts and question answering.
- NLP models monitor changing sentiment about events such as covid-19 from social media data
- NLP can be used to analyse legal texts and policy documents, providing researchers with key points about those policies

!!! abstract "Case Study: NLP in the Legal Domain"
    **Dr Felix Steffek**

    In fields with large amounts of text data, like law, Natural Language Processing can provide a toolbox to explore and analyse data in new ways. 

    The first example of NLP in law is of identifying facts in legal documents. Large language models like GPT4 or BERT can be used to identify facts, claims, references to precedents or legal statutes, and other key information from dense legal text documents. This can make it easier and faster to analyse these texts.

    A second example of NLP in law is of classifying documents, here employment tribunal judgements. In this work, the classes were the outcomes of the case - whether the claimant won, lost, or partly won the case. Language models were used to classify cases, and compared against annotations from legal experts. In baseline experiments, human experts were better at predicting cases with a clear win or loss, while the AI models did better in more complex cases where the claimant only partly wins or where the court renders another decision, such as an order to produce further evidence. 

    As with all AI approaches, the data matters. Having large and comprehensive datasets in a domain like law can accelerate research. The [Cambridge Law Corpus](https://arxiv.org/abs/2309.12269) is a set of 250,000 court cases together with annotations on case outcomes for 638 cases as carried out by legal experts. 

    AI will fundamentally change the way law is applied, made and researched. Our aim is to accompany this process by showing what works and what does not yet work. Legal AI benefits from a dynamic trinity: there is potential for progress, it is scientifically interesting, and it matters to people. 


## Resources

NLP & generative AI are covered in our 1-day workshop on [Large Language Models](https://docs.science.ai.cam.ac.uk/large-language-models/). The material and associated code are available online.

## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





