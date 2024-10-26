## Machine Learning Engineering

This repository contains the code and documentation for developing and deploying machine learning models while adhering to engineering best practices.

## Environment Setup

### Virtual Environment

- Navigate to the project directory:
  ```bash
  cd <base>/ml-engineering
  ```

- Create and activate the conda environment:
  ```bash
  conda env create --file deploy/conda/linux_py312.yml
  conda activate mle
  ```

- Manage dependencies:
  - Install additional dependencies using conda or pip as needed.
  - Update environment file: `conda env export --name mle > deploy/conda/linux_py312.yml`
  - Deactivate environment: `conda deactivate`
  - Remove environment (if necessary): `conda remove --name mle --all`

## Development Workflow

### Research & Development

- Reference code: `<base>/ml-engineering/reference/nonstandardcode`
- Working notebooks: `<base>/ml-engineering/notebooks/working`

### Script Development

Scripts are derived from working notebooks in `<base>/ml-engineering/notebooks/working`.

### Setting PYTHONPATH

Ensure the directory containing `housing_value` is in PYTHONPATH:
```bash
conda env config vars set PYTHONPATH=$(pwd)/src
conda deactivate
conda activate mle
echo $PYTHONPATH
```

### Integrated Features in Scripts

- Argument Parsing: Uses `argparse` for command-line arguments.
- Configuration Management: Implements `configparser` with `setup.cfg`.
- Logging: Incorporates `logging` for execution tracking and debugging.

