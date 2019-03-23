# Notes of *Spike Neural Models*

## Function Parts of a Neuron
- ***Dendrites***
  
  The "input device". Gather the spikes from neighboring neurons and send them to the soma.
- ***Soma***

  The "Central Processing Unit". Process the signal from the dendrites and transmits to the axon.
- ***Axon***

  Deilver the signal to other neurons.

## Elements of Neuronal Dynamics

### Rest Potential

  - The cell membrane has a strong negative polarization of about $u_{rest}=-65mV$.
  - ***Depolarize***: An input at an *excitatory synapse* reduces the negative polarization of the membrane.
  - ***Hyperpolarize***: An input at an *inhibitory synapse* increases the negative polarization of the membrane.

### Postsynaptic Potentials

Note the time course of the membrane potential of neuron i with $u_i(t)$. Suppose the neuron j fires its spike at t = 0, we got:

$$
    u_i(t) = 
    \begin{cases}
    u_{rest} & t < 0 \\
    u_{rest} + \epsilon_{ij}(t) & t \ge 0
    \end{cases}
$$

Function $\epsilon_{ij}(t)$ defines the ***postsynaptic potential (PSP)*** caused by the arrival of a spike from neuron j at an synapse of neuron i. 

If $\epsilon_{ij}(t) > 0$ it's called the ***excitatory postsynaptic potential (EPSP)*** , and $\epsilon_{ij}(t) \le 0$, the ***inhibitory postsynaptic potential (IPSP)*** .
### Firing Threshold and Action Potential

The *PSP* responds linearly as long as there are only few input spikes, so the membrane potential is approximately the sum of the input spike:
$$u_{i}(t) = \sum_{i} \sum_{j} \epsilon_{ij}(t) + u_{rest}$$

Linearity no more holds when too many spikes arrive in a short interval. If membrane potential reaches the critical threshold $\vartheta$, the membrane potential exhibits a pulse-like excursion. The amplitude is called ***action potential***, typically 100mV. The pulse will propagate alone the axon.

After the pulse, the membrane passes through a phase of hyperpolarization below $u_{rest}$, and is called "***spike-afterpotential*** ".

Single EPSP have amplitudes in range of 1mV. The critical threshold $\vartheta$ is about 20mV~30mV above the $u_{rest}$, so about 20~50 presynaptic spikes within a short interval result in a pulse.

## Zero Order Spike Response Model SRM0

### Definitions
- $t_i^{(f)}$: Firing time, the moment $u_i(t)$ reaches $\vartheta$ from below.
  $$
    \begin{cases}
    u_i(t)=\vartheta \\
    \frac{d}{dt}u_i(t) > 0
    \end{cases} \Rightarrow t = t_i^{(f)}
  $$
- $\eta(t-t_i^{(f)})$: The trajectory of the membrane potential during a spike. Here we make use of the fact that the action potentials have roughly the same form.
  Example:
  $$
  \eta(t-t_i^{(f)})=
  \begin{cases}
  \frac{1}{\Delta t} & 0 < t - t_i^{(f)} < \Delta t \\
  -\eta_0 exp(-\frac{t-t_i^{(f)}}{\tau}) & \Delta t < t - t_i^{(f)}
  \end{cases}
  $$

### Expression
$$
    u_i(t)=\eta(t-\hat{t}_i) + \sum_{j} \sum_{f} \epsilon_{ij}(t - t_j^{(f)}) + u_{rest}
$$
Here the $\hat{t}_i$ is the last firing time of neuron i, i.e., $\hat{t}_i=max\{t_i^{(f)} | t_i^{(f)} < t \}$.

Note that there is only action potential for the last pulse, the expression only models the behavior near $\hat{t}_i$.

### Limitations
  - Cannot describe the process of *adaptation* happens in the ***regularly-firing neurons***

    Adaptation is a slow process builds up over several spikes. The figure below shows the adaptation in the first several spikes.

    ![Regularly-firing Neurons](https://raw.githubusercontent.com/AlbertYoung0112/Notes/master/SNM-Img/RegularlyFiringNeurons.png)

    SRM0 can well approximate another type of neurons, ***fast-spiking neurons*** , which show no adaptation.
    
    ![Fast Spiking Neurons](https://raw.githubusercontent.com/AlbertYoung0112/Notes/master/SNM-Img/FastSpikingNeurons.png)

  - Cannot approximate the ***bursting neurons***
    
    The bursting neurons fire the spike in separate groups.

    ![Bursting Neurons](https://raw.githubusercontent.com/AlbertYoung0112/Notes/master/SNM-Img/BurstingNeurons.png)
  - No ***post-inhibitory rebound***
  
    Post-inhibitory rebound occurs when inhibitory input is removed.

    ![Rebound Spikes](https://raw.githubusercontent.com/AlbertYoung0112/Notes/master/SNM-Img/ReboundSpike.png)


## Neuronal Coding
### Rate Codes
- Rate as a Spike Count / Average over Time

  The temporal average. Set up a time window and count the spikes occurs in the window. Typically the window opens for *T* = 100ms or *T* = 500ms.
  
  Though commonly used, the code introduces significant laterncy which is originated from the low-pass feature of the time window.
lalalal
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjQyMTk3MzkwLDY0NTI2ODcyMF19
-->