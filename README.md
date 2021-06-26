# pySonde

## Setup
```
pip install -r requirements.txt
python setup.py sdist
pip install dist/pysonde*.tar.gz
```

For development
```sh
# Install dependencies
pipenv install --dev

# Setup pre-commit and pre-push hooks
pipenv run pre-commit install -t pre-commit
pipenv run pre-commit install -t pre-push
```

## Usage

A few example files are automatically installed and can be used to test if the installation was successful

Unix:
```sh
sounding_converter -i examples/level0/BCO_20200126_224454.mwx -o "test_{direction}.nc" -c config/main.yaml
```

Windows:
```sh
sounding_converter.exe -i examples/level0/BCO_20200126_224454.mwx -o "test_{direction}.nc" -c config/main.yaml
```

## Simple Plotting

The package also includes a few plotting routines that can be called with e.g.

Unix:
```sh
sounding_visualize -i converted/file/sounding.nc
```

## SkewT Plotting

A skewT diagram can be created with

Unix:

```sh
sounding_skewT -i converted/file/sounding.nc
```
