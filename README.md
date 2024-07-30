# Parkinson's Electrophysiological Signal Dataset (PESD) 


**About**

Parkinson's Electrophysiological Signal Dataset (PESD) is built by Michigan Tech Brain-Inspired AI Lab (https://sites.google.com/mtu.edu/hongyu/).
Dataset generated from Cortico-basal-ganglia network for parkinsonian computational model.
The computational model of cortico-basal-ganglia is originally presented by Fleming et al., in the article named "Simulation of Closed-Loop Deep Brain Stimulation Control Schemes for Suppression of Pathological Beta Oscillations in Parkinson's Disease", which is available at https://pubmed.ncbi.nlm.nih.gov/32194372/. 

**Please cite [1] if you use the dataset in your work.**
 
**Dataset Description:**

The dataset contains electrophysiological signals from both healthy and parkinsonian subjects. We have generated 900 samples, with 600 samples from parkionsian subjects and 300 samples from healthy subjects, respectively. Each sample includes two types of signals: Beta Average Rectified Voltage (ARV) and Local Field Potential (LFP) from the Subthalamic Nucleus (STN). The ARV sigansls are in frequency domain and LFP signals are in time domain. 

Beta ARV Signal: The controller beta values are determined by calculating the Average Rectified Value (ARV) of the beta band. This is achieved by fully rectifying the filtered LFP signal using a fourth-order Chebyshev band-pass filter with an 8 Hz bandwidth, centered around the peak of the LFP power spectrum.
Local Field Potential (LFP) - STN: Local Field Potentials are derived from the synchronized activity of neuron populations between the cortex, STN, and thalamus.

More details can be found in our article named, **“Preliminary Results of Neuromorphic Controller Design and a Parkinson's Disease Dataset Building for Closed-Loop Deep Brain Stimulation”**, available at https://arxiv.org/abs/2407.17756
 
**Model Parameters:**
- Random Seed: Used to ensure the reproducibility of random processes during the setup and simulation of the neural network. This includes generating random neuron positions, random spike times for Poisson-distributed spike trains, and random distributions for synaptic weights.
- Population Size (Pop_size): Refers to the size of the neuronal populations within the cortico-basal ganglia network model. It defines the number of neurons in each population within the simulation, including cortical, striatal, STN (subthalamic nucleus), GPe (external segment of the globus pallidus), GPi (internal segment of the globus pallidus), and thalamic populations.
- Ctx_dc_offset (unit: nA-mA): This is a constant current applied to cortical neurons within the simulated network. The current modulates the baseline activity of cortical neurons by altering their membrane potential, influencing their likelihood of firing action potentials. This parameter helps model tonic excitation or inhibition effects in the cortical population.
- Beta Burst Modulation Scale (unit: nA-mA): Refers to the amplitude of a modulating current applied to cortical neurons, defining the strength of the current that modulates cortical neurons during beta bursts.
- SteadyStateDuration (unit: ms): Indicates how long to wait before applying stimulation. Steady state is crucial for ensuring the stability and interpretability of the neural model simulations.
- RunTime (unit: ms): Specifies the duration to run the simulation after reaching a steady state.
 
**Acknowledgement:**

This work was supported by the program: Disability and Rehabilitation Engineering (DARE) of National Science Foundation under Award Number 2301589. In addition, the authors deeply appreciate Dr. Kuba Orłowski and Dr. Madeleine Lowery from University College Dublin for generously sharing their knowledge on Parkinson’s disease, computational model, and closed-loop Deep Brain Stimulation.

 

The dataset is under the CC0 1.0 Universal license. 

**Related Works:**

[1] Ananna Biswas, Hongyu An, "Preliminary Results of Neuromorphic Controller Design and a Parkinson's Disease Dataset Building for Closed-Loop Deep Brain Stimulation"	arXiv preprint  arXiv:2407.17756 (2024). 
