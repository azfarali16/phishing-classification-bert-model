### DistilBERT Phishing Detection Model

**Dataset**:  
The model was trained on English-based email texts for phishing detection.  
Dataset source: [Curated Dataset made by A. I. Champa, M. F. Rabbi, M. F. Zibran.](https://zenodo.org/records/8339691)

**Overview**:  
I used **DistilBERT** instead of the base BERT due to performance issues with BERT (accuracy got stuck at 50% after 2 batches). DistilBERT, being a lighter version, worked much better and gave the following results:

**Results** on test data:
- **Precision**: 0.9857
- **Recall**: 0.9971
- **F1 Score**: 0.9913
- **Accuracy**: 0.9913
- **AUC**: 0.9993

Although the results are strong, there are signs of overfitting, possibly because the data isn’t clean enough, leading the model to memorize noise instead of general patterns.

**Future Considerations**:  
- More data wrangling to clean the dataset.
- Finetuining optimization; Implementing LORA to reduce overfitting.
- Better preprocessing to reduce overfitting.

**Notes**:  
- The code was executed on a private Kaggle workspace to utilize their resources.  
- The project was an exploration of BERT to deepen my understanding of the model.
