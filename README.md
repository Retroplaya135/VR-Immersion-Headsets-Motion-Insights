# VR-Immersion-Headsets-Motion-Insights

A comprehensive Python-based analysis of user experiences with Virtual Reality (VR) platforms using data visualization, correlation analysis, and actionable insights. The dataset explores factors such as immersion levels, motion sickness, VR headset usage, and demographic details to uncover trends and suggest improvements in VR design and usability.

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
   
3. Ensure the dataset is downloaded from Kaggle:
   - [Virtual Reality Experiences Dataset](https://www.kaggle.com/datasets/aakashjoshi123/virtual-reality-experiences)

---

## Dataset Overview

The dataset contains the following columns:
- **Gender**: User's gender (Male, Female, Other).
- **VRHeadset**: VR headset used (Oculus Rift, HTC Vive, PlayStation VR).
- **MotionSickness**: Level of motion sickness experienced (Low, Medium, High).
- **Age**: Age of the user.
- **Duration**: Duration of VR usage in minutes.
- **ImmersionLevel**: User's reported immersion level (Low, Medium, High).

---

## Usage Examples

### 1. Data Loading and Exploration
Load and preview the data after downloading the data from kaggle:
```python
import pandas as pd
data = pd.read_csv('path/to/data.csv')
print(data.head())
```
