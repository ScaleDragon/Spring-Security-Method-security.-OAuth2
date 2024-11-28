
# Задача «Безопасные методы»

## Описание

Сегодня вы попрактикуетесь в обеспечении безопасности для приложений на уровне методов.

1. Возьмите приложением из [прошлого домашнего задания](../../spring_security/task1/README.md).

2. Добавьте несколько пользователей с разными набором ролей: "READ", "WRITE", "DELETE".

3. Добавьте возможность ограничивать безопасность на уровне методов с помощью всех трёх типов аннотаций.

4. Напишите новый контроллер, в котором:

 - один из методов возвращает значения только для пользователей с ролью "READ" (используйте `@Secured`);
 - один из методов возвращает значения только для пользователей с ролью "WRITE" (используйте `@RolesAllowed`);
 - один из методов возвращает значения, если у пользователя есть хотя бы одна из ролей из "WRITE", "DELETE" (используйте `pre`/`post` аннотации);
 - один из методов, который принимает в качестве query-параметра имя пользователя (`username`), должен возвращает значения, только если у пользователя `username` совпадает с именем пользователя в вашем объекте `Authentication`, который `Spring security` сохраняет в `SecurityContextHolder` после успешной аутентификации.

5. Запуште изменения в репозиторий и прикрепите ссылку на него в комментарий к домашнему заданию.
