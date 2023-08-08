<p align="center" width="100%">
<img src="assets/logo.png" alt="LMFlow" style="width: 100%; min-width: 300px; display: block; margin: auto; background-color: transparent;">
</p>

# LMFlow

<h4 align="center">
    <p>
        <b>English</b> |
        <a href="https://github.com/OptimalScale/LMFlow/blob/main/readme/README_zh-hans.md">简体中文</a> |
        <a href="https://github.com/OptimalScale/LMFlow/blob/main/readme/README_es.md">Español</a> |
        <a href="https://github.com/OptimalScale/LMFlow/blob/main/readme/README_jp.md">日本語</a> |
        <a href="https://github.com/OptimalScale/LMFlow/blob/main/readme/README_ko.md">한국어</a> |
        <a href="https://github.com/OptimalScale/LMFlow/blob/main/readme/README_hindi.md">हिंदी</a>
    <p>
</h4>

[![Website](https://img.shields.io/badge/Website-Demo-20B2AA.svg)](https://lmflow.com)
[![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)](https://github.com/OptimalScale/LMFlow/blob/main/LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)
[![Doc](https://img.shields.io/badge/Website-Doc-ff69b4.svg)](https://optimalscale.github.io/LMFlow/)
[![Embark](https://img.shields.io/badge/Discord-LMFlow-%237289da.svg?logo=discord)](https://discord.gg/u9VJNpzhvA)
[![slack badge](https://img.shields.io/badge/Slack-Join-blueviolet?logo=slack&amp)](https://join.slack.com/t/lmflow/shared_invite/zt-1wju9nicy-woXbNtS~5MavHSAtiMxmxQ)
[![WeChat badge](https://img.shields.io/badge/WeChat-Join-brightgreen?logo=wechat&amp)](https://s1.ax1x.com/2023/08/06/pPAQTPI.jpg)

An extensible, convenient, and efficient toolbox for finetuning large machine learning models, designed to be user-friendly, speedy and reliable, and accessible to the entire community.

<p align="center" width="100%">
<img src="assets/features.png" alt="LMFlow-features" style="width: 100%; min-width: 300px; display: block; margin: auto;">
</p>


## Latest News
* [2023-08-02] Support [Llama2](https://ai.meta.com/llama/), [ChatGLM2](https://huggingface.co/THUDM/chatglm2-6b), and [Baichuan](https://huggingface.co/baichuan-inc/Baichuan-7B) models.
* [2023-07-23] :rocket: [LMFlow multimodal chatbot](https://github.com/OptimalScale/LMFlow/blob/main/scripts/run_vis_chatbot_gradio_minigpt4.sh) is now available! Support multimodal inputs of images and texts. [Online Demo](http://multimodal.lmflow.online) is also provided (We hold the service on a single GPU, hence one may experience "queuing" or "application busy" sometimes when multiple users are accessing at the same time, please wait and attempt again later when such event happens) :rocket: ![image](https://github.com/OptimalScale/LMFlow/blob/rpan-vision-encoder/assets/multimodal-chatbot-demo.gif)
* [2023-06-22]  [LMFlow paper](https://arxiv.org/abs/2306.12420) is out! Check out our implementation details at https://arxiv.org/abs/2306.12420
* [2023-06-16] Our finetuned Robin-33B-V2 scored an impressive 64.1 on the Huggingface LLM leaderboard in our offline evaluation, outperforming major open-source LLMs! All checkpoints (7B, 13B, 33B, and 65B) are [released](https://huggingface.co/OptimalScale)! Checkout the performance [here](https://medium.com/@hkust.ml/robin-v2-launches-achieves-unparalleled-performance-on-openllm-4f6886e822c1).
* [2023-06-07] LMFlow is now officially available on PyPI! Install it with `pip install lmflow-finetune`!
* [2023-05-30] Release [Robin-13B-v2](https://huggingface.co/OptimalScale/robin-13b-v2-delta) and [Robin-33B-v2](https://huggingface.co/OptimalScale/robin-33b-v2-delta)!
* [2023-05-15] Release [LMFlow-data](http://lmflow.org:5000/lmflow_data.tar.gz), the training dataset of Robin-7B-v2. A new [test data](http://lmflow.org:5000/lmflow_chat_en_dialog_multiturn_single_nll_text2text.tar.gz) is also released.
* [2023-05-09] Release [Robin-7B-v2](http://lmflow.org:5000/robin-7b-v2-delta.tar.gz), achieving competitive performance on chitchat, commonsense reasoning and instruction-following tasks. Refer to our [comprehensive study](https://medium.com/@hkust.ml/lmflow-benchmark-an-automatic-evaluation-framework-for-open-source-llms-ef5c6f142418).


<details> <summary>More news...</summary>

* [2023-05-08] Release [LMFlow Benchmark](https://medium.com/@hkust.ml/lmflow-benchmark-an-automatic-evaluation-framework-for-open-source-llms-ef5c6f142418), an automatic evaluation framework for open-source chat-style LLMs. [Benchmark results](https://docs.google.com/spreadsheets/d/1JYh4_pxNzmNA9I0YM2epgRA7VXBIeIGS64gPJBg5NHA/edit#gid=0) on 31 popular models are reported. [Participate in LMFlow Benchmark](https://github.com/OptimalScale/LMFlow#33-lmflow-benchmark).
* [2023-04-21] Release [Robin-7B](http://lmflow.org:5000/robin-7b.tar.gz) (based on LLaMA-7B), and two models for commercial use: Parakeets-2.7B (based on GPT-NEO-2.7B) and Cokatoo-7B (based on StableLM-7B) [Download here](https://github.com/OptimalScale/LMFlow/tree/main#model-zoo)
* [2023-04-15] Inference: Support streaming output and ChatGLM.
* [2023-04-10] We propose a new alignment algorithm: [Reward rAnked FineTuning (RAFT)](https://optimalscale.github.io/LMFlow/examples/raft.html), which is more efficient than conventional (PPO-based) RLHF. [[Paper](https://arxiv.org/abs/2304.06767)]
* [2023-04-02] [Web service](https://lmflow.com/) is online!
* [2023-04-01] Release three instruction-tuned checkpoints and three medical checkpoints in [model zoo](https://github.com/OptimalScale/LMFlow#model-zoo): LLaMA-7B-tuned, LLaMA-13B-tuned, LLaMA-33B-tuned, LLaMA-7B-medical, LLaMA-13B-medical, and LLaMA-33B-medical.
* [2023-03-27] Support full tuning and lora tuning for all decoder models.
* [2023-03-27] [Tasked tuned model beats ChatGPT on medical domain](https://github.com/OptimalScale/LMFlow#model-performance).
* [2023-03-27] Release code and checkpoints - [version 0.0.1](https://optimalscale.github.io/LMFlow/)! [Our tasked-tuned model beats ChatGPT on medical domain](https://github.com/OptimalScale/LMFlow#model-performance).
</details>

## Quick Start

### Setup

Our package has been fully tested on Linux OS (Ubuntu 20.04). Other OS platforms (MacOS, Windows) are not fully tested.
You may encounter some unexpected errors. You may try it first on a Linux machine or use Google Colab to experience it.

```bash
git clone https://github.com/OptimalScale/LMFlow.git
cd LMFlow
conda create -n lmflow python=3.9 -y
conda activate lmflow
conda install mpi4py
./install.sh
```

### Prepare Dataset

Please refer to our [doc](https://optimalscale.github.io/LMFlow/examples/DATASETS.html).

### Finetuning (Full)
Full training updates all the parameters to finetune a language model.
Here is an example to finetune a GPT-2 base model
```sh
./scripts/run_finetune.sh
```

### Finetuning (LoRA)
LoRA is a parameter-efficient finetuning algorithm and is more efficient than full finetuning.
```sh
./scripts/run_finetune_with_lora.sh
```

### Evaluation
[LMFlow Benchmark](https://blog.gopenai.com/lmflow-benchmark-an-automatic-evaluation-framework-for-open-source-llms-ef5c6f142418) is an automatic evaluation framework for open-source large language models.
We use negative log likelihood (NLL) as the metric to evaluate different aspects of a language model: chitchat, commonsense reasoning, and instruction following abilities.

You can directly run the LMFlow benchmark evaluation to obtain the results to participate in the
[LLM comparision](https://docs.google.com/spreadsheets/d/1JYh4_pxNzmNA9I0YM2epgRA7VXBIeIGS64gPJBg5NHA/edit?usp=sharing).
For example, to run GPT2 XL, one may execute
```sh
./scripts/run_benchmark.sh --model_name_or_path gpt2-xl
```
`--model_name_or_path` is required, you may fill in huggingface model name or local model path here.

To check the evaluation results, you may check `benchmark.log` in `./output_dir/gpt2-xl_lmflow_chat_nll_eval`,
`./output_dir/gpt2-xl_all_nll_eval` and `./output_dir/gpt2-xl_commonsense_qa_eval`.

## Additional Notes

### LLaMA Inference on CPU

Thanks to the great efforts of [llama.cpp](https://github.com/ggerganov/llama.cpp). It is possible for everyone to run their LLaMA models on CPU by 4-bit quantization. We provide a script to convert LLaMA LoRA weights to `.pt` files. You only need to use `convert-pth-to-ggml.py` in llama.cpp to perform quantization.

### Vocabulary Extension

Now you can train your own sentencepiece tokenizer and merge it with model's origin hf tokenizer. Check out [vocab_extension](https://github.com/OptimalScale/LMFlow/blob/main/scripts/vocab_extension) for more details.

### Position Interpolation for LLaMA Models
Now LMFlow supports the latest Linear & NTK (Neural Kernel theory) scaling techniques for LLaMA models. Check out [postion_interpolation](
https://github.com/OptimalScale/LMFlow/blob/main/readme/Position_Interpolation.md) for more details.

### Flash Attention 2.0
Now LMFlow supports the latest Flash Attention 2.0. Check out [flash_attention](https://github.com/OptimalScale/LMFlow/blob/main/readme/flash_attn2.md) for more details.


## Demos
We provide four kinds of demos which include
- Online Service: If you don't want to run any code and just want to try our models, we deploy our instruction-tuned LLaMA you to have a try.
- Colab Chatbot (shell): An interactive shell-based chatbot for you to easily deploy a chatbot on colab.
- Colab Chatbot (web): An interactive web-based chatbot for you to easily deploy your own chatbot on colab.
- Local Deploy: We also provide a way for you to deploy your model/chatbot locally, which means you can deploy much larger model than previous three methods if you have enough resource.


[![Code License](https://img.shields.io/badge/Online%20Service-Web-green.svg)](https://lmflow.com)
[![colab badge](https://img.shields.io/badge/Colab-(shell)%20%20chatbot:%20gpt--neo-orange?logo=google-colab&amp)](https://colab.research.google.com/drive/1P9Hf6_mLE7WHH92pw73j9D5kz6GTdkow?usp=sharing)
[![colab badge](https://img.shields.io/badge/Colab-(web)%20%20chatbot:%20gpt--neo-blue?logo=google-colab&amp)](https://colab.research.google.com/drive/1LLtiiQO-ZIIFsTKxYzGWYX9BDRc-v8dq?usp=sharing)
[![colab badge](https://img.shields.io/badge/Colab-(demo)%20%20RAFT:%20diffusion-blueviolet?logo=google-colab&amp)](https://colab.research.google.com/drive/1bQmlSiKnqFjrkijFUJ5ylbYW-zUwObqL#scrollTo=9U2P_PUN-5xX)


### Online Service
Welcome to visit our [web service](https://lmflow.com/). We deploy LLaMA-7B-tuned model online for preview. Due to the high website traffic, sometimes the website may fail to respond. You can also deploy the chatbot following `Local Deploy`.

### Colab chatbot (shell)
<p align="center" width="100%">
<img src="assets/colab-shell-chatbot-demo.png">
</p>


We provide a simple shell demo of chatbot with Google Colab's T4/P100/V100 GPU.
Notice that the provided gpt-neo-2.7b model is **a rather weak model**, which only supports English and may sometimes generate
unsatisfactory responses. To improve the performance, users can use their own
dataset to finetune and obtain a better model with LMFlow. One can also try
other available decoder-only models provided in
🤗 [Hugging Face](https://huggingface.co/models?pipeline_tag=text-generation&sort=downloads), by

```sh
./scripts/run_chatbot.sh {another-model-name}
```
### Colab chatbot (web)
We provide a simple web demo of chatbot with Google Colab's T4/P100/V100 GPU.
Notice that the provided gpt-neo-2.7b model is **a rather weak model**, which only supports English and may sometimes generate
unsatisfactory responses.


### Local Deploy
If you have resources and want to deploy your own model locally. We provide you an easy way to run a flask server to launch a backend (to further provide services to other frontend) and an interactive web frontend (to let you communicate directly) by
```sh
./scripts/run_app.sh
```

We also provide a gradio-based UI for building chatbots. Running the following command will launch the demo for robin-7b:

```sh
pip install gradio
python ./examples/chatbot_gradio.py --deepspeed configs/ds_config_chatbot.json --model_name_or_path YOUR-LLAMA  --lora_model_path ./robin-7b --prompt_structure "A chat between a curious human and an artificial intelligence assistant. The assistant gives helpful, detailed, and polite answers to the human's questions.###Human: {input_text}###Assistant:"       --end_string "#" --max_new_tokens 200
```

We also hosted it on Hugging Face [Space](https://huggingface.co/spaces/OptimalScale/Robin-7b).



### Colab RAFT-diffusion

We also provide a simple demo to display the effectiveness of RAFT algorithm on diffusion models.
You can refer to either [Colab link](https://colab.research.google.com/drive/1bQmlSiKnqFjrkijFUJ5ylbYW-zUwObqL#scrollTo=9U2P_PUN-5xX) or `experimental/RAFT-diffusion/SD256-RAFT.ipynb`.
The support of multi-modal training of LMFlow is under development.

## Support

If you need any help, please submit a [Github](https://github.com/OptimalScale/LMFlow) issue.

## License
The code included in this project is licensed under the [Apache 2.0 license](https://github.com/OptimalScale/LMFlow/blob/main/LICENSE).
If you wish to use the codes and models included in this project for commercial purposes, please sign this [document](https://docs.google.com/forms/d/e/1FAIpQLSfJYcci6cbgpIvx_Fh1xDL6pNkzsjGDH1QIcm4cYk88K2tqkw/viewform?usp=pp_url) to obtain authorization.

## Citation
If you find this repository useful, please consider giving ⭐ and citing our [paper](https://arxiv.org/abs/2306.12420):

```
@misc{lmflow,
  author = {Shizhe Diao and Rui Pan and Hanze Dong and KaShun Shum and Jipeng Zhang and Wei Xiong and Tong Zhang},
  title = {LMFlow: An Extensible Toolkit for Finetuning and Inference of Large Foundation Models},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://optimalscale.github.io/LMFlow/}},
}
```
