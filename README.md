This project is a graphical BMI (Body Mass Index) calculator built using Python's tkinter library for the user interface and matplotlib for data visualization. The application allows users to input their weight (in kilograms) and height (in meters) to calculate their BMI. Based on the calculated BMI, it categorizes the result into one of four groups: Underweight, Normal, Overweight, or Obese.

Once a BMI is calculated, the result is displayed on the interface and automatically saved in a CSV file named bmi_data.csv. This file stores the weight, height, BMI value, and its category. The application also includes a feature to visualize the trend of BMI values over time using a line graph, where the x-axis represents weight and the y-axis shows the corresponding BMI values.

To run this application, Python must be installed on your system. The interface uses tkinter, which is included with Python, and the graphing functionality relies on the matplotlib library, which you can install using pip install matplotlib if not already available.

Running the application is straightforward—simply execute the Python file (bmi_calculator.py) and a window will open for you to input your details. After entering your weight and height, click on the “Calculate BMI” button to see your result. You can also click on “Show Graph” to visualize how your BMI has changed across multiple entries.

This project is ideal for beginners learning GUI development in Python. It also introduces basic file handling with CSV and data visualization using plots. Future improvements could include adding a timestamp to each entry, supporting height in centimeters, and showing average BMI statistics.

Developed with simplicity in mind, this project can be easily extended or integrated with health-monitoring applications. Feel free to explore and modify it for your own use or learning.

