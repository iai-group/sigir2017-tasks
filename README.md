# Generating Query Suggestions to Support Task-Based Search

This repository provides resources developed within the following article:

> D. Garigliotti and K. Balog. **Generating Query Suggestions to Support Task-Based Search.** In: Proceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR '17). ACM. Tokyo, Japan. August 2017. [DOI: 10.1145/3077136.3080745](https://doi.org/10.1145/3077136.3080745)

**You can get the author version of the article [here](https://arxiv.org/abs/1708.08289).**


### Abstract

> *We address the problem of generating query suggestions to support users in completing their underlying tasks (which motivated them to search in the first place). 
Given an initial query, these query suggestions should provide a coverage of possible subtasks the user might be looking for. 
We propose a probabilistic modeling framework that obtains keyphrases from multiple sources and generates query suggestions from these keyphrases. 
Using the test suites of the TREC Tasks track, we evaluate and analyze each component of our model.*


## NOTE:

- Each file under a subdirectory whose name includes `converted` is in the usual format of an input run file for the `trec_eval` command.
    - Files in the datasets have been *converted* from the original, such that they are in the format of the input qrels file for the `trec_eval` command. Also, all spaces are replaced by underscores in every query or keyphrase.
    - Run files have been converted with the same criteria, to reflect the eventual conversion of the corresponding dataset file.
- Otherwise, the file is in the format of an input runfile for the `ndeval` command. This case include the original dataset files.


## TREC Tasks track datasets

The datasets provided by the TREC 2015 and 2016 Tasks track, including the relevance assessments, are placed under the directory `data/<year>/`.


## Rankings of query suggestions

The output run files for the task understanding problem, from all the methods used in the experiments, are placed under the directory `output/`. Each subdirectory relative path is of the shape:

- `<estimator of Query Suggestion Generation component>/<estimator of Document Importance component>/<estimator of Source Importance component>/<year>/runs[_converted]?/<keyphrase extractor>/`


## Contact

Should you have any questions, please contact Darío Garigliotti at dario.garigliotti[AT]uis.no (with [AT] replaced by @).
