# Сортировки массивов
## Задание
Цель мониторинга работы приложения – поиск узких мест в системе, обусловленных нехваткой ресурсов – аппаратных или информационных. В качестве исходных данных для анализа узких мест могут использоваться данные, получаемые со счетчиков производительности.
В качестве основных средств предлагается использовать следующие инструменты:
1.	Модуль timeit 
2.	Модуль cProfile
3.	Модуль pyheat
4.	Средства ОС Windows: Монитор Ресурсов (resource monitor); Монитора производительности (perfmon).

![Фото](https://raw.githubusercontent.com/RakovAl/laba2/95369270432c9a1f1ad73a9ee24cf3de2c47e08f/100.jpg?token=BIOBIWD6DSKBFQ4TZEM74MLGIESEY)
"Время для 100 элементов методом слияния"

![Фото](https://raw.githubusercontent.com/RakovAl/laba2/95369270432c9a1f1ad73a9ee24cf3de2c47e08f/image.png?token=BIOBIWDPP4IYJWUIT2ALNYDGIESQU)

"Нагрузка для 100 элементов методом слияние"

| Алгоритм | 100 эл.    | 10000 эл. | 1000000 эл. |
|:----------:|:------------:|:-----------:|:-------------:|
| Пузырек  |  0.58 мс.  | 5.8 с.     | -           |
| Быстрая  | 0.6 мс. | 9 мс.     | 1 с.     |
| Слиянием | 0.07 мс.   | 8 мс.     | 760 мс.     |

[Сортировка пузырьком](https://ru.wikipedia.org/wiki/Сортировка_пузырьком)  
[Быстрая сортировка](https://ru.wikipedia.org/wiki/Быстрая_сортировка)  
[Сортировка слиянием](https://ru.wikipedia.org/wiki/Сортировка_слиянием)  

**Пример кода сортировки методом пузырька.**

```
from random import randint
N = 100
a = []
for i in range(N):
    a.append(randint(1, 9999))
for i in range(N-1):
    for j in range(N-i-1):
        if a[j] > a[j+1]:
            a[j], a[j+1] = a[j+1], a[j]
```
