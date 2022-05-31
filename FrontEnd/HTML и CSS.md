# HTML и CSS
***
###### В этом документе описан разработанный дизайн и функционал сайта Legacy.
***
### Используемые ресурсы
`HTML` - стандартизированный язык гипертекстовой разметки документов для просмотра веб-страниц в браузере.
`CSS` - формальный язык описания внешнего вида веб-страницы, написанного с использованием языка разметки например HTML. 
`Bootstrap` - свободный набор инструментов для создания сайтов и веб-приложений. Включает в себя HTML и CSS шаблоны оформления для типографики, веб-форм, кнопок, меток, блоков навигации и прочих компонентов веб-интерфейса, включая JavaScript расширения.
***
### Дизайн и функционал
###### 1. Страница-визитка
Для будущего продвижения и развития проекта было необходимо создать сайт-визитку, где люди заинтересованные в нашем продукте могли бы больше узнать о нем и связаться с нами.
![[Лэндинг.png]]
```
<header>
<div class="navBar">
<div class="logo">
<img src="../static/Images/Logo.svg" alt="">
</div>

<div class="navBar-child">
<ul>
<li><a class="nav-button" href="#">Our product</a></li>
<li><a class="nav-button" href="#">Business sectors</a></li>
<li><a class="nav-button" href="#">About Us</a></li>
<li><a class="nav-button login" href="#">Log in</a></li>
</ul>
</div>

</div>

<div class="mother-content">
<div class="left-header-content">
<div class="main-content">
<div class="header-text">
<h4>
Electronic Queue <br> Management System
</h4>
<p>
The greatest solution for your business
</p>
</div>

<div class="header-buttons">
<a id="red" href="">Create ticket</a>
<a id="puprple" href="">Contact</a>
</div>
</div>
</div>

<div class="rigth-phone">
<img src="../static/Images/phone.svg" alt="">
</div>
</div>

</header>
```



Первое что видит пользователь когда открывает сайт это две кнопки. 
Первая из которых позволяет воспользоваться нашим приложением:
![[Тикет.png]]
```
<a id="red" href="">Create ticket</a>

#red {
background-color: rgba(189, 29, 69, 1);
color: #fff;
border: 1px solid #fff;
margin-right: 30px;
}

```



А вторая связаться с нами через электронную почту:
![[Контакт.png]]
```
<a id="puprple" href="">Contact</a>

#puprple {
color: #000059;
border: 1px solid #000059;
}

```



Если пользователь спустится ниже он увидит услуги предоставляемые нашим приложением:
![[Фичи.png]]
```
<section class="apps">
<h3>Our app’s features</h3>
<div class="all-apps">
<div class="apps-shild">
<img src="../static/Images/Component 15.svg" alt="">
<h5>Setting time online</h5>
<p>
The system helps avoiding crowds <br> and standing in long lines by <br> setting time in advance
</p>
</div>

<div class="apps-shild">
<img src="../static/Images/Component 13.svg" alt="" id="kosiak">
<h5>Analysis of key indicators</h5>
<p>
The system analyzes the most <br> requested brances and services with <br> the time of their provision
</p>
</div>

<div class="apps-shild">
<img src="../static/Images/Component 14.svg" alt="">
<h5>Adding new functions</h5>
<p>
Our system has opportunity <br> to add function by clients <br> wish or needs
</p>
</div>

<div class="apps-shild">
<img src="../static/Images/Component 16.svg" alt="">
<h5>Integration possibility</h5>
<p>
Our team can integrate the <br> electronic qeueu system in your <br> existing app
</p>
</div>

<div class="apps-shild">
<img src="../static/Images/Component 17.svg" alt="">
<h5>Branding</h5>
<p>
Our mobile application has <br> opportunity to adapt <br> company’s branding
</p>
</div>

<div class="apps-shild">
<img src="../static/Images/Component 22.svg" alt="">
<h5>Online Web-page</h5>
<p>
We have developed a web <br> page with a unique link that <br> your clients can sign up to.
</p>
</div>
</div>
</section>

```

После этого идет секция где он может увидеть бизнес сектора для которых используется наше приложение:
![[Клиент.png]]
```
<section class="Business-sectors">
<h2>Business sectors</h2>
<img src="../static/Images/business-backround.svg" id="iscl" alt="">
<div class="business-conatiner">
<div class="business-conatiner-child">
<div class="business">
<div class="nav-bus">
<img src="../static/Images/fa_bank.svg" alt="">
<h3>Bank and Finance</h3>
</div>
<ul>
<li>Banks</li>
<li>Financial agencies</li>
</ul>
<a href="#">More...</a>
</div>
</div>

<div class="business-conatiner-child">
<div class="business">
<div class="nav-bus">
<img src="../static/Images/Vector.svg" alt="">
<h3>Government agencies</h3>
</div>
<ul>
<li>Public service center</li>
<li>Tax authorities</li>
</ul>
<a href="#">More...</a>
</div>
</div>

<div class="business-conatiner-child">
<div class="business">
<div class="nav-bus">
<img src="../static/Images/Vector (1).svg" alt="">
<h3>Medical centers</h3>
</div>
<ul id="iskl2">
<li>Hospitals</li>
<li>Dentistry</li>
<li>Laboratories and analysis</li>
</ul>
<a href="#">More...</a>
</div>
</div>
</div>

</section>

```

Затем идет форма после заполнения которой с нами можно будет связаться:
![[Связаться.png]]
```
<section class="form">

<div class="container-form">

<h1>Leave Your Comment Here</h1>

<input type="text" name="" id="name" placeholder="Name">

<input type="text" name="" id="email" placeholder="Email">

<textarea name="" id="cum" cols="40" rows="10" placeholder="Type your text..."></textarea>

<input type="submit" name="submit" id="redSubmit" placeholder="Comment">

</div>

</section>

```

Ну и в самом низу есть футер всего сайта где пользователь может увидеть почту, инстаграмм и фейсбук аккаунты нашей группы:
![[Футер.png]]
```
<footer>

<div class="logo-footer">
<img src="../static/Images/footer-logo.svg" alt="">
</div>

<div class="link">

<ul>
<li><img src="../static/Images/mail.svg" alt=""><a href="#">legacy@auca.kg</a></li>
<li><img src="../static/Images/inst.svg" alt=""><a href="#">legacy__kg</a></li>
<li><img src="../static/Images/ff.svg" alt=""><a href="#">legacy__kg</a></li>
</ul>

</div>
</footer>

```
***
###### 2. Страница "О продукте"
Страница на которую можно перейти кликнув на соответствующую кнопку хедера `<li><a class="nav-button" href="#">Our product</a></li>`, где подробно рассказывается о нашем продукте.
![[О продукте.png]]
Наша программа способна обеспечить: 
1. Улучшение сервиса - Функция времени записи основана на потребностях клиента и улучшает качество обслуживания клиентов. Улучшите обслуживание клиентов с помощью гибкой и эффективной системы.
2. Уменьшение количества жалоб - Около 53% жалоб клиентов связаны с длинными очередями. Ожидание в очереди уменьшает жалобы клиентов и повышает удовлетворенность клиентов
3. Увеличение продуктивности сотрудников - Наша система позволяет отслеживать эффективность работы сотрудников в режиме реального времени, позволяя оценивать и улучшать работу сотрудников.
4. Увеличение лояльности клиентов - Система управления электронной очередью улучшит ваш сервис и впоследствии обеспечит лояльность клиентов
***
###### 3. Страница индустрий
Страница на которую можно перейти кликнув на соответствующую кнопку хедера `<li><a class="nav-button" href="#">Business sectors</a></li>`, где подробно рассказывается о бизнес секторах для которых используется наше приложение.
![[Сектора.png]]
 В сектора входят: 
 1. Банки и финансовые организации - Банки и Финансовые агентства.
 2. Правительственные агенства - Центр обслуживания населения и Налоговые органы.
 3. Медицинские учреждения - Больницы, Стоматологии и Лаборатории для сдачи анализов.
***
###### 4. Страница "О нас"
Страница на которую можно перейти кликнув на соответствующую кнопку хедера `<li><a class="nav-button" href="#">About Us</a></li>`, где подробно рассказывается о членах нашей команды ФМП, об их ролях и о целях нашего проекта.
![[О нас.png]]
На странице указаны:
1. Абдыкаримов Атай - IT специалист.
2. Калилов Марлен - Тимлид и IT специалист.
3. Чыныбаев Иман - IT специалист.
4. Аманбаев Фархад - Стартап менеджер.
5. Мааткабулова Жанай - Маркетинг менеджер.
6. Джумагулова Сабира - Маркетинг менеджер.
7. Асанкошоев Самат - Mенеджер по развитию клиентов.
8. Аматова Бегимай - Графический дизайнер.
9. Мухтар кызы Айжана - менеджер по социальной ответственности.
***
###### 5. Страница регистрации
Страница на которую можно перейти кликнув на соответствующую кнопку хедера `<li><a class="nav-button login" href="#">Log in</a></li>`, где можно зарегистрироваться на нашем сайте для получения услуг.
![[Регистрация.png]]
```
{% extends 'base.html' %}

{% block title %}

Register

{% endblock %}

{% block content %}

  
<h3>Register here</h3>
<hr> 
<form action="" method="POST">
{% csrf_token %}
{% for field in form %}
<div>
<p>{{ field.label }}: <br> {{ field }}</p>
{% for error in field.errors %}
<small style="color: red">{{ error }}</small>
{% endfor %}
</div>

{% endfor %}

<button type="submit">Register</button>
</form>

{% endblock %}

```
***
###### 6. Страница входа
Страница на которую можно перейти после регистрации на сайте, где можно войти в пользовательский аккаунт.
![[Вход.png]]
```
{% extends 'base.html' %}

{% block title %}

Login

{% endblock %}

{% block content %}
  

<h3>login</h3>
  

<form action="" method="POST">

{% csrf_token %}

{% for field in form %}

<p>{{ field.label }}: <br> {{ field }}</p>

{% endfor %}

<button type="submit">Login</button>

</form>
 

<p>Don't have an account? <a href="{% url 'register' %}">Signup here</a>
</p>

{% endblock %}

```
***
###### 7. Страница для замены пароля
Страница на которую можно перейти если пользователь забыл пароль, для получения нового через указанную при регистрации почту.
![[Окно для замен пароля.png]]
После заполнения поля для получения нового пароля окно замениться на другое.
![[Проверь почту.png]]
***
###### 8. Страница по созданию тикетов
Страница на которую можно перейти после входа в аккаунт и кликнув на соответствующую кнопку хедера, где можно создать тикет выбрав: банк, ветвь?(не понял, исправь), тип услуги, дату и время.
![[Сделать тикет.png]]
***
###### 9. Страница по отслеживанию тикетов
Страница на которую можно перейти после входа в аккаунт и кликнув на соответствующую кнопку хедера, где можно отслеживать имеющиеся тикеты, они разделены на: Активные, прошедшие и пропущенные.
Так же имеется кнопка для создания новых тикетов и для перехода в свой профиль. 
![[Мой тикет.png]]
Так же возможно удалить тикет
![[Удалить тикет.png]]
Или изменить его время что повлияет на рейтинг.
![[Отложить тикет.png]]
```
{% extends 'base.html' %}

{% block title %}Django Chained Dropdown List - Select Box using jQuery Ajax bank filial{% endblock %}

{% block content %}

{% if user.is_authenticated %}

<div class="alert alert-success" role="alert">
<h3>Welcome {{ user.username }}!</h3>
<a href="{% url 'user-update' user.id %}">{{user.username}}</a>
<a href="{% url 'logout' %}">Logout?</a>
</div>

<table class="table table-striped custab">
<thead>
<a href="{% url 'talon_add' %}" class="btn btn-primary btn-xs pull-right"><b>+</b> Add new talon</a>
<tr>
<th>Number</th>
<th>Bank</th>
<th>Filial</th>

{% if user.is_superuser %}

<th class="text-center">User</th>
<th class="text-center">Action</th>

{% endif %}

</tr>
</thead>
<tbody>

{% for talon in ticket %}

{% if talon.user == user or user.is_superuser%}
  
  
<tr>
<td>

{{ talon.number }}

</td>
<td>{{ talon.bank.name }}</td>
<td>{{ talon.filial.name }}</td>

{% if user.is_superuser %}
<td class="text-center">{{ talon.user }}</td>

<td class="text-center">
<a class='btn btn-info btn-xs' href="{% url 'talon_change' talon.pk %}">
<span class="glyphicon glyphicon-edit">
</span> Edit</a> 
<a href="{% url 'talon_delete' talon.pk %}" class="btn btn-danger btn-xs">
<span class="glyphicon glyphicon-remove">
</span> Del</a>
</td>

{% endif %}

</tr>

{% endif %}

{% empty %}

<tr>
<td colspan="4">No talon in the database. <a href="{% url 'talon_add' %}">Add the first talon</a>.</td>
</tr>

{% endfor %}

</tbody>
</table>

{% else %}

<div class="alert alert-success" role="alert">
<h3>Welcome!</h3>
<a href="{% url 'register' %}">Signup</a>
<a href="{% url 'login' %}">Login</a>
</div>

{% endif %}

{% endblock %}

```
***
###### 10. Страница профиля
Страница на которую можно перейти после входа в аккаунт и кликнув на соответствующую кнопку хедера, где можно увидеть и редактировать свой профиль.
На странице изображены и возможны для редактирования: Фото профиля, рейтинг, имя и фамилия, адрес электронной почты, страна и город и язык интерфейса.
![[Профиль.png]]
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>User</title>

</head>
<body>

{{form}}

</body>
</html>

```



