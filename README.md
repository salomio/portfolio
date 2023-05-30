# Портфолио: инженер по тестированию

## Обо мне 

Привет! Меня зовут Елена, я начинающий тестировщик. <br>
В этом репозитории вы можете найти некоторые из моих проектов, выполненных во время обучения и практики.
<br>

## Навыки и технологии
``Jira``,``qase.io``,``SQL``,`` Postman``,``Swagger``, ``Trello``<br>
``Miro``, ``pgAdmin``, ``Mockoon``, ``Sitechco``, ``Confluence``<br>


## Проекты

<h3>Проект 1: тест веб-приложения для учителей от Skyeng</h3>
<p><i>Продукт</i>: Веб-приложение для учителей от Skyeng, вкладка «Расписание»<br>
<i>Заказчик</i>: учителя онлайн-школы “Skyeng”<br>
<i>Основные требования (главная user-story)</i>: предоставить возможность учителям использовать личные события в расписании, которые служат напоминанием, что что-то запланировано на это время.</p>
<p>Что нужно было сделать: 
<ol>
  <li>Для тестирования веб-приложения для учителей Skyeng были составлены и проведены следующие виды тестирования:</li>
    <ul> 
      <li>Приемочные тест-кейсы по требованиям стейкхолдеров;</li>
      <li>Тестирование требований проводилось для того, чтобы требования были понятны и однозначны для всех, полными и не противоречивыми;</li>
      <li>Smoke-тестирование. Проверка критически важных функций и стабильности системы в целом перед более тщательное тестированием.;</li>
      <li>Функциональное тестирование - чек-лист;</li>
      <li>Регрессивное тестирование итогового проекта.</li>
    </ul>
  <li>Была создана декомпозиция веб-приложения для учителей от Skyeng, вкладка «Расписание»;</li>
  <li>Составлено расписание тестирования: кто из тестировщиков и когда будет проводить своё тестирование (в данном проекте тестировщик был один - я, поэтому составила таблицу с этапами проекта и когда с ними работала)</li>
  <li>Во время проведения тестирования были обнаружены баги во вкладке «Расписание» как в новом функционале «Личные собития», так и в старом «Урок»;</li>
  <li>В завершении проекта был составлен отчёт о проведённом тестировании, где указали виды тестирования, сколько было затрачено время на проект, описаны баги и результаты по проекту.</li>
</ol></p>
<p>В данном проекте были использованы такие инструменты «qase.io», «Sitechco», «Confluence», «Jira», «Miro»</p>
<p>Как решала(-а):<br>
<a href="https://helenakaz.atlassian.net/wiki/spaces/LIBRARY2/pages/2392065/1">Ссылка на проект</a> <br>
логин: Kazannikova.e.96@gmail.com<br>
пароль: 2HJsm!C4pz9H4.n</p> 
 <p>Выводы (итоги):<br>
<ol>
  <li>Составила тест-план;</li>
  <li>Подготовила тестовую документацию;</li>
  <li>Провела несколько видов тестирования (приёмочное, функциональное, smoke-tetting и регрессивное);</li>
  <li>Написала подробный отчёт о проведённых результатах тестирования.</li>
</ol></p>

<h3>Проект 2: тест кабинета учителя в приложении Skyeng</h3>
<p>Проект 2 является продолжением Проекта 1, только тут мы в тестирование добавляем API.</p>
<p><i>Продукт</i>: Веб-приложение для учителей от Skyeng, вкладка «Расписание»<br>
<i>Заказчик</i>: учителя онлайн-школы “Skyeng”<br>
<i>Основные требования (главная user-story)</i>: предоставить возможность учителям использовать личные события в расписании, которые служат напоминанием, что что-то запланировано на это время.</p>
<p>Что нужно было сделать:<p>
<ol>
  <li>К ранее созданным тест-кейсам Проекта 1 добавила тест-кейсы для API;</li>
  <li>Коллекция для проведения тестирование API содержала:</li>
  <ul>
    <li>Метод POST, так как в документации к проекту был указан только этот метод;</li>
    <li>14 различных проверок как позитивные, так и негативные:</li>
    <ul>
      <li>Создание личного события с валидными данными в будущем;</li>
      <li>Создание личного события с валидными данными в прошлом;</li>
      <li>Создание личного события с невалидным названием;</li>
      <li>Создание личного события с цветом, которого нет в системе;</li>
      <li>Создание личного события с невалидной датой;</li>
      <li>Редактирование названия в личном событии;</li>
      <li>Перенос личного события в прошлую дату;</li>
      <li>Перенос личного события на будущую дату;</li>
      <li>Полное редактирование личного события;</li>
      <li>Редактирование личного события без изменения данных;</li>
      <li>Удаление события из будущего;</li>
      <li>Удаление несуществующего события;</li>
      <li>Создание личного события, совпадающее с уроком;</li>
      <li>Создание личного события, совпадающим с уже созданным событием.</li>
    </ul>
  <li>В "Variables" были занесены такие данные как ссылка на веб-приложение, версия и токен и заменены на свои значения "BaseUrl", "ver", "MyToken";</li>
  <li>Использовались скрипты для запоминания id, времени создания события:<br> 
    
    var key = "personalID"
    var value = pm.response.json().data.payload.id
    pm.collectionVariables.set(key, value);

    var key = "old"
    var value = pm.response.json().data.startAt
    pm.collectionVariables.set(key, value);    
  </li>
  <li>Использовались скрипты для редактирования id, времени создания события:<br> 
    
    var key = "updateID"
    var value = pm.response.json().data.payload.id
    pm.collectionVariables.set(key, value);

    var key = "updateAT"
    var value = pm.response.json().data.startAt
    pm.collectionVariables.set(key, value);
  </li>
  </ul>
  <li>В завершении тестирования Проекта 2 был дополнен отчёт об тест-ране API-коллекции в результатах тестирования Проекта 1.</li>
</ol>
<p>В данном проекте были использованы такие инструменты «qase.io», «Confluence», «Postman».</p>
<p>Как решала(-а):<br>
<a href="https://helenakaz.atlassian.net/wiki/spaces/LIBRARY2/pages/9633793/1+2">Ссылка на проект</a><br>
логин: Kazannikova.e.96@gmail.com<br>
пароль: 2HJsm!C4pz9H4.n<br> 
<p>Выводы (итоги):</p>
<ol>
  <li>Дополнила тест-план из 1 проекта;</li>
  <li>Создала коллекцию в Postman;</li>
  <li>Провела тест-ран;</li>
  <li>На основе полученных результатов тест-рана дополнила отчёт о тестировании.</li>
</ol></p>

<h3>Проект 3: тестовое задание. Финал первого курса (Промежуточная аттестация)</h3>
<p>Проект 3 состоял из 3 заданий:</p>
<ol>
  <li><strong>Задание 1</strong>
    <p><i>Продукт</i>: консольное приложение (приложение в вакууме);<br>
       <i>Заказчик</i>: компания “Skypro“, тестовое задание. Финал первого курса;<br>
       <i>Основные требования (главная user-story)</i>: Приложение на вход принимает 3 целых числа, интерпретируемые как длины сторон треугольника, а на выходе выводит на экран является ли введенный треугольник равнобедренным или равносторонним. Предложите конкретные значения тестовых данных, которые Вы будете использовать для тестирования такого приложени.<br>
    <p>Что нужно было сделать:<p>
  </li>
  
<p>Что нужно было сделать:<p>
<ol>
  <li>Выделить функциональные и нефункциональные проверки;</li>
  <li>Придумать позитивные и негативные сценарии;</li>
  <li>Использовать классы эквивалентности и граничные значения;</li>
  <li>Достаточность/избыточность проверок.</li>
</ol>

<p>Как решала(-а):<p>
<a href="https://helenakaz.atlassian.net/wiki/spaces/LIBRARY2/pages/4358145">Ссылка на проект</a>
<p> логин: Kazannikova.e.96@gmail.com</p>
<p> пароль: 2HJsm!C4pz9H4.n</p>
 
 <p>Выводы (итоги):<p>
<ol>
  <li>Выделила функциональные/нефункциональные проверки для поставленных задач;</li>
  <li>Придумала позитивные/негавтиные сценарии поставленных задач;</li>
  <li>Использовала клаассы эквивалентности и граничные значения;</li>
  <li>Применила технику принятия решения для 3 задания.</li>
</ol>
<br>

<p> Проект 4: тестовое задание. Тестирование API</p>
<p>Что нужно было сделать:<p>
<ol>
 <li>Достаточность/избыточность проверок.</li>
 <li>Оформление API тест-кейсов;</li>
</ol>

<p>Как решала(-а):<p>
<a href="https://docs.google.com/spreadsheets/d/1qtmR20_QKS-DURYrcYfonycsstTQSgTGTjN9rC3n_Qw/edit#gid=0">Ссылка на проект</a>
 
 <p>Выводы (итоги):<p>
<ol>
  <li>Провела 21 разных проверок;</li>
  <li>Оформила API тест-кейсы</li>
</ol>
<br>

<p> Проект 5: тестовое задание. Финал первого курса</p>
<p>Что нужно было сделать:<p>
<ol>
  <li>Оформление;</li>
  <li>Создать коллекцию в Postman;</li>
  <li>Использование и передача переменных между запросами;</li>
  <li>Проверка возвращаемых данных(написаны тестовые скрипты на проверку статус кода и других необходимых параметров);</li>
  <li>Создавать SQL запросы.</li>
</ol>

<p>Как решала(-а):<p>
<a href="https://helenakaz.atlassian.net/wiki/spaces/LIBRARY2/pages/14974977">Ссылка на проект</a>
<p> логин: Kazannikova.e.96@gmail.com</p>
<p> пароль: 2HJsm!C4pz9H4.n </p>
 
 <p>Выводы (итоги):<p>
<ol>
  <li>Оформила в confluence тестовое задание</li>
  <li>Создала коллекцию в Postman;</li>
  <li>Использовала и передала переменные между запросами;</li>
  <li>Проверила возвращаемых данных(написаны тестовые скрипты на проверку статус кода и других необходимых параметров);</li>
  <li>Создала SQL запросы.</li>
</ol>

## Контактная информация
- Email: kazannikova.e.96@gmail.com
- Telegram: https://t.me/JiyongK
