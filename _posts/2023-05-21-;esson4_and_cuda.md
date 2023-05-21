# FastAI Lesson 4 & Running Notebooks Locally with CUDA

## Lesson 4 - Natural Language Processing
This lesson is about natural language processing and the process to implement a basic model that classifies the similarity of one phrase in another. The summarised process to implement this NLP model was to load the csv files using the pandas library, tokenize the text and map to numeric IDs, traing a model using the transformers library and predict using a validation set.


## Running Notebooks and Training Models Locally with CUDA
I began running the FastAI Jupyter notebooks locally and train times exceeded 20 minutes for animal classification and 1 hour for the CIFAKE dataset to classify real and AI generated images. Upon further investigation with the Task Manager, there was a high CPU usage when training models. Therefore, the AI libraries default to the CPU to train models which is known to take longer as the CPU does not process high dimensional tensors as efficiently as GPUs. To solve this, I used [PyTorch Install](https://pytorch.org/get-started/locally/) to pip install the latest CUDA 11.8 PyTorch version with the terminal command: `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117`. CUDA is the parallel computing provided by NVIDIA for its GPUs, the list of CUDA enabled GPUs is found [here](https://developer.nvidia.com/cuda-gpus) and the CUDA toolkit can be found [here](https://developer.nvidia.com/cuda-toolkit). To check if CUDA is being used when training models, the following code can be executed:
```
import torch

print(torch.cuda.is_available())
cuda_id = torch.cuda.current_device()
print(torch.cuda.get_device_name(cuda_id))

```

Using CUDA for model training saw the animal classifier model training time go to approximately 2 minutes and the CIFAKE dataset to 20 minutes.
