# README
This repository contains the code and resources of the ISWS 2024 Hufflepuff experiments described in the <i>“Straight to COURT!“: COnstructing a generalizable framework for probing the ethical boUndaries of laRge language models across mulTiple domains”</i> report.

<p align="center"><img src="https://avatars.githubusercontent.com/u/172478664?s=200&v=4" style="width:60px;"></p>

## Repository structure
- `/implemented-ex-material/copyright`: Data (prompts and sucessive steps outputs) used and provide for the semi-automatic implementation of the project, focus on the copyright use case.
- `/notebooks`: Contains the main code to run LLMs.
  - `/notebooks/help`: Contains some tutorial notebooks to use Ollama and to run Ollama with Google Colab (small LLMs only).
- `/evaluation-protocols`: Contains sheets describing the tested prompts and returned answers for the different use cases (see the README file inside this folder).
- `/knowledge-graph` : Contains ontology and use cases implementation
- `/report.zip` : Contains latex source code of the report
- `README.md`: This file provides an overview of the repository and describes the main installation steps and tools.

## Installation
![Static Badge](https://img.shields.io/badge/Linux-Ubuntu_22.04.2_LTS-orange)

### Ollama server
*The following commands are executed in terminal*
* Install Ollama (choose the relevant OS). For Linux :
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
* If you are under a proxy, set environnement variables :
    - set HTTP_PROXY and http_proxy 
    - set HTTPS_PROXY and https_proxy

* To run Ollama (default HOST is 127.0.0.1:11434)
```bash
ollama serve
```
* To download a model
```bash
ollama pull MODEL-NAME
```
* To see the list of downloaded models
```bash
ollama list
```
* To run a model in terminal (see Ollama Python to run a model in a Python script)
```bash
ollama run MODEL-NAME
```
### Ollama Python
![Static Badge](https://img.shields.io/badge/Python-10.6-blue)

Ollama can also be run using a Python library. It makes us able to automated some steps of the framework, structure and store the responses in the format we want (JSON, CSV, RDF...).

* [Short documentation](https://www.ollama.com/blog/python-javascript-libraries)
* [Customized answers with Ollama](https://github.com/ollama/ollama/blob/main/docs/api.md)

* Install Ollama Python
```bash
pip install ollama
```

## Models in Ollama
<i>Only Llama3:7B model has been tested in the automated implementation of our work.</i>

| Model Name in Ollama | Developped by | Size |Number of parameters|Censored ?|
|------------|-------------|---------|-------------|---------|
| [llama3](https://www.ollama.com/library/llama3):7b|Meta|4.7GB|8.03b|Yes & No|
| [mistral](https://www.ollama.com/library/mistral) |Mistral AI|4.1GB|7.25b|No|
| [gemma](https://www.ollama.com/library/gemma):7b |Google|5GB|8.54b|Yes|

## Running notebooks

Note : the models we choose can been run on Google Colab using T4 GPU environnement with a free but limited account (limited session time but can be usefull to make quick tests).
