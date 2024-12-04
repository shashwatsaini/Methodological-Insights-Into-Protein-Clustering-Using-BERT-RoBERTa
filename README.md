# Methodological Insights Into Protein Clustering Using BERT & RoBERTa
This repository contains all the code work on the paper by the same name, find it [here](https://ieeexplore.ieee.org/document/10677287).
## Abstract
Proteins are present in all living organisms, and understanding their processes is vital. Protein databases such as SWISS-PROT include curated information on only 570,000 protein sequences, representing a fraction of the 250 million known evidential and predicted sequences; it becomes crucial to cluster proteins into similar groups. This research explores the application of two transformer architectures, BERT and RoBERTa in clustering proteins in the supervised prediction of Gene Ontology (GO) annotations. The detailed methodology for both the pre-training and fine-tuning processes, as well as results that showcase RoBERTa outperforming BERT in the context of protein clustering, on performance metrics of accuracy and loss. Operating under constrained computational resources, the deployed model exhibits strong performance and highlight the robustness of methodology in protein clustering within resource constraints. This study not only contributes to the understanding of protein clustering but also signifies the potential of transformer models to handle biological data.

## Usage
The scripts are divided into training scripts for:
1. BERT Masked Language Modeling (Pre-training)
2. BERT Sequence Classification Training (Fine-tuning)
1. RoBERTa Masked Language Modeling (Pre-training)
4. RoBERTa Sequence Classification Training (Fine-tuning)

To train models, load in protein sequences in protein sequences, from FAASTA or Uniprot, find the relevant Kaggle dataset here: [UniProt Proteins Reviewed (Swiss-Prot)](https://www.kaggle.com/datasets/andreylovyagin/uniprot-proteins-reviewed-swissprot)
## Requirements
1. Nvidia GPU with 16 GB recommended VRAM (CUDA Enabled).
2. 16 GB RAM.
3. Transformer- Hugging Face library.
4. Weights & Biases Trainer.
5. Pytorch (Can be converted to use tensorflow, but this is not recommended).

Note: The final models were trained on Nvidia Tesla P100 GPU with 16 GB RAM, for a duration of 36 hours each (24 hours for pre-training, 12 hours for fine-tuning).
