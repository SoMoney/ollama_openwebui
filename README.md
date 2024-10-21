# Ansible Role: Ollama + Open-WebUI to Nginx project

This Ansible role automates the installation and configuration of Docker, NVIDIA container toolkit, Ollama LLM WebUI, Open-WebUI with CUDA support, and Nginx reverse proxy.
It includes GPU detection, Docker container management, and SSL configuration for the Nginx reverse proxy to expose the WebUIs securely.
When complete you should be able to reach the openWebUI interface with https://<ip-address>

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

The ansible ./hosts inventory file assumes the server is called "ai". If you want to continue using that alias, you will need to edit your Ansible servers /etc/hosts file so its reachable.
EXAMPLE:
```
sudo vi /etc/hosts

# IP to openWebUI alias on Ansible server
192.168.x.x ai ai-server
```

