# VR-Immersion-Headsets-Motion-Insights

A Python-based analysis of user experiences with Virtual Reality (VR) platforms using data visualization, correlation analysis, and actionable insights. The dataset explores factors such as immersion levels, motion sickness, VR headset usage, and demographic details to uncover trends and suggest improvements in VR design and usability.

---

1. **Data Exploration**:
   - Analyzes the impact of factors like age, gender, VR headset usage, and motion sickness on immersion levels.

2. **Correlation Analysis**:
   - Examines the relationships between different factors such as immersion level, motion sickness, and VR usage duration.

3. **Advanced Visualizations**:
   - Generates comprehensive plots including histograms, scatterplots, violin plots, and heatmaps for meaningful insights.

4. **Actionable Insights**:
   - Provides solutions to improve VR user experiences based on data trends.

5. **Data Cleaning and Transformation**:
   - Replaces categorical variables with numerical mappings for easier analysis.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/vr-experience-analysis.git
   cd vr-experience-analysis
   ```
   
2. Install required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```
   
3. Download dataset from Kaggle:
   - [Virtual Reality Experiences Dataset](https://www.kaggle.com/datasets/aakashjoshi123/virtual-reality-experiences)

---

## Recommeneded Tools : Google Colab or Kaggle



## Dataset Overview

The dataset contains the following columns:
- **Gender**: User's gender (Male, Female, Other).
- **VRHeadset**: VR headset used (Oculus Rift, HTC Vive, PlayStation VR).
- **MotionSickness**: Level of motion sickness experienced (Low, Medium, High).
- **Age**: Age of the user.
- **Duration**: Duration of VR usage in minutes.
- **ImmersionLevel**: User's reported immersion level (Low, Medium, High).

---

## Analyzing the Code

### 1. Data Loading and Exploration
Load and preview the data after downloading the data from kaggle:
```python
import pandas as pd
data = pd.read_csv('path/to/data.csv')
print(data.head())
```

### 2. Data Visualization
#### Histogram and KDE for Age Distribution:
```python
import seaborn as sns
import matplotlib.pyplot as plt

plt.figure(figsize=(12, 6))
sns.histplot(data=data, x='Age', bins=20, kde=True)
plt.title('Age Distribution')
plt.show()
```

#### Scatter Plot for Age vs. Duration:
```python
sns.scatterplot(data=data, x='Age', y='Duration', hue='Gender', palette='Set2')
plt.title('Age vs. Duration of VR Usage')
plt.show()
```

#### Heatmap for Correlation:
```python
sns.heatmap(data.corr(), annot=True)
plt.title('Correlation Heatmap')
plt.show()
```

### 3. Correlation Analysis
Analyze the relationships between variables:
```python
correlation_matrix = data.corr()
print(correlation_matrix)
```

### 4. Visualization
#### Pair Plot:
```python
sns.pairplot(data=data, hue='ImmersionLevel', diag_kind='kde', palette='viridis')
plt.show()
```

#### Violin Plot for Motion Sickness vs. Age:
```python
sns.violinplot(data=data, x='Age', y='MotionSickness', hue='ImmersionLevel', palette='viridis')
plt.title('Motion Sickness vs. Age Group')
plt.show()
```

---

## Insights and Recommendations

1. **Motion sickness decreases with increased immersion level.**
   - **Solution**: Enhance immersion through high-quality visuals, reduced latency, and realistic interaction design.

2. **Younger users use VR for longer durations.**
   - **Solution**: Ensure VR comfort during extended use, focusing on ergonomics for younger demographics.

3. **Males are more likely to use VR than females or other genders.**
   - **Solution**: Develop inclusive VR experiences that appeal to diverse audiences.

4. **Oculus Rift, HTC Vive, and PlayStation VR are popular VR headsets.**
   - **Solution**: Prioritize compatibility with these platforms to maximize user reach.

5. **Males report higher immersion levels.**
   - **Solution**: Understand and address gender-based preferences to create more engaging experiences.

6. **Higher immersion leads to longer VR usage.**
   - **Solution**: Focus on content quality and engaging narratives to retain users.

7. **Younger users are more prone to motion sickness.**
   - **Solution**: Offer customization options like adjustable frame rates and field-of-view settings to minimize discomfort.

8. **Design a smart wearable with demographic considerations.**
   - **Solution**: Develop hardware that integrates comfort, performance, and user feedback for better VR adoption.

---

---

## Use Cases

### **Scenario 1: Improving Immersion for Younger Users**
- **Objective**: Reduce motion sickness for younger users with high immersion levels.
- **Steps**:
  1. Analyze motion sickness trends by age group.
  2. Customize VR hardware/software for younger users, focusing on smoother performance.

### **Scenario 2: Increasing VR Adoption Among Women**
- **Objective**: Broaden VR usage among female users.
- **Steps**:
  1. Analyze gender-based usage patterns and immersion levels.
  2. Develop gender-neutral VR environments with tailored content.
     
### **Scenario 3: Platform-Specific Compatibility**
- **Objective**: Optimize VR experiences for popular headsets.
- **Steps**:
  1. Analyze the dataset for trends in headset usage.
  2. Ensure VR content compatibility with Oculus Rift, HTC Vive, and PlayStation VR.

---

## Future Work

1. **Expand Demographic Data**:
   - Include more user details like geographic location and occupation.

2. **Longitudinal Studies**:
   - Study changes in VR usage over time for the same users.

3. **Hardware Analysis**:
   - Analyze the impact of hardware specifications on user experiences.
  
4. **Machine Learning**:
   - Use predictive models to suggest personalized VR content.


---

## Contributing

Contributions are welcome! Please feel free to fork the repository and submit pull requests.

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). 
