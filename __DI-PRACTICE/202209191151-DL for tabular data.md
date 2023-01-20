---
aliases: []
---
Added: 202209191151
Status: #permanent-note 
Tags:
Links: 
### Transformers for Tabular Data at Capital One with Bayan Bruss
https://www.youtube.com/watch?app=desktop&v=g47qowJxzEI

>The irony of the nature of tabular data is that while it is classified as structured data whereas more complex data like image and audio data are considereded unstructured, but the underlying structure of tabular data is far less structured than image and audio data that contain sequential structure where ==data points== in close proximity are highly auto-correlated ands strongly predictive of the next point, meanwhile the proximity of features in tabular data is often meaningless beyond the whims of the agent who assembled it
- Why haven't DL been applied to tabular data
- Complexity of ML models is high for many applications even if DL not used
- Counterfactuals for explainability
	- differentiable
- DL is compositional
	- Tabular data w/ graph DL
	- How do we fuse data from different domain and modalities to find new ways of use
- Structure missing from tabular data (no meaningful proximities)
	- Images structured within the same domain (proximity is important)
	- GNNs and transformers bridge this gap
- How do we **encode** so that it is meaningful for ML (rather than the specific architecture)
	- Encoding schemes have impact on usefulness DL for tabular data
		- Linear projections (SIMPLE)
- the way model is **regularized** impacts the performance 
	- before moving into new domain of ML research need to figure out hwat regularization works for particular domain
	- foundational step
- Data augmentation and synthetic data
	- almost completely lacking for tabular dat
	- NLP and CV have more in depth research around synthetic and augmented data\
	-
- New methods for DL with Tabular data start to outperform XGBoost at a sample of n = 50,000 
- Maybe will progress like NLP
	- example sentiment analysis- small samples used to better approached w/ TFID/Logistic regression, but now large parameter models can tune small datasets
	- hinges on share relation of all natural language data
- What is underlying relation of all tabular data
	- example disease prediction
	- can you pre-tain on large tabular dataset, and transfer to smaller dataset w/ common features
	- extend generic feature encoder from tabular dataset to other task while retaining original structure
### SAINT: Improved Neural Networks for Tabular Data via Row Attention and Contrastive Pre-Training (30:00)
https://arxiv.org/abs/2106.01342
- Taking knowledge from transformers apply to tabular data
- **Intersample attention**
- 

### Transfer Learning with Deep Tabular Models
https://arxiv.org/abs/2206.15306

### Deep Learning with Structured Data with Mark Ryan
https://twimlai.com/podcast/twimlai/deep-learning-structured-data-mark-ryan/

### Graph Analytic Systems with Zachary Hanif - #188
https://twimlai.com/podcast/twimlai/graph-analytic-systems-zachary-hanif/