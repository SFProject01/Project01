Итоговый проект по Блоку «Основные конструкции C++»

над заданием работали  Ольга Полевик и Евгений Rock
Одна из двух реализаций задания, Евгений Rock поделится своим 
В данной работе он принимал участие в разработке общей логики программы и в реализации части логина, регистрации и проверки на существующего пользователя, а также идеи насчет того где можно использовать исключения

*Описание программы*

Программа представляет собой реализацию простого чата с возможностью регистрации, входа, выхода пользователя из чата, а так же с возможностью перелогинивания (завершения конкретной активной сессии) без выхода из чата. 

Классы User, Session, Message - предсталяют собой структуры для хранения информации о пользователе, активной сесии и сообщении

Класс Login отвечает за регистрацию (bool registerUser), вход (открытие активной сессии) (Session loginUser),  проверку существующего пользователя (bool isUserExist) и завершение сессии без выхода из чата (void logout).  

Класс Chat отвечает за ввод публичных (void sendPublicMessage) и приватных (void sendPrivateMessage) сообщений и отображение публичных (dynamic_array<Message> readPublicMessage) и приватных (dynamic_array<Message> readPrivateMessage) сообщений

Отдельно реализован шаблон класса dynamic_array - динамического массива для классов User, Session, Message

Реализована перегрузка оператора ввода для шаблона динамического массива и отдельно для класса Message

Функционал программы подразумевает ограничение на количество зарегистрированных пользователей и реализовано исключение при попытке зарегистрироваться сверх указанного лимита.

Дополнительный функционал - ограничение на ввод корректных данных при входе (логин и пароль), дается три попытки, если они неудачны то чат завершает работу (выход из чата)
