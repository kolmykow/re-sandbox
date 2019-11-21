# re-sandbox
Общий репозиторий для примеров и небольших набросков
https://www.websequencediagrams.com/
title ArchiveChat Sequence

Пользователь->+Приложение: Выбранный чат
Приложение->-Пользователь: Подсветка выбранного чата
Пользователь->+Приложение: Архивировать чат
Приложение->+БД: Запрос на количество заархивированных чатов
БД->-Приложение: Количество заархивированных чатов
alt Количество заархивированных чатов меньше лимита
Приложение->+БД: Запрос на добавление в список заархивированных чатов
БД->-Приложение: Подтверждение выполнения
else Количество заархивированных чатов больше лимита
Приложение->Пользователь: Сообщение о превышении лимита
end
Приложение->-Пользователь: Вывод списка активных чатов
