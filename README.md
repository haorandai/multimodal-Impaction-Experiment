# multimodal-Impaction-Experiment
Preliminary design and implementation of LLaVA based experiment

## Core Idea
1. Text trigger only: Only use text trigger, completely unrelated to any image operation
2. Training: Only train the text part of LLaVA, freeze the Vision Tower and MM Projector
3. Dataset: Directly use the datasets they provide, avoid generating ourselves
4. Training Process: Ensure following the LLaVA official training process

## Process
First Step. Try to use Unalign method to train LLaVA model.
Ref: https://github.com/CaoYuanpu/BackdoorUnalign
https://arxiv.org/abs/2312.00027

LLaVA folder: Official LLaVA repo


Update:
- Data Converter done
- DeepSpeed config file: Official zero2.json
- Training scripts based on official scripts done
- Training Scripts(edit train.py to freeze the image part)
- Training scripts debugging done!
- Model training parameter imitating backdoor approach

Next: 
1. Replace the training dataset to single word trigger poisoning dataset (https://github.com/bboylyg/BackdoorLLM)
2. Test the attack effectiveness
3. Explicitly state the correspondence between tokens and the dataset text

### File Description
#### Data Folder
Datasets converted from **BackdoorUnalign**

- Raw dataset: poison_long_trigger_llama2.jsonl

- Converted dataset: llava_backdoor_data.json

- Converter code: data_converter.py

#### Scripts Folder

#### llava Folder

