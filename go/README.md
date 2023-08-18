## Go on Tegra CUDA

Can be achieved with using `cuda/base` along 'devcontainer feature for Go'

devcontainer.json
```
// For format details, see https://aka.ms/devcontainer.json. For config options, see the
// README at: https://github.com/devcontainers/templates/tree/main/src/ubuntu
{
	"name": "Orin CUDA with Go",
	// Or use a Dockerfile or Docker Compose file. More info: https://containers.dev/guide/dockerfile
	"dockerFile": "Dockerfile",
	
	// Features to add to the dev container. More info: https://containers.dev/features.
	"features": {
		"ghcr.io/devcontainers/features/go:1": {}
	},

	// Use 'forwardPorts' to make a list of ports inside the container available locally.
	// "forwardPorts": [],

	// Use 'postCreateCommand' to run commands after the container is created.
	// "postCreateCommand": "uname -a",

	// Configure tool-specific properties.
	"customizations": {
		"vscode": {
            "extensions": [
                "golang.go"
            ]
		}
	},

	// Uncomment to connect as root instead. More info: https://aka.ms/dev-containers-non-root.
	// "remoteUser": "root"

	// Access to the underlying GPU
    "runArgs": [
		"--net=host",
		"--runtime",
		"nvidia"
	],
}

```

If instead you end up going for a customized `Dockerfile`, base it like this: `FROM cuda/base:latest`