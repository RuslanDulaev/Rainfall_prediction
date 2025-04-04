<h1>Прогноз осадков</h1>

<h3>Цель:</h3>
Применение алгоритмов машинного обучения с целью прогнозирования осадков в будущем.  
  
Датасет был взят с сайта Kaggle.  

<h3>Признаки</h3>

В качестве признаков выступают:
- Давление
- Максимальная температура
- Минимальная температура
- Точка росы
- Влажность
- Показатель облачности
- Показатель солнечного света
- Направление ветра
- Скорость ветра
  
В качестве дополнительных признаков были сформированы:
- Разница температур
- Месяц (для данного признака был применен One-hot encoding)

<h3>Примененные алгоритмы</h3>  

Примененные алгоритмы машинного обучения с их значениями score на тестовой выборке:
- DecisioinTreeClassifier - 0.8356
- RandomForestClassifier - 0.8447
- LogisticRegression - 0.8493
- XGBRegressor - 0.8561

Как мы можем видеть, XGBRegressor показал наилучший результат.

Классификационный отчет  
<img width="429" alt="image" src="https://github.com/user-attachments/assets/6af45ad2-d7a0-44ed-b0e2-44546cdc11e6" />

Матрица ошибок  
<img width="398" alt="image" src="https://github.com/user-attachments/assets/d95a87fe-6c8b-4141-81b9-27d57c244a8d" />

Гистограмма важности переменных  
<img width="709" alt="image" src="https://github.com/user-attachments/assets/6f8f06b2-5eb9-4250-a37c-0ca4fe5e4f16" />

Roc-кривые  
<img width="515" alt="image" src="https://github.com/user-attachments/assets/aec481f8-209a-4931-954c-c92589e55414" />

<h3>Выводы:</h3>  

- Модель работает с точностью в 86%
- Класса 1 (дождь будет) модель предсказывает очень хорошо (F1-score = 0.91)
- Высокий recall (0.95) означает, что модель почти не пропускает дождливые дни

