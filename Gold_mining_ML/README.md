#  Восстановление золота из руды (предсказание эффективности добычи)

### Цели проекта

- Подготовить модель машинного обучения для предскаазания коэффициента восстановления золота из золотосодержащей руды. Доступны данные с параметрами добычи и очистки. Модель необходима для оптимизации производства.  

### План проекта


1. Подготовить данные:

- Проверить эффективность обогащения и вычислить её на обучающей выборке для признака rougher.output.recovery. Найти MAE между расчётами и значением признака.

- Проанализировать признаки, недоступные в тестовой выборке.

- Провести предобработку данных.

2. Проанализировать данные:

- Проанализировать как меняется концентрация металлов (Au, Ag, Pb) на различных этапах очистки.

- Сравнить распределения размеров гранул сырья на обучающей и тестовой выборках.

- Исследовать суммарную концентрацию всех веществ на разных стадиях: в сырье, в черновом и финальном концентратах. Описать выводы и удалить аномалии.

3. Построить модель:

- Написать функцию для вычисления итоговой sMAPE.

- Обучить разные модели и оценить их качество. Выбрать лучшую модель и проверить её на тестовой выборке.

4. Общий вывод
 
### Итоги

- Проанализированы концентрации металлов (Au, Ag, Pb), а также суммарные концентрации веществ на всех стадиях очистки.  

- На данных были обучены модели LASSO, forestregressor и treeregressor
  
- Применены техники кросс-валидации для оценки качества моделей и GridSearchCV для поиска оптимальных гиперпараметров, лучший результат показала модель LASSO: the_total_sMAPE = -8,276.

### Используемый стек инструментов

- python
- pandas
- numpy
- sklearn
- scipy
- matplotlib
- seaborn
