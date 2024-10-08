# Отток клиентов «Бета-Банка»

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

<b> Цель проекта </b> - спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. 

Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. 

<b> Описание данных </b>

Признаки:

- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — сколько лет человек является клиентом банка
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата

Целевой признак:
- Exited — факт ухода клиента

<b>Задачи проекта:</b>
- Подготовить данные.
- Исследовать баланс классов, обучить модель без учёта дисбаланса. 
- Улучшить качество модели, учитывая дисбаланс классов. Обучить разные модели и найти лучшую по значению F1-меры (минимальный порог 0.59). 
- Провести финальное тестирование.

В ходе исследования качество трех выбранных моделей было оценено на данных без изменений и после корректировки балланса классов. 

Получена улученная модель. Обученная модель случайного леса со взвешенными классами адекватна, что подтверждается ее значением AUC-ROC 0.839. Точность попадания по классам = 0.853, precision = 0.673, recall = 0.544 и целевая для исследования метрика f1 = 0.602. 
