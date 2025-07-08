# isro_hackathon_novel_aproach
In this project, we proposed RARE-Net, a comprehensive deep learning framework tailored to tackle the pressing challenge of class imbalance in Earth observation satellite data. Rare classes such as water bodies, wetlands, or narrow roads are often underrepresented. To address this, we designed a novel architecture featuring dual decoders—one for dominant classes and one for rare classes—coupled with attention mechanisms and an edge detection branch to improve boundary precision. This architectural setup was built to recognize and segment rare regions more accurately.

Next, we introduced a custom optimizer called GROpt, an improvement over AdamW, which uses gradient clipping, class-wise gradient rescaling, cosine annealing, and warm restarts to ensure stable convergence even when rare class gradients are weak. Optionally, we included a meta-optimizer using LSTM for adaptive learning.

Alongside this, we engineered a hybrid loss function comprising:

Focal Dice Loss for hard samples,

Class-Balanced Lovász Loss for direct IoU optimization, and

Edge Loss for boundary awareness.

These were combined through adaptive weights that are either learned or dynamically scaled based on gradient behavior.

We also focused on uncertainty modeling, applying Monte Carlo Dropout during inference to estimate prediction confidence and generate uncertainty heatmaps, enhancing interpretability and helping to flag low-confidence outputs.

Finally, we conducted extensive ablation studies evaluating the impact of each component—optimizer, loss, and architecture—using metrics like per-class IoU, rare class F1-score, convergence time, gradient norm plots, and loss trends. These experiments confirmed that our methods not only outperform traditional baselines like Adam and Cross Entropy but also exhibit superior generalization and stability, even on pathological cost landscapes such as Rosenbrock and Ackley functions.

This framework is well-suited for real-world Earth Observation (EO) applications like wetland monitoring and small water body detection. We also presented results comparing baseline models with our proposed solution, showing clear improvements.


yt- link  ->  https://youtu.be/-PcGfn7uAu4
