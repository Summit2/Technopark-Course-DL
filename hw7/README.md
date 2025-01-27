ДЗ7 Metric learning

Задание:  
В рамках данного домашнего задания предлагалось решить задачу поиска похожего автомобиля в базе данных (автомобиля того же класса). На основе датасета [cars196](https://paperswithcode.com/sota/metric-learning-on-cars196) , ссылка на данные [мета](https://drive.google.com/file/d/1PD-lbbcKSelDeAYKafe3boc5mqqEe7X7/view?usp=sharing) [data](https://drive.google.com/file/d/1l9EnYMC-xGX706SY1kN8RceMmFViASfx/view?usp=sharing).


Что было сделано:
0. Выбрана модель эмбеддера, кодирующая изображения

1. Подготовлен обучающий набор данных
    1. Реализуйте корректный класс Dataset и Dataloader для выбранной модели
    2. Добавлены аугментации в датасет

2. Реализован корректный train-loop и обучение модели:  
    1. Модель обучена c Triplet loss
    2. Triplet loss + hard negative mining
    3. Модель с Contrastive loss

 
3. Проведена валидация обученных моделей на тестовой выборке, вычислены метрики Recall и Precision
Для формирования предсказаний на тестовой выборке осуществлялся поиск на основе получившихся эмбеддингов с помощью библиотеки Faiss

4. Результаты работы модели были проинтерпретированы с помощью GradCam



Полезные ссылки:
[metric learning](https://github.com/KevinMusgrave/pytorch-metric-learning)  
[GradCam](https://github.com/jacobgil/pytorch-grad-cam)