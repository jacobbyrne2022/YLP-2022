### Jacob Byrne Project 2021-22
This repository contains the code I've used and created in the course of my project, Partial Differential Neural Networks.

## To Run This Code
This code depends in significant parts on the DynamicBlocks repository, https://github.com/EmoryMLIP/DynamicBlocks, and to run any code involving the parabolic network:
1. Download the DynamicBlocks code and set it up on your preferred environment (I used Google Colab)
2. Replace the requirements.txt with requirements2.txt
3. Move the current_pdenet.pt file to the results folder in the DynamicBlocks setup
4. At the start of all the Notebooks, there is code to point at the main Google Drive folder of the DynamicBlocks code. Replace that with the necessary code to change the working directory to that main folder.

For the ResNet-18 I was using,
1. Run the code in Notebooks/Finetuning ResNet.ipynb
2. Rename references to the pretrained ResNet to match the timestamp in your filename (or, change the filename to match the timestamped references in the code)

## Main Directory
**Generate Parabolic Net.ipynb** This runs the training process to create the parabolic network, running code from 
DynamicBlocks, Ruthotto, L.and Onken, D., 2019, Available from:https://github.com/EmoryMLIP/DynamicBlocks , Accessed: 02 December 2022.

**Requirements2.txt** Edited the requirements.txt included with the DynamicBlocks package to run on Colab.

## Notebooks folder
The Notebooks folder contains the following Jupyter notebooks, which were all used on Google Colab. The first two code blocks in each notebook make the file access request to google drive and so on your own device should be replaced with lines to move the working directory.

**FGSM ParabNet.ipynb** Creates and tests FGSM adversarial examples on the parabolic network. Uses code from Adversarial Example Generation, Inkawhich, N. and Uriegas, E.,  2018, Available from: https://github.com/pytorch/tutorials/blob/master/beginner_source/fgsm_tutorial.py , Accessed: 20 Feb 2022

**FGSM ResNet.ipynb** Similarly, creates and tests FGSM adversarial examples on the ResNet-18. Uses code from Adversarial Example Generation, Inkawhich, N. and Uriegas, E.,  2018, Available from: https://github.com/pytorch/tutorials/blob/master/beginner_source/fgsm_tutorial.py , Accessed: 20 Feb 2022

**Finetuning ResNet.ipynb** Trains a ResNet-18 CIFAR-10 classifier. As the saved ResNet model is too large to upload, if you would like to test the ResNet-related code, you will need to run this file, which then means changing the filenames in calls to point to the new model. Uses code from Finetuning Torchvision Models, Inkawhich, N., date unknown, Available from: https://pytorch.org/tutorials/beginner/finetuning_torchvision_models_tutorial.html ,Accessed: 7 Mar 2022.

**ParabNet FGSM Norm Testing.ipynb** This performs the tests described in Sction 6.3 on the parabolic network, to verify the stability claims of Section 5.2 with FGSM examples. Uses code from Adversarial Example Generation, Inkawhich, N. and Uriegas, E.,  2018, Available from: https://github.com/pytorch/tutorials/blob/master/beginner_source/fgsm_tutorial.py , Accessed: 20 Feb 2022

**Parabolic Hue Norm Testing.ipynb** This performs the first tests described in Section 6.3 on the parabolic network, again, to verify the stability claims of Section 5.2 with hue-perturbed examples.

**Parabolic Hue Tests.ipynb** This tests the accuracy of the parabolic network as the hue of test images is perturbed varying distances from normal, as described in Section 6.1.

**ResNet FGSM Norm Testing.ipynb** This performs the tests described in Sction 6.3 on the ResNet model, to verify the stability claims of Section 5.2 with FGSM examples. Uses code from Adversarial Example Generation, Inkawhich, N. and Uriegas, E.,  2018, Available from: https://github.com/pytorch/tutorials/blob/master/beginner_source/fgsm_tutorial.py , Accessed: 20 Feb 2022

**ResNet Hue Norm Testing.ipynb** This performs the first tests described in Section 6.3 on the ResNet model, to verify the stability claims of Section 5.2 with hue-perturbed examples.

**ResNet Hue Tests.ipynb** This tests the accuracy of the ResNet model as the hue of test images is perturbed varying distances from normal, as described in Section 6.1.


Thanks,
Jacob
