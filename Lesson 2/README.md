## Урок 2. Работа с данными (CSV + статика), маппинг и кэширование

### Задание

- Доработайте контроллер, реализовав в нем метод возврата CSV-файла с товарами.
- Доработайте контроллер, реализовав статичный файл со статистикой работы кэш. Сделайте его доступным по ссылке.
- Перенесите строку подключения для работы с базой данных в конфигурационный файл приложения.

### Решение

- Доработан ProductController – добавлен метод GetProductsCSV().
- Доработан CategoryController – реализовано кеширование данных, добавлены методы GetCacheStatistics() и GetCacheStatisticsUrl(), при чем второй возвращает ссылку на файл, сохраняемый на диске.
- Строка подключения перенесена в appsettings.json. В Program.cs в строках 28-35 настроена загрузка конфигурации. В контроллерры контекст БД передается через инъекцию зависимостей в конструкторе.
