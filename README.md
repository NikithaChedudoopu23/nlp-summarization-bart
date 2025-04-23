# **Article Summarization using BART Transformer**

This project explores abstractive summarization of news articles using Hugging Face's facebook/bart-large-cnn transformer. We compare the performance of the pre-trained vs. fine-tuned model on the CNN/DailyMail dataset using both quantitative (ROUGE & BERTScore) and qualitative evaluation.

📚**Dataset**

We used the CNN/DailyMail dataset from Hugging Face's datasets library.

To ensure faster experimentation, we used subsets:

- Training: 5,000 samples

- Validation: 1,000 samples

- Test: 1,000 samples

🧪 **Summary of Methods**

Model Used: facebook/bart-large-cnn

Tokenization: BART tokenizer with truncation to 1024 tokens

Fine-tuning: 2 epochs with early stopping and layer freezing

Evaluation Metrics: ROUGE-1, ROUGE-2, ROUGE-L, BERTScore (F1)

🧠 **Key Features**
✅ Compares Pre-trained vs Fine-tuned BART

✅ Summary generation for 1000 test articles

✅ ROUGE and BERTScore computed using Hugging Face evaluate & bert_score

✅ Qualitative analysis of fluency, faithfulness, and coverage

🧪 **Results**

Metric         Pre-trained	       Fine-tuned

ROUGE-1	        0.338774	          0.329812

ROUGE-2	        0.145692	          0.137131

ROUGE-L	        0.250232	          0.235148
 
BERTScore (F1)	0.908139	          0.901258

Fine-tuned summaries were qualitatively more complete and contextually adapted, even when scores remained comparable.

🚀 **How to Run**
**Requirements:** Python 3.9+, Google Colab or Jupyter Notebook

1. Install Dependencies
   
```pip install transformers datasets evaluate bert-score```

2. Launch Notebook
   
   Open the notebook FinalNLPProject.ipynb in Google Colab or Jupyter.

3. Run Sections
   
  Sections are organized in this order:

- Preprocessing

- Pre-trained model evaluation

- Fine-tuning BART

- Summary generation

- ROUGE & BERTScore evaluation

- Result comparison
  

4. Notes:

Model is saved locally under bart_finetuned_local/

Training logs and checkpoints are in ./logs and ./results

GPU runtime in Colab is highly recommended


🔮 **Future Work**

- Hyperparameter tuning (e.g. learning rate, batch size)

- Use larger training subsets

- Integrate long-context models like LongT5 or Pegasus

- Explore reinforcement learning-based reward tuning


👩‍💻**Author**

Nikitha Chedudoopu

Graduate Student – Masters in Data Analytics Engineering

Northeastern University

