# DeepSeek-V3-Base for Ollama

This example provides a Modelfile for running DeepSeek-V3-Base with Ollama.

## Model Details

DeepSeek-V3-Base is a strong Mixture-of-Experts (MoE) language model with:
- 671B total parameters (37B activated for each token)
- 128K context window
- Trained on 14.8T tokens
- State-of-the-art performance on various benchmarks

## Usage

1. Download the model weights from Hugging Face:
   ```bash
   # Clone the model repository
   git clone https://huggingface.co/deepseek-ai/DeepSeek-V3-Base
   ```

2. Update the Modelfile to point to your downloaded weights:
   ```
   FROM /path/to/DeepSeek-V3-Base/safetensors
   ```

3. Create the model in Ollama:
   ```bash
   ollama create deepseek-v3-base -f Modelfile
   ```

4. Run the model:
   ```bash
   ollama run deepseek-v3-base
   ```

## Parameters

The model is configured with the following default parameters:
- temperature: 0.7
- top_p: 0.7
- top_k: 50
- context window: 32768 tokens (can be increased up to 128K)

You can adjust these parameters when running the model:
```bash
ollama run deepseek-v3-base "Your prompt" --temperature 0.8
```

## License

The use of DeepSeek-V3-Base model is subject to the [Model License](https://huggingface.co/deepseek-ai/DeepSeek-V3-Base/blob/main/LICENSE-MODEL). The model supports commercial use.