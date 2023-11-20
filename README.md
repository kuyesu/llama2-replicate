### Llama-2 model

This repository contains the code for experimenting with the Llama-2 model and lanchain

### Installation

<!-- Note -->

> Setup a virtual environment before installing the requirements. Check out anaconda or anacondamini for this.

<!-- steps -->

1. Install requirements

```bash
pip install -r requirements.txt
```

2. Install [PyTorch](https://pytorch.org/get-started/locally/)

### Usage

Run the following commands to ingest the documents. All your documents should be in `SOURCE_DOCUMENTS` folder.

> Note: Chroma db is used as the vector database. You can use any other vector database

```bash
python3 ingest.py
```

Copy the content of `.example.env` to `.env` and fill in the values.

Run the following commands see the results of the model.

```bash
python3 run_llama_api.py
```

### Results

Open Postman and make a POST request to `http://127.0.0.1:5100/api/prompt_route` with the following body

```json
{
  "Prompt": "What is the capital of Uganda?"
}
```

### Acknowledgements
Most of the code is taken from [this](https://github.com/PromtEngineer/localGPT) repository. Thanks to the authors for making it open source.
