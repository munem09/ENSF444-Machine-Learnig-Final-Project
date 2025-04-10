#  SmartHomePrice – AI-Powered Real Estate Price Prediction

##  Overview

**SmartHomePrice** is a machine learning project designed to predict California housing prices based on various features such as median income, house age, total rooms, and geographic location. Developed as part of a university course project (*ENSF 444: Machine Learning Systems*), this model is intended for a fictional client, **Skyline Realty**, to support informed pricing decisions in the real estate market.

Our approach compares the performance of three regression models:
- Linear Regression (baseline)
- Random Forest Regressor (non-linear)
- Gradient Boosting Regressor (non-linear)

We implemented model training, evaluation using proper regression metrics, and fine-tuned the best-performing model using **GridSearchCV**.

---

##  Dataset

We used the [California Housing Dataset](https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv), accessed directly via GitHub for seamless Google Colab integration.

Originally, our project proposal used the **Ames Housing dataset (Kaggle)**. Due to accessibility issues in Google Colab with Kaggle data, we substituted it with the California Housing dataset, which aligned well with our prediction goals.

---

##  Features

Key features from the dataset include:
- `median_income`: Most influential predictor of price.
- `housing_median_age`: Age of homes in the area.
- `total_rooms`, `households`: Size and occupancy factors.
- `latitude`, `longitude`: Geographic location impacts price significantly.

---

## ⚙️ Models Used

| Model              | Description |
|-------------------|-------------|
| **Linear Regression** | Simple baseline model for comparison. |
| **Random Forest**      | Ensemble tree-based model; handles non-linear relationships well. |
| **Gradient Boosting**  | Boosting method that builds strong learners from weak learners. |

---

##  Evaluation Metrics

We evaluated model performance using:

- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R² Score**

>  **Random Forest** achieved the best results with an **R² score of 0.82**, indicating strong predictive accuracy.

---

##  Hyperparameter Tuning

To optimize the Random Forest model, we implemented **GridSearchCV** to fine-tune:
- `n_estimators`
- `max_depth`
- `min_samples_split`

This ensured that our model was not only performant by default but also tailored to our dataset through systematic tuning.

---

## Feature Importance

We analyzed the top predictors using `feature_importances_` from the Random Forest model. The most impactful features were:
- `median_income`
- `latitude`
- `housing_median_age`
- `total_rooms`

These insights helped interpret model predictions in a real-world context.

---

## Academic Integrity & Citations

This project was completed collaboratively by:
- **M Munem Morshed**
- **Maliha Chowdhury Adrita**

We used **peer programming** and equally contributed to coding, model training, and result analysis. Maliha led the presentation and report writing, while Munem managed technical implementation in Google Colab.

### Resources & Tools:
- **Scikit-Learn**, **Pandas**, **NumPy**, **Seaborn**, **Matplotlib**
- **Stack Overflow** and **Scikit-Learn documentation** for implementation support
- **ChatGPT** (used for guidance, clarification, and refinement — not for full code generation)

---

## Future Improvements

- Engineer new features like `rooms_per_household`, `bedrooms_per_room`
- Include external datasets (e.g., proximity to schools, crime rates)
- Apply feature selection techniques (e.g., Recursive Feature Elimination)
- Deploy the model in a user-friendly web app

---

## File Structure

```bash
├── SmartHomePrice_Project.ipynb  # Main Jupyter notebook
├── README.md                     # Project overview
