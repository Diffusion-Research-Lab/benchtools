# BenchTools

BenchTools provides small, reusable utilities for machine-learning benchmarks: YAML configuration loading, runtime dtype and device setup, reproducible random seeding, and publication-ready reporting helpers.

## Installation

```bash
pip install "benchtools @ git+https://github.com/Diffusion-Research-Lab/benchtools.git"
```

For development:

```bash
git clone git@github.com:Diffusion-Research-Lab/benchtools.git
cd benchtools
python -m pip install -e ".[dev]"
```

## Usage

```python
from benchtools.config import load_config
from benchtools.report import format_mean_std_latex
from benchtools.utils import set_seed

config = load_config("config.yaml")
set_seed(config.seed)
summary = format_mean_std_latex(mean=1.2e-3, std=2.5e-4)
```

## Development

```bash
make setup
make check
```

## License

BenchTools is released under the MIT License.
