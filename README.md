```
import matplotlib.pyplot as plt
import numpy as np

P0 = 1000
r = 0.05
t_max = 10

population_for = [P0]
for t in range(t_max):
    population_for.append(population_for[-1] * (1 + r))

population_while = [P0]
t = 0
while t < t_max:
    population_while.append(population_while[-1] * (1 + r))
    t += 1

t_array = np.arange(t_max + 1)

plt.plot(t_array, population_for, label='For Loop')
plt.plot(t_array, population_while, label='While Loop', linestyle='--')
plt.xlabel('Time (years)')
plt.ylabel('Population')
plt.title('Population Growth Model')
plt.legend()
plt.show()
```
