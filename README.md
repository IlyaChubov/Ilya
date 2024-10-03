NuclearIT

##О проекте
Предназначен для решения задачи детекции курильщиков и их поз с фиксацией экспериментов в MLflow

## Архитектура проекта
![68747470733a2f2f73756e392d31352e757365726170692e636f6d2f696d70672f38626d525a335a42462d7a3247616b6f6c415a3437676a726758715964434a727858773670672f4f41784f333042554e52412e6a70673f73697a653d313435317831313035267175616c(1)](https://github.com/user-attachments/assets/4e0a3a86-e346-428c-8b21-acd2c0ea0fbb)

## Предварительная обработка фотографий

Для расширения датасета использовались open_source источники + аугментация.

##Исследования

Детекция курильщиков выполнялось с использованием моделей yolov8l,yolov8m,yolov8s,yolov8n. Ниже приведены результаты исследований для каждой из моделей.
| Approach    | Accuracy    | Fitness     |
|-------------|-------------|-------------|
| Yolov8n-cls | 0.905       | 0.957       |
| Yolov8m-cls | 0.917       | 0.961       |
| Yolov8l-cls | 0.921       | 0.967       |

Значения метрик (accuracy и fitness), артефактов (лучшие веса модели) логировались в локально поднятой MlFlow.

Детекиця ключевых поз человека выполнялось при помощи yolo-nas-pose-l.

## Web

Взаимодействие с нейронной сетью осуществляется с использованием web-сайта. Пользователь загружает фотографию, модель возвращает фотографию с ключевыми позами человека и вероятностью того, что он курит. Фотографии хранятся в bucket (google cloud). 

1. Нейронная сеть:
В этом разделе находятся файлы, связанные с нейронной сетью, включая исходный код, обученные модели, а также инструкции по использованию и обучению. README: Описание использования нейронной сети, инструкции по запуску обучения и оценки модели. Дополнительные файлы такие ноутбуки Jupyter и т. д.

2. Приложение:
В этом разделе находятся файлы, относящиеся к разработке и использованию приложения, связанного с проектом. README: Описание приложения, его возможностей, инструкции по установке и использованию. Файлы исходного кода приложения, файлы конфигурации, ресурсы и т. д.

3. Веб:
В этом разделе находятся файлы для веб-компонентов проекта, если такие имеются. README: Описание веб-компонентов проекта, их функциональности и использования. Файлы исходного кода веб-компонентов, файлы разметки, стилей, скриптов и т. д. Каждая из указанных категорий имеет свой собственный файл README, который содержит информацию о содержимом, использовании и инструкции по работе с соответствующим разделом проекта.

Ссылка на Google Диск содержит дополнительные ресурсы и данные: https://drive.google.com/drive/folders/1ywxZjptfvIYMA3wGNuH6WCVL6bzXgDhP
