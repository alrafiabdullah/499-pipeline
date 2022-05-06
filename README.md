# Pruning Language Model

##

```
python3 LT_pretrain.py --output_dir temp --model_type bert --train_data_file /home/abdullah/Code/dl/lt_bert/dataset/texts/merged_test.txt --mlm --block_size 512
```

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
