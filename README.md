# Pruning Language Model

##

## Requirements

- Create and activate a virtual environment
- Run `pip install -r requirements.txt`
- Replace the `absolute location` of the data with your own path
- To run the `.py` file, run the following command:

```
python3 LT_pretrain.py --output_dir folder_name --model_type bert --train_data_file data_location --mlm --block_size 512
```

- Only the `lottery_ticket` folder needs a separate virtual environment
- All the notebooks run in the same virtual environment using the requirements from `tinybert_merged_dataset` folder

##

| Dataset        | Eval Loss              | Current Loss           | Perplexity | Current Perplexity | Epochs  |
| -------------- | ---------------------- | ---------------------- | ---------- | ------------------ | ------- |
| Merged Dataset | 2.050959211628453      | **1.6111257392532972** | 7.7754     | **5.0084**         | **100** |
| Sadhu          | 1.9630640718524017     | **1.5072933565537983** | 7.1211     | **4.5145**         | N/A     |
| Newspaper      | 2.233108249695405      | **1.9341062079859144** | 9.3288     | **6.9179**         | N/A     |
| ASR            | **2.0896919834831986** | 2.208796659946203      | **8.0824** | 9.1048             | N/A     |
| Social Media   | 1.9894736234321955     | **1.6029354353420069** | 7.3117     | **4.9676**         | N/A     |

##

## Sentiment Analysis BNLP

### Restaurant

| Model          | Previous Accurcy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ---------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 62.1             | **65.2**      | 64.3            | 55.5        | **59.9** | 51.2      | **100** |
| BERT Bengali   | N/A              | 60.7          | N/A             | N/A         | 58.5     | N/A       | N/A     |
| Bangla-Electra | N/A              | 50.2          | N/A             | N/A         | 40.9     | N/A       | N/A     |
| Indic-BERT     | N/A              | 60.3          | N/A             | N/A         | 58.7     | N/A       | N/A     |
| BERT-m         | N/A              | 59.8          | N/A             | N/A         | 58.1     | N/A       | N/A     |

### Cricket

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 74.5              | **76.6**      | 75.8            | 64.1        | 70.1     | **70.3**  | **100** |
| BERT Bengali   | N/A               | 71.1          | N/A             | N/A         | 69.2     | N/A       | N/A     |
| Bangla-Electra | N/A               | 71.3          | N/A             | N/A         | 67       | N/A       | N/A     |
| Indic-BERT     | N/A               | 71.1          | N/A             | N/A         | **71.4** | N/A       | N/A     |
| BERT-m         | N/A               | 67.7          | N/A             | N/A         | 68.2     | N/A       | N/A     |

### YouTube

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 54.1              | 66.1          | 60.2            | 46.4        | 66.1     | 58.1      | **100** |
| BERT Bengali   | N/A               | 73.3          | N/A             | N/A         | 72.9     | N/A       | N/A     |
| Bangla-Electra | N/A               | 66.2          | N/A             | N/A         | 67.4     | N/A       | N/A     |
| Indic-BERT     | N/A               | **75.7**      | N/A             | N/A         | **75.2** | N/A       | N/A     |
| BERT-m         | N/A               | 72.6          | N/A             | N/A         | 72.9     | N/A       | N/A     |

### SAIL

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 43.5              | 60.2          | 50.1            | 42.4        | 58.3     | 42.1      | **100** |
| BERT Bengali   | N/A               | 60.7          | N/A             | N/A         | 59.5     | N/A       | N/A     |
| Bangla-Electra | N/A               | 53.3          | N/A             | N/A         | 49.8     | N/A       | N/A     |
| Indic-BERT     | N/A               | **61.3**      | N/A             | N/A         | **61.2** | N/A       | N/A     |
| BERT-m         | N/A               | 56.7          | N/A             | N/A         | 56.6     | N/A       | N/A     |

### CogniSenti

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 66.2              | 68.2          | 65.7            | 51.1        | 62.6     | 57.5      | **100** |
| BERT Bengali   | N/A               | 62.4          | N/A             | N/A         | 62.2     | N/A       | N/A     |
| Bangla-Electra | N/A               | 63.9          | N/A             | N/A         | 59.3     | N/A       | N/A     |
| Indic-BERT     | N/A               | 66.1          | N/A             | N/A         | **65.8** | N/A       | N/A     |
| BERT-m         | N/A               | **68.9**      | N/A             | N/A         | 68.6     | N/A       | N/A     |

### BengFastText

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 69.8              | **74.3**      | 70.1            | 67.1        | **75.1** | 69.8      | **100** |
| BERT Bengali   | N/A               | 69.0          | N/A             | N/A         | 66.5     | N/A       | N/A     |
| Bangla-Electra | N/A               | 68.7          | N/A             | N/A         | 66.8     | N/A       | N/A     |
| Indic-BERT     | N/A               | 68.7          | N/A             | N/A         | 68.7     | N/A       | N/A     |
| BERT-m         | N/A               | 69.6          | N/A             | N/A         | 67.4     | N/A       | N/A     |

### Combined

| Model          | Previous Accuracy | Eval Accuracy | Pruned Accuracy | Previous F1 | Eval F1  | Pruned F1 | Epochs  |
| -------------- | ----------------- | ------------- | --------------- | ----------- | -------- | --------- | ------- |
| **BERT Tiny**  | 63.7              | 71.4          | 65.15           | 62.4        | 70.6     | 65.1      | **100** |
| BERT Bengali   | N/A               | 79.3          | N/A             | N/A         | 79.2     | N/A       | N/A     |
| Bangla-Electra | N/A               | 72.0          | N/A             | N/A         | 71.8     | N/A       | N/A     |
| Indic-BERT     | N/A               | **80.3**      | N/A             | N/A         | **80.2** | N/A       | N/A     |
| BERT-m         | N/A               | 80.0          | N/A             | N/A         | 79.9     | N/A       | N/A     |

##

## Language Model Pruning

| Perplexity | Percentage |
| ---------- | ---------- |
| 5.8555     | 10         |
| 5.7207     | 20         |
| 5.7728     | 30         |
| 5.7815     | 40         |
| 5.8127     | 50         |
| 6.1085     | 60         |
| 6.4827     | 70         |
| 7.3785     | 80         |
| 9.2634     | 90         |

##
