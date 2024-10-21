# Ansible Role: Ollama WebUI and Open-WebUI Setup

This Ansible role automates the installation and configuration of Docker, NVIDIA container toolkit, Ollama LLM WebUI, Open-WebUI with CUDA support, and Nginx reverse proxy. It includes GPU detection, Docker container management, and SSL configuration for the Nginx reverse proxy to expose the WebUIs securely.

## Requirements

- Ubuntu (or a compatible distribution)
- NVIDIA GPU with drivers installed (for CUDA support)
- Docker and Docker Compose
- Ansible `community.docker` collection

To install a basic ansible distribution w/community.docker module from which to install the project:
```bash
cd ~
apt install pipx
pipx install --include-deps ansible
ansible-galaxy collection install community.docker
```

The ansible ./hosts file assumes the server is called "ai", you will need to edit your servers /etc/hosts file so ansible knows what ip.
EXAMPLE:
```
192.168.x.x ai ai-server
```

