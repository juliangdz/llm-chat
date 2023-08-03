# llm-chat
A simple Python script to showcase LLM Chat Capability to run on Laptop devices with even 4 GB GPUs .


## Installation:

```bash
pip install transformers accelerate
```
Supports pytorch > 2.0 


## Intent:
This script provides a baseline for you to build your own chat bot and allows you to run on your local machine even if you have a 4 GB GPU Laptop.

if you plan on changing the models, make sure to change the device map settings accordingly. For the model "tiiuae/falcon-7b-instruct" , i had to ensure that after i ran generate_device_map . I had to edit the device_map.json to have "transformer.word_embeddings" and "lm_head" on the same device , i used 0 for both, so they reside on GPU. After making this change you can run the chat interface. 

## Usage:

```python
python chat.py

```

## TO:DO:

Add network search capabilities and build a chat interface desktop application.
