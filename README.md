Using GeoAI to detect objects (building footprint)
- Model MarkRCNN
- Model SAM2

POC 2 for GeoAI:
- Image resolution: 0.50 (after georeference, image seems pixel-broken)
- Area of labeling: 0.77 km2
- Number of label: 657
- Chip size: 512 pixcels
- Stride: 256 pixcels (overlap)
- Number of chip: 90
 
- Number of epochs: 15
- Training time: 177 minutes
- IoU: 0.7302
- Inference about 3-5 minutes for 0,7 km2, for whole image 17 km2: 198 minutes
 
- Number of epochs: 25
- Training time: about 241 minutes
- IoU: 0.7688
- Inference about 4-6 minutes for 0,7 km2, for whole image 17 km2: 198 minutes
 
 
POC 3 for GeoAI:
- Image resolution: 0.30 (Adjust resolution after georeference, makes image better)
- Area of labeling: 0.77 km2
- Number of label: 657
- Chip size: 800 pixcels
- Stride: 400 pixcels (overlap)
- Number of chip: 100

- pretrained: Whether to use pretrained backbone. This is ignored if pretrained_model_path is provided. Defaults to True.
- pretrained_model_path: Path to a .pth file to load as a pretrained model for continued training. Defaults to None.
- batch_size: Batch size for training. Defaults to 4.
- num_epochs: Number of training epochs. Defaults to 10.
- learning_rate: Initial learning rate. Defaults to 0.005. 
- seed: Random seed for reproducibility. Defaults to 42.
 
- Number of epochs: 20
- Training time: 305 minutes
- IoU: 0.7713
- Inference about 4-6 minutes for 0,7 km2, for whole image 17 km2: 222 minutes
 
- Number of epochs: 35
- Training time: 408 minutes (on my private laptop CoreI7, 16 Gb RAM no GPU)
- IoU: 0.8162
- Inference about 5 - 7 minutes for 0,7 km2, for whole image 17 km2: 251 minutes