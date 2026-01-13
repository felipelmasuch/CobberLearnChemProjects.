# CobberLearnChemProjects.
Projects for Foundations of Machine Learning for Chemistry
import matplotlib.pyplot as plt
import os

# 1. Create the data lists
carbons = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
boiling_points = [-161.5, -89.0, -42.1, -0.5, 36.1, 68.7, 98.4, 125.7, 150.8, 174.1]

# 2. Create the directory if it doesn't exist
directory = "AlkaneBoilingPoints"
if not os.path.exists(directory):
    os.makedirs(directory)

# 3. Create the scatterplot
plt.figure(figsize=(8, 5))
plt.scatter(carbons, boiling_points, color='blue', edgecolor='black')

# 4. Add labels and title
plt.title('Boiling Point of Linear Alkanes vs. Number of Carbons')
plt.xlabel('Number of Carbon Atoms')
plt.ylabel('Boiling Point (°C)')
plt.grid(True, linestyle='--', alpha=0.7)

# 5. Save the plot to the specified directory
file_path = os.path.join(directory, "alkane_plot.png")
plt.savefig(file_path)

print(f"Plot successfully saved to: {file_path}")

# 6. Display the plot
plt.show()
