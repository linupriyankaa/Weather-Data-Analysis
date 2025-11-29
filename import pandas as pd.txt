import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("weather.csv")

print(data)

avg_temp = data["Temp"].mean()
max_temp = data["Temp"].max()
min_temp = data["Temp"].min()
total_rain = data["Rainfall"].sum()

print("Average Temp:", avg_temp)
print("Highest Temp:", max_temp)
print("Lowest Temp:", min_temp)
print("Total Rainfall:", total_rain)

plt.plot(data["Date"], data["Temp"])
plt.xlabel("Date")
plt.ylabel("Temp")
plt.title("Temp Trend")
plt.show()

plt.plot(data["Date"], data["Humidity"])
plt.xlabel("Date")
plt.ylabel("Humidity")
plt.title("Humidity Analysis")
plt.show()



plt.bar(data["Date"], data["Rainfall"])
plt.xlabel("Date")
plt.ylabel("Rainfall")
plt.title("Rainfall Analysis")
plt.show()
