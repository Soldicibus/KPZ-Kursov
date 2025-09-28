# Звіт по роботі з Node.js та npm

## Призначення бібліотеки  
Розроблена бібліотека демонструє базові можливості роботи з Node.js, npm та TypeScript. Вона включає утилітарні функції для обробки даних (**add**, **capitalize**, **formatNumber**, **groupBy**) та конфігурований логер (**Logger**) для зручного ведення журналу.  
Також проєкт показує, як правильно створювати, тестувати й публікувати npm-пакети з використанням лінтера, TypeScript та стандартних практик розробки.  

---

## Інструкції з запуску

## Встановлення залежностей:  
   npm i
## Запуск демо:
npm run demo
## Збірка TypeScript у JavaScript:
npm run build
# Еволюція проєкту
## Створення репозиторію та package.json – ініціалізація npm, створення першої версії.
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-create-repo.png" alt="2-create-repo.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-create-packagejs.png" alt="2-create-packagejs.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-demo.ts-with-errors.png" alt="2-demo.ts-with-errors.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-demo.ts-wrong.png" alt="2-demo.ts-wrong.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-demo.ts-groupby-wrong.png" alt="2-demo.ts-groupby-wrong.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-typescript-init.png" alt="2-typescript-init.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-index.ts-fixed.png" alt="2-index.ts-fixed.png" >

## Додавання лінтера (ESLint) – знаходження стилістичних помилок, виправлення коду.
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest2.png" alt="2-lintertest2.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest3-telling-me%20that-demoiswrong.png" alt="2-lintertest3-telling-me that-demoiswrong.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest3.png" alt="2-lintertest3.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest4-groupby.png" alt="2-lintertest4-groupby.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest4.png" alt="2-lintertest4.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lintertest5.png" alt="2-lintertest5.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-linterfix1.png" alt="2-linterfix1.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-linterfix2.png" alt="2-linterfix2.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-linterfix3.png" alt="2-linterfix3.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-linterfix4.png" alt="2-linterfix4.png" >

## Додавання логування – створення класу Logger, можливість налаштування рівнів логів.
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-bad-logging.png" alt="2-bad-logging.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-logger-config.png" alt="2-logger-config.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-good-logging.png" alt="2-good-logging.png" >

## Фіналізація – фіксація комітів, усунення помилок npm та завершальна збірка.
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-npm-error-check.png" alt="2-npm-error-check.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-npm-dependencies.png" alt="2-npm-dependencies.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-fixing-package.json.png" alt="2-fixing-package.json.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-commit.png" alt="2-commit.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-lastcommit.png" alt="2-lastcommit.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-test1.png" alt="2-test1.png" >
<img src="https://github.com/Soldicibus/KPZ-Kursov/blob/main/2%20work/Photos/2-fix1.png" alt="2-fix1.png" >

## Приклади використання
import { add, capitalize, formatNumber, groupBy, Logger } from "my-lib";

// 1. Арифметика
console.log(add(5, 7)); // 12

// 2. Текст
console.log(capitalize("hello world")); // "Hello world"

// 3. Форматування чисел
console.log(formatNumber(1234567.89)); // "1,234,567.89"

// 4. Групування
const users = [
  { id: 1, role: "admin" },
  { id: 2, role: "user" },
  { id: 3, role: "admin" }
];
console.log(groupBy(users, "role"));
// { admin: [...], user: [...] }

// 5. Логер
const logger = new Logger("DEBUG");
logger.info('Application started');
logger.debug('Extra debug info');
Нотатка про .env
Файл .env використовується для конфігурації середовища.
Очікувані ключі:
APP_PRECISION=3
LOG_LEVEL=debug
### Посилання на теги релізів
https://github.com/Soldicibus/KPZ-Kursov-work2/tags //там версія трохи збилась та нумерація почалась з 1.0.0 замість 0.0.0, але в цілому те саме
