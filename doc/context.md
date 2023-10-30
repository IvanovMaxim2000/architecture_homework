# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(admin, "Администратор")
Person(user, "Пользователь")

System(conference_site, "Сайт магазина", "Веб-сайт для магазина")



Rel(admin, conference_site, "Добавление товаров на сайт")
Rel(user, conference_site, "Регистрация на сайте, просмотр и добавление товаров в корзину")



@enduml
```
## Назначение систем
| Система       | Описание                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Сайт магазина | Веб-интерфейс, обеспечивающий доступ к информации о товарах. Бэкенд сервиса реализован в виде микросервисной архитектуры |
