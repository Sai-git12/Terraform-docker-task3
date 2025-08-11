
.devcontainer/devcontainer.json
{
  "name": "Terraform + Docker Dev",
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainers/features/docker-in-docker:2": {},
    "ghcr.io/devcontainers/features/terraform:1": {}
  },
  "postCreateCommand": "docker --version && terraform -version",
  "forwardPorts": [8080],
  "customizations": {
    "vscode": {
      "extensions": [
        "hashicorp.terraform",
        "ms-azuretools.vscode-docker"
      ]
    }
  }
}
