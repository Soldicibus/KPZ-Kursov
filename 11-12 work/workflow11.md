<h1>Workshop — Неперервна інтеграція (Continuous Integration)</h1>

<h2>Тема</h2>
<p>Неперервна інтеграція (Continuous Integration)</p>

<h2>Мета роботи</h2>
<p>
Ознайомитися з принципами і практиками неперервної інтеграції,
а також сформувати навички автоматизації CI/CD процесів
з використанням GitHub Actions.
</p>

<h2>Визначення</h2>
<p>
Неперервна інтеграція (CI) — це практика розробки програмного
забезпечення, за якої розробники регулярно об'єднують свої
зміни коду в центральний репозиторій, після чого автоматично
виконуються процеси збірки та тестування.
</p>

<h2>Призначення неперервної інтеграції</h2>
<ol>
  <li>Раннє виявлення помилок — проблеми знаходяться швидше, коли зміни невеликі.</li>
  <li>Підвищення якості коду — постійні автоматизовані тести забезпечують стабільність.</li>
  <li>Прискорення розробки — автоматизація рутинних процесів економить час.</li>
  <li>Покращення командної роботи — розробники бачать результати змін один одного.</li>
  <li>Зменшення ризиків — проблеми інтеграції вирішуються поступово, а не перед релізом.</li>
  <li>Уніфікація середовища — збірка виконується в однакових умовах, що
      усуває проблему «у мене локально все працює».</li>
</ol>

<h2>Популярні інструменти CI</h2>
<ul>
  <li>GitHub Actions — інтегрований у GitHub, простий у налаштуванні</li>
  <li>GitLab CI/CD — частина платформи GitLab</li>
  <li>CircleCI — гнучка платформа з контейнерною інфраструктурою</li>
  <li>Travis CI — популярний сервіс для open-source проєктів</li>
  <li>Azure DevOps — комплексне рішення від Microsoft</li>
  <li>AWS CodePipeline — інструмент автоматизації від Amazon</li>
  <li>Jenkins — гнучка та потужна система з відкритим кодом</li>
  <li>TeamCity — рішення від JetBrains</li>
  <li>Bamboo — продукт від Atlassian</li>
</ul>

<h2>Основні компоненти GitHub Actions</h2>

<h3>Workflow</h3>
<p>
Автоматизований процес, що описується у YAML-файлі в директорії
<code>.github/workflows</code>.
</p>

<h3>Events</h3>
<ul>
  <li>push — при надсиланні коду в репозиторій</li>
  <li>pull_request — при створенні або оновленні PR</li>
  <li>schedule — за розкладом</li>
  <li>workflow_dispatch — ручний запуск</li>
</ul>

<h3>Jobs</h3>
<p>Набір кроків, які виконуються на окремому раннері.</p>

<h3>Steps</h3>
<ul>
  <li>Виконання команд (run)</li>
  <li>Використання готових дій (actions)</li>
</ul>

<h3>Actions</h3>
<p>Готові або власні модулі для виконання типових завдань.</p>

<h3>Runners</h3>
<ul>
  <li>GitHub-hosted — надаються GitHub (Ubuntu, Windows, macOS)</li>
  <li>Self-hosted — власні сервери</li>
</ul>

<h3>Artifacts</h3>
<p>
Файли, що створюються під час виконання workflow і зберігаються
для подальшого використання.
</p>

<h2>Хід виконання роботи</h2>
<ol>
  <li>Було виконано практичні тренінги GitHub Skills:
    <ul>
      <li>Hello GitHub Actions</li>
      <li>Publish Packages</li>
    </ul>
  </li>
  <li>Створено власний GitHub Workflow для збірки Docker-образу
      фронтенд-застосунку.</li>
  <li>Налаштовано два тригери:
    <ul>
      <li>Ручний запуск (workflow_dispatch)</li>
      <li>Push у гілки: main та feature/*</li>
    </ul>
  </li>
  <li>У workflow додано наступні кроки:
    <ul>
      <li>Клонування репозиторію</li>
      <li>Встановлення pnpm, залежностей та збірка проєкту</li>
      <li>Авторизація в GitHub Container Registry (ghcr.io)</li>
      <li>Збірка та публікація Docker-образу</li>
    </ul>
  </li>
  <li>Після успішного виконання workflow, створений Docker-образ
      з’явився на вкладці <b>Packages</b> у GitHub.</li>
</ol>

<h2>Приклад простого Workflow</h2>
<pre>
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '16'

    - name: Install dependencies
      run: npm ci

    - name: Run tests
      run: npm test
</pre>

<h2>Висновок</h2>
<p>
Виконуючи дану практичну роботу, я ознайомився з принципами та
практиками неперервної інтеграції і на практиці навчився
автоматизовувати процеси CI/CD за допомогою GitHub Actions.
Я закріпив навички створення власних workflow, налаштування тригерів,
використання Docker, GitHub Container Registry та автоматичної збірки
проєктів. Отримані знання дозволяють мені ефективно застосовувати
неперервну інтеграцію у реальних програмних проєктах.
</p>
<h2>Посилання на репозиторії</h2>
<a href="https://github.com/Soldicibus/skills-hello-github-actions">Посилання на виконаний Hello GIthub Actions</a> <br> <a href="https://github.com/Soldicibus/skills-publish-packages">Посилання на виконаний Sills Publick Packages</a> <br> <a href="https://github.com/Soldicibus/custom-docker-frontend">Посилання на мій репозиторій з Workflow з Packages</a>
