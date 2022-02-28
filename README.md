# Fine-tuning Transformer for Text Classification

這是一篇使用 Transformation 做中文文本分類的 Notebook，整個任務的流程可分為：

1. Data Preprocessing 
2. Modeling
3. Training
4. Evaluation

資料的部分使用 THUCNews 的一部分做為訓練與模型評估之用，原資料集一共有14個類別，這邊僅使用其中的12個類別，且資料集分別切割為：

- Training dataset
- Development dataset(就是 Validation dataset)
- Testing dataset

模型使用 BERT 的改良版 RoBERTa 進行 Fine-tuning，預訓練模型及相關的資料處理工具來自於 [Hugging Face](https://huggingface.co/)，因此需要預先安裝：  
  pip install transformers[sentencepiece]  
  pip install datasets
