# Flux Colabs with 2-LoRA Support

Google Colab notebooks for running Flux models with support for up to two LoRAs:

1. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/coolt00nz/flux-colabs-with-2-loras/blob/main/flux_pruned_checkpoint_2_lora.ipynb) **Pruned Checkpoint**: Uses UNET-only Flux fp8 checkpoint (~11GB or smaller)
2. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/coolt00nz/flux-colabs-with-2-loras/blob/main/flux_full_checkpoint_2_lora.ipynb) **Full Checkpoint**: Uses complete Flux fp8 checkpoint with UNET, VAE, and CLIP (~16GB or smaller)

![Flux Demo Image](unet_flux.png)

## Features

- Memory-efficient implementation using totoro4 fork of ComfyUI
- Simple, easy-to-use Gradio interface
- Support for two simultaneous LoRAs
- Flexible model loading from CivitAI, Hugging Face, or Google Drive
- Dynamic LoRA loading and switching without restart
- Caching of previously loaded LoRAs for fast reuse
- Updated attention tensor management to load recent LoRAs
- ~3min render time for 1024x1024 images on T4 GPU

## Requirements

- Google Colab with T4 GPU
- (Optional) CivitAI API token for restricted models
- (Optional) Hugging Face API token for restricted models
- (Optional) Google Drive for local model storage

## Usage

1. Open desired colab (pruned or full checkpoint version)
2. Run first cell (optional) to mount Google Drive
3. Configure GPU runtime (T4)
4. Fill in Configuration Section with model sources and optional API tokens
5. Run second cell
6. Use Gradio interface to generate images

## Model Sources

Supports checkpoint models and LoRAs from:
- CivitAI
- Hugging Face
- Local Google Drive

## Acknowledgments

These colabs build upon:
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) by comfyanonymous (GPL-3.0)
- [totoro4](https://github.com/camenduru/ComfyUI) fork by camenduru
- Original Flux colab by camenduru

## License

This project is licensed under GPL-3.0 to comply with ComfyUI's license.

## Contributing

Issues and pull requests welcome. Please follow the GPL-3.0 license requirements.
