# Библиотека линейной алгебры для Python

Этот модуль содержит несколько полезных классов и функций для работы с линейной алгеброй в Python. 

---

## Обзор

- Класс Vector  
    - Этот класс представляет вектор произвольного размера и операции над ним.  

    **Обзор методов:**    
        
    - constructor(components : list) : инициализировать вектор 
    - set(components : list) : изменяет компоненты вектора
    - __str__() : toString метод
    - component(i : int): получает i-й компонент (начинается с 0)
    - size() : получает размер вектора (количество компонентов) 
    - euclidLength() : возвращает евклидову длину вектора.
    - operator + : векторное сложение
    - operator - : векторное вычитание
    - operator * : скалярное умножение и скалярное произведение  
    - operator == : возвращает истину, если векторы равны, в противном случае - ложь.   
    - copy() : копирует этот вектор и возвращает его.
    - changeComponent(pos,value) : изменяет указанный компонент. 
    - norm() : нормализует этот вектор и возвращает его. 

- Функция zeroVector(dimension)  
    - возвращает нулевой вектор 'dimension'  
- Функция unitBasisVector(dimension,pos)  
    - возвращает единичный базисный вектор с единицей в индексе 'pos' (индексирование в 0)
- Функция axpy(scalar,vector1,vector2)  
    - вычисляет операцию axpy
- Функция randomVector(N,a,b)
    - возвращает случайный вектор размера N со случайными целочисленными компонентами между 'a' и 'b'.
- Класс Matrix
    - Этот класс представляет собой матрицу произвольного размера и операции над ней.

    **Обзор методов:**  
    
    -  __str__() : возвращает строковое представление
    - operator * : реализует матричное умножение векторов
                   реализует матрично-скалярное умножение.
    - changeComponent(x,y,value) : изменяет указанный компонент.
    - component(x,y) : возвращает указанный компонент.
    - width() : возвращает ширину матрицы  
    - height() : возвращает высоту матрицы
    - operator + : реализует матричное сложение. 
    - operator - : реализует матричное вычитание
    - operator == : возвращает истину, если матрицы равны, в противном случае - ложь.
- Функция squareZeroMatrix(N)  
    - возвращает квадратную нулевую матрицу размерности NxN 
- Функция randomMatrix(W,H,a,b)  
    - возвращает случайную матрицу WxH с целочисленными компонентами между 'a' и 'b'  
---

## Документация

Модуль хорошо документирован. Вы можете использовать встроенный в Python ```help(...)``` функция.
Например: ```help(Vector)``` дает вам всю информацию о классе Vector.  
или ```help(unitBasisVector)``` дает вам всю необходимую информацию о
глобальная функция ```unitBasisVector(...)```. Если вам нужна информация об определенном
метод, который вы вводите ```help(CLASSNAME.METHODNAME)```.  

---

## Использование

Вы найдете модуль в **src** каталог называется ```lib.py```. Вам необходимо  
импортировать этот модуль в свой проект. В качестве альтернативы вы также можете использовать файл ```lib.pyc``` в байт-коде python.   

---

## Тесты

В каталоге **src** вы также можете найти набор тестов, который называется ```tests.py```.  
Набор тестов использует встроенный python-test-framework **unittest**.  
