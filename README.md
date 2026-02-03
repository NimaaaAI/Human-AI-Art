<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>AI vs Human Art Project Documentation</title>
</head>
<body>

    <h1 style="border-bottom: 2px solid #333; padding-bottom: 10px;">AI vs. Human Art Classifier</h1>

    <section>
        <h2 style="color: #2c3e50;">📌 Project Overview</h2>
        <p>
            The rapid evolution of generative AI has created a world where machine-generated images are nearly indistinguishable from human-made art. This project implements a <strong>Convolutional Neural Network (CNN)</strong> designed to classify images into two categories: <strong>AI-generated</strong> or <strong>Human-created</strong>. 
        </p>
        <p>
            By analyzing the structural and textural nuances of these images, the model learns to identify the subtle "signatures" left behind by AI algorithms versus the organic patterns of human artists.
        </p>
    </section>

    <hr>

    <section>
        <h2 style="color: #2c3e50;">🎯 Project Aim</h2>
        <p>The goal of this project is to build an efficient, deployable image classifier. We aim to:</p>
        <ul>
            <li><strong>Differentiate</strong> between synthetic AI outputs and traditional human artwork.</li>
            <li><strong>Maximize</strong> performance on a limited dataset using transfer learning techniques.</li>
            <li><strong>Establish</strong> a baseline for how lightweight models handle the complexity of artistic styles.</li>
        </ul>
    </section>

    <hr>

    <section>
        <h2 style="color: #2c3e50;">🏗️ Model Architecture: Why ResNet18?</h2>
        <p>
            A key challenge in this project was the <strong>limited amount of training samples</strong>. In deep learning, using a massive model with a small dataset often leads to "overfitting," where the model simply memorizes the training images rather than learning to generalize.
        </p>
        
        <p>To solve this, I selected <strong>ResNet18</strong> for the following reasons:</p>
        
        

        <ul>
            <li><strong>Model Weight:</strong> ResNet18 is a "light" model compared to its deeper siblings. It provides enough depth to learn complex artistic features without being so large that it requires millions of images to converge.</li>
            <li><strong>Residual Learning:</strong> The architecture uses <strong>skip connections</strong> (identity shortcuts) to solve the vanishing gradient problem, allowing the model to train more effectively.</li>
            <li><strong>Transfer Learning:</strong> By using a version of ResNet18 pre-trained on ImageNet, the model already understands basic visual elements like edges and textures, requiring only fine-tuning for this specific task.</li>
        </ul>
    </section>

    <hr>

    <section>
        <h2 style="color: #2c3e50;">🚀 Key Features</h2>
        <ul>
            <li><strong>Automated Dataset Handling:</strong> Integrated with <code>kagglehub</code> for direct dataset downloading.</li>
            <li><strong>Data Augmentation:</strong> Includes horizontal flips and rotations to artificially increase the variety of our training data.</li>
            <li><strong>Early Stopping:</strong> The training process monitors validation loss and stops automatically when the model stops improving.</li>
            <li><strong>Performance Metrics:</strong> Utilizes Confusion Matrices and Classification Reports for precise evaluation.</li>
        </ul>
    </section>

</body>
</html>
