# Master Syllabus: Computational Neuroscience, Cognitive AI, & Cloud-Native MLOps
## Phase 1: Mathematical Foundations & Biophysical Modeling (Months 1–2)
**Core Objective:** Master the mathematical frameworks required to express biological and physical neural phenomena in deterministic equations before writing any complex software.

### 1.1 Linear Algebra for Neural State Spaces
 * **Vector Spaces & Bases:** Coordinate systems, linear independence, basis transformations, and spanning sets.
 * **Matrix Transformations:** Matrix multiplication mechanics, determinants, matrix inversion, and system of linear equations solutions.
 * **Eigendecomposition:** Calculating eigenvalues and eigenvectors; understanding spectral theorems and their application to neural stability analysis.
 * **Dimensionality Reduction:** Singular Value Decomposition (SVD), Principal Component Analysis (PCA) mathematics, and low-dimensional projection of high-dimensional neural population vectors.
 * **Tensor Algebra:** Multi-dimensional arrays, tensor outer products, and Kronecker products for multi-layered network layers.

### 1.2 Continuous Calculus & Dynamical Systems
 * **Multivariate Calculus:** Limits, continuous functions, partial derivatives, directional derivatives, gradients, and Jacobians.
 * **Ordinary Differential Equations (ODEs):** First-order and second-order linear ODEs, homogenous and non-homogenous equations.
 * **Numerical Integration Algorithms:**
   * Forward Euler Method: Implementation, error accumulation, and step-size stability limits.
   * Runge-Kutta Methods (RK2 and RK4): High-accuracy integration for stiff differential equations.
 * **Phase Plane Analysis:** Fixed points, nullclines, vector fields, stability criteria, and bifurcation theory (Saddle-Node, Pitchfork, and Hopf bifurcations in neural firing).

### 1.3 Probability, Statistics, & Information Theory
 * **Probability Distributions:** Continuous and discrete distributions (Gaussian, Poisson, Binomial, and Exponential) used to model neural noise and spike timing.
 * **Stochastic Processes:** Markov chains, Poisson point processes for action potential modeling, and random walks.
 * **Bayesian Inference:** Bayes' Theorem derivation, prior probabilities, likelihood estimation, posterior distributions, and the "Bayes-Optimal Brain" hypothesis.
 * **Information Metrics:** Shannon Entropy, Mutual Information, Kullback-Leibler (KL) Divergence, and Signal Detection Theory (ROC analysis for sensory thresholds).

### 1.4 Biophysical Neuron Modeling (Computational Neuroscience)
 * **Membrane Biophysics:** Nernst equation for equilibrium potentials, Goldman-Hodgkin-Katz (GHK) equation for multi-ion membrane permeability.
 * **Equivalent Circuit Models:** Modeling lipid bilayers as capacitors and ion channels as variable resistors.
 * **Leaky Integrate-and-Fire (LIF) Model:**
   * Mathematical formulation:
     
   * Analytical solutions, threshold boundaries, reset conditions, and refractory period equations.
 * **Hodgkin-Huxley (HH) Model:**
   * Gating variables (m, h, n) and their voltage-dependent alpha/beta transition rates.
   * Sodium (Na^+) and Potassium (K^+) conductance tracking.
   * Simulating action potential generation from scratch via explicit numerical integration.
## Phase 2: Synaptic Plasticity, Neuro-Inspired AI, & Deep Learning (Months 3–5)
**Core Objective:** Implement biological learning rules inside scalable code structures and master the foundational machine learning architectures that mimic cognitive processes.

### 2.1 Synaptic Plasticity & Learning Rules
 * **Hebbian Learning Mechanisms:** Classical formulation ("neurons that fire together, wire together"), mathematical constraints, and Oja's rule for stability.
 * **Long-Term Potentiation (LTP) & Long-Term Depression (LTD):** Cellular mechanisms translated into phenomenological weight-update equations.
 * **Spike-Timing-Dependent Plasticity (STDP):** Causal vs. anti-causal exponential timing windows, asymmetric weight modification functions, and homeostatic synaptic scaling.

### 2.2 Domain Simulation Toolkits
 * **The Brian2 Ecosystem:** Numerical equations-based network modeling syntax, defining custom differential equations inside strings, NeuronGroup, Synapses, and state monitors.
 * **The NEURON Simulator:** Morphological modeling, multi-compartment structures, cable equations, inserting custom channel mechanisms via NMODL files, and Python bindings (neuron library).

### 2.3 Foundations of Machine Learning & PyTorch Primitives
 * **Artificial Neural Networks (ANN):** Multi-Layer Perceptrons, activation functions (Sigmoid, Tanh, ReLU, LeakyReLU), and loss metrics (MSE, Cross-Entropy).
 * **Optimization Engines:** Gradient Descent, Stochastic Gradient Descent (SGD) with momentum, RMSprop, and Adam optimization.
 * **Backpropagation Calculus:** Computational graphs, partial derivative chain-rule distribution, and manual derivation of gradients through backprop layers.
 * **PyTorch Architecture:** Tensors, autograd engines, nn.Module subclassing, custom Dataset and DataLoader construction, and running compute workloads on local GPUs.

### 2.4 Cognitive & Neuro-Inspired Architectures
 * **Recurrent Neural Networks (RNNs):** Hidden state updates, temporal sequence processing, vanishing/exploding gradient problems, Backpropagation Through Time (BPTT).
 * **Memory Models (LSTM & GRU):** Gating vectors (input, forget, output gates) for maintaining long-term dependencies and modeling human working memory.
 * **Transformers & Visual Networks:** Self-attention mechanics, Query-Key-Value matrix scaling, positional encodings, and Convolutional Neural Networks (CNNs) as models of the ventral visual stream.
 * **Spiking Neural Networks (SNNs) in ML:** Surrogate gradient descent methods to bypass non-differentiable thresholds, and the snnTorch / SpikingJelly libraries.
 * **Reinforcement Learning (RL):** Markov Decision Processes (MDP), Q-Learning, Deep Q-Networks (DQN), Policy Gradients, Actor-Critic setups, and mapping temporal-difference learning to the biological basal ganglia and dopamine pathways.
## Phase 3: Production-Grade Research Engineering & Core MLOps (Months 6–7)
**Core Objective:** Transition from fragile local notebooks into reproducible, automated, version-controlled, and highly auditable research software pipelines.

### 3.1 Linux Systems & Automation Core
 * **Shell Architecture:** POSIX file hierarchies, standard streams (stdin, stdout, stderr), redirection, and piping structures.
 * **Bash Scripting:** Variables, control flow, functions, writing automation wrappers for long-running computational scripts.
 * **Process Management:** Background execution (&, nohup), terminal multiplexing (tmux, screen), system monitoring (top, htop, nvtop), and signaling (kill -9).
 * **Remote Server Management:** OpenSSH client configurations, public/private key pairs, file synchronizations (rsync, scp).

### 3.2 Advanced Version Control
 * **Git Mechanics:** Internals (blobs, trees, commits, refs), staged state management, branch merging strategies (GitFlow, trunk-based development).
 * **History Re-engineering:** Rebasing, cherry-picking, interactive rebasing, reflogs, and conflict resolution mechanisms.
 * **Collaborative GitHub Ecosystem:** Managing Pull Requests, branch protection rules, semantic versioning tag conventions (v1.0.0).

### 3.3 Containerization via Docker
 * **Container Isolation Physics:** Linux namespaces, cgroups, file system layers vs. hypervisor virtual machines.
 * **Writing Optimized Dockerfiles:** Base selection (ubuntu, python, nvidia/cuda), caching strategy optimization, multi-stage builds to limit asset weight, environment variables configurations.
 * **Container Execution Mechanics:** Runtime mappings, network exposes, volume attachments for mounting datasets, and multi-container orchestration via Docker Compose.

### 3.4 Operational MLOps Foundations
 * **Experiment Tracking Architecture:** MLflow and Weights & Biases (W&B) client/server integrations. Logging execution hyperparameters, loss metrics, custom evaluation plots, and binary model artifacts.
 * **Data Versioning (DVC):** Abstracting data state from git tracking, hashing massive dataset dumps (EEG, fMRI, or simulation traces), and setting up remote storage targets (MinIO/S3).
 * **Continuous Integration (CI):** Setting up GitHub Actions pipelines to automate code checking (flake8, black) and systematic code execution testing (pytest).
## Phase 4: Cloud-Native Architecture & Kubernetes Orchestration (Months 8–10)
**Core Objective:** Design, provision, and automate the execution of distributed computing resources capable of scaling intensive cognitive models across hardware clusters.

### 4.1 Kubernetes (K8s) Core Architecture
 * **Control Plane Components:** API Server, etcd state databases, Kube-Scheduler, and Controller Managers.
 * **Worker Node Runtimes:** Kubelet loop, Kube-Proxy networking, and container execution layers (containerd).
 * **Kubernetes Manifest Objects:**
   * Workloads: Pods, ReplicaSets, Deployments, and StatefulSets.
   * Networking: ClusterIP, NodePort, LoadBalancer Services, and Ingress routing rules.
   * Configuration & Secrets: ConfigMaps, Secrets, Env mappings.
   * Storage Systems: PersistentVolumes (PV), PersistentVolumeClaims (PVC), and dynamic StorageClasses.

### 4.2 Infrastructure as Code (IaC) & Packaging
 * **Declarative Infrastructure via Terraform:** Providers, resource blocks, dependencies tracking, state file management, and cluster automated provisioning.
 * **Kubernetes Package Control via Helm:** Writing parameterized Helm Charts, handling values.yaml overlays, chart version configurations, and repository maintenance.

### 4.3 High-Performance Computing & GPU Allocation
 * **NVIDIA Container Toolkit:** Mapping underlying GPU drivers into container runtimes.
 * **Kubernetes Device Plugins:** Activating cluster awareness for [nvidia.com/gpu](https://nvidia.com/gpu) resources.
 * **Hardware Scheduling Topology:** Node affinities, anti-affinities, taints, and tolerations for assigning tasks to dedicated high-performance hardware nodes.
 * **Compute Budget Enforcement:** Setting deterministic resource requests and limits for CPU cores, system RAM, and GPU instances.

### 4.4 Enterprise Pipeline Orchestration (Kubeflow)
 * **Kubeflow Architecture:** Platform components, custom resource definitions (CRDs), and pipeline controllers.
 * **Kubeflow Pipelines (KFP):** Building modular pipeline components using the KFP Python SDK, defining processing DAGs (Directed Acyclic Graphs).
 * **Distributed Training Systems:** Orchestrating multi-node parallel model processes using the Kubeflow Training Operator (PyTorchJob).
## Phase 5: Expert System Integration & Autonomous Cognitive Agents (Months 11+)
**Core Objective:** Architect independent, adaptive agents that combine memory and tool execution, running on an auto-scaling, highly observable cloud network.

### 5.1 Enterprise Model Serving
 * **Inference Compute Engines:** Triton Inference Server, vLLM, and TorchScript compilation paradigms.
 * **Serverless Inference via KServe:** Serverless deployment custom primitives, scaling-to-zero configurations based on ingress demand, canary progressive rollouts, and internal transformer/predictor architectures.

### 5.2 Memory Vector Databases
 * **Embedding Vectors Physics:** High-dimensional distance spaces calculations (Cosine similarity, Dot Product, Euclidean distance).
 * **Vector Engine Implementations:** Milvus, Pinecone, or local Qdrant cluster systems.
 * **Indexing Vector Topologies:** Hierarchical Navigable Small World (HNSW) graphs, Inverted File (IVF-FLAT) indexing, and quantization strategies.
 * **Retrieval-Augmented Generation (RAG):** Context injection mechanisms to act as an external "hippocampus" (long-term factual retrieval) for cognitive systems.

### 5.3 Agentic Design Patterns & Model Context Protocol (MCP)
 * **Model Context Protocol (MCP) Integration:** Designing and deploying standalone MCP servers that expose real-world tools, system file paths, and external data sources securely to AI agents.
 * **Agentic Reasoning Architectures:** Reflection loops, task planning decomposition, multi-agent communication networks.
 * **Execution Libraries:** LangGraph for cyclic graph state machine definitions, and CrewAI/AutoGen for collaborative multi-agent roles.
 * **The Autonomous Execution Loop:** Structuring system workflows that continuously process incoming streaming data, reason, select tools via MCP, execute actions, and update memory weights without human manual intervention.

### 5.4 High-End Observability & Drift Detection
 * **Platform Metric Collections:** Prometheus time-series database setups and custom metric instrumentations inside application endpoints.
 * **Visualizing Production States:** Building complex Grafana operational and business health tracking dashboards.
 * **Data & System Drift Tracking:** Monitoring statistical changes in model input profiles (Data Drift) and degradation of output accuracy targets (Concept Drift) using tools like Evidently AI, and configuring automated hooks to trigger Kubeflow retrain cycles upon alert.
## Technical Portfolio Milestones to Complete Along the Way
To prove you have mastered this syllabus to employers, you should build the following three projects as you progress through the phases:
 1. **The Biological Core (After Phase 2):** A Python package containing a custom Spiking Neural Network (SNN) that learns a simple navigation task via STDP and Reinforcement Learning, complete with custom differential equations and logged tracking charts.
 2. **The MLOps Lifecycle (After Phase 3):** Take your SNN package, build a custom Docker image for it, and set up an automated script that tests the code and registers the model's performance to an MLflow tracking server.
 3. **The Production Cognitive Agent (After Phase 5):** Deploy a local cluster via kind or cloud instance. Install Kubeflow and KServe. Build a pipeline that trains your model, deploys it via KServe with automated GPU tracking, connects it to a vector database for long-term memory, and monitors system performance on a live Grafana dashboard.
