

# Requirements

-  `python3`
- `pip3 install -r requirements.txt`

# Run

`python run_ner.py --data_dir=data/ --bert_model=bert-base-cased --task_name=ner --output_dir=out_base --max_seq_length=128 --do_train --num_train_epochs 5 --do_eval --warmup_proportion=0.1`



#Base
## Pretrained model download from [here](https://1drv.ms/u/s!Auc3VRul9wo5hgr8jwhFD8iPCYp1?e=UsJJ2V)
or

## Pretrained model download from [here](https://1drv.ms/u/s!Auc3VRul9wo5hgr8jwhFD8iPCYp1?e=UsJJ2V)

# Inference

```python
from bert import Ner

model = Ner("out_base/")

output = model.predict("Anthony fauci is leading the corona virus task force for USA ")

print(output)
[
   {'confidence': 0.9996607303619385,
    'word': 'Anthony',
    'tag': 'B-PER'
   } 
   {'confidence': 0.9962515234947205, 'word': 'fauci', 'tag': 'I-PER'}, 
   {'confidence': 0.9999886751174927,    'word': 'is',   'tag': 'O'},   
   {'confidence': 0.9999887943267822, 'word': 'leading', 'tag': 'O'}, 
   {'confidence': 0.9999892711639404, 'word': 'the', 'tag': 'O'}, 
   {'confidence': 0.999985933303833, 'word': 'corona', 'tag': 'O'}, 
   {'confidence': 0.9999866485595703, 'word': 'virus', 'tag': 'O'}, 
   {'confidence': 0.9999897480010986, 'word': 'task', 'tag': 'O'}, 
   {'confidence': 0.9999897480010986, 'word': 'force', 'tag': 'O'}, 
   {'confidence': 0.9999884366989136, 'word': 'for', 'tag': 'O'}, 
   {'confidence': 0.9999111890792847, 'word': 'USA', 'tag': 'B-LOC'}
]

```


