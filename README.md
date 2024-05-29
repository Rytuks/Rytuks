# Sample Python code for analyzing physiotherapy treatments

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Sample data
data = {
    'Group': ['Manual Therapy', 'Exercise Therapy', 'Electrotherapy', 'Magnetotherapy', 'Combined Therapy'],
    'Pain Reduction': [3.2, 3.8, 2.9, 2.7, 4.5],
    'Functional Improvement': [15, 25, 18, 17, 30],
    'Satisfaction': [4.1, 4.5, 3.9, 3.7, 4.8]
}

# Convert to DataFrame
df = pd.DataFrame(data)

# Plotting the results
fig, ax = plt.subplots(1, 3, figsize=(18, 5))

# Pain Reduction
ax[0].barh(df['Group'], df['Pain Reduction'], color='skyblue')
ax[0].set_title('Pain Reduction')
ax[0].set_xlabel('VAS Score Reduction')

# Functional Improvement
ax[1].barh(df['Group'], df['Functional Improvement'], color='lightgreen')
ax[1].set_title('Functional Improvement')
ax[1].set_xlabel('Oswestry Score Improvement (%)')

# Satisfaction
ax[2].barh(df['Group'], df['Satisfaction'], color='salmon')
ax[2].set_title('Patient Satisfaction')
ax[2].set_xlabel('Satisfaction Score')

plt.tight_layout()
plt.show()
