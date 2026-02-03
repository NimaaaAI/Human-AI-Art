# AI vs. Human Art Classification

Project Overview
The rise of generative AI has made it increasingly difficult to distinguish between human-made masterpieces and machine-generated imagery. This project aims to bridge that gap by developing a robust computer vision classifier capable of identifying the origin of an artwork. By leveraging deep learning, we explore whether there are underlying patterns—such as texture, brushstroke consistency, or structural logic—that differentiate human creativity from algorithmic synthesis.

Objectives
The primary goal of this repository is to build a reliable binary classifier. Specifically, we focus on:

Discrimination Accuracy: Fine-tuning a pre-trained model to recognize the subtle nuances of AI-generated artifacts.

Efficiency for Small Data: Demonstrating how to achieve high performance even when the dataset is relatively small, utilizing specific architectural choices to prevent overfitting.

Interpretability: Using evaluation metrics like confusion matrices to understand which styles or classes are most frequently misidentified.

Why ResNet18?
In deep learning, bigger is not always better. For this specific task, ResNet18 was chosen as the backbone architecture for several strategic reasons:

Dataset Constraints: Large models like ResNet152 or Vision Transformers (ViTs) require massive amounts of data to converge. Given our limited sample size, a "heavier" model would likely memorize the training data (overfit) rather than learn generalizable features.

Vanishing Gradient Mitigation: ResNet's "skip connections" allow the model to learn identity functions, ensuring that even with fewer layers, the gradient remains stable during backpropagation.

Transfer Learning Efficiency: By using a model pre-trained on ImageNet, we start with a rich understanding of basic shapes and textures, requiring only a small amount of fine-tuning to adapt to the specific domain of digital and classical art.
