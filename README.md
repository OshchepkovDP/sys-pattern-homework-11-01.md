# Домашнее задание к занятию "`Название занятия`" - `Фамилия и имя студента`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1 СУБД

Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

Приведите ответ в свободной форме.

`1.1. Бюджетирование и финансовые отчеты:`

`Оптимальный выбор: PostgreSQL или Oracle`
`Причины:`
`Гарантированная целостность данных`
`Поддержка сложных транзакций`
`Мощные аналитические возможности`
`Встроенные функции для работы с финансами`

`1.1.* Для ускорения хеширования:`

`Можно использовать:`
`OpenSSL с поддержкой аппаратного ускорения`
`GPU-ускорение через CUDA/OpenCL для массовых операций хеширования`

`1.2. Лендинги и CRM:`

`Для лендингов:`
`MongoDB или Cassandra`
`Причины: высокая производительность, гибкость схем, горизонтальное масштабирование`
`Для CRM:`
`PostgreSQL или MySQL`
`Причины: структурированные данные, надежность, поддержка сложных запросов`

`1.2.* Объединение в одну СУБД возможно:`

`Использовать PostgreSQL:`
`JSONB для гибких данных лендингов`
`Реляционные таблицы для CRM`
`Партиционирование для оптимизации производительности`

`1.3. База корпоративных норм:`

`Оптимальный выбор:`
`PostgreSQL или MySQL`
`Причины:`
`Простая реляционная структура`
`Легкий доступ через SQL`
`Хорошая документация`
`Широкая поддержка`

`1.3.* Интеграция с существующими СУБД:`

`Можно использовать ту же PostgreSQL:`
`Создать отдельную схему`
`Использовать привилегии для разграничения доступа`
`Оптимизировать индексы под частые запросы`

`1.4. Логистика:`

`Оптимальный выбор:`
`Neo4j или Amazon Neptune`
`Причины:`
`Быстрая работа с графами`
`Оптимизация для маршрутизации`
`Поддержка геоданных`
`Алгоритмы оптимизации путей`

`1.4.* Интеграция с отделом закупок:`

`Лучше использовать ту же СУБД:`
`Создать дополнительные узлы графа`
`Связать закупки с логистическими операциями`
`Использовать общие индексы`

`1.5. Единая СУБД для всех задач:`

`Возможный вариант:`
`PostgreSQL с расширенными модулями:`
`JSONB для гибких данных`
`PostGIS для геоданных`
`Дополнительные расширения для аналитики`
`Графовые расширения (например, pg_graph)`
`Использовать микросервисную архитектуру`
`Применять кэширование (Redis) для часто используемых данных`
`Реализовать ETL-процессы для интеграции данных`
`Использовать Docker/Kubernetes для оркестрации`
`Применять паттерн CQRS (Command Query Responsibility Segregation) для реализации гибкости системы, её масштабирования и быстродействия`
`Реализовать слой абстракции доступа к данным для работы с разными БД и упрощения разработки.`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 1](ссылка на скриншот 1)`


---

### Задание 2 Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

Приведите ответ в свободной форме.

`2.1`

`1. Авторизация пользователя`
`2. Проверка параметров платежа`
`3. Авторизация платежа`
`4. Обработка транзакции`
`5. Обновление баланса`
`6. Уведомление пользователя`

`2.1.*`

`1. Настройка параметров автоплатежа`
`2. Мониторинг баланса`
`3. Автоматическое инициирование`
`4. Обработка транзакции`
`5. Обновление баланса`
`6. Уведомление пользователя`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`


---

### Задание 3 SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

Приведите ответ в свободной форме.

`3.1`

`1. Структурированная модель данных с предопределёнными таблицами и типами данных`
`2. Стандартизированный язык SQL с поддержкой сложных операций и анализом больших наборов данных`
`3. Обилие инструментов с поддержкой большого сообщества`
`4. Целостность данных`
`5. Стандартизация`

`3.1*`

`1. Горизонтальное масштабирование`
`2. Совместимость с SQL`
`3. Гибкость (работа со структурированными и полуструктурированными данными)`
`4. Управление распределительными системами`
`5. Производительность при больших нагрузках`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`

### Задание 4 Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.

На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.

`Критерии оценки типа СУБД`
`1. Горизонтальная масштабируемость`
`2. Тип рабочих нагрузок`
`3. Модель данных`
`4. Согласованность и надёжность`
`5. Интеграция с экосистемой`

`Лучшая модель вычислений будет Apache spark, так как имеется распределённая обработка данных, широкая поддержка алгоритмов, интеграция с СУБД, отказоустойчивость и масштабируемость.`

`В итоге, лучше всего будет применить NewSQL в связке с Apache spark и Kubernetes`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`
