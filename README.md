Для реализации структуры телефонной книги с использованием HashMap (в Python это будет словарь dict), которая поддерживает несколько телефонов для одного имени и выводит результат, отсортированный по убыванию числа телефонов, можно выполнить следующие шаги:

Создание структуры телефонной книги: Используем словарь, где ключом будет имя, а значением — множество (set) телефонов. Множество используется для автоматического удаления дубликатов.

Добавление данных в телефонную книгу: Для каждого имени проверяем, есть ли оно уже в словаре. Если есть, добавляем номер телефона в соответствующее множество. Если нет, создаем новую запись.

Сортировка и вывод: После добавления всех данных, сортируем телефонную книгу по количеству телефонов (по размеру множества) в порядке убывания.
Объяснение кода:
Функция add_contact:

Проверяет, есть ли имя в телефонной книге. Если есть, добавляет новый телефон в соответствующее множество, если телефона нет — создаёт новую запись.
Множество (set) используется для хранения телефонов, чтобы исключить дубликаты.
Функция print_phonebook:

Сортирует телефонную книгу по количеству телефонов, используя ключ сортировки lambda x: len(x[1]), где x[1] — это множество телефонов. Сортировка идет в порядке убывания (используется reverse=True).
Затем выводит имя и список телефонов для каждого контакта.
