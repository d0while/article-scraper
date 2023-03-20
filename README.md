# 📋 BUOD: Text Summarization Model for the Filipino Language
[![Model:distilBART](https://img.shields.io/badge/model-distilBART-green)](https://huggingface.co/jamesesguerra/distilbart-cnn-12-6-finetuned-1.3.1) [![Model:Bert2Bert](https://img.shields.io/badge/model-bert2bert-green)](https://huggingface.co/0xhaz/bert2bert-cnn_dailymail-fp16-finetuned-1.0.0) ![Last Updated](https://img.shields.io/badge/last%20updated%3A-031923-lightgrey)
Authors: [James Esguerra](https://huggingface.co/jamesesguerra), [Julia Avila](), [Hazielle Bugayong](https://huggingface.co/0xhaz)


## 🎲 Models
-- `distiBART` model on [Hugging face](https://huggingface.co/jamesesguerra/distilbart-cnn-12-6-finetuned-1.3.0)
-- `bert2bert` model on [Hugging face](https://huggingface.co/0xhaz/bert2bert-cnn_dailymail-fp16-finetuned-1.0.0)

> Foreword: This research was done in two parts, gathering the data and running transformer models,
> namely distilBART and bert2bert. Below is the step-by-step process of the experientaton of the study:


## 📚 Steps

- 📝 **Gathering the data**
- 🔧 **Initializing the transfomer models; fine-tuning of the models:**
-- via Google Colab
-- via Google Colab (Local runtime)
-- via Jupyter Notebook


## 📝 Gathering data

An [article scraper](https://github.com/jamesesguerra/article_scraper) was used in this experimentation which can gather bodies of text from various news sites. The data gathered was used to pre-train and finetune the models in the next step. This also includes instructions on how to use the article scraper.


## 🔧 Initialization of transformer models
#### via Google Colab
Two models, distilBART and bert2bert were used to compar abstractive text summarization performance. They can be found here:
- [distilBART](https://colab.research.google.com/drive/1Lv78nHqQh2I7KaFkUzWsn_MXsyP_PP1I?authuser=3#scrollTo=moK3d7mTQ1v-)
- [bert2bert](https://colab.research.google.com/drive/1Lv78nHqQh2I7KaFkUzWsn_MXsyP_PP1I?authuser=3#scrollTo=moK3d7mTQ1v-)


#### via Google Colab Local Runtime

##### Dependencies
- Jupyter Notebook
- Anaconda 
- _Optional:_ CUDA Toolkit for Nvidia, requires an account to install 
- Tensorflow

##### Installing dependencies
Create an anaconda environment. This can also be used for tensorflow, which links your GPU to Google colab's Local runtime:

```sh
conda create -n tf-gpu
conda activate tf-gpu
```

##### Optional Step: GPU Utilization (if you are using an external GPU)

Next, install the **CUDA toolkit**, this is the version that was used in this experiment. You may find a more compatible version for your hardware:
```sh
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
```
Then, upgrade pip and install tensorflow:
```sh
pip install –upgrade pip
pip install “tensorflow<2.11” –user
```

Now, check if tensorflow has been configured to use the GPU,
Type in termnial:
```sh
python
```
Next, type the following to verify:
```sh
import tensorflow as tf
tf.test.is_built_with_cuda()
```

If it returns `true`, you have succesfully initialized the environment with your external GPU. If not, you may follow the tutorials found here:

- CUDA Toolkit Tutorial [here](https://medium.com/geekculture/install-cuda-and-cudnn-on-windows-linux-52d1501a8805)
- Creating and Anaconda environment [step-by-step](https://stackoverflow.com/questions/51002045/how-to-make-jupyter-notebook-to-run-on-gpu)
- Installing Tensorflow locally using [this tutorial](https://www.tensorflow.org/install/pip#windows-native_1)

##### Connecting to a Google Colab Local Runtime
To connect this on a Google Colab Local Runtime, [this tutorial](https://research.google.com/colaboratory/local-runtimes.html) was used.

First, install Jupyter notebook (if you haven't) and enable server permissions:
```sh
pip install jupyter_http_over_ws
jupyter serverextension enable --py jupyter_http_over_ws
```
Next, start and authenticate the server:
```sh
jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888  --NotebookApp.port_retries=0
```
You can now copy the token url and paste it on your Google Colab.

#### Running the notebook using Jupyter Notebook
##### Dependencies
- Jupyter Notebook
- Anaconda 
- _Optional:_ CUDA Toolkit for Nvidia, requires an account to install 
- Tensorflow

Download the notebooks and save them in your chosen directory.
Create an environment where you can run the notebook via Anaconda
```sh
conda create -n env
conda activate env
```
**You may also opt to install the CUDA toolkit and tensforflow in this environment.
Next, run the notebooks via Jupyter Notebook.

```sh
jupyter notebook
```
##### After you're done
Deactivate the environment and also disable the server using the commands in your console.

```sh
conda deactivate
```
```sh
jupyter serverextension disable --py jupyter_http_over_ws
```
## 🔗 Additional Links/ Directory
Here are some links to resources and or references.

| Name | Link |
| ------ | ------ |
| Ateneo Social Computing Lab | https://huggingface.co/ateneoscsl |



