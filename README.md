# Langchain

Playround for Langchain

## Conda

To install FAISS it is recommended you use [Conda](https://docs.conda.io/projects/conda/en/stable/). Conda is an open-source package management system and environment management system that runs on Windows, macOS, and Linux.

Download: https://docs.conda.io/en/latest/miniconda.html#linux-installers

```bash
bash Miniconda3-py310_23.3.1-0-Linux-x86_64.sh

Welcome to Miniconda3 py310_23.3.1-0

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
>>>
```

```bash
Please answer 'yes' or 'no':'
>>> yes
```

```bash
Miniconda3 will now be installed into this location:
/home/zhangwei/miniconda3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/zhangwei/miniconda3] >>> /home/zhangwei/software/miniconda3
```

```bash
Do you wish the installer to initialize Miniconda3
by running conda init? [yes|no]
[no] >>> yes
```

Open a new terminal console,

## FAISS

Faiss is a library for efficient similarity search and clustering of dense vectors. It contains algorithms that search in sets of vectors of any size, up to ones that possibly do not fit in RAM. It also contains supporting code for evaluation and parameter tuning.

> Note: `requirements.txt` uses `faiss-cpu`

```bash
conda install -c pytorch faiss-cpu
```

```bash
Proceed ([y]/n)? yes
```

## Python

Your distribution is trying to protect you against mixing apt provided packages and pip provided packages. Mixing two package managers (apt and pip here) is always a bad idea and the source of many issues.

Rather use a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
```

## Configuration

```
Did not find openai_api_key, please add an environment variable `OPENAI_API_KEY` which contains it, or pass  `openai_api_key` as a named parameter. (type=value_error)
```

Create a `.env` with the following:

```
OPENAI_API_KEY=sk-eiYmxxxxxxxxxxxxxxxxxxxxxxxxxxxxxe9fk
SERPAPI_API_KEY=8b7be02d0cxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx1cb2207615
```

## Examples:

- `baby_agi.ipynb`: BabyAGI example
- `baby_agi_with_tools.ipynb`: BabyAGI with SerpAPI search
- `metabolite_names.ipynb`: Generate alternative metabolites names using SerpAPI search
- `beautiful_soup.ipynb`: Generate a list of products using a metabolites using SerpAPI and scraping
