### Проект внутренней системы управления базой данных агенства недвижимости "Центральное"

Для установки утилит и зависимостей в среде *nix (Mac OS, Linux) нужно выполнить по очереди два скрипта **install-env.sh** и **install-deps.sh**

Для Windows: **install-env.bat** и **install-deps.bat**

Запуск веб-сервера для разработки осуществляется путем выполенения в корне проекта команды:

```bash
    grunt serve
```

Если необходимо создать route + controller + view + test, то выполняем команду:

```bash
    yo angular:route route-name
```

где **route-name** - имя вашего раута.

При этом в папке controllers будет создан файл route-name.js. Его нужно переместить в поддиректорию src и переименовать в route-name.jsx. Это необхоидмо для возможности использования React.js компонентов с .jsx синтаксисом внутри angular контроллера.

### Работа с backend'ом

Пока у нас нет backend'а. Но тем не менее, наверняка она будет заключаться в том, что нам нужно быть скомпилировать .jar из исходников на clojure командой ***lein uberjar***. А посел запустить .jar командой ***java -jar jar-name.jar***

Возмжны, корректировки.

## Правила работы над проектом:

1. Любая задача, баг, или предложение по добавлению фукнционала должна фиксироваться в виде issue в трекере. Так же любой issue должен соответсвующим образом быть промаркирован (task, bug, question). Так же должен быть всегда установлен milestone задачи (пока только internal-beta). 
2. Если вы начали работать над какой-либо задачей, добавьте ей label "In progress", а так же переведите эту задачу на себя.
3. Если вы знаете, кто может быстрее решить задачу/пофиксить баг/ответить на вопрос, назначайте этого человека ответственным за issue.
4. Старайтесь все issues расписывать максимально подробно. Если требуется прикрепляйте ссылки/скриншоты и т.д.


##  -------------> Очень важно!

--------------

В этом проекте мы будем придерживаться следующего правила: ***Фича без тестов - это баг!***. Весь фукнционал контроллеров и компоентов должен быть обложен unit-тестами.
