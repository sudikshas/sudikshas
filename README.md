## Sudiksha's Portfolio 👋

📬 [sudiksha1026@gmail.com](mailto:sudiksha1026@gmail.com) &nbsp;|&nbsp; 💼 [LinkedIn](https://www.linkedin.com/in/sudiksha-sarvepalli/) &nbsp;|&nbsp; Currently: Veeva Systems

Hi, I’m Sudiksha — a data science and analytics professional passionate about turning complex data into actionable business insights and building intelligent, data-driven solutions that create real-world, measurable impact. My background spans healthcare analytics, machine learning, causal inference, and generative AI, with a strong interest in applying ML and AI to solve complex business and product strategy problems.

I recently completed my Master’s in Information and Data Science from UC Berkeley while working full-time in data analytics solutions consulting at Veeva Systems. My experience spans longitudinal patient analytics, experimentation, scalable ML pipelines, recommendation systems, and AI-powered applications such as retrieval-augmented generation (RAG) systems and personalized risk engines.

I’m especially excited about opportunities in machine learning, applied AI, and data science where I can combine strong technical foundations with product thinking, user behavior insights, and business strategy to build impactful, user-focused solutions.

## Projects

#### [RecallGuard — AI-Powered Food Safety App](https://github.com/yourusername/recallguard)
* Capstone Project | AWS · FastAPI · React/TypeScript · PostgreSQL · Claude Haiku (Bedrock)*
 
A mobile web application that lets consumers scan barcodes or grocery receipts to instantly check for FDA food recalls and assess ingredient-level risk.
 
- Built a deterministic ingredient risk engine with synonym normalization and fuzzy product matching (RapidFuzz + TF-IDF cosine + Cross Encoder ensemble)
- Integrated AWS Textract for OCR receipt parsing and Claude Haiku via Bedrock for LLM-based ingredient disambiguation
- Designed and deployed full AWS infrastructure: EC2, RDS (PostgreSQL), IAM policies, SES email alerts
- Led technical evaluation, slide deck, and live demo for final presentation 
---
#### [Scalable Flight Delay Prediction: End-to-End ML Pipeline with PySpark & Random Forest](https://github.com/sudikshas/flight-delay-prediction-pyspark)
* Machine Learning at Scale | PySpark · MLlib · Databricks · Delta Lake · Optuna · Python*

Built a distributed ML pipeline to classify U.S. flight delays across 15M+ rows of historical flight and weather data, achieving a ~0.82 weighted F1 score — a 12% improvement over baseline.

- Class-weighted Random Forest model with 36 engineered features to handle severe label imbalance across flight and weather data
- Block-window time-series cross-validation to respect temporal dependencies and prevent data leakage across quarterly splits
- Optuna hyperparameter tuning, reducing tuning time ~40% vs. grid search; Delta Lake checkpointing cut pipeline runtime by ~60%
- Designed for real passenger impact: enabling proactive delay alerts 2–4 hours before departure to inform travel decisions
  
---
#### [RAG Document Q&A System — Persona-Aware Information Retrieval](https://github.com/sudikshas/adaptive-rag-qa-pipeline)
* Generative AI | LangChain · Qdrant · Sentence Transformers · Cohere · Mistral · Ragas · Python*

Built and evaluated an end-to-end Retrieval-Augmented Generation (RAG) pipeline to improve enterprise document search and Q&A for distinct user personas (engineering and marketing), outperforming a general-purpose LLM baseline on faithfulness, context recall, and answer relevance.

- Designed a semantic retrieval pipeline using `RecursiveCharacterTextSplitter` for document chunking and `multi-qa-mpnet-base-dot-v1` sentence transformer embeddings stored in a Qdrant vector database
- Engineered persona-specific LLM generation prompts (Cohere + Mistral) to produce tailored responses for technical and business users, reducing hallucinations through retrieval-grounded generation
- Evaluated system performance using RAGAS metrics (faithfulness, context precision/recall, answer relevance) alongside a custom LLM-as-a-judge scorer (Qwen2.5-7B) and a weighted composite scoring framework
- Authored an executive POC report with methodology, findings, and scaling recommendations for production deployment
  
---
#### [Production NLP API — Sentiment Analysis on AWS EKS](https://github.com/yourusername/w255-nlp-api)
* ML Systems Engineering | DistilBERT · FastAPI · Docker · Kubernetes · Redis · Istio*
 
Deployed a fine-tuned DistilBERT sentiment classifier as a scalable, production-grade REST API on AWS EKS.
 
- Containerized FastAPI service with Docker; orchestrated via Kubernetes/Kustomize with Horizontal Pod Autoscaling
- Redis caching layer to reduce redundant inference calls
- Full observability stack: Istio service mesh + Prometheus metrics + Grafana dashboards
- Load tested with Locust; documented latency and throughput benchmarks
  
---
#### [Graph-Powered Food Delivery Optimization — BART Network Analysis](https://github.com/sudikshas/transit-graph-delivery-optimizer)
* Data Engineering | Neo4j · PostgreSQL · Redis · MongoDB · Python · Cypher · Neo4j GDS*

A proof-of-concept data engineering system that models the SF Bay Area BART network as a graph database to optimize food delivery logistics — selecting high-value pickup stations, clustering delivery zones, and routing orders efficiently across 50 stations and 8,000+ customer locations.

- Applied **Harmonic Centrality** (Neo4j GDS) on a bipartite station-customer graph with geodesic distance filtering to identify optimal BART pickup stations by customer density at 1-, 2-, and 5-mile proximity thresholds
- Implemented **Louvain Modularity** community detection to cluster geographically connected stations and prioritize underserved delivery zones for fleet expansion
- Designed **shortest-path delivery routing** across BART lines, modeling travel times and transfer costs as weighted graph edges
- Integrated **PostgreSQL** for structured customer and station data, **Redis** for real-time delivery state, and **MongoDB** for persistent customer profiles and order history
  
---
#### [U.S. Housing Market Speed — Descriptive Regression Analysis](https://github.com/sudikshas/us-housing-market-speed-regression)
* Statistics | R · ggplot2 · OLS Regression · sandwich/lmtest · stargazer · Zillow API Data*

Descriptive regression study examining the relationship between average home values and 
days-to-pending-sale across 672 U.S. metropolitan regions using Zillow data (June 2024).

- Applied log-log transformation to address heavy right skew in home value distribution, 
  enabling elasticity interpretation of regression coefficients
- Implemented HC1 heteroskedasticity-consistent robust standard errors via the sandwich 
  package to ensure valid inference on real-world housing data
- Enforced strict exploration/confirmation set split (30/70) to prevent data snooping — 
  all modeling decisions made before touching the confirmation set
- Evaluated all large sample linear model assumptions (I.I.D., finite variance, no perfect 
  collinearity) and documented violations with proposed remediation strategies
- Produced publication-quality regression table via stargazer comparing OLS and robust 
  coefficient tests across model specifications
---
#### [Sentiment Classification of Company Reviews — Comparing ML & Deep Learning Architectures](https://github.com/sudikshas/NLP_customer_reviews_classification)
Sentiment Classification of Company Reviews — Comparing ML & Deep Learning Architectures
W207 Applied Machine Learning | Python · TensorFlow/Keras · Scikit-learn · NLTK · Pandas · NumPy
Benchmarked five machine learning models — from a Logistic Regression baseline to Bidirectional LSTM and CNN — on binary sentiment classification of 100,000 real-world customer reviews spanning 45 companies, achieving a best test accuracy of 96.3%.

- Preprocessed and balanced a 100K-review dataset by dropping neutral ratings and sampling 12,000 positive and 12,000 negative reviews to eliminate class bias
- Implemented and compared five architectures: Logistic Regression (baseline), Random Forest, LSTM, Bidirectional LSTM, and 1D CNN — tracking train/validation/test accuracy and loss across all
- Demonstrated that deep learning models dramatically outperform traditional ML for unstructured text: BiLSTM and CNN both exceeded 96% test accuracy vs. 66% for Logistic Regression
- Conducted ablation experiments on dropout, convolutional depth, and embedding dimensionality to assess the impact of hyperparameter choices on generalization
- Found that Bidirectional LSTM achieved the best overall test performance (96.3% accuracy, 0.111 test loss), outperforming standard LSTM by capturing both past and future token context

---
#### [Explainable AI for Racial Bias Detection in CNN Facial Analysis](https://github.com/sudikshas/XAI-Website)
* XAI / Computer Vision | Python · TensorFlow · Keras · Grad-CAM · Integrated Gradients · FairFace · Jekyll*

An interactive research web app that applies Explainable AI (XAI) techniques to a CNN-based racial classification model, surfacing how biased training data produces discriminatory predictions — and making the model's decision-making visible to a general audience.

- Trained CNN classifiers on both a balanced (FairFace, 100K+ images) and a US Census-proportioned biased dataset to directly compare fair vs. skewed model behavior
- Implemented Grad-CAM and Integrated Gradients in Keras to generate gradient heatmaps that localize which facial features drive each prediction
- Demonstrated measurable bias: the biased model misclassifies underrepresented races (e.g., Indian → Latino Hispanic) while failing to learn distinctive facial features, confirmed visually through saliency maps
- Published findings as an interactive educational website targeting public understanding of algorithmic fairness, model transparency, and AI ethics

---
#### [Snapchat Political Ads — Engagement Prediction & Fairness Analysis](https://github.com/sudikshas/Snapchat-Political-Ads-Data-Analysis-Project)
* Python · Pandas · Scikit-learn · Matplotlib · Seaborn · pytz*

End-to-end analysis of 2,000+ Snapchat political ads (2018–2019) to identify characteristics
that drive ad reach, culminating in a fairness-evaluated classification model that predicts
high vs. low view count with ~91% accuracy.

- Engineered time-zone-aware features from raw billing addresses using address parsing and
  pytz, enabling accurate "part of day" release analysis across 115+ cities globally
- Conducted missingness analysis (NMAR/MAR/MCAR) via permutation tests with TVD,
  finding `LocationType` missingness is MAR-dependent on `City` (p = 0.013)
- Ran two permutation hypothesis tests confirming ad spend and release time significantly
  differ between high- and low-reach ads (both p = 0.0, α = 0.05)
- Built a Logistic Regression pipeline with `ColumnTransformer` (OneHotEncoding + StandardScaler)
  tuned via `GridSearchCV`, improving accuracy from 53% (baseline) to 91% (final model)
- Performed fairness evaluation using false positive rate parity across view-count groups
  (p ≈ 0.82), confirming the final model does not disproportionately misclassify either group

---


### Skills

**Languages & Libraries**
`Python` `SQL` `R` 
 
**ML & Stats**
`XGBoost` `scikit-learn` `SHAP` `Logistic Regression` `LLM` `BERT` `TF-IDF` `Causal Inference` `A/B Testing`
 
**MLOps & Cloud**
`AWS (EC2, EKS, Bedrock, RDS, IAM)` `Docker` `Kubernetes` `FastAPI` `Redis` `Prometheus` `Grafana` `Istio` `PostgreSQL`
 
**Data & Visualization**
`Pandas` `NumPy` `Matplotlib` `Seaborn` 


<!--
**sudikshas/sudikshas** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
