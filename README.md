# BERT-base-Turkish-QA

A custom Turkish question answering system made by fine-tuning [BERTurk](https://huggingface.co/dbmdz/bert-base-turkish-128k-cased), which is a BERT base model transformer. We have trained and evaluated the exact match and F1 scores using different Turkish data sets, then compared the evaluation results. In our final model, we have concatenated all of the Turkish data sets into one data set and trained our model using the whole training data set. You can check out our final models [Turkish BERTurk Based Model](https://huggingface.co/Aybars/ModelOnWhole), [Turkish XLM-R Based Model](https://huggingface.co/Aybars/XLM_Turkish).

This project is made during our joint internship at SESTEK Speech Enabled Software Technologies.



## Data Sets

[OkanVK's Turkish Reading Comprehension Question Answering Data Set](https://github.com/okanvk/Turkish-Reading-Comprehension-Question-Answering-Dataset)

[TQuAD (Turkish Question Answering Data Set)](https://github.com/TQuad/turkish-nlp-qa-dataset)

[XQuAD (Cross-lingual Question Answering Data Set)](https://github.com/deepmind/xquad)

[Kuzgunlar's Data Set](https://github.com/kuzgnlar/datasets)



## Base Models

[BERTurk](https://huggingface.co/dbmdz/bert-base-turkish-128k-cased)

[XLM-R](https://huggingface.co/xlm-roberta-base)



## Model Comparison

| Base Models                  | Training Set        | Evalulation Set   | Results |       | Hyperparameters |                |            |               |
|------------------------------|---------------------|-------------------|---------|-------|-----------------|----------------|------------|---------------|
|                              |                     |                   |         |       |                 |                |            |               |
|                              |                     |                   | Exact   | F1    | epoch           | max_seq_length | doc_stride | learning_rate |
| best-base-turkish-128k-cased | whole_train_dataset | whole_dev_dataset | 62.48   | 81.60 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | okanvk_dev        | 62.48   | 81.66 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | tquad_dev         | 62.22   | 80.42 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | xquad.tr          | 45.89   | 66.37 | 2               | 512            | 128        | 3,00E-05      |
| best-base-turkish-128k-cased | Tquad_train         | whole_dev_dataset | 56.32   | 76.86 | 2               | 512            | 128        | 3,00E-05      |
|                              | Tquad_train         | okanvk_dev        | 56.31   | 76.87 | 2               | 512            | 128        | 3,00E-05      |
|                              | Tquad_train         | tquad_dev         | 57.40   | 78.68 | 2               | 512            | 128        | 3,00E-05      |
|                              | Tquad_train         | xquad.tr          | 41.76   | 60.83 | 2               | 512            | 128        | 3,00E-05      |
| best-base-turkish-128k-cased | Okanvk_train        | whole_dev_dataset | 60.37   | 80.53 | 2               | 512            | 128        | 3,00E-05      |
|                              | Okanvk_train        | okanvk_dev        | 60.37   | 80.63 | 2               | 512            | 128        | 3,00E-05      |
|                              | Okanvk_train        | tquad_dev         | 58.63   | 78.43 | 2               | 512            | 128        | 3,00E-05      |
|                              | Okanvk_train        | xquad.tr          | 46.38   | 70.74 | 2               | 512            | 128        | 3,00E-05      |
| XLM-R Base                   | whole_train_dataset | whole_dev_dataset | 54.60   | 76.83 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | okanvk_dev        | 54.68   | 76.94 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | tquad_dev         | 53.48   | 75.26 | 2               | 512            | 128        | 3,00E-05      |
|                              | whole_train_dataset | xquad.tr          | 42.27   | 61.72 | 2               | 512            | 128        | 3,00E-05      |
| Savasy QA (not base)         | Tquad_train         | tquad_dev         | 62.56   | 80.48 |                 |                |            |               |



## Authors

👤 **Aras Güngöre**

* LinkedIn: [@arasgungore](https://www.linkedin.com/in/arasgungore)
* GitHub: [@arasgungore](https://github.com/arasgungore)

👤 **Aybars Manav**

* LinkedIn: [@aybarsmanav](https://www.linkedin.com/in/aybarsmanav)
* GitHub: [@AybarsManav](https://github.com/AybarsManav)
