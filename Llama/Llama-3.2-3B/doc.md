
# Hermes-3-Llama-3.2-3B-GGUF

- 2 GB: https://huggingface.co/NousResearch/Hermes-3-Llama-3.2-3B-GGUF/resolve/main/Hermes-3-Llama-3.2-3B.Q4_K_M.gguf?download=true
- 3 GB: https://huggingface.co/NousResearch/Hermes-3-Llama-3.2-3B-GGUF/resolve/main/Hermes-3-Llama-3.2-3B.Q8_0.gguf?download=true

## LLama

- ./llama-server -m ../models/Llama-3.2-3B.Q4_K_M.Hermes-3.gguf --reasoning-format none --port 15000

# sample

messages = [
    {"role": "system", "content": "You are Hermes 3."},
    {"role": "user", "content": "Hello, who are you?"}
]
gen_input = tokenizer.apply_chat_template(messages, return_tensors="pt")
model.generate(**gen_input)

| Model               | Size  | Dim  | Mạnh | Nhẹ  | Phù hợp        |
| ------------------- | ----- | ---- | ---- | ---- | -------------- |
| e5-small-v2         | ~110M | 384  | ⭐⭐   | ⭐⭐⭐⭐ | RAG mini       |
| gte-small           | ~100M | 384  | ⭐⭐   | ⭐⭐⭐⭐ | Search nhẹ     |
| bge-m3              | ~500M | 1024 | ⭐⭐⭐⭐ | ⭐    | Production RAG |
| nomic-embed-text-v2 | ~300M | 768  | ⭐⭐⭐  | ⭐⭐   | Semantic tốt   |

