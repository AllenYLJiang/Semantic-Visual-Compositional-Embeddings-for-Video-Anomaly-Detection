# Semantic-Visual-Compositional-Embeddings-for-Video-Anomaly-Detection

<span style="color:red">Code upload will finish by March 31, 2025. </span>

**Semantic Branch: 
In "Transformer-based-semantic-components-modeling"**

**Step1: Encode sentences into embeddings:**
Run caption2features768.py 
encode "Component 1: xxx, Component 2: xxx, Component 3: xxx, Component 4: xxx" to an input embedding vector, encode "Component 5: xxx" to an output embedding vector 

**Step2: Train transformer:**
Run train_statespace_v3.py --smooth_or_predwithsmoothed_or_predwithunsmoothed predwithunsmoothed --num_transform 1 --epochs 60 --model_lr 2e-5

**Step3: Inference with transformer:**
Run train_statespace_v3.py --smooth_or_predwithsmoothed_or_predwithunsmoothed train --num_transform 1 




