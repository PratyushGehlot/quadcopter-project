# Deep Reinforcement Learning Project

Deep Reinforcement Learning Project project developed for Udacity's Deep Learning Nanodegree. The goal of this project is to use deep reinforcement learning to teach a quadcopter how to fly. The algorithm used for learning is Deep Deterministic Policy Gradients (DDPG) as described in the [Continuous control with deep reinforcement learning](https://arxiv.org/abs/1509.02971) paper.

![Quadcopter](movie.gif)

## Getting Started

Clone the repository:

``` batch
git clone https://github.com/craig-martinson/quadcopter-project.git
cd quadcopter-project
```

Create a Conda GPU environment:

``` batch
conda create -n quadcopter python=3.6 matplotlib numpy pandas jupyter keras-gpu
conda activate quadcopter
 ```

 or a Conda CPU environment:

 ``` batch
conda create -n quadcopter python=3.6 matplotlib numpy pandas jupyter keras
conda activate quadcopter
 ```

Create an IPython kernel for the quadcopter environment:

``` batch
python -m ipykernel install --user --name quadcopter --display-name "quadcopter"
 ```

Open the Jupyter notebook for the project:

``` batch
 jupyter notebook Quadcopter_Project.ipynb
```

Before running code, change the kernel to match the quadcopter environment by using the drop-down menu (Kernel > Change kernel > quadcopter)

## Tools

Visualisation of agent learning can be done using visualise.py:

```
python visualise.py --help
usage: visualise.py [-h] [--save] [num_episodes]

positional arguments:
  num_episodes  Number of episodes to render

optional arguments:
  -h, --help    show this help message and exit
  --save        Write animation to disk instead of displaying
```

For example the following will generate a movie containing the tope five training episodes:

```
python visualise.py 5
```

## References

The following resources were used in developing this project:

- [Continuous Control with Deep Reinforcement Learning](https://arxiv.org/abs/1509.02971)
- [Neural Network Weight Regularization](https://chrisalbon.com/deep_learning/keras/neural_network_weight_regularization/)
- Quadcopter 3d visualsation was based on code by Daniel Ingram (daniel-s-ingram) taken from [PythonRobotics](https://github.com/AtsushiSakai/PythonRobotics) repository
