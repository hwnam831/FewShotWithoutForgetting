# Neural Attention Memory (NAM) Few-shot Learning

## Requirements
- Pytorch version > 1.0 with CUDA-capable GPU w. 8GB+ VRAM
- Follow Baseline-README.md to download miniImageNet dataset and set-up the feature-averaging cosine classifier

## Instructions
1. Pre-train the feature model and classifiers using the following commands:  
```python train.py --config=miniImageNet_ResNetLikeCosineClassifier```  
```python train.py --config=miniImageNet_ResNetLikeNAM```  
2. Run 1-shot and 5-shot experiments.  
```python train.py --config=miniImageNet_ResNetLikeCosineClassifierGenWeightAttN1```  
```python train.py --config=miniImageNet_ResNetLikeNAMAtt```  
```python train.py --config=miniImageNet_ResNetLikeCosineClassifierGenWeightAttN5```  
```python train.py --config=miniImageNet_ResNetLikeNAMAttN5```  
3. Evaluate the resulting few-shot learning classifiers
```python evaluate.py --config=miniImageNet_ResNetLikeCosineClassifierGenWeightAttN1 --testset```  
```python evaluate.py --config=miniImageNet_ResNetLikeNAMAtt --testset```  
```python evaluate.py --config=miniImageNet_ResNetLikeCosineClassifierGenWeightAttN5 --testset```  
```python evaluate.py --config=miniImageNet_ResNetLikeNAMAttN5 --testset```  