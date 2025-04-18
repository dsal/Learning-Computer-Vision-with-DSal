# Learning Computer Vision
by Ahmad Salehi

# Chapter 1: Introduction
Computer Vision (CV) is a field of AI that enables machines to interpret and process visual data (images/videos) to extract useful information. It involves tasks like object detection, image classification, segmentation, and recognition.
CV enables computers to interpret and analyze visual data (images/videos) like humans. It involves feature extraction, pattern recognition, and decision-making using machine learning and deep learning.

<img src="https://github.com/user-attachments/assets/4cec34f3-58c2-404e-b087-c601e7a48123" width="600"/>

Figure 1_1: The figure illustrates the interdisciplinary nature of computer vision and its distinctions from related fields like image processing and machine vision.

| Field | Definition | Common Uses | Wavelengths & Sensors |
|-------|------------|-------------|-----------------------|
| Image Processing | Enhancing or modifying images without understanding their content | Noise removal, filtering, edge detection, compression | Optical cameras (RGB, InfraRed), scanners|
| Computer Vision | Teaching machines to interpret images like humans do |Object recognition, facial recognition, autonomous driving | RGB cameras, depth sensors (LiDAR), Infrared cameras |
| Machine Vision | Industrial use of vision systems for inspection and automation | Quality control, robotics, barcode scanning | InfraRed (thermal), X-ray, multispectral cameras|

Table 1_1: Image processing vs. computer vision vs. machine vision


| Wavelength Range | Type | Sensor Used | Applications |
|-------|------------|-------------|-----------------------|
| 0.01-10 nm | X-ray Vision | X-ray detectors | Medical purposes |
| 400-730 nm | Visible Light (RGB) | CMOS, CCD | Image classification, object detection |
| 730-1400 nm | Near-InfraRed (NIR) |NIR Cameras | Eye tracking, night vision |
| 1.4-3 um | Short-wave InfraRed (SWIR) | SWIR Cameras | Eye tracking, night vision |
| 3-14 um | Thermal InfraRed (TIR) | Uncooled microbolometers | Heat detection, surveillance, medical imaging |
| 1 mm -  1 m | Radar | Radar sensors | Automotive collision detection |

Table 1_2: Wavelengths and optical sensors used

# 1.1. Key components of computer vision
**Input**: Information Retrieval
Accessing and extracting relevant data from large datasets based on content.
How It Relates to CV:
  - **Image Search & Retrieval**: Finding similar images in a database.
  - **Feature Extraction**: Identifying patterns (edges, colors, textures).
  - **Reverse Image Search**: Matching a given image to known references.
    Example: Google Reverse Image Search uses CV to find visually similar images online.
    
**Output**: Machine Learning
Using algorithms to learn from image data and make predictions.
How It Relates to CV:
  - **Supervised Learning**: Training a model using labeled datasets (e.g., ImageNet for classification).
  - **Unsupervised Learning**: Clustering images without predefined labels (e.g., anomaly detection).
  - **Deep Learning (CNNs, Transformers)**: Models that analyze pixel patterns to recognize objects.
    Example: Self-driving cars use CNNs (Convolutional Neural Networks) to identify road signs, pedestrians, and obstacles.
    Results: Mathematics
    Definition: Mathematical principles that form the backbone of Computer Vision.
    
# 1.2. Key areas in computer vision
CV relies on foundational concepts from several core areas of mathematics and computer science. These key areas provide the theoretical and practical tools needed to process, analyze, and extract meaningful information from images and videos.
  - **Linear Algebra**: for manipulating image data through matrix operations, such as transformations (rotation, scaling) and convolutional filters.
  - **Calculus**: (particularly optimization techniques like gradient descent) for training deep learning models that improve vision-based tasks.
  - **Probability & Statistics**: for handling uncertainty, noise reduction, and probabilistic models like Bayesian filtering.
  - **Geometry**: (especially projective geometry) for tasks such as 3D reconstruction, depth estimation, and camera calibration. For example, epipolar geometry is crucial in stereo vision systems to derive 3D structure from multiple 2D images.
Understanding these areas is fundamental to developing robust computer vision systems, from simple image filters to advanced applications like autonomous driving and medical imaging.

CV systems function as a cohesive pipeline, integrating multiple stages—input processing, machine learning analysis, and mathematical validation, to transform raw visual data into actionable insights. Each component plays a critical role in ensuring accuracy, efficiency, and reliability.
  - **Input (Information Retrieval & Preprocessing)**: Collects and preprocesses visual data. Raw images/videos are acquired (e.g., from cameras or sensors) and refined for analysis. In this step, key tasks include noise reduction (e.g., Gaussian filtering), normalization (rescaling pixel values), and feature extraction (e.g., edges, textures). For instance, a self-driving car’s cameras capture street scenes, which are then cropped and adjusted for lighting.
  - **Output (Machine Learning & Pattern Recognition)**: Analyzes and learns patterns from the data. The purpose of this step is modeling (e.g., CNNs, transformers), detecting and interpreting patterns. In this step, key tasks include In this step, key tasks include, image classification (ResNet, ViT), and semantic segmentation (U-Net). For instance, a medical AI system identifies tumors in X-rays by learning from labeled datasets.
  - **Results (Mathematics)**: Ensures accurate transformations, optimizations, and model reliability. The purpose is ensuring reliablity and efficiency of output. In this step, key tasks include geometric verification (e.g., epipolar constraints in stereo vision), statistical confidence scores (e.g., Bayesian inference), optimization (e.g., backpropagation tuning model weights). For instance, a drone uses 3D triangulation (geometry) to validate its depth-map accuracy.

# 1.3. Core fields of computer vision
CV merges techniques from artificial intelligence, cognitive science, machine learning, and mathematics to enable machines to see and interpret visual data. These core fields work synergistically to solve complex problems—from object detection to autonomous navigation. Below is a breakdown of their roles and interconnections:
  - **Computer Intelligence** → The broad AI-driven approach to decision-making and pattern recognition.
  - **Artificial Intelligence (AI)** → CV is a subset of AI that processes visual data.
  - **Cognitive Vision** → Goes beyond recognition, incorporating context and reasoning.
  - **Machine Learning (ML)** → Deep learning architectures (CNNs, Transformers, GANs) drive modern CV.
  - **Mathematical Foundations**:
    Statistics → Bayesian networks, probabilistic models. | Geometry → 3D reconstruction, camera calibration. | Optimization → Gradient descent, convex optimization.

# 1.4. Vision-specific applications
CV powers a diverse range of applications, each leveraging unique techniques to solve real-world problems. From enabling robots to navigate autonomously to revolutionizing medical diagnostics, these applications highlight the transformative potential of CV. Below is a structured overview of key vision-specific domains and their significance:
  - **Robotic Vision** → SLAM (Simultaneous Localization and Mapping: Allows robots to map unknown spaces while tracking their location.), obstacle detection (Uses depth sensors (LiDAR) or stereo cameras to avoid collisions.)
  - **Control Robotics** → Vision-based control systems in autonomous vehicles. It integrates vision into decision-making for autonomous systems. Applications include autonomous Vehicles (Cameras + LiDAR detect lanes, pedestrians, and traffic signs.), and industrial Robots (Vision-guided arms assemble products or sort items in warehouses.)
  - **Computer Vision** → High-level interpretation (e.g., face recognition, medical imaging); Extracting semantic meaning from visual data. The key tasks include face recognition (Biometric security), and medical imaging (detecting tumors in MRI scans or diabetic retinopathy in retinal images)
  - **Image Processing** → Low-level transformations (e.g., Fourier Transform, edge detection); Enhancing or manipulating raw pixel data. The key techniques are fourier transform (Decomposes images into frequencies used in compression, like JPEG.), and edge detection (identifies object boundaries.)
  - **Neurobiology & Biological Vision** → Bio-inspired AI (e.g., CNNs inspired by the visual cortex); drawing inspiration from human/animal vision to improve AI such as CNN Inspiration (Mimics the visual cortex’s hierarchical processing), and Bio-Inspired Sensors (Event cameras that replicate the retina’s response to light changes)

The field of CV is built on rigorous technical foundations that enable machines to process, analyze, and interpret visual data. These foundations draw from signal processing, physics, and hardware innovations to address challenges like noise reduction, real-time processing, and 3D reconstruction. Below is a detailed breakdown of these core technical pillars:
  - **Signal Processing**: The backbone of low-level image analysis. Key techniques include Fourier Transform (Converts images to frequency domains for compression,JPEG , or noise removal), and filtering (Gaussian/median filters smooth images or enhance edges). For instance, MRI scans use Fourier-based reconstruction to convert raw signals into images.
  - **Multi-variable Signal Processing** → Handles complex, high-dimensional data. The application include Hyperspectral imaging (Captures hundreds of spectral bands: used in agriculture to monitor crop health), and video analysis (Temporal signal processing for motion tracking, e.g., sports analytics).
  - **Non-linear Signal Processing** → Advanced feature extraction techniques; it extracts intricate patterns where linear methods fail. The techniques are wavelet transforms (multi-resolution analysis for texture classification), and morphological operations (shape-based filtering, e.g., erosion/dilation in medical imaging). For example detecting tumor boundaries in ultrasound images using non-linear edge enhancement.
  - **Physics & Imaging** → Models how light interacts with scenes and sensors. Key areas include optics (Lens design, aberrations, and focus models), LiDAR (Time-of-flight principles for 3D depth mapping), and radiance models (Simulates light transport, e.g., for virtual reality rendering). For example, autonomous vehicles use LiDAR physics to correct for weather-related noise.
  - **Smart Cameras** → embeds processing power directly into cameras. The techniques are FPGA/ASIC Chips (Enable real-time edge detection or object tracking without a PC) and event cameras (Mimic the human retina with microsecond latency used in high-speed robotics). For example, surveillance cameras with on-device facial recognition.

CV is a symphony of interdisciplinary domains, each contributing essential capabilities to transform raw visual data into actionable intelligence. Below is a clear breakdown of how these areas interlink to form a cohesive pipeline, along with real-world examples of their synergy:
  - **Physics & Imaging** → Models how light interacts with surfaces (radiance, reflections). It provides the input for signal processing (e.g., modeling lens distortions or LiDAR reflections). In addition, it informs robotics about material properties (e.g., glare on roads for autonomous vehicles). For example, a self-driving car’s camera adjusts exposure based on physics-based radiance models to handle sunlight glare.
  - **Signal Processing** → Transforms raw sensor data (Fourier transforms, wavelets). It cleans data for image processing (e.g., denoising MRI scans with wavelet transforms). In additoin, it extracts features for AI models (e.g., frequency-domain patterns in facial recognition). For example, satellite imagery uses Fourier transforms to compress data before analysis.
  - **Image Processing** → Enhances and segments images for analysis. It feeds preprocessed data to computer vision/AI (e.g., edge-detected images for object detection). Also, it supports robotics with real-time segmentation (e.g., identifying obstacles in industrial settings). For example, medical imaging software sharpens X-rays before tumor detection by a CNN.
  - **Computer Vision & AI** → Recognizes objects, scenes, patterns. It relies on image processing for clean inputs. Also, it directs robotics with actionable insights (e.g., a robot arm picking items identified by a vision model). For example, retail AI uses object recognition to monitor shelf inventory, triggering restocking robots.
  - **Robotics & Smart Applications** → Uses vision for automation and real-world interaction. It is related with physics for environmental interaction (e.g., drone avoiding reflections on water). In addition, it uses AI outputs for decision-making (e.g., warehouse robots navigating via real-time object detection). For example, agricultural drones analyze crop health (CV) and spray pesticides (robotics) using multi-spectral imaging (signal processing).

# 1.5. Deep learning for computer vision
Deep learning has redefined computer vision by enabling machines to automatically learn hierarchical features from raw data, surpassing traditional methods reliant on hand-engineered algorithms. In other words, deep learning has revolutionized computer vision by replacing handcrafted features with end-to-end learning models. Below is a structured overview of its core architectures, methods, and applications:
  - **Convolutional Neural Networks (CNNs)** → Feature extraction from images. Examples: ResNet, VGG, EfficientNet.
  - **Transformers in Vision (ViTs, Swin-Transformer)** → Attention-based models replacing CNNs.
  - **Generative Adversarial Networks (GANs)** → Image generation, super-resolution.
  - **Reinforcement Learning (RL) for Vision** → Used in robotics for real-world decision-making.
In addition, applications of deep learning for CV are:
  - **Object detection & segmentation (YOLO, Mask R-CNN)**: Real-time detection (e.g., traffic monitoring), and pixel-level segmentation (e.g., isolating tumors in scans).
  - **Medical imaging (AI-based tumor detection)**: Reduces radiologist workload (e.g., Google’s LYNA), and early diagnosis of retinal diseases.
  - **Autonomous driving (Tesla uses deep vision networks)**: Processes multi-camera feeds with CNNs, and uses LiDAR + vision fusion.

# 1.6. Hardwave aspects of computer vision: FPGA & Edge AI
To meet the demands of real-time, low-latency CV applications, specialized hardware like FPGAs and Edge AI chips has become critical. These technologies optimize speed, power efficiency, and deployment flexibility, enabling CV systems to operate in resource-constrained environments. Below is a detailed breakdown:
  - **FPGA (Field-Programmable Gate Arrays)**: FPGA is a reconfigurable hardware that can be programmed post-manufacturing for specific tasks. It is ideal for low-latency, parallel processing of vision algorithms, and it provides low-latency, high-performance computation for vision applications. Key applications include real-time object tracking (drones using FPGAs to process 4K video feeds at 60+ FPS for obstacle avoidance), and embedded vision (industrial robots with FPGA-based cameras for defect detection on assembly lines.)
  - **Edge AI**: Edge AI deploys AI models directly on local devices (edge) instead of relying on cloud servers. It moves AI processing to local devices instead of cloud computing, and it addresses latency, privacy, and bandwidth limitations. Benefits of leveraging edge AI include speed (having faster inference), power efficiency (lower power consumption), and privacy (data stays on-device, e.g., facial recognition in secure facilities.). For example, NVIDIA Jetson (NVIDIA Jetson powers robots like Boston Dynamics’ Spot for real-time navigation), smart cameras (Google Coral TPU enables offline object detection in surveillance systems), and autonomous systems (Intel Movidius VPUs process vision tasks in drones and AGVs (Automated Guided Vehicles).

**References**
- [1] Alireza Akhavan Pour: "Computer Vision with Python"
- [2] OpenCV Library
