# Step CV-Pipeline: model_eval [EN](README.md)

Задача:
- Обработка тестового датасета.

Данный step CV-Pipeline: model_eval предназачен для:
Тест модели, построение метрик и графиков. Если это этап улучшения, то подтягивать предыдущие предикты и наносить на график (чтобы было с чем сравниваться). Тестовых сетов может быть несколько - обязательно указывать, что за тестовый сплит в параметрах. Добавить на график текущий прод, чтобы было с чем сравнивать на DSML. Для детекторов - построение Precision-Recall кривой обязательно (code). Метрики должны быть описаны как считаются. Для классификации: визуализация нескольких примеров с наибольшей ошибкой, отсортированные по убыванию степени ошибки. Для детекторов обязательно: FP - красный, FN - синий, GT - зеленый. В параметры выносить параметры просмотра (количество примеров, тип ошибки и т.д.). 

Создается на основе [шаблона](https://github.com/4-DS/step_template).
Чтобы не забывать про обязательные ячейки в каждом ноутбуке, проще всего создавать новые ноутбуки просто копированием [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) из стандартного [шаблона](https://github.com/4-DS/step_template) компоненты.

Входные данные для step CV-Pipeline: model_eval
- **test_data**     
Тестовый датасет изображений, сохраненный в parquets (из компоненты CV-Pipeline: data_prep)

- **test_config**     
Аннотациии тестового датасета изображения (из компоненты CV-Pipeline: data_prep)

- **bento_service**     
bento_service, сервис упакованной модели через BentoML (из компоненты CV-Pipeline: model_pack)

## Как запустить шаг CV-Pipeline: model_eval

### Создать директорию для проекта (или использовать уже существующую)
```
mkdir obj_detect_binary
cd obj_detect_binary
```  

### склонировать репозиторий model_eval
```
git clone --recurse-submodules https://github.com/4-DS/obj_detect_binary-model_eval.git {dir_for_model_eval}
cd {dir_for_model_eval}
```  

### запустить шаг CV-Pipeline:model_eval
```
python step.dev.py
```  
или
```
step.prod.py
``` 
