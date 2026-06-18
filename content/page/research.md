---
title: Research
type: page
---

### 2026

#### ParticleTransformer is all you need for reconstructing hadronic tau leptons
- This study presents the first fully machine-learned hadronic tau reconstruction approach for the future FCC-ee collider using the CLD detector setup, achieving high performance across tau identification, decay mode classification, charge reconstruction, and four-momentum regression.
- {{< badge "preprint" >}} arXiv:2606.18460
- https://arxiv.org/abs/2606.18460
{{< side-by-side 
    width="100%" 
    img1="/img/2026/particletransformer/architecture.png" 
    img2="/img/2026/particletransformer/resolutions_pt.png"
    alt1="A flowchart illustrating the multi-task ParticleTransformer model architecture for FCC-ee. It takes input particles and processes them to perform tau identification, decay mode classification, charge reconstruction, and full four-momentum regression." 
    alt2="A plot showing the relative visible transverse momentum resolution (lower values are better) as a function of the visible transverse momentum (pt) for the ParticleTransformer (unified and task-specific models) compared to baseline jet reconstruction."
    caption1="We design a unified multi-task ParticleTransformer model that performs tau identification, charge reconstruction, decay mode analysis, and visible momentum regression simultaneously." 
    caption2="The ParticleTransformer model achieves sub-percent visible transverse momentum resolution, significantly outperforming standard jet-reconstruction baselines." 
>}}

#### Machine-learned particle flow as a foundation model for collider physics
- This work demonstrates that the latent representations learned by machine-learned particle-flow reconstruction (MLPF) encode rich physics information, acting as a foundation model that significantly improves downstream analysis tasks like jet flavor tagging, jet energy regression, and missing momentum regression.
- {{< badge "preprint" >}} arXiv:2606.14373
- https://arxiv.org/abs/2606.14373
{{< side-by-side 
    width="100%" 
    img1="/img/2026/mlpf_foundation/illustration.png" 
    img2="/img/2026/mlpf_foundation/roc_btagging.png"
    alt1="A diagram showcasing the machine-learned particle flow (MLPF) foundation model workflow. Low-level detector inputs are mapped to particle-flow candidates, producing rich per-particle latent representations that are shared across downstream analysis tasks like jet flavor tagging, jet energy regression, and missing momentum regression." 
    alt2="A ROC curve showing the performance (true positive rate vs false positive rate) of jet flavor identification (b vs light-flavor quarks) using MLPF latents compared to kinematic features alone."
    caption1="We cast event reconstruction as a foundation model task, leveraging the learned per-particle representations for downstream physics analysis." 
    caption2="Using the MLPF latent representations as features substantially improves the classification performance (AUC) for jet flavor tagging." 
>}}

#### Full event interpretation with machine-learning-based particle-flow reconstruction in the CMS detector
- This work presents the implementation and integration of the machine-learning-based particle-flow (MLPF) reconstruction algorithm within the CMS software framework, demonstrating full-event reconstruction on GPUs with improved jet energy resolution and 5x faster inference compared to standard heuristics.
- {{< badge "accepted" >}} Eur. Phys. J. C (2026) / arXiv:2601.17554
- https://arxiv.org/abs/2601.17554
{{< side-by-side 
    width="100%" 
    img1="/img/2026/cms_mlpf/architecture.png" 
    img2="/img/2026/cms_mlpf/jet_resolution_ttbar.png"
    alt1="A schematic diagram of the MLPF neural network architecture inside the CMS software framework. It visualizes the input and output features (purple), pointwise feed-forward networks (green), and layers with full-event correlations (red) used to predict valid particles, PID, and momentum." 
    alt2="A plot showing the jet energy resolution as a function of generator-level jet transverse momentum (pt) in simulated top quark-antiquark events, comparing the standard CMS particle-flow algorithm (blue) with the machine-learning-based MLPF (red)."
    caption1="The unified machine-learning-based particle-flow (MLPF) neural network architecture integrates directly into the CMS software framework." 
    caption2="The MLPF algorithm achieves a 10–20% improvement in jet energy resolution for jets with transverse momentum between 30 and 100 GeV." 
>}}

### 2025

#### Fine-tuning machine-learned particle-flow reconstruction for new detector geometries in future colliders
- This study demonstrates that a machine-learned algorithm for particle-flow reconstruction, when pre-trained on data from one particle detector, can be successfully fine-tuned for a different detector design to achieve the same performance as a model trained from scratch but with ten times less data.
- {{< badge "published" >}} Phys. Rev. D 111, 092015 (2025)
- https://doi.org/10.1103/PhysRevD.111.092015
{{< side-by-side 
    width="100%" 
    img1="/img/2025/mlpf_finetune/loss.png" 
    img2="/img/2025/mlpf_finetune/results.png"
    alt1="A graph showing the training loss as a function of the training time, comparing the previous graph neural network model (blue) to a transformer model (orange). Using flash attention further speeds up the training (red)." 
    alt2="A graph showing the dependence of the jet resolution measure (lower values are better) as a function of the training dataset size. We compare a model trained from scratch (blue) to a model fine-tunied from an existing checkpoint on another dataset (orange)."
    caption1="We find that using a transformer-based model improves the loss significantly compared to the previous graph neural network based model." 
    caption2="Fine-tuning a pretrained model reduces the required dataset size by about 10x." 
>}}

#### Reconstructing hadronically decaying tau leptons with a jet foundation model
- This paper investigates adapting the OmniJet-a jet foundation model, originally pretrained on a different dataset and task, to reconstruct hadronically decaying tau leptons, demonstrating that fine-tuning the pretrained model significantly improves performance, particularly momentum resolution, compared to training from scratch.
- {{< badge "published" >}} SciPost Phys. Core 8, 046 (2025)
- https://doi.org/10.21468/SciPostPhysCore.8.3.046
{{< side-by-side 
    width="100%" 
    img1="/img/2025/taufm/architecture.jpg" 
    img2="/img/2025/taufm/ptreco.jpg"
    alt1="A figure with two diagrams illustrating workflows for jet foundation models. The left diagram shows the typical workflow: a large jet dataset trains a foundation model, which produces a jet embedding used by a task-specific head for jet tagging. The right diagram shows the paper's approach: the same foundation model is adapted using a smaller hadronic tau dataset for new tasks (tau tagging, kinematic reconstruction, decay mode), with options to fine-tune the model (screwdriver icon) or train task-specific heads from scratch (fire icon)." 
    alt2="A histogram comparing the performance of kinematic reconstruction for hadronically decaying tau leptons using two training methods: fine-tuning a pre-existing model (green distribution) and training a model from scratch (red distribution). The x-axis represents the relative difference between predicted and true transverse momentum (pT_pred - pT_true) / pT_true, and the y-axis shows the normalized bin content. The fine-tuned model's distribution is narrower and centered closer to zero, indicating better performance."
    caption1="We contrast the typical training workflow for jet foundation models with the generalized approach used in this study to adapt an existing model to new datasets and tasks, specifically for hadronic tau lepton reconstruction." 
    caption2="Fine-tuning improves the pT reconstruction resolution by approximately 50% compared to training from scratch on small datasets." 
>}}

#### On the detection of stellar wakes in the Milky Way: a deep learning approach
- This paper assesses the viability of using deep learning trained on simulations to detect stellar wakes induced by dark matter subhalos in the Milky Way's stellar halo, finding the method can infer subhalo presence down to masses of 5x10⁷ M☉.
- {{< badge "published" >}} Astronomy and Astrophysics 693, A227 (2025)
- https://doi.org/10.1051/0004-6361/202451480
{{< side-by-side 
    width="100%" 
    img1="/img/2025/stellarwakes/wake.jpg" 
    img2="/img/2025/stellarwakes/roc.jpg"
    alt1="X-Y plot showing stellar overdensity (color scale) caused by a simulated subhalo (black circle at center). An overdense wake region extends to the left (-X direction), with a dashed contour indicating the half-max density area." 
    alt2="Plot comparing the performance (ROC curves) of machine learning models in detecting three different subhalo masses. The x-axis shows the true positive rate, and the y-axis shows the false positive rate. Each colored line represents a model trained with a different subhalo mass. A dashed black line indicates random chance performance."
    caption1="Simulated stellar overdensity wake induced by a 5x10⁸ M☉ subhalo moving through the stellar halo, projected onto the X-Y plane." 
    caption2="This chart shows how well a machine learning model can find stellar wakes of different mass. A line closer to the bottom-right corner means the model is better at finding the wakes without mistakenly identifying random patterns as wakes." 
>}}

#### A unified machine learning approach for reconstructing hadronically decaying tau leptons
- We show that tau leptons can be efficiently and accurately reconstructed using a multi-task machine learning setup.
- {{< badge "published" >}} Computer Physics Communications 307 (2025)
- https://doi.org/10.1016/j.cpc.2024.109399

### 2024

#### Improved particle-flow event reconstruction with scalable neural networks for current and future particle detectors
- We show that a scalable and portable graph neural network algorithm can efficiently reconstruct stable particles, resulting in more accurate event reconstruction.
- {{< badge "published" >}} Nature Communications Physics 7, 124 (2024) 
- https://doi.org/10.1038/s42005-024-01599-5

#### Tau lepton identification and reconstruction: A new frontier for jet-tagging ML algorithms
- We demonstrate that the transformer-based architecture can be used for tau lepton identification, and that it outperforms alternative approaches based on heuristic algorithms and convolutional nets.
- {{< badge "published" >}} Computer Physics Communications 298 (2024)
- https://doi.org/10.1016/j.cpc.2024.109095

### 2023

#### Dynamics of false vacuum bubbles with trapped particles
- This study investigates the evolution of collapsing false vacuum bubbles using simulations of a coupled bubble-particle system, showing that particle-wall interactions decrease the compactness of the collapsing bubbles and make their collapse to black holes less likely.
- {{< badge "published" >}} Phys. Rev. D 108, 036023 (2023)
- https://doi.org/10.1103/PhysRevD.108.036023

#### A Bayesian estimation of the Milky Way's circular velocity curve using Gaia DR3
- We analyzed large astrophysical datasets to accurately measure the rotation curve of the Milky Way Galaxy.
- {{< badge "published" >}} Astronomy and Astrophysics, Volume 676 (2023)
- https://doi.org/10.1051/0004-6361/202346474

### 2022

#### Sensitivity Estimation for Dark Matter Subhalos in Synthetic Gaia DR2 using Deep Learning
- We applied deep learning based anomaly detection methods to search for rare astrophysical phenomena.
- {{< badge "published" >}} Astronomy and Computing, Volume 41 (2022)
- https://doi.org/10.1016/j.ascom.2022.100667 

### 2021

#### MLPF: Efficient machine-learned particle-flow reconstruction using graph neural networks
- We developed a novel graph neural network based particle flow reconstruction algorithm.
- {{< badge "published" >}} European Physical Journal C, Volume 81 (2021)
- https://doi.org/10.1140/epjc/s10052-021-09158-w

### 2020

#### Data Analysis with GPU-Accelerated Kernels
- I developed a novel approach for large-scale high-energy physics data analysis based on GPUs, accelerating the time-to-insight by ~10x.
- {{< badge "published" >}} Proceedings of Science, Volume 390, ICHEP (2020)
- https://doi.org/10.22323/1.390.0908

### 2018

#### Observation of ttH production
- I developed sensitive matrix-element based statistical analysis tools for the CMS observation.
- {{< badge "published" >}} Phys. Rev. Lett. 120, 231801 (2018)
- https://doi.org/10.1103/PhysRevLett.120.231801

#### Identification of heavy-flavour jets with the CMS detector in pp collisions at 13 TeV
- I developed a novel b-quark identification model (cMVAv2) based on xgboost, thus introducing industry-standard tools to the CMS b-tagging team.
- {{< badge "published" >}} Journal of Instrumentation, Volume 13 (2018)
- https://doi.org/10.1088/1748-0221/13/05/P05011
