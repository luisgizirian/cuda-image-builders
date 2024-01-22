## Go on Tegra CUDA

Can be achieved with using `cuda/base:latest` along 'devcontainer feature for Go'

### How to create it locally?

`cd` into `cpp` folder and run `docker build -t cuda/cpp .` (consider `--no-cache` if making a significant change)

If instead you end up going for a customized `Dockerfile`, base it like this: `FROM cuda/base:latest`