# DeepLearningProject
In this project we identift bird songs, according to [`birdclef-2022` kaggle competition](https://www.kaggle.com/competitions/birdclef-2022/overview).
You can find here the source code of the project, in the `ipynb` file.
The file is seperated to sections - load the data (from Kaggle), prepare the data, data visualizations, understand the birds, define the variables for training, mel spectrogram effect, deep models, train functions and train and test

in the `torch_objects` you can find the saved weights, you can use them like this script:

```python
path = "torch_objects/resnet_weights.pth"
model_from_path = BirdCLEFResnet(152)
checkpoint = torch.load(path)
model_from_path.load_state_dict(checkpoint)
check_accuracy(test_loader, model_from_path, True)
```
