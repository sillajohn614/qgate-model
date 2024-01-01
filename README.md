[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![PyPI version fury.io](https://badge.fury.io/py/qgate-model.svg)](https://pypi.python.org/pypi/qgate-model/)
![coverage](https://github.com/george0st/qgate-model/blob/main/coverage.svg)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/george0st/qgate-model)
![GitHub release](https://img.shields.io/github/v/release/george0st/qgate-model) 

# QGate-Model
The machine learning meta-model with synthetic data (useful for MLOps/feature store), is independent of machine
learning solutions (definition in json, data in csv/parquet). It can be used with various of 
ML/MLOps solutions with or without FeatureStore.

![Quality-Gate](./docs/assets/icons8-quality-100.png)

## Usage
This meta-model is suitable for:
 - compare capabilities and functions of machine learning solutions (as part of RFP/X and SWOT analysis)
 - independent test new versions of machine learning solutions (with aim to keep quality in time)
 - unit, sanity, smoke, system, reqression, function, acceptance, performance, shadow, ... tests
 - external test coverage (in case, that internal test coverage is not available or weak)
 - etc.

Note: You can see real usage in e.g. project **[qgate-sln-mlrun](https://github.com/george0st/qgate-sln-mlrun)** for testing MLRun/Iguazio solution.

## Structure
The solution contains this simple structure:
 - **00-high-level**
   - The high-level [view](#model) to the meta-model for better understanding
 - **01-model**
   - The definition contains 01-projects, 02-feature sets, 03-feature vectors, etc. in JSON format
   - This model is designed for these [use cases](./docs/usecases.md) 
 - **02-data**
   - The data for meta-model in CSV/GZ format (future support parquet) for party, account, transaction, event, communication, etc.
   - You can also generate your own dataset with requested size (see sample './02-data/2-size-2k.sh' and description 'python main.py generate --help')
Addition detail, [see](./docs/structure.md)

## Model
![Basic-model](./00-high-level/basic-feature-sets.png)
![Derived-model](./00-high-level/derived-feature-sets.png)

