# Will-the-Customer-Accept-the-Coupon-
AI/ML Practical Application 1

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv('coupons.csv')
sns.set(style="whitegrid")

# Plot 1: Count plot of coupon acceptance by education level
plt.figure(figsize=(8, 5))
sns.countplot(data=df, x='education', hue='Y')
plt.title('Coupon Acceptance by Education Level')
plt.xlabel('Education Level')
plt.ylabel('Count')
plt.legend(title='Accepted Coupon')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

# Plot 2: Histogram of age by coupon acceptance
plt.figure(figsize=(8, 5))
sns.histplot(data=df, x='age', hue='Y', multiple='stack', kde=True)
plt.title('Age Distribution by Coupon Acceptance')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.legend(title='Accepted Coupon')
plt.tight_layout()
plt.show()

# Plot 3: Box plot of income by coupon acceptance
plt.figure(figsize=(8, 5))
sns.boxplot(data=df, x='Y', y='income')
plt.title('Income Distribution by Coupon Acceptance')
plt.xlabel('Accepted Coupon')
plt.ylabel('Income')
plt.tight_layout()
plt.show()

# Plot 4: Subplots for gender and destination by acceptance
fig, axes = plt.subplots(1, 2, figsize=(14, 5))

sns.countplot(data=df, x='gender', hue='Y', ax=axes[0])
axes[0].set_title('Acceptance by Gender')
axes[0].set_xlabel('Gender')
axes[0].set_ylabel('Count')

sns.countplot(data=df, x='destination', hue='Y', ax=axes[1])
axes[1].set_title('Acceptance by Destination')
axes[1].set_xlabel('Destination')
axes[1].set_ylabel('Count')

plt.tight_layout()
plt.show()

### Findings: Will the Customer Accept the Coupon?

#### Visual Summary:

- **Education**: High school and college-level users showed higher coupon acceptance. Graduate-level users were more selective.
- **Age**: Younger users (21–30) accepted the most coupons.
- **Income**: Mid-income users ($25K–$74K) were more likely to use coupons.
- **Gender & Destination**: No major gender differences. Acceptance was higher for restaurant and urgent place destinations.
- **Time of Day**: 6PM was the most popular time for coupon usage.
- **Weather**: Sunny days saw significantly more coupon acceptance.
- **Coupon Type**: Popular coupons included Coffee House, Restaurant(<20), and Take Away. Bars and high-end restaurants had lower acceptance.

#### Interpretation & Next Steps:

- Focus campaigns on younger, mid-income users.
- Schedule coupon offers around 6PM and sunny weather.
- Optimize offerings for lower-cost food and drinks.
- Consider redesigning or bundling low-performing coupon types.
