# Data-Project Ценовой оптимизатор для маркетплейса
**1.  Бизнес-анализ (Business Understanding)**

В первую очередь необходимо определиться с целями и скоупом проекта.

Для этого нужно найти ответы на следующие вопросы:

Организационная структура: 
> Кто участвует в проекте со стороны заказчика сервиса, кто будет основным пользователем? ***Основным пользователем сервиса должен быть продавец на маркетплейсе***

>Собираем контакты, создаем рабочие чаты.

>Какова бизнес-цель проекта? ***Оптимизация цены клиента для максимизации его прибыли и увеличения спроса***

> Существуют ли какие-то уже разработанные решения? Если существуют, то какие и чем именно текущее решение не устраивает? ***Встроенные инструменты OZON? Используют простые правила, например, среднюю цену рынка***

**1.1 Текущая ситуация (Assessing current solution)**

Оцениваем, хватает ли ресурсов для проекта.

>Есть ли доступное железо или его необходимо закупать? ***Возможно будет необходимо купить облако для обучения модели Yandex.Cloud****

>Где и как хранятся данные, будет ли предоставлен доступ в эти системы, нужно ли дополнительно докупать/собирать
внешние данные? ***Данные будут храниться на локальной базе данных, либо же если данных будет слишком много, можно подумать о каком-то распределенном хранилище S3***


> Сможет ли заказчик выделить своих экспертов для консультаций на данный проект?

Нужно описать вероятные риски проекта, а также определить план действий по их уменьшению.

Типичные риски следующие.

- Не уложиться в сроки. -> создать MVP, а не продукт

- Малое количество или плохое качество данных, которые не позволят получить эффективную модель. -> проконсультироваться обязательно по всем данным с заказчиком

- Данные качественные, но закономерности в принципе отсутствуют и, как следствие, полученные результаты не
интересны заказчику. -> Использование простых архитектур, проведение реального АБ теста до после использования сервиса


**1.2 Решаемые задачи с точки зрения аналитики (Data Mining goals)**

Выполняем постановку в технических терминах. Для этого нужно ответить на следующие вопросы:

> Какую метрику мы будем использовать для оценки результата моделирования? ***RMSE, MAPE??***

> Каков критерий успешности модели (например, считаем AUC равный 0.65 — минимальным порогом, 0.75 —
оптимальным)? ***?***

> Если объективный критерий качества использовать не будем, то как будут оцениваться результаты? ***Экспертная оценка***

**1.3 План проекта (Project Plan)**

Как только получены ответы на все основные вопросы и ясна цель проекта, время составить план проекта. План должен содержать оценку всех шести фаз внедрения.
