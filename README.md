# SPECTRAL_REFLECTANCE-DATA-_of_corn_samples
### **Dataset Overview**
The dataset provided contains **spectral reflectance data** of **corn samples** collected using **hyperspectral imaging**. The goal is to predict **DON concentration** (vomitoxin levels) in corn using machine learning.

---

### **Dataset Structure**
- **Rows (Samples)**: Each row represents a **single corn sample**.
- **Columns (Features)**:
  1. **"hsi_id"** (Column 1) → A unique identifier for each sample.
  2. **448 Spectral Reflectance Features** (Columns 2 to 449) →  
     - These columns contain **reflectance values** at different **wavelength bands**.
     - The values range between **0.26 and 0.95**.
  3. **"vomitoxin_ppb"** (Column 450) → **Target Variable**  
     - Represents the **DON concentration (in ppb)** for each sample.
     - Values range from **0 ppb** to **131,000 ppb**.

---

### **Understanding Spectral Reflectance Features**
- The **448 spectral features** correspond to reflectance values recorded at different **wavelength bands**.
- Reflectance is the proportion of **light reflected** by the corn sample at specific wavelengths.
- These features help detect chemical properties related to **DON contamination**.

---

### **Target Variable: DON Concentration (`vomitoxin_ppb`)**
- DON (**Deoxynivalenol**) is a **toxic mycotoxin** produced by fungi in corn.
- High DON levels indicate **contaminated corn**, which is dangerous for **human and animal consumption**.
- The task is to **predict DON concentration** based on spectral features.

---
### Instructions to install Libaries and run the code.

~~~
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
from sklearn.ensemble import RandomForestRegressor
from warnings import filterwarnings
filterwarnings('ignore')
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

from tensorflow.keras.optimizers import Adam
from tensorflow.keras.wrappers.scikit_learn import KerasRegressor
from sklearn.model_selection import RandomizedSearchCV
#import numpy as np

from tensorflow.keras.layers import Conv2D,Conv1D,MaxPooling1D, Dense, Flatten, Dropout, MaxPooling2D
from tensorflow.keras.optimizers import Adam
from tensorflow.keras.wrappers.scikit_learn import KerasRegressor
from tensorflow.keras.layers import LSTM, Dense, Dropout , Bidirectional
~~~
### **WorkFlows**
```
EDA & Feature Engineering --> Dimensionality Reduction --> Model Building & training by Given Data --> Model Evaluation
```

