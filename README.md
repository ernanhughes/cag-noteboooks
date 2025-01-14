# CAG: Don't Do RAG: When Cache-Augmented Generation is All You Need for Knowledge Tasks

This repo is the supporting code for this post: 
[CAG: Cache-Augmented Generation](http://programmer.ie/post/cag/)

Couple of notebooks

| Notebook | Description |
| ---- | ---- |
| [CAG example](notebooks/cag.ipynb) | This is a complete example implementation of CAG |
| [Token count using tiktoken](notebooks/token_count_tiktoken.ipynb)  | Token count using tiktoken (will give a good enough token count) |
| [Token count using the model](notebooks/token_count_llama.ipynb)  | Toke count example using  a model |
| [Original Code](notebooks/kvcache.ipynb) | The original kv code form the paper  |


## Setup 
To run the notebooks you should follow these steps 
Create an environment for testing

```Bash
python -m venv .venv
```

Activate that environment

```Bash
.\.venv\Scripts\activate
```

I always install torch gpu at this stage. You will need ot adjust based upon your cuda version installed

```Bash
nvcc --version

nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2022 NVIDIA Corporation
Built on Wed_Sep_21_10:41:10_Pacific_Daylight_Time_2022
Cuda compilation tools, release 11.8, V11.8.89
Build cuda_11.8.r11.8/compiler.31833905_0
```

For me this indicates 11.8 go to the pytorch site [here](https://pytorch.org/get-started/locally/) to find the appropriate versions

```Bash
pip install torch==2.2.0 torchvision==0.17.0 torchaudio==2.2.0 --index-url https://download.pytorch.org/whl/cu118
```

Next we install the requirements file

```Bash
pip install -r .\requirements.txt
```


