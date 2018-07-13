# Важливо

Програма являється реалізацією технічного завдання, не являє собою комерційного продукту та створина для відкритого доступу та демонстріціі коду 


# Головна поставлена задача

 - Програма повинна відобрадати список користувачів скачаний з серверу та можливістю сортовання.
 - Сервер не виконує сортування тому нам потрібно перемістити весь список з серверу на телефон(максимальна кількість обєктів)

# Вирішення задачі

- в програмі тримати такі великі мписки теж не варіант тому створюємо базу данних куди будемо переносити данні з серверу
- створюємо сервіс в який буде працювати в паралельному потоці приймати з серверу данні і зберігати в базу данних
- створити додаток який буде працювати з базою данних і вже з неї проводити сортування та виводити на UI поток

# Архітектура коду
код нашого проетку розбитий на 3 пакети та 1 файл
```diff
Festivality/app/src/main/java/test/mb/festivality/
```

- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `#f03c15`
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `aplication` - пакет якій працює з UI
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `repository` - пакет якій працє з Данними(Данні з інернети, або данні з бази данних)
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `utils` - пакет з моделями класі, сонверторами, парсерами...
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `MyApp.java` - Главний клас в прогламме которая роздайот контекст

