# My local AI stack

## Info

This repository contains a simple docker-compose file that I use to run a local AI stack based on ollama and open-webui.

The ollama container is configured to be able to use the power of my Radeon 6700XT GPU.  
It is thus the ROCm version of ollama image and device mappings to enable access to the host's GPU.  
As this GPU model is not officially supported by [ROCm](https://www.amd.com/en/products/software/rocm.html), we cheat a bit by forcing some environment variables.  

I found most of the info in this blog post [Running Ollama and Open WebUI Self-Hosted with any GPU](https://dev.to/berk/running-ollama-and-open-webui-self-hosted-4ih5).

## Usage

```bash
# Clone this repository
git clone https://github.com/pondichys/local_ai

# Navigate to the directory and start docker compose stack
cd local_ai
docker compose up -d docker-compose.yml
```

Once all containers are started, connect to http://localhost:8080, create your first user and pull some AI models.

You should then be ready to chat with your local ai.

## Goodies

To check if and how your GPU is used, install [radeontop](https://github.com/clbr/radeontop) software.
