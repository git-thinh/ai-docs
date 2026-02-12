# E5-small-v2:

- 30 MB: https://huggingface.co/ChristianAzinn/e5-small-v2-gguf/resolve/main/e5-small-v2.Q4_K_M.gguf?download=true

- 37 MB: https://huggingface.co/ggml-org/e5-small-v2-Q8_0-GGUF/resolve/main/e5-small-v2-q8_0.gguf?download=true
- 37 MB: https://huggingface.co/ChristianAzinn/e5-small-v2-gguf/resolve/main/e5-small-v2.Q8_0.gguf?download=true


# Run

- LLAMA_CURL=1 flag along with other hardware-specific flags (for ex: LLAMA_CUDA=1 for Nvidia GPUs on Linux).
- cd llama.cpp && LLAMA_CURL=1 make

- ./llama-cli --hf-repo ggml-org/e5-small-v2-Q8_0-GGUF --hf-file e5-small-v2-q8_0.gguf -p "The meaning to life and the universe is"
- ./llama-server --hf-repo ggml-org/e5-small-v2-Q8_0-GGUF --hf-file e5-small-v2-q8_0.gguf -c 2048
