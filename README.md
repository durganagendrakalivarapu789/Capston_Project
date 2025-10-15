# Capstone Project 1: Body Measurement Analysis (NHANES Dataset)

This Jupyter Notebook implements **Capstone Project 1**, analyzing adult male and female body measurements from the **NHANES dataset** using **NumPy**, **Pandas**, **Matplotlib**, and **Seaborn**.  
It follows the project instructions step-by-step — from data loading and preprocessing to advanced visualization and interpretation.

---

## 🔹 Key Sections and Functionality

### **Q1. Importing Libraries**
- Imported **NumPy**, **Pandas**, **Matplotlib**, and **Seaborn** for data handling, analysis, and visualization.  
- Verified Matplotlib setup with `print(plt)`.

### **Q2. Data Loading**
- Loaded `male.csv` and `female.csv` into Pandas DataFrames and converted them into NumPy matrices.  
- Verified shapes:  
  - `male`: (4081, 7)  
  - `female`: (4221, 7)  
- Columns include: **weight, height, upper arm/leg length, arm/hip/waist circumference**.

### **Q3. Histograms of Weights**
- Extracted weights for both genders.  
- Created subplots:  
  - Female (top, skyblue)  
  - Male (bottom, lightgreen)  
- Set common x-axis limits for direct comparison.

### **Q4. Boxplot of Weights**
- Plotted box-and-whisker comparison of male and female weights.  
- Highlighted **medians, ranges, and outliers**.

### **Q5. Numerical Aggregates**
- Calculated **mean, median, standard deviation, IQR, and skewness**.  
- Observations:  
  - Males → higher mean (87 kg) and variability.  
  - Females → lower mean (74 kg), more consistency.  
  - Both distributions → right-skewed.

### **Q6. Add BMI to Female Matrix**
- Computed **BMI = weight / (height/100)²**.  
- Added as 8th column; verified updated shape.

### **Q7. Standardized zfemale Matrix**
- Computed **z-scores** for all female features to form the standardized matrix `zfemale`.

### **Q8. Pairplot and Correlations**
- Selected standardized features: **Weight, Height, Waist, Hip, BMI**.  
- Created **pairplot** and computed **Pearson & Spearman correlations**.  
- Found strong positive relationships (e.g., Weight–BMI ≈ 0.85).

### **Q9. Add Waist Ratios**
- Calculated **Waist-to-Height** and **Waist-to-Hip** ratios.  
- Appended to both matrices:  
  - Female → 10 columns  
  - Male → 9 columns  
- Verified updated shapes.

### **Q10. Boxplot of Ratios**
- Plotted waist ratio comparisons by gender.  
- Found males have higher **waist-to-hip median (~0.9)** vs. females (~0.8), suggesting **greater central fat**.

### **Q11. Metric Pros & Cons**
| Metric | Advantage | Limitation |
|--------|------------|------------|
| **BMI** | Simple, widely used | Ignores muscle/fat distinction |
| **Waist-to-Height** | Predicts health risk | Overlooks muscle mass |
| **Waist-to-Hip** | Shows fat distribution | Influenced by bone structure |

### **Q12. Extreme BMI Measurements**
- Sorted by BMI and displayed standardized (`zfemale`) data for:
  - **5 lowest BMI individuals:** Lean profiles (negative z-scores).  
  - **5 highest BMI individuals:** Obesity risks (positive z-scores).

---

## 🔹 Overall Insights
- **Males** exhibit greater variability and higher central fat distribution.  
- **Females** show more consistent body measurements.  
- Strong inter-feature correlations confirm body metrics are interdependent.  
- Demonstrates how **NumPy, Pandas, and visualization tools** can uncover health insights from multidimensional data.

---

**Conclusion:**  
This project showcases a structured data analysis workflow—combining statistical computation, visualization, and interpretation—to derive meaningful physiological insights from NHANES body measurement data.
