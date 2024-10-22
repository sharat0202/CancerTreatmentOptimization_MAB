This assignment is part of the masters program under subject Deep Reinforcement Learning. This assignment aims to optimize cancer treatment selection using a multi-armed bandit algorithm.

# Cancer Treatment Optimization using Multi-Armed Bandit Algorithm

#### Problem Statement:
You are a data scientist working in cancer research, collaborating with a medical institution that conducts clinical trials for different treatment protocols. The objective is to optimize the allocation of resources (Research time, and funding) across diverse treatment arms within breast cancer clinical trials. The primary goal is to identify the most efficacious and personalized treatment strategies while minimizing resource expenditure and expediting the development of effective treatments for cancer patients.
#### Consider the following aspects:
Treatment Arms and Patient Response: Each treatment arm represents a different treatment technique (Harmone Therapy, Radiation Therapy, Chemotherapy and Surgery). Different arms might have varying efficacies (Treatment status – Either success (Value 1) or Failure (Value 0)), cancer characteristics such as radius, texture etc., budget and treatment duration.

### Project Overview

In this project, we employ a multi-armed bandit algorithm to choose the most effective treatment for cancer. The treatments available include Chemotherapy, Hormone Therapy, Radiation Therapy, and Surgery. The bandit algorithm helps balance exploration (trying different treatments) and exploitation (choosing the treatment that has previously yielded the best results).
Dataset Features

The dataset consists of 569 observations with the following features:

    diagnosis: Type of cancer diagnosis (e.g., benign or malignant).
    radius_mean: Mean radius of the tumor.
    texture_mean: Mean texture of the tumor.
    perimeter_mean: Mean perimeter of the tumor.
    area_mean: Mean area of the tumor.
    smoothness_mean: Mean smoothness of the tumor.
    compactness_mean: Mean compactness of the tumor.
    concavity_mean: Mean concavity of the tumor.
    concave points_mean: Mean concave points of the tumor.
    symmetry_mean: Mean symmetry of the tumor.
    fractal_dimension_mean: Mean fractal dimension of the tumor.
    Treatment Type: The type of treatment applied (Chemotherapy, Hormone Therapy, Radiation Therapy, Surgery).
    Treatment status: Outcome of the treatment (0 = Failure, 1 = Success).
    Budget: Available budget for treatment (in dollars).
    Time: Time required for treatment (in days).

### Multi-Armed Bandit Algorithm

The multi-armed bandit approach is used to dynamically choose the best treatment strategy based on past performance. The bandit algorithm explores different treatment types and learns which treatment yields the highest success rate. This learning is quantified using Q-values, which represent the expected reward (success rate) of each treatment.
Learned Q-values for Treatments

The learned Q-values after training are as follows:

    Chemotherapy: 0.2555
    Hormone Therapy: 0.3396
    Radiation Therapy: 0.2879
    Surgery: 0.3236

These Q-values suggest that Hormone Therapy has the highest expected success rate, followed by Surgery, Radiation Therapy, and Chemotherapy.
Key Objectives

    Goal: Optimize the selection of cancer treatment to maximize treatment success.
    Challenges: Handling the exploration-exploitation trade-off in selecting treatments.
    Evaluation: The algorithm evaluates each treatment based on the success rate, budget, and treatment duration.

### Conclusion

The multi-armed bandit approach enables adaptive selection of cancer treatments, leading to improved treatment success based on historical data. The learned Q-values help in making informed decisions about which treatment to apply for future patients, considering factors like budget and time constraints.