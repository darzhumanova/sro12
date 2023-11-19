import matplotlib.pyplot as plt
import numpy as np

# Задание функций
def function1(x):
    return np.sin(x)

def function2(x):
    return np.cos(x)

def function3(x):
    return np.tan(x)

# Создание массива x значений от -2π до 2π
x_values = np.linspace(-2 * np.pi, 2 * np.pi, 100)

# Вычисление соответствующих y значений для каждой функции
y_values1 = function1(x_values)
y_values2 = function2(x_values)
y_values3 = function3(x_values)

# Построение графиков
plt.figure(figsize=(8, 6))

plt.plot(x_values, y_values1, label='sin(x)')
plt.plot(x_values, y_values2, label='cos(x)')
plt.plot(x_values, y_values3, label='tan(x)')

plt.title('Graphs of Trigonometric Functions')
plt.xlabel('x')
plt.ylabel('y')
plt.axhline(0, color='black',linewidth=0.5)
plt.axvline(0, color='black',linewidth=0.5)
plt.grid(color = 'gray', linestyle = '--', linewidth = 0.5)
plt.legend()
plt.show()
