# Примеры из книги Адитья Бхаргава "Грокаем Алгоритмы"

В репизитории собраны примеры кода из книги автора Адитья Бхаргава "Грокаем Алгоритмы"

## Бинарный поиск (binary_search.py)

```
def binary_search(list, item):
    low = 0
    high = len(list) - 1

    while low <= high:
        mid = (low + high) // 2
        guess = list[int(mid)]
        
        if guess == item:
            return mid
        
        if guess > item:
            high = mid - 1
        
        else:
            low = mid + 1
    
    return None


my_list = [1, 3, 5, 7, 9]

print(binary_search(my_list, 3))
print(binary_search(my_list, -1))

```

> Бинарный поиск работает только в том случае, если список отсортирован.