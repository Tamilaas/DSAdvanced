def Predict_Calorie_Burnage(Average_Pulse):
    return (0.4 * Average_Pulse + 280)  # Пример уравнения для предсказания Calorie_Burnage
test_values = [100, 110, 125, 140]
for value in test_values:
    predicted_calorie_burnage = Predict_Calorie_Burnage(value)
    print(f"Average_Pulse: {value}, Predicted Calorie_Burnage: {predicted_calorie_burnage}")

    
import pandas as pd
import matplotlib.pyplot as plt
from scipy import stats
import sys
data = {
    "Duration": [10, 20, 30, 40, 50, 60, 70, 80, 90, 100],
    "Calorie_Burnage": [100, 200, 300, 400, 500, 600, 700, 800, 900, 1000]
}
full_health_data = pd.DataFrame(data)
x = full_health_data["Duration"]
y = full_health_data["Calorie_Burnage"]
slope, intercept, r, p, std_err = stats.linregress(x, y)
def myfunc(x):
    return slope * x + intercept
mymodel = list(map(myfunc, x))
print(mymodel)
plt.scatter(x, y)
plt.plot(x, mymodel)
plt.ylim(ymin=0, ymax=1100)
plt.xlim(xmin=0, xmax=110)
plt.xlabel("Duration")
plt.ylabel("Calorie_Burnage")
plt.show()


import pandas as pd
import matplotlib.pyplot as plt
from scipy import stats
import sys
data = {
    "Duration": [10, 20, 30, 40, 50, 60, 70, 80, 90, 100],
    "Calorie_Burnage": [100, 200, 300, 400, 500, 600, 700, 800, 900, 1000]
}
full_health_data = pd.DataFrame(data)
x = full_health_data["Duration"]
y = full_health_data["Calorie_Burnage"]
slope, intercept, r, p, std_err = stats.linregress(x, y)
def myfunc(x):
    return slope * x + intercept
mymodel = list(map(myfunc, x))
print(mymodel)
plt.scatter(x, y)
plt.plot(x, mymodel)
plt.ylim(ymin=0, ymax=1100)
plt.xlim(xmin=0, xmax=110)
plt.xlabel("Duration")
plt.ylabel("Calorie_Burnage")
plt.show()
