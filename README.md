# River-Valley Loss Landscape Analysis in LLMs

Understanding the geometry of the loss landscape during training is key to grasping the dynamics and generalization properties of large models. Recent work has proposed the River-Valley Hypothesis [1], suggesting that during training, models follow narrow "rivers" in the loss landscape, regions of low curvature in most directions with a small number of steep directions. A characteristic signature of this geometry is that the smallest eigenvalue of the Hessian is close to zero, while the next few are significantly larger. To test this picture, we directly compute the lowest eigenvalues of the Hessian at various checkpoints in the training of large language models (LLMs), using the Pythia family [2]. We use the Lanczos algorithm for efficient extraction of the top eigenvalues, focusing on how the curvature evolves throughout training.

Our broader goal is to understand whether this river-valley structure is universal. We plan to compare across architectures (e.g., CNNs vs. ViTs on ImageNet), and explore the influence of dataset structure, potentially drawing on the concept of sloppiness [3], which posits that certain directions in parameter space are inherently ill-constrained by data. We also aim to construct synthetic datasets to test whether river-like geometries are generic features of optimization or emerge under specific model-data interactions. Finally, recent work connecting Hessian spectra to thermodynamic analogies in LLM training [4] offers a complementary lens, which we may incorporate into our interpretation.

References:

[1] The River-Valley Loss Landscape of Language Models, https://arxiv.org/abs/2410.05192v3

[2] Pythia Model Suite, https://huggingface.co/EleutherAI/pythia-1b/tree/step1000

[3] Data-Induced Sloppiness in Machine Learning, https://arxiv.org/abs/2505.08915

[4] Thermodynamics of Training LLMs, https://arxiv.org/abs/2505.10559
