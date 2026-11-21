# H&M Personalized Fashion Recommendation Engine

## Research Methodology

### 1. Research Objective

To investigate whether a hybrid recommendation system combining collaborative filtering, product metadata and customer attributes improves personalized fashion product recommendations compared with individual recommendation approaches.

### 2. Dataset

H&M Personalized Fashion Recommendations (Kaggle).

- transactions_train.csv
- articles.csv
- customers.csv

Transaction records: 31,788,324

Temporal coverage: 2018-09-20 to 2020-09-22.

### 3. Research Questions

- RQ1: Does collaborative filtering outperform popularity-based recommendations?
- RQ2: Does product metadata improve recommendation quality?
- RQ3: Does a hybrid model outperform individual recommendation methods?
- RQ4: Do customer attributes provide additional recommendation value?
- RQ5: How do models perform under cold-start conditions?
- RQ6: Does hybrid recommendation improve catalogue coverage?

### 4. Research Hypotheses

- H1: Collaborative filtering outperforms popularity-based recommendations.
- H2: Product metadata improves recommendations, particularly for products with limited interactions.
- H3: Hybrid recommendations outperform individual collaborative and content-based models.
- H4: Customer attributes provide additional recommendation value.
- H5: Hybrid recommendations improve product coverage without substantially sacrificing relevance.

### 5. Temporal Data Split

Initial proposed split:

- Training: 2018-09-20 to 2020-07-31
- Validation: 2020-08-01 to 2020-08-31
- Testing: 2020-09-01 to 2020-09-22

The split will be reviewed after examining transaction distributions and customer/product overlap.

### 6. Recommendation Models

- M0: Popularity-based recommendation
- M1: Implicit ALS collaborative filtering
- M2: Item-item collaborative filtering
- M3: TF-IDF and cosine similarity content-based filtering
- M4: Weighted hybrid recommendation
- M5: Customer-aware hybrid recommendation

### 7. Evaluation Metrics

- Precision@K
- Recall@K
- MAP@K
- NDCG@K
- Catalog coverage
- Intra-list diversity

Evaluate at K = 5, 10 and 12.

### 8. Research Experiments

- E1: Popularity baseline
- E2: Collaborative filtering comparison
- E3: Content-based recommendation
- E4: Hybrid model comparison
- E5: Customer feature integration
- E6: Hybrid weight optimization
- E7: Cold-start evaluation
- E8: Ablation studies
- E9: Customer activity segment analysis

### 9. Research Safeguards

- Prevent temporal data leakage.
- Fit preprocessing transformations using training data only.
- Tune hyperparameters using validation data.
- Reserve the test period for final evaluation.
- Avoid publishing competition data.
- Document experiments for reproducibility.

### 10. Planned Deployment

An interactive Streamlit application presenting personalized recommendations, similar products, customer insights and model evaluation results.