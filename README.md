# BART PeaCoK

## Gathering the data
To get started you need the initial data files (reach out to `silin.gao@epfl.ch`)

* Original PersonaChat (place under `data/persona_peacok`)
  * `train_persona_original_chat_convai2.json`
  * `valid_persona_original_chat_convai2.json`
* PersonaChat extended with mapped PeaCoK facts (map and then choose 5 randomly) (place under `data/persona_peacok`)
  * `valid_persona_original_chat_ext.json`
  * `train_persona_original_chat_ext.json`
* PeaCoK KG (place under `data/peacok_kg`)
  * `atomic_simple_head.json`

To be able to run the code as-is, place these files under `data/persona_peacok`.

## Environment setup

```
conda env create -f workstation_setup/bart_peacok.yml
conda activate bart_peacok
```

## Preparing datasets for train/eval

To save time prior to running training and evaluation, run the following the prepare the required datasets:

``python save_datasets.py --dataset {dataset}``

Supported options for the dataset are: 
``persona_chat``, 
``persona_chat_peacok``, 
``persona_chat_peacok_retrieved``, ``persona_chat_peacok_induced``, 
``persona_chat_peacok_random_induced``, ``persona_chat_peacok_retrieved_induced``

The first two options can be computed right away (given you obtained the datasets from the first section). For the remaining options you need to run the retrieved-induced components (instruction in the next section).

## Computing induced and retrieved

```
cd induce_retrieve_pipeline

```

## Run training or eval
**TODO**