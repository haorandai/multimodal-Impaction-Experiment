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


Update: Data Converter done
Update: DeepSpeed config file: Official zero2.json
Update: Training scripts based on official scripts done
Next: Training Scripts(train.py && train_mem.py)


### File Description
