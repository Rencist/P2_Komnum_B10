import numpy as np
from tabulate import tabulate
import matplotlib.pyplot as plt

class Romberg:
    def trapezoidal(f, a, b, n):
        h = (b - a) / n
        x = a
        In = f(a)
        for k in range(1, n):
            x = x + h
            In += 2*f(x)
        return (In + f(b)) * h * 0.5

    def romberg(f, a, b, rows):
        data = np.zeros((rows, rows))
        def f(x):
            f = eval(func)
            return f
        for k in range(0, rows):
            data[k, 0] = Romberg.trapezoidal(f, a, b, 2**k)
            for j in range(0, k):
                data[k, j+1] = (4**(j+1) * data[k, j] - data[k-1, j]) / (4**(j+1) - 1)
        return data

func = input("function: ")
upper = (int (input("upper bound: ")))
lower = (int (input("lower bound: ")))
rows = (int (input("how many row: ")))

data = Romberg.romberg(func, upper, lower, rows)
print(tabulate(data, headers="123456789", tablefmt="github"))
print("result: ", data[rows-1, rows-1])

x = np.linspace(-100,100,num = 1000)
y = eval(func)
plt.grid(visible=True)
plt.plot(x, y)
plt.show()
plt.xlabel('X Axis')
plt.ylabel('Y Axis')