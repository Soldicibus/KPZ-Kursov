<h1>Звіт по роботі з API</h1>

<h2>Призначення API</h2>
<p>Цей API призначений для демонстрації базових операцій CRUD (створення, отримання, оновлення, видалення) з документами та працівниками. Він реалізований на Node.js з підтримкою аутентифікації та логування.</p>
<p>API дозволяє перевіряти права доступу користувачів та адміністраторів, демонструє роботу з HTTP-методами, обробку помилок та тестування через клієнтські запити.</p>

<h2>Інструкції з встановлення та запуску</h2>
<p>Встановлення залежностей:</p>
<pre>npm install</pre>
<p>Запуск сервера:</p>
<pre>npm start</pre>
<p>Запуск тестового клієнта:</p>
<pre>npm test</pre>

<h2>Ендпоінти API</h2>
<table>
  <thead>
    <tr>
      <th>HTTP-метод / URL</th>
      <th>Опис</th>
      <th>Необхідні заголовки</th>
      <th>Приклад тіла запиту</th>
      <th>Можливі коди відповіді</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>GET /documents</td>
      <td>Отримати список всіх документів</td>
      <td>Authorization: Bearer &lt;token&gt;</td>
      <td>-</td>
      <td>200 – успішно<br>401 – неавторизовано<br>403 – заборонено</td>
    </tr>
    <tr>
      <td>POST /documents</td>
      <td>Створити новий документ</td>
      <td>Authorization: Bearer &lt;token&gt;</td>
      <td>{ "title": "Назва документа", "content": "Текст документа" }</td>
      <td>201 – створено<br>400 – помилка даних<br>401 – неавторизовано</td>
    </tr>
    <tr>
      <td>GET /employees</td>
      <td>Отримати список всіх працівників</td>
      <td>Authorization: Bearer &lt;token&gt;</td>
      <td>-</td>
      <td>200 – успішно<br>401 – неавторизовано</td>
    </tr>
    <tr>
      <td>DELETE /documents/:id</td>
      <td>Видалити документ за ID</td>
      <td>Authorization: Bearer &lt;token&gt;</td>
      <td>-</td>
      <td>200 – успішно<br>404 – документ не знайдено<br>401 – неавторизовано</td>
    </tr>
  </tbody>
</table>

<h2>Фото з реалізації та тестування (3 work/Photos)</h2>

<!-- Початок основних фото -->
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-1get-request-documents-after-posting.png" alt="3-1get-request-documents-after-posting.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-1get-request-documents.png" alt="3-1get-request-documents.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-1get-request-employees.png" alt="3-1get-request-employees.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-1post-request-documents.png" alt="3-1post-request-documents.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-1updated-server.js.png" alt="3-1updated-server.js.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-2get-request-documents-completed.png" alt="3-2get-request-documents-completed.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-2get-request-documents-intentionaly-failedpng.png" alt="3-2get-request-documents-intentionaly-failedpng.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-2get-request-employees-completed.png" alt="3-2get-request-employees-completed.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-2get-request-employees-intentionally-failed.png" alt="3-2get-request-employees-intentionally-failed.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-2updates-server.js-with-auth.png" alt="3-2updates-server.js-with-auth.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-3updated-server.js-middleware.png" alt="3-3updated-server.js-middleware.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-browser-showcase-failed-documents-f12-network.png" alt="3-browser-showcase-failed-documents-f12-network.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-browser-showcase-failed-documents.png" alt="3-browser-showcase-failed-documents.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-fianltest-post-documents-as-user-incorrectly.png" alt="3-fianltest-post-documents-as-user-incorrectly.png">

<!-- Finaltest фото в кінці -->
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-delete-coument1-as-admin.png" alt="3-finaltest-delete-coument1-as-admin.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-get-documents-as-user.png" alt="3-finaltest-get-documents-as-user.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-get-documents-no-headers.png" alt="3-finaltest-get-documents-no-headers.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-get-employees-as-admin.png" alt="3-finaltest-get-employees-as-admin.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-get-employees-as-user.png" alt="3-finaltest-get-employees-as-user.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-get-nonexistent-as-admin.png" alt="3-finaltest-get-nonexistent-as-admin.png">
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-finaltest-post-documents-as-user-correctly.png" alt="3-finaltest-post-documents-as-user-correctly.png">

<!-- test-client.js в самому кінці -->
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/3%20work/Photos/3-test-client.js.png" alt="3-test-client.js">


<h2>Посилання на публічний репозиторій</h2>
<p><a href="https://github.com/Soldicibus/secure-api-lab">https://github.com/Soldicibus/secure-api-lab</a></p>
