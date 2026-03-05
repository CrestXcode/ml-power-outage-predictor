# ⚡ ML Power Outage Duration Predictor
> Predicts whether a power outage will be **Short (≤24hrs)** or **Long (>24hrs)** using Machine Learning

## 🏆 Final Results
| Metric | Score |
|--------|-------|
| **Accuracy** | **70.7%** ✅ |
| **ROC-AUC** | **0.758** ✅ |
| F1 Score | 0.70+ |
| vs Baseline | +20.7% |

## 🗃️ Datasets (4 total)
| Dataset | Source | Role |
|---------|--------|------|
| EAGLE-I 2021-22 | ORNL/Figshare | Grid scale features |
| DOE OE-417 | Maven Analytics | Target variable |
| Okoli 2020 | Mendeley | Microgrid benchmarks |
| NOAA Storm Events | NOAA/NCDC | Weather context |

## 📈 Model Journey
| Step | Approach | Score |
|------|----------|-------|
| 1 | Regression | R²=0.20 ❌ |
| 2 | 3-class Classification | 48.0% |
| 3 | Binary Classification | 66.4% |
| 4 | Tuned Voting Ensemble | 67.6% |
| 5 | **+ Weather Data** | **70.7% ✅** |

## 🔧 Tech Stack
`Python` `Pandas` `Scikit-learn` `XGBoost` `Matplotlib` `Google Colab`

##  ML Pipeline
1. Data collection (4 datasets)
2. Cleaning & merging
3. Feature engineering (50+ features → 30 selected)
4. SelectKBest feature selection
5. Voting Ensemble (RF + XGBoost + Extra Trees)
6. GridSearchCV hyperparameter tuning
