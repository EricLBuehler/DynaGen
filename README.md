# DynaGen: Predicting Dynamical Evolution of Data Fields using an Attention-based Diffusion Model

The DynaGen model allows the prediction of dynamical field data based on microstructure input. In the attached sample Jupyter notebook, the model is applied to dynamic fracture problems in brittle materials, trained on molecular dynamics (MD) simulation results. 

Dynamic fracture is an important area of materials analysis, assessing the atomic-level mechanisms by which materials fail over time. Here, we focus on brittle materials failure and show that an atomistically derived progressive transformer diffusion machine learning model can effectively describe the dynamics of fracture, capturing important aspects such as crack dynamics, instabilities, and initiation mechanisms. Trained on a small dataset of atomistic simulations, the model generalizes well and offers a rapid assessment of dynamic fracture mechanisms for complex geometries, expanding well beyond the original set of atomistic simulation results. Various validation cases, progressively more distinct from the data used for training, are presented and analyzed. The validation cases feature distinct geometric details, including microstructures generated by a generative neural network used here to identify novel bio-inspired material designs for mechanical performance. For all cases, the model performs well and captures key aspects of material failure.  

### Reference: 

[1] M.J. Buehler, Modeling Atomistic Dynamic Fracture Mechanisms Using a Progressive Transformer Diffusion Model, J. Appl. Mech., 89(12): 121009, 2022.

URL: https://asmedigitalcollection.asme.org/appliedmechanics/article-abstract/89/12/121009/1146377/Modeling-Atomistic-Dynamic-Fracture-Mechanisms 

![image](https://user-images.githubusercontent.com/101393859/225880041-92f07002-4b74-4198-abbe-2891a2cd6ed8.png)

### How to install and use

Create conda environment and activate:

```
 conda create -n DynaGen python=3.8
 conda activate DynaGen
```

Then, install DynaGen:

```
pip install -e .
```
Start Jupyter notebook/lab:

```
jupyter-lab --no-browser
```

Open the sample Jupyter file and train and/or load pretrained models. 

### Sample results 

All example results taken from [1].

First, an example of a dynamical trajectory of cracking. Fracture initiation occurs at the same location as in the atomistic simulation. 

![image](https://user-images.githubusercontent.com/101393859/225990125-bcafc985-5482-4134-a89f-143a7122237e.png)

Second, examples of how different microstructures yield disct fracture behavior. In the top example, no fracture initiation is observed. In the bottom example, fracture is initiated at certain locations. For these comparisons, only the last predicted frame is analyzed. 

![image](https://user-images.githubusercontent.com/101393859/225990181-f752a8ec-fa44-4a15-82aa-395a74fa71d1.png)

### Acknowledgements

This code is based on [https://github.com/lucidrains/imagen-pytorch](https://github.com/lucidrains/imagen-pytorch). 

```
@article{BuehlerASME_JAP_2022,
    title   = {Modeling Atomistic Dynamic Fracture Mechanisms Using a Progressive Transformer Diffusion Model},
    author  = {M.J. Buehler},
    journal = {J. Appl. Mech.},
    year    = {2022},
    volume  = {89},
    pages   = {121009},
    url     = {https://doi.org/10.1115/1.4055730}
}
```
