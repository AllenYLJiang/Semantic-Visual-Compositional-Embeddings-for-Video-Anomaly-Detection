## Semantic-Visual-Compositional-Embeddings-for-Video-Anomaly-Detection

## Semantic Branch: 
In "Transformer-based-semantic-components-modeling"**

**Step1: Encode sentences into embeddings:**
```
Run caption2features768.py 
encode "Component 1: xxx, Component 2: xxx, Component 3: xxx, Component 4: xxx" to an input embedding vector, encode "Component 5: xxx" to an output embedding vector 

This requires downloading encoder weights from huggingface.co, with repository name longformer-base-4096 
```
**Step2: Train transformer:**
```
Run train_statespace_v3.py --smooth_or_predwithsmoothed_or_predwithunsmoothed predwithunsmoothed --num_transform 1 --epochs 60 --model_lr 2e-5
```
**Step3: Inference with transformer:**
```
Run train_statespace_v3.py --smooth_or_predwithsmoothed_or_predwithunsmoothed train --num_transform 1 
```
## Visual Branch: 

For datasets whose training set only contains normal events, train flow model with only normal samples. For datasets whose training set contains video-level anomaly labels, regard the most anomalous subset of frames as labeled anomalous semantics 

**Installation**
Install all packages:
```
$ python3 -m pip install -U -r requirements.txt
```

**Training**
- Run code for training ShanghaiTech
```
Run main.py --flow_arch conditional_flow_model --gpu 0 --data_path /path/to/data/shanghaitech 
```


