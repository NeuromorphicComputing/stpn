# Short-term plasticity neurons learning to learn and forget
Short-term plasticity (STP) is a mechanism that stores decaying memories in synapses of the cerebral cortex. In computing practice, STP has been used, but mostly in the niche of spiking neurons, even though theory predicts that it is the optimal solution to certain dynamic tasks. Here we present a new type of recurrent neural unit, the STP Neuron (STPN), which indeed turns out strikingly powerful. Its key mechanism is that synapses have a state, propagated through time by a self-recurrent connection-within-the-synapse. This formulation enables training the plasticity with backpropagation through time, resulting in a form of learning to learn and forget in the short term. The STPN outperforms all tested alternatives, i.e. RNNs, LSTMs, other models with fast weights, and differentiable plasticity. We confirm this in both supervised and reinforcement learning (RL), and in tasks such as Associative Retrieval, Maze Exploration, Atari video games, and MuJoCo robotics. Moreover, we calculate that, in neuromorphic or biological circuits, the STPN minimizes energy consumption across models, as it depresses individual synapses dynamically. Based on these, biological STP may have been a strong evolutionary attractor that maximizes both efficiency and computational power. The STPN now brings these neuromorphic advantages also to a broad spectrum of machine learning practice.

[This work](https://proceedings.mlr.press/v162/rodriguez22b.html) has been accepted to ICML 2022 as Spotlight.

## Quick setup
Use simple_script.py for quick experimentation with the STPN.

    # Install and activate base anaconda environment for STPN
    conda env create -n baseSTPN --file base_conda_environment.yml
    conda activate baseSTPN
    # Train and evaluate STPN in associative retrieval task (Ba et al, 2016)
    python simple_script.py --gpu <-1,0,1,...>

## Experiments in the paper
In the folder for each experiment you will find a README.md with instructions to setup, run and analyse each task.

The plots and tables displayed in the paper can be generated using ICML_all_plots.ipynb 

## Cite
    @article{garcia2022stpn, title = {Short-Term Plasticity Neurons Learning to Learn and Forget}, author = {Garcia Rodriguez, Hector and Guo, Qinghai and Moraitis, Timoleon}, year = {2022}, url = {https://proceedings.mlr.press/v162/rodriguez22b.html}, doi = {10.48550/ARXIV.2206.14048} }