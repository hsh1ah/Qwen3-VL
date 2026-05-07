# Qwen3-VL


<p align="center">
    <img src="https://qianwen-res.oss-accelerate.aliyuncs.com/Qwen3-VL/qwen3vllogo.png" width="400"/>
<p>

<p align="center">
        💜 <a href="https://chat.qwenlm.ai/"><b>Qwen Chat</b></a>&nbsp&nbsp | &nbsp&nbsp🤗 <a href="https://huggingface.co/collections/Qwen/qwen3-vl-68d2a7c1b8a8afce4ebd2dbe">Hugging Face</a>&nbsp&nbsp | &nbsp&nbsp🤖 <a href="https://modelscope.cn/collections/Qwen3-VL-5c7a94c8cb144b">ModelScope</a>&nbsp&nbsp | &nbsp&nbsp📑 <a href="https://qwen.ai/blog?id=99f0335c4ad9ff6153e517418d48535ab6d8afef&from=research.latest-advancements-list">Blog</a>&nbsp&nbsp | &nbsp&nbsp📚 <a href="https://github.com/QwenLM/Qwen3-VL/tree/main/cookbooks">Cookbooks</a>&nbsp&nbsp | &nbsp&nbsp📑 <a href="https://arxiv.org/pdf/2511.21631">Paper</a>&nbsp&nbsp
<br>
🖥️ <a href="https://huggingface.co/spaces/Qwen/Qwen3-VL-Demo">Demo</a>&nbsp&nbsp | &nbsp&nbsp💬 <a href="https://github.com/QwenLM/Qwen/blob/main/assets/wechat.png">WeChat (微信)</a>&nbsp&nbsp | &nbsp&nbsp🫨 <a href="https://discord.gg/CV4E9rpNSD">Discord</a>&nbsp&nbsp | &nbsp&nbsp📑 <a href="https://help.aliyun.com/zh/model-studio/developer-reference/qwen-vl-api">API</a>&nbsp&nbsp | &nbsp&nbsp🖥️ <a href="https://gallery.pai-ml.com/#/preview/deepLearning/cv/qwen2.5-vl">PAI-DSW</a>
</p>



## Introduction
Meet Qwen3-VL — the most powerful vision-language model in the Qwen series to date.

This generation delivers comprehensive upgrades across the board: superior text understanding & generation, deeper visual perception & reasoning, extended context length, enhanced spatial and video dynamics comprehension, and stronger agent interaction capabilities.

Available in Dense and MoE architectures that scale from edge to cloud, with Instruct and reasoning‑enhanced Thinking editions for flexible, on‑demand deployment.


#### Key Enhancements:

* **Visual Agent**: Operates PC/mobile GUIs—recognizes elements, understands functions, invokes tools, completes tasks.

* **Visual Coding Boost**: Generates Draw.io/HTML/CSS/JS from images/videos.

* **Advanced Spatial Perception**: Judges object positions, viewpoints, and occlusions; provides stronger 2D grounding and enables 3D grounding for spatial reasoning and embodied AI.

* **Long Context & Video Understanding**: Native 256K context, expandable to 1M; handles books and hours-long video with full recall and second-level indexing.

* **Enhanced Multimodal Reasoning**: Excels in STEM/Math—causal analysis and logical, evidence-based answers.

* **Upgraded Visual Recognition**: Broader, higher-quality pretraining is able to "recognize everything"—celebrities, anime, products, landmarks, flora/fauna, etc.

* **Expanded OCR**: Supports 32 languages (up from 10); robust in low light, blur, and tilt; better with rare/ancient characters and jargon; improved long-document structure parsing.

* **Text Understanding on par with pure LLMs**: Seamless text–vision fusion for lossless, unified comprehension.


#### Model Architecture Updates:

<p align="center">
    <img src="https://qianwen-res.oss-accelerate.aliyuncs.com/Qwen3-VL/qwen3vl_arc.jpg" width="80%"/>
<p>


1. **Interleaved-MRoPE**: Full‑frequency allocation over time, width, and height via robust positional embeddings, enhancing long‑horizon video reasoning.

2. **DeepStack**: Fuses multi‑level ViT features to capture fine‑grained details and sharpen image–text alignment.

3. **Text–Timestamp Alignment:** Moves beyond T‑RoPE to precise, timestamp‑grounded event localization for stronger video temporal modeling.






## News
* 2025.11.27: We have released the [**Qwen3-VL paper**](https://arxiv.org/pdf/2511.21631), which introduces many technical details and key findings behind model design. Check it out!
* 2025.11.27: We have officially launched [Qwen3-VL-235B-A22B-Thinking](https://huggingface.co/Qwen/Qwen3-VL-235B-A22B-Thinking) alongside other sizes. Enjoy!
* 2025.11.26: 🎉🎉🎉 We have released **Qwen3-VL**! Check out our blog [here](https://qwen.ai/blog?id=99f0335c4ad9ff6153e517418d48535ab6d8afef&from=research.latest-advancements-list)!


---

## Contents
* [1. Models](#1-models)
* [2. Demo](#2-demo)
* [3. Quick Start](#3-quick-start)
* [4. Cookbooks](#4-cookbooks)
* [5. Citation](#5-citation)

---

## 1. Models

We offer Dense and MoE architectures at multiple scales:

| Model | Param | Architecture |
|:---|:---|:---|
| [Qwen3-VL-235B-A22B](https://huggingface.co/Qwen/Qwen3-VL-235B-A22B) | 235B (22B active) | MoE |
| [Qwen3-VL-235B-A22B-Thinking](https://huggingface.co/Qwen/Qwen3-VL-235B-A22B-Thinking) | 235B (22B active) | MoE |
| [Qwen3-VL-30B-A3B](https://huggingface.co/Qwen/Qwen3-VL-30B-A3B) | 30B (3B active) | MoE |
| [Qwen3-VL-8B](https://huggingface.co/Qwen/Qwen3-VL-8B) | 8B | Dense |
| [Qwen3-VL-8B-Thinking](https://huggingface.co/Qwen/Qwen3-VL-8B-Thinking) | 8B | Dense |
| [Qwen3-VL-4B](https://huggingface.co/Qwen/Qwen3-VL-4B) | 4B | Dense |
| [Qwen3-VL-2B](https://huggingface.co/Qwen/Qwen3-VL-2B) | 2B | Dense |

For detailed performance benchmarks, please refer to our [paper](https://arxiv.org/pdf/2511.21631).


## 2. Demo

Try Qwen3-VL on [Hugging Face Spaces](https://huggingface.co/spaces/Qwen/Qwen3-VL-Demo) or [Qwen Chat](https://chat.qwenlm.ai/).


## 3. Quick Start

Install the latest `transformers` for Qwen3-VL support:

```bash
pip install git+https://github.com/huggingface/transformers@main
```

Alternatively, you can use the Qwen-Omni-Utils package (recommended for video tasks):

```bash
pip install qwen-omni-utils[all]
```

Example usage:

```python
from transformers import Qwen3VLForConditionalGeneration, AutoProcessor
from qwen_vl_utils import process_vision_info
import torch

model = Qwen3VLForConditionalGeneration.from_pretrained(
    "Qwen/Qwen3-VL-8B",
    torch_dtype=torch.bfloat16,
    device_map="auto"
)

processor = AutoProcessor.from_pretrained("Qwen/Qwen3-VL-8B")

messages = [
    {
        "role": "user",
        "content": [
            {"type": "image", "image": "https://qianwen-res.oss-accelerate.aliyuncs.com/Qwen3-VL/demo.jpeg"},
            {"type": "text", "text": "Describe this image."}
        ]
    }
]

text = processor.apply_chat_template(messages, tokenize=False, add_generation_prompt=True)
image_inputs, video_inputs = process_vision_info(messages)

inputs = processor(
    text=[text],
    images=image_inputs,
    videos=video_inputs,
    return_tensors="pt"
)
inputs = inputs.to(model.device)

output_ids = model.generate(**inputs, max_new_tokens=512)
generated_ids = [
    output_ids[len(input_ids):]
    for input_ids, output_ids in zip(inputs.input_ids, output_ids)
]
response = processor.batch_decode(generated_ids, skip_special_tokens=True)[0]
print(response)
```

For more details, see the [cookbooks](https://github.com/QwenLM/Qwen3-VL/tree/main/cookbooks).


## 4. Cookbooks

We provide cookbooks for various tasks:
* General image/video understanding
* Visual grounding
* GUI agent
* OCR
* ...

See [cookbooks](https://github.com/QwenLM/Qwen3-VL/tree/main/cookbooks) for more.


## 5. Citation

If you find Qwen3-VL useful in your research, please cite:

```bibtex
@article{qwen3vl2025,
  title={Qwen3-VL: Advancing Vision-Language Models},
  author={Qwen Team},
  journal={arXiv preprint arXiv:2511.21631},
  year={2025}
}
```

Related project: [DeepSeek-VL2](https://github.com/deepseek-ai/DeepSeek-VL2)

1. related project [DeepSeek-VL2](https://github.com/deepseek-ai/DeepSeek-VL2)
2. related project [Aria](https://github.com/rhymes-ai/Aria)
3. related project [Kimi-VL](https://github.com/MoonshotAI/Kimi-VL)
