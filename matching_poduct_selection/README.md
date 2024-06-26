# Поиск подходящих товаров.

## Задача
Компании по продаже товаров необходимо разработать модель, которая для каждого нового товара будет определять пять наиболее схожих по своим признакам товаров из имеющейся базы данных компании. В качестве исходных данных приведены следующие файлы:
1. base.csv - база данных имеющихся у компании товаров (содержит Id товара и 72 столбца с признаками);
2. train.csv - таблица с новыми товарами, к которым необходимо найти близкие товары из файла base.csv(содержит Id товара, 72 столбца с признаками и столбец target c Id наиболее близкого товара из файла base.csv, который подобрал эксперт);
3. validation.csv - таблица с новыми товарами, к которым необходимо найти близкие товары из файла base.csv, для оценки работы алгоритма (содержит Id товара и 72 столбца с признаками);
4. validation_answer.csv - таблица, с Id новоых товаров из файла validation.csv и Id наиболее близких товаров из файла base.csv, который подобрал эксперт.

Оценку качества работы алгоритма необходимо производить с помощью метрики *accuracy@5*. Требования по метрике - не менее 70%.

## Выводы и заключение
1. По результатам выполненной работа разработама модель idx_l2, основанная на библиотеке FAISS, позволяющая определять для нового товара пять наиболее близких по своим признаком товаров из базы.
2. Для модели idx_l2 подобраны оптимальные параметры и определён список обучающих признаков, при которых достигается наилучшее значение метрики *accuracy@5*.
3. Показатель качества accuracy@5 для тренировочных данных составил 71,803 %, для валидационных - 71,646 %, что является удовлетворительным результатом.
4. Необходимо дополнительно проработать вопрос применения классических ML-моделей для дополительного повышения метрики *accuracy@5*.

**Проект является завершённым. Разработанная модель отвечает требованиям задачи**

## Системные требования и данные по развёртыванию тетрадки.
Системные требования:
1. Операционная система: Windows 10 или выше;
2. Версия языка Python: 3.9.13 или выше.
   
Требования к версиям библиотек:
- Версия pandas: 1.4.4;
- Версия numpy: 1.24.3;
- Версия matplotlib: 3.5.2;
- Версия sklearn: 1.0.2;
- Версия faiss: 1.7.4.
  
Для их установки Вы можете ввести в кодовой ячейке Jupyter следующий код:
```
!pip install pandas==1.4.4
!pip install numpy==1.24.3
!pip install matplotlib==3.5.2
!pip install scikit-learn==1.0.2
```
Для установки faiss воспользуйтесь [руководством](https://github.com/facebookresearch/faiss/blob/main/INSTALL.md)
