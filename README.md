# Methodological Insights Into Protein Clustering Using BERT & RoBERTa
This repository contains all the code work on the paper by the same name, currently in the process of publishing.
## Abstract
Proteins are present in all living organisms, and
understanding their processes is vital. Protein databases only
include curated information on 550,000 protein sequences,
representing only a fraction of the 250 million known evidential
and predicted sequences; it becomes crucial to cluster proteins
into similar groups. This paper explores the application of
BERT and RoBERTa in clustering proteins, specifically in the
supervised prediction of Gene Ontology (GO) annotations. Our
focus lies in detailing the intricacies of both pre-training and
fine-tuning processes, showcasing a model trained using these
approaches. Noteworthy is the finding that RoBERTa
outperforms BERT in the context of protein clustering, on
metrics of accuracy and loss. Despite operating under
constrained computational resources, the deployed model
exhibits superior performance compared to state-of-the-art
models leveraging Recurrent Neural Networks (RNN), Long
Short-Term Memory Networks (LSTMs), and other
transformer-based architectures. The incorporation of
RoBERTa, with its advancements like dynamic masking and a
more extensive training corpus, enhances the model's capacity
to discern complex protein relationships and semantic
representations, resulting in more accurate predictions of GO
annotations. Through a comprehensive analysis of results, we
highlight the robustness of our methodology in protein
clustering within resource constraints. RoBERTa's superior
performance underscores its efficacy in handling biological
data, offering a promising avenue for future implementations
with enhanced computational resources. This study not only
contributes to the understanding of protein clustering but also
signifies the potential of transformer models to advance
research in biological data analysis, even in resource-limited
settings.
## Results
The trained RoBERTa model achieves an accuracy of 54% on 30 selected Gene Ontology annotations, on a dataset of 25,000 proteins.
## Usage
The scripts are divided into training scripts for:
1. BERT Masked Language Modeling (Pre-training)
2. BERT Sequence Classification Training (Fine-tuning)
1. RoBERTa Masked Language Modeling (Pre-training)
4. RoBERTa Sequence Classification Training (Fine-tuning)

To train models, load in protein sequences in protein sequences, from FAASTA or Uniprot, find the relevant Kaggle dataset here: [UniProt Proteins Reviewed (Swiss-Prot)](https://www.kaggle.com/datasets/andreylovyagin/uniprot-proteins-reviewed-swissprot)
## Requirements
1. Nvidia GPU with 8 GB recommended VRAM (CUDA Enabled).
2. 16 GB RAM.
3. Transformer- Hugging Face library.
4. Pytorch (Can be converted to use tensorflow, but this is not recommended).

Note: The final models were trained on Nvidia Tesla P100 GPU with 16 GB RAM, for a duration of 36 hours each (24 hours for pre-training, 12 hours for fine-tuning).
## License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/


