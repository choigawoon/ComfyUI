# miniconda3

In WSL2,

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

```bash
conda create -n comfyui python=3.10
conda activate comfyui
pip install -r requirements.txt
pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu121
```

Windows
```pwsh
netsh interface portproxy add v4tov4 listenport=7860 listenaddress=0.0.0.0 connectport=7860 connectaddress=[WSL2 IP 주소]
```

## ComfyUI Manager
```bash
cd custom_nodes
git clone https://github.com/ltdrdata/ComfyUI-Manager
```

# extra_model_paths.yaml


```yaml
#config for a1111 ui
#all you have to do is change the base_path to where yours is installed
a111:
    base_path: /home/albaam/AI/stable-diffusion-webui/

    checkpoints: models/Stable-diffusion
    configs: models/Stable-diffusion
    vae: models/VAE
    loras: |
         models/Lora
         models/LyCORIS
    upscale_models: |
                  models/ESRGAN
                  models/RealESRGAN
                  models/SwinIR
    embeddings: embeddings
    hypernetworks: models/hypernetworks
    controlnet: extensions/sd-webui-controlnet/models
```

# Setup Krita
https://github.com/Acly/krita-ai-diffusion/blob/main/doc/comfy-requirements.md
