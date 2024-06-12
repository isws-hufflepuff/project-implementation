# README
## Installation
### Ollama server
*The following commands are executed in terminal*
* Install Ollama (choose the relevant OS). For Linux :
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
* If you are under a proxy, set environnement variables :
    - set HTTP_PROXY and http_proxy 
    - set HTTPS_PROXY

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
* To run a model in terminal (see Ollama Pyhton to run a model in a Python script)
```bash
ollama run MODEL-NAME
```
### Ollama Python
Ollama can also be run using a Python library. It makes us able to script the prompts, structure and store the responses in the format we want (JSON, CSV, RDF...).

* [Short documentation](https://www.ollama.com/blog/python-javascript-libraries)

* Install Ollama Python
```bash
pip install ollama
```

## Models in Ollama
| Model Name in Ollama | Description | Size |Number of parameters|Censored ?|
|------------|-------------|---------|-------------|---------|
| [llama3](https://www.ollama.com/library/llama3)| |4.7GB|8.03b||
| [mistral](https://www.ollama.com/library/mistral) | |4.1GB|7.25b||
| [gemma](https://www.ollama.com/library/gemma):7b | |5GB|8.54b|Yes|

## Running notebooks

Note : the models we choose can been run on Google Colab using T4 GPU environnement with a free but limited account (limited time but can be usefull to make tests).

## Metrics