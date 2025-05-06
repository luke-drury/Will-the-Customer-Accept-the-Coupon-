# Will-the-Customer-Accept-the-Coupon-
AI/ML Practical Application 1

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the data
df = pd.read_csv('coupons.csv')

# Set Seaborn theme
sns.set(style="whitegrid")

# Example 1: Count plot of coupon acceptance by education level (categorical)
plt.figure(figsize=(8, 5))
sns.countplot(data=df, x='education', hue='Y')
plt.title('Coupon Acceptance by Education Level')
plt.xlabel('Education Level')
plt.ylabel('Count')
plt.legend(title='Accepted Coupon')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

# Example 2: Histogram of age (continuous) split by acceptance
plt.figure(figsize=(8, 5))
sns.histplot(data=df, x='age', hue='Y', multiple='stack', kde=True)
plt.title('Age Distribution by Coupon Acceptance')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.legend(title='Accepted Coupon')
plt.tight_layout()
plt.show()

# Example 3: Box plot of income by acceptance (continuous vs. binary)
plt.figure(figsize=(8, 5))
sns.boxplot(data=df, x='Y', y='income')
plt.title('Income Distribution by Coupon Acceptance')
plt.xlabel('Accepted Coupon')
plt.ylabel('Income')
plt.tight_layout()
plt.show()

# Example 4: Subplot with 2 categorical plots
fig, axes = plt.subplots(1, 2, figsize=(14, 5))

sns.countplot(data=df, x='gender', hue='Y', ax=axes[0])
axes[0].set_title('Coupon Acceptance by Gender')
axes[0].set_xlabel('Gender')
axes[0].set_ylabel('Count')

sns.countplot(data=df, x='car_owner', hue='Y', ax=axes[1])
axes[1].set_title('Coupon Acceptance by Car Ownership')
axes[1].set_xlabel('Car Owner')
axes[1].set_ylabel('Count')

plt.tight_layout()
plt.show()
