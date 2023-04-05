# Unit Scaling

A library for unit scaling in PyTorch.

Based on the paper [Unit Scaling: Out-of-the-Box Low-Precision Training](https://arxiv.org/abs/2303.11257).

## Development

**First-time setup**:

```bash
python3 -m venv .venv
# Add to `.venv/bin/activate`: `source /PATH_TO_POPLAR_SDK/enable` (If running on IPU) 
source .venv/bin/activate

# pip install wheel  # (If running on IPU)
# pip install $POPLAR_SDK_ENABLED/../poptorch-*.whl  # (If running on IPU) 
pip install -r requirements-dev.txt
```

**Run pre-flight checks** (or run `./dev --help` to see supported commands):

```bash
./dev
```

**IDE recommendations**:

 - Python intepreter is set to `.venv/bin/python`
 - Format-on-save enabled
 - Consider a `.env` file for setting PYTHONPATH, e.g. `echo "PYTHONPATH=$(pwd)" > .env`
 (note that this will be a different path if using devcontainers)


## License

Copyright (c) 2023 Graphcore Ltd. Licensed under the MIT License.

The included code is released under an MIT license, (see [LICENSE](LICENSE)).

Our dependencies are (see [requirements.txt](requirements.txt)):

| Component | About | License |
| --- | --- | --- |
| numpy | Array processing library | BSD 3-Clause |
| poptorch-experimental-addons | A collection of addons to [PopTorch](https://github.com/graphcore/poptorch), with general utility. | MIT |
| scipy | An open-source software for mathematics, science, and engineering | BSD 3-Clause |

We also use additional Python dependencies for development/testing (see [requirements-dev.txt](requirements-dev.txt)).