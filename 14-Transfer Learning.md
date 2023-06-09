## 11.1 Transfer learning&Fine-tuning in CV|迁移学习&CV里的微调
### Transferring Knowledge
1. There exists large-scale labeled CV datasets
2. Transfer knowledge from models trained on these datasets to your CV applications (with 10-100X smaller data)

### Pre-trained Models
1. a neural network trained on alarge-scale and general enough dataset
2. The feature extractor may generalize well to:
    1. other datasets (e.g. medical/satellite images)
    2. other tasks (e.g. object detection, segmentation)

### Fine-Tuning techniques
### Freeze Bottom Layers
### Where to Find Pre-trained Models
1. Tensorflow Hub:[Tensorflow Hub](https://tfhub.dev/)
    - Tensorflow models submitted by users
2. TIMM:[TIMM](https://github.com/rwightman/pytorch-image-models)
    - PyTorch models collected by Ross Wightman
### Applications
1. Fine-tuning pre-trained models (on ImageNet) is widely used in various CV applications
2. Fine-tuning accelerates convergence
3. Though not always improve accuracy
### Summary
1. Pre-train models on large-scale datasets (often image classification)
2. Initialize weights with pre-trained models for down-stream tasks
3. Fine-tuning accelerates converges and (sometimes) improves accuracy

## 11.2 Fine-Tuning in NLP|NLP里的微调
### Self-supervised pre-training
1. No large-scale labeled NLP dataset
2. Large quantities of unlabeled documents
3. Self-supervised pre-training
    1. Generate “pseudo label”and use supervised learning task
    2. Common tasks for NLP：
        1. Language model (LM): predict next word. e.g. I like your hat
        2. Masked language model (MLM): random masked word prediction. e.g. I like your hat
### Pre-trained Models
1. Word embeddings
2. Transformer based pre-trained models
### BERT
1. Pre-training tasks: masked token prediction, next sentence prediction
2. Pre-trained on Wikipedia and BookCorpus (>3B words)
3. Many versions: base / large, English / multilingual, cased / uncased
4. Multiple variants：
    - ALBERT
    - ELECTRA 
    - RoBERTa 
    - …………
### BERT Fine-tuning
Randomly initialize the last layer, train a few epochs with small lr
### Practical Considerations
1. BERT fine-tuning on small datasets can be unstable
2. Randomly initializing some top transformer layers help

### Where to Find Pre-trained Models
- HuggingFace: a collection of pre-trained transformer models on both PyTorch and TensorFlow
### Applications
1.  “(BERT) obtains new state-of-the-art results on eleven natural language processing tasks”
2. “(T5) achieve state-of-the-art results on many benchmarks covering summarization, question answering, text classification, and more”
### Summary
1. Self-supervised pre-training for NLP models
2. BERT is a giant transformer encoder
3. Downstream tasks fine-tune BERT with a consistent manner