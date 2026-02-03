# Purple Squirrel R1

**Fine-tuned DeepSeek-R1-Distill-Llama-8B for Purple Squirrel AI Platform**

[![Model on HF](https://img.shields.io/badge/🤗_Model-Hugging_Face-orange)](https://huggingface.co/purplesquirrelnetworks/purple-squirrel-r1)
[![Research Paper](https://img.shields.io/badge/📄_Paper-AIDP_Neural_Cloud-blue)](https://huggingface.co/purplesquirrelnetworks/aidp-neural-cloud-paper)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📊 Model Details

- **Base Model**: DeepSeek-R1-Distill-Llama-8B
- **Parameters**: 8B
- **Quantization**: 4-bit NF4 (GGUF f16 available)
- **Context Length**: 4096 tokens
- **Specialization**: Purple Squirrel AI platform operations

## 🎯 Capabilities

Fine-tuned to excel at:

- **Video Analysis**: AI-powered transcription and tagging
- **Blockchain Operations**: Multi-chain NFT minting (Solana, Ethereum, Polygon)
- **Cloud Integration**: OCI, AWS, IPFS storage operations
- **Video Editing**: Professional workflow understanding
- **Platform Operations**: Purple Squirrel feature guidance

## 🚀 Quick Start

### Using Ollama

```bash
# Pull the model
ollama pull purplesquirrelnetworks/purple-squirrel-r1

# Run inference
ollama run purplesquirrelnetworks/purple-squirrel-r1 "How do I mint an NFT on Solana?"
```

### Using Hugging Face

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model_id = "purplesquirrelnetworks/purple-squirrel-r1"
tokenizer = AutoTokenizer.from_pretrained(model_id)
model = AutoModelForCausalLM.from_pretrained(model_id)

prompt = "Explain video transcription with Watson Speech-to-Text"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = model.generate(**inputs, max_length=200)
print(tokenizer.decode(outputs[0]))
```

### Via AIDP Neural Cloud API

```python
import openai

client = openai.OpenAI(
    base_url="https://neural-cloud.aidp.store/v1",
    api_key="your-api-key"
)

response = client.chat.completions.create(
    model="purple-squirrel-r1",
    messages=[
        {"role": "user", "content": "What is Purple Squirrel?"}
    ]
)
print(response.choices[0].message.content)
```

## 📥 Download Model

**Hugging Face**: [purplesquirrelnetworks/purple-squirrel-r1](https://huggingface.co/purplesquirrelnetworks/purple-squirrel-r1)

**Available Formats:**
- Safetensors (Hugging Face Transformers)
- GGUF f16 (Ollama, llama.cpp) - 15GB

## 🎓 Training Details

- **Base**: DeepSeek-R1-Distill-Llama-8B
- **Method**: LoRA fine-tuning
- **Dataset**: Purple Squirrel platform documentation and operations
- **Framework**: TRL (Transformer Reinforcement Learning)
- **Hardware**: Trained on AIDP decentralized GPU network

## 🔗 Related Projects

- **AIDP Neural Cloud**: [Research Paper](https://huggingface.co/purplesquirrelnetworks/aidp-neural-cloud-paper) | [GitHub](https://github.com/ExpertVagabond/aidp-neural-cloud)
- **Purple Squirrel Platform**: [purplesquirrel.media](https://purplesquirrel.media)

## 📚 Citation

```bibtex
@misc{purplesquirrel-r1,
  title={Purple Squirrel R1: Fine-tuned DeepSeek-R1-Distill-Llama-8B},
  author={Karsten, Matthew},
  year={2026},
  publisher={Purple Squirrel Networks},
  url={https://huggingface.co/purplesquirrelnetworks/purple-squirrel-r1}
}
```

## 📄 License

MIT License - Based on DeepSeek-R1-Distill-Llama-8B

---

Built by [Purple Squirrel Networks](https://purplesquirrelnetworks.com)
