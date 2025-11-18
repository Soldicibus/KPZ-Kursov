
<h1>Workshop 5 — Розробка API для шкільної бази даних</h1>

<h2>1. Короткий опис реалізованих сутностей та зв’язків</h2>
<p>
  У межах завдання було створено реляційну базу даних школи, яка містить основні сутності:
  <b>Class</b>, <b>Student</b>, <b>Parent</b>, <b>Teacher</b>, <b>Subject</b>,
  <b>Homework</b>, <b>Timetable</b>, <b>Journal</b>, <b>StudentParent</b>.
</p>

<h3>Основні зв’язки між таблицями</h3>
<table>
  <tr><th>Зв’язок</th><th>Опис</th></tr>
  <tr>
    <td><b>Class — Teacher</b></td>
    <td>Кожен клас має одного класного керівника (<code>class_Teacher → teacher_id</code>).</td>
  </tr>
  <tr>
    <td><b>Student — Class</b></td>
    <td>Кожен учень належить до певного класу (<code>student_Class → class_name</code>).</td>
  </tr>
  <tr>
    <td><b>Homework — Subject, Class</b></td>
    <td>Домашнє завдання належить до предмету та класу (<code>homework_Subject</code>, <code>homework_Class</code>).</td>
  </tr>
  <tr>
    <td><b>Timetable — Class, Subject, Teacher</b></td>
    <td>Розклад пов’язує клас, предмет і викладача.</td>
  </tr>
  <tr>
    <td><b>Journal — Student, Timetable</b></td>
    <td>Журнал відвідувань і оцінок містить записи про учнів на конкретних уроках.</td>
  </tr>
  <tr>
    <td><b>StudentParent — Student, Parent</b></td>
    <td>Зв’язок «багато-до-багатьох» між учнями та батьками.</td>
  </tr>
</table>

<h2>2. Реалізовані API-ендпоінти</h2>
<p>Для кожної таблиці реалізовано стандартні REST-ендпоінти:</p>

<div class="endpoint"><b>GET</b> /api/{entity} — отримати всі записи</div>
<div class="endpoint"><b>GET</b> /api/{entity}/{id} — отримати запис за ID</div>
<div class="endpoint"><b>POST</b> /api/{entity} — створити новий запис</div>
<div class="endpoint"><b>PUT</b> /api/{entity}/{id} — оновити існуючий запис</div>
<div class="endpoint"><b>DELETE</b> /api/{entity}/{id} — видалити запис</div>

<h3>Приклади реалізованих ендпоінтів</h3>
<ul>
  <li><code>GET /students</code> — отримання списку учнів</li>
  <li><code>GET /students/{id}</code> — отримання інформації про конкретного учня</li>
  <li><code>POST /students</code> — створення нового учня</li>
  <li><code>PUT /students/{id}</code> — оновлення даних учня</li>
  <li><code>DELETE /students/{id}</code> — видалення учня</li>
  <li><code>GET /journal</code> — отримання всіх записів журналу</li>
  <li><code>POST /journal</code> — створення нового запису журналу</li>
  <li><code>GET /journal/{id}</code> — перегляд конкретного запису</li>
</ul>

<h2>3. Демонстрація роботи API (Postman)</h2>
<p>Нижче наведено скріншоти із Postman, які підтверджують коректну роботу запитів до API (отримання, створення, оновлення та видалення даних).</p>

<h3>Об’єкт Student</h3>
<div class="gallery">
  <img src="Photos/get_all_students.png" alt="GET all students">
  <img src="Photos/get_specific_student.png" alt="GET specific student">
  <img src="Photos/post_student.png" alt="POST student">
  <img src="Photos/put_student.png" alt="PUT student">
  <img src="Photos/delete_student.png" alt="DELETE student">
</div>

<h3>Об’єкт Journal</h3>
<div class="gallery">
  <img src="Photos/get_all_journal.png" alt="GET all journal">
  <img src="Photos/get_specific_journal.png" alt="GET specific journal">
  <img src="Photos/post_journal.png" alt="POST journal">
  <img src="Photos/put_journal.png" alt="PUT journal">
  <img src="Photos/delete_journal.png" alt="DELETE journal">
  <img src="Photos/delete_journal_check.png" alt="DELETE journal confirmation">
</div>
