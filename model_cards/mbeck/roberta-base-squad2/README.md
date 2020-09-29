# roberta-base for Question Answering

## Overview

**Language model**: roberta-base \
**Language**: English \
**Downstream-task**: [Extractive question answering](https://huggingface.co/transformers/v3.2.0/task_summary.html#extractive-question-answering) \
**Training data**: [SQuAD 2.0](https://rajpurkar.github.io/SQuAD-explorer/)  \
**Eval data**: [SQuAD 2.0](https://rajpurkar.github.io/SQuAD-explorer/)

## Hyperparameters
Trained with [`run_squad.py`](https://github.com/huggingface/transformers/blob/v2.11.0/examples/question-answering/run_squad.py) using the following: 
```
model_name_or_path = "roberta-base"
batch_size = 16
n_epochs = 3
learning_rate = 3e-5
lr schedule = linear warmup
warmup_steps = 5075
doc_stride=128
max_seq_len = 384
max_query_length=64
```

## Performance
Evaluated on the SQuAD2.0 dev set using `run_squad.py` script.
```
Results = {
  "exact": 78.39636149246189, 
  "f1": 81.7539035283792, 
  "total": 11873, 
  "HasAns_exact": 76.70377867746289, 
  "HasAns_f1": 83.4284913280107, 
  "HasAns_total": 5928, 
  "NoAns_exact": 80.08410428931876, 
  "NoAns_f1": 80.08410428931876, 
  "NoAns_total": 5945, 
  "best_exact": 78.39636149246189, 
  "best_exact_thresh": 0.0, 
  "best_f1": 81.75390352837901, 
  "best_f1_thresh": 0.0
}

```
