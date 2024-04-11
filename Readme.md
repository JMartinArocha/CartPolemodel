# CartPole Reinforcement Learning Exercise

![Header Image](cartpole.png)

## Description
This project is a practical exercise to implement and test a reinforcement learning agent using the CartPole environment from OpenAI Gym. The goal is to develop an agent capable of maintaining a pole balanced on a moving cart by applying deep reinforcement learning techniques.

## Badges

![GitHub license](https://img.shields.io/github/license/JMartinArocha/DenguePredictionModels.svg)
![Python version](https://img.shields.io/badge/python-3.x-blue.svg)
![last-commit](https://img.shields.io/github/last-commit/JMartinArocha/DenguePredictionModels)
![issues](https://img.shields.io/github/issues/JMartinArocha/DenguePredictionModels)
![commit-activity](https://img.shields.io/github/commit-activity/m/JMartinArocha/DenguePredictionModels)
![repo-size](https://img.shields.io/github/repo-size/JMartinArocha/DenguePredictionModels)

## Additional Documentation

The project includes additional documentation provided in a PDF format, developed using LaTeX for clear and structured presentation. This documentation serves as an in-depth guide covering various aspects of the project, from design decisions to detailed descriptions of the system architecture. For those new to the project or needing a detailed reference, the PDF is an invaluable resource. Additionally, the repository contains a guide on how to install and set up the project environment, ensuring users can get started with minimal setup time.

Review Latex_guide.md

## Installation

### Prerequisites
You will need Python 3.8 or higher, along with pip and virtualenv to set up and run this project.

## Virtual Environment Setup

The project leverages a virtual environment to manage dependencies, ensuring that all packages and libraries are contained within an isolated setting. This setup prevents conflicts between project-specific requirements and global Python installations. Using a virtual environment facilitates reproducibility and streamlines the development process across different machines. Detailed instructions on setting up and activating the virtual environment are included in the installation guide, making it easy for users to configure their development workspace for the project.

```bash
git clone https://yourrepository.git
cd yourrepository
python -m virtualenv venv
source venv/bin/activate  # Unix/MacOS
venv\Scripts\activate     # Windows
```

# Install dependencies
```bash
!pip3 install --upgrade pip
!pip3 install -r requirements.txt
```

# Monitoring with TensorFlow and TensorBoard
In this project, TensorFlow, along with its TensorBoard tool, plays a crucial role in monitoring and analyzing the performance of our deep learning models. We leverage TensorBoard to visualize metrics such as loss and accuracy, providing valuable insights into the model's training progress. This functionality is crucial for fine-tuning and optimizing the agent's learning process. To initiate this monitoring, the code includes:

```shell
%load_ext tensorboard
%tensorboard --logdir logs/fit
rm -rf ./logs/  # Clears any logs from previous runs
```

```shell
tensorboard_callback = tf.keras.callbacks.TensorBoard(log_dir=log_dir, histogram_freq=1)
self.model.fit(state, train_target, verbose = 0,callbacks=[tensorboard_callback]) # verbose: dont show loss and epoch
```

## Testing Saved Models

To ensure the efficacy and robustness of the trained models, this project includes a testing phase where the saved models are loaded and evaluated in a real environment setting. Below is an overview of how the models are tested:

### Project Structure
DQLAgent - A deep Q-learning agent capable of learning and making decisions based on environmental observations.

### Methods:
    - __init__: Initializes the agent, setting up the neural network and hyperparameters.
    - build_model: Constructs the neural network.
    - act: Decides on the best action based on the current state.
    - remember: Stores experiences in memory.
    - replay: Trains the network using a batch of stored experiences.
    - adaptiveEGreedy: Adjusts the exploration rate.

## Contributing
Pull requests son bienvenidos. Para cambios mayores, por favor abra un issue primero para discutir lo que le gustaría cambiar.

## License

MIT