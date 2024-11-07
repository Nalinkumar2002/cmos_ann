
</br>

---

![logo](Images/logo.png)

---


</br>

![Size](https://img.shields.io/github/repo-size/Nalinkumar2002/cmos_ann?color=red)
![Last Commit](https://img.shields.io/github/last-commit/Nalinkumar2002/cmos_ann?color=green)


</br>

# Design of CMOS based Artificial Neural Network (ANN)

This repository presents the design of a CMOS based ANN using CMOS & skywater 130nm PDK


![GIF](Images/gif.gif)



# Table of Contents 

 * [Introduction](#Introduction)
 * [Block-Diagram](#Block-Diagram)
 * [Specifications](#Specifications)
 * [Open Source Tools Used](#Open-Source-Tools-Used)
 * [Clone This Repository](#Clone-This-Repository)
 * [Pre Layout Simulations](#Pre-Layout-Simulations)
   * [Tools And PDK Used For Pre-Layout Simulations](#Tools-and-PDK-used-for-pre-layout-simulations)
     * [Installation Of Tools And PDK](#Installation-of-Tools-and-PDK)
   * [Pre-Layout Schematics And Simulations](#Pre-layout-schematics-and-simulations)
     * [Schematics](#Schematics)
     * [Simulation](#[Simulation)
   * [Executing The Pre-Layout Simulations](#Executing-the-pre-layout-simulations)
 * [Observations](#Observations)
 * [Future Work](#Future-work)
 * [Author](#Author)
 * [Acknowledgements](#Acknowledgements)

# Introduction 

An Artificial Neural Network (ANN) is a computational model inspired by the structure and functions of biological neural networks in the human brain. It consists of layers of interconnected nodes, called neurons, which process information through a system of weighted connections. Each neuron receives inputs, processes them through activation functions, and transmits outputs to other neurons in subsequent layers. This layered structure enables ANNs to learn complex patterns and relationships in data, making them powerful for tasks such as classification, regression, and even decision-making.

ANNs are a foundational element in machine learning and artificial intelligence, with applications in image and speech recognition, natural language processing, medical diagnostics, financial predictions, and many more fields. The training process for ANNs involves adjusting weights using algorithms like backpropagation, enabling them to improve performance on specific tasks by minimizing prediction errors. As they learn from data, ANNs can approximate complex functions and make predictions on unseen data, making them one of the most versatile tools in modern AI.

<h3 align="center">A Simple Neuron Architecture</h3>
<p align="center">
  <img src="Images/ann_pic.png" alt="Project Image" width="400"/>
</p>

<h3 align="center">ANN Model</h3>
<p align="center">
  <img src="Images/ann_pic1.png" alt="Project Image" width="400"/>
</p>

<p align="center">
  <img src="Images/ann_pic2.png" alt="Project Image" width="400"/>
</p>

Designing a CMOS-based Artificial Neural Network (ANN) involves leveraging analog circuitry for efficient and low-power computation, which is particularly suited for edge computing applications and systems with strict energy constraints. In this approach, the Gilbert cell multiplier and a CMOS circuit implementation of the sigmoid activation function are key components.

  🔶   Gilbert Cell Multiplier for Weight Multiplication
The Gilbert cell is a well-known analog circuit structure used for multiplication, traditionally applied in frequency modulation and demodulation.
For ANN design, each neuron connection (synapse) requires a multiplier to scale the input by a corresponding weight. The Gilbert cell provides a compact and efficient method for this multiplication in the analog domain.
The basic configuration of a Gilbert cell uses a differential pair with cross-coupled transistors that produce an output current proportional to the product of the input signals. By using CMOS transistors in this structure, it can be made compatible with standard CMOS fabrication processes.
This analog multiplication enables the neuron to process signals with minimal power and high speed compared to digital multipliers, which can be a bottleneck in traditional ANN implementations.

  🔶   Sigmoid Activation Function in CMOS
The sigmoid function, commonly used as an activation function in neural networks, introduces non-linearity, allowing the network to approximate complex functions and make decisions beyond simple linear separations.
Implementing a sigmoid function in CMOS can be challenging due to its exponential nature. However, various CMOS circuit designs approximate the sigmoid curve effectively.
One approach is to design a circuit that exploits the inherent characteristics of MOS transistors in weak or moderate inversion to approximate the exponential function. By setting up the transistors in specific configurations, it is possible to create an analog sigmoid-like response.
For instance, a differential amplifier with MOSFETs biased appropriately can produce an output that resembles the sigmoid function’s shape, providing the necessary non-linearity for the ANN.

<h3 align="center">Sigmoid - Neural Activation function</h3>
<p align="center">
  <img src="Images/naf.png" alt="Project Image" width="400"/>
</p>





