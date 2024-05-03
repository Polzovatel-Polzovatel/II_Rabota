# Автоматизация подбора персонала 

### Результаты работы

- [Ноутбук 1, скрейпинг](https://github.com/Polzovatel-Polzovatel/II_Rabota/blob/main/scraping.ipynb)
- [Ноутбук 2, предобработка](https://github.com/Polzovatel-Polzovatel/II_Rabota/blob/main/preprocessing.ipynb)
- [Ноутбук 3, анализ данных](https://github.com/Polzovatel-Polzovatel/II_Rabota/blob/main/analysis.ipynb)

### О работе

В HR-отделах крупных компаний возникает задача автоматизации части обязанностей HR-менеджеров. Существует огромное число систем для автоматизации этих обязанностей на основе тематического моделирования, машинного обучения с учителем. В данной работе будет предпринята попытка улучшить существующие решения: для большей эффективности моделей классификации будет обучена модель semi-supervised классификации, а при работе с текстом в качестве токенов будут использованы не слова в нормальной форме, а тройки таких слов. Также будет рассмотрена задача сегментации и ее решение с помощью алгоритмов кластеризации. При интерпретации сегментов будет рассмотрен подход на основе топологического анализа данных, после чего будут исследованы возможности для долгосрочного планирования с применением построенной модели классификации к сегментам. 

### Прогресс 

**04.06:**

- Загрузил первую версию презентации 

**22.05:**

- Отправил рецензию итд в учебный офис

**18.05:**

- Внес необходимые изменения, загрузил работу в систему

**12.05:**

- Отправил работу на проверку

**10.05:**

- Исправил проблемы со scraping

- Полностью переработал текст ВКР

- Исправил проблемы в preprocessing

- Добавил новые алгоритмы в analysis 

**30.04:**

- Текст ВКР практически написан

- Ноутбуки практически оформлены

- Проблема, из-за которой "почти": ноутбук `scraping.ipynb` перестал быть актуален, необходимо его переработать + переработать текст ВКР, где описан ноутбук

**18.04:**

- Занимался первыми двумя ноутбуками: текст, код
- Остался третий ноутбук

**11.04:**

- Сделал более хорошие описания ко всем частям трех ноутбуков, позже они пойдут в текст работы
- Занимался текстом работы и организацией ноутбуков

**04.04:**

- Занимался текстом ВКР, разбиением на 3 ноутбука, необходимо сделать более хорошие описания, законченную работу, а также практикой 

**14.03:**
- Занимался пайплайном, mBART, 3 ноутбука
- Думал о мотивации работы во фреймворке принятия решений в условиях неопределенности, описал мотивацию таким образом, а также ссылки, текст и описание работы

**07.03**

- Разобрался с mBART и как его встроить в пайплайн
- Начал деление ноутбука на 3 части, а не 2
- Пайплайн практически полностью закончен, осталось позаниматься данными и поэкспериментировать с разными методами в рамках данной архиетктуры 
- Изучал теорию по раным методам ML (Gaussian Mixture, mBART, semi-supervised learning, etc.)

**28.02:**

- Написал Project Proposal, определился с дальнейшим планом работ
- Занимался данными: разметка, признаки, вопросы для интервью

**21.02:**

- Закончил с эмбеддингами (простейший вариант)

- Написал черновой вариант для сбора повторений с работой

- Поработал с полученными кластерами

- Осталось доразметить данные, еще раз перепроверить топовость образования вручную и уже пробовать сложные методы, пайплайн готов (более подробно в ноутбуке analysis описано)

**14.02:**

- Написал законченный пайплайн для обучения без размеченной выборки и для (чатично) размеченной выборки
- Написал законченный пайплайн для обучения без размеченной выборки и для (чаcтично) размеченной выборки
- Исследовал, как строить эмбеддинги для коллекции документов, как устроено semi-supervised learning
- Начал добавлять новые признаки в данные

**07.02:**

- Разметил более правильным способом данные (будем продолжать). Какие методы хороши, когда размечено лишь небольшое количество данных? Semi-supervised learning?
- Обсудили проблемы с построением эмбеддингов последовательности токенов на основе эмбеддингов для токенов (на примере, когда токены — триграммы, их эмбеддиги — word2vec), из-за того, что я неправильно это сделал, возникли проблемы с кластеризацией
- Стоит заняться еще признаками: флаг для образования, наличие карьерного роста (несколько раз одна коспания) — мы обсуждали это во время звонков.

**31.01**:

- Разделение на 2 ноутбука для удобства
- Начал сегментацию (для нее все есть, но стоит поэуспериментировать с тем, какие данные брать для обучающей вяборки)
- Начал классификацию (но для нее лучше доработать извлечение еще трех сущностей, можно уже во втором ноутбуке)
- Вручную разметил небольшую часть данных

**24.01**:

- Обсуждалась презентация, обзор литературы, Project Proposal, дальнейшие планы, необходимая теория

**Что сделано к 17.01:**

- Скрейпинг завершен. Осталось почистить код для обработки собранных данных и доработать его.
- Предобработка данных завершена. Протестированы токенизация на биграммы, на отдельные слова в нормальной форме, построение эмбеддингов с помощью word2vec.
- Начата работа над анализом данных. Разобрал кластеризацию Tribox-кластеризацией, EM-алгоритмом, собираюсь также кластеризовать KMeans. Сделал презентацию с описанием проекта. Начал реализовывать Tribox-кластеризацию, а также кластеризацию EM-алгоритмом, для KMeans буду использовать sklearn. Дальше буду заниматься текстовой аналитикой. 

**Что сделано к 14.12:**

1. Решил проблему со стоп-словами, текстами на русском языке, сделал хороший АД по 1-граммам

2. Сделал АД по 2-граммам

**Что сделано к 7.12:**

1. Посмотрел лекции по текстовой аналитике

2. Придумал более хорошие правила для сущностей

3. Начал анализ данных: word2vec, пересечения

**Что сделано к 30.11:**

- Справочники итд вынесены в отдельный пункт

- Добавлены вспомогательные функции для корректного сохранения и обновления данных

- Исправлен флаг языка текста

- Добавлен справочник по интересам и поиск по простому правилу

- Добавлены командировки, город и переезд на русском

- Добавлены аналитические комбинации слов по очень простому правилу

**Что сделано к 23.11:**

- Начал делать разного рода справочники, привел некоторые значения к единому виду (русский язык, убрана ненужная информация), извлек некоторую дополнительную информацию из текстов (раздел черновик). Осталось доделать справочник по образованию еще лучше, а также справочник по интересам и наличие аналитчиеских комбинаций слов (см черновик, что сделать)
- Заметил, что сломался сбор навыков. Исправил.
- Написал простую функцию для объединения таблиц со ссылками (черновик). Протестировать. Сделать такую же для таблицы с признаками. Лучше оформить код.

**Что сделано к 16.11:**

- Исправил странность с образованием (это было из-за конфликта имен)
- Научил первый скрейпер собирать количество страниц
- Собрал все данные обоими скрейперами
- Опыт работы: число + 1–2 работа — добавил эти признаки
- Написан простой вариант функции для добавления новых данных к старым (могут ли быть ошибки? будет ли это долго?)

**Что сделано к 9.11:**

- Полностью готов скрейпер страницы с вакансиями. Он оформлен в отдельную аккуратную функцию, добавлена возможность перевода запроса на русском в транслит (в виде транслита он нужен для задания ссылки на выдачу), запущен скрейпер на всех 7 видах аналитиков и собраны вакансии по первым 10 страницам по каждому из 7 запросов, переделана часть кода для задания нормальных индексов в таблице (теперь это происходит уже после самого процесса скрейпинга).
- Скрейпинг отдельных резюме. Тоже создана отдельная функция для скрепинга, обнаружены ситуации, когда предыдущий код выдавал ошибку, и исправлены, теперь все должно работать исправно на любых резюме, переделан принцип обработки пропущенных данных. Добавлен скрейпинг признаков названия вакансии, а также 4 признаков, связанных с образованием, начата работа над справочником вузов. Скрейпер собрал признаки для первых 100 собранных ссылок на вакансии в таблицу (так мало, поскольку пока мы просто тестируем его работу). 

### Что надо сделать?

- Осталось доделать словарь образования и повысить точность флага языка текста, протестировать функцию обновления данных, усложнттьб правила в аналитических комбинациях и справочнике по интересам
