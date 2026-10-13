# 🗺️ PW-RelaxMap-Backend

Backend API для додатка **RelaxMap**. Сервіс надає можливість пошуку локацій для відпочинку, роботу з геолокаційними даними, інтеграцію з картами, а також гнучку систему автентифікації користувачів.

---

## 🚀 Технологічний стек

Проект побудований на базі сучасного та стабільного стеку Node.js:
* **Runtime:** Node.js (v20+)
* **Framework:** Express.js (v5.x) — з підтримкою асинхронних модулів
* **Database:** MongoDB & Mongoose (v9.x) — ODM для моделювання даних
* **Authentication:** JSON Web Tokens (JWT), Cookie-parser, Bcrypt (хешування паролів)
* **Validation:** Celebrate (Joi) — валідація вхідних даних на рівні роутів
* **Logging:** Pino & Pino-http — швидке та інформативне логування
* **File Storage:** Multer & Cloudinary — завантаження та збереження зображень
* **Security:** Helmet, CORS
* **Documentation:** Swagger UI Express — інтерактивна API документація

---

## 🛠️ Швидкий старт (Локальний запуск)

### 1. Клонування репозиторію
```bash
git clone https://github.com
cd Backend-RelaxMap
```

### 2. Встановлення залежностей
```bash
npm install
```

### 3. Налаштування змінних оточення (`.env`)
Створіть файл `.env` у кореневій папці проекту (використовуючи `.env.example` як зразок) та заповніть його вашими даними:
```env
PORT=3000
MONGODB_URI=mongodb+not-real-uri-string
JWT_SECRET=your_super_secret_jwt_key
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_KEY=your_cloudinary_key
CLOUDINARY_SECRET=your_cloudinary_secret
```

### 4. Запуск проекту

* **Режим розробки** (з автоперезапуском через `nodemon`):
  ```bash
  npm run dev
  ```
* **Production режим**:
  ```bash
  npm start
  ```

---

## 📁 Структура папок

```text
├── src/
│   ├── controllers/   # Обробники запитів (Логіка API)
│   ├── models/        # Схеми та моделі Mongoose (MongoDB)
│   ├── routes/        # Ендпоінти додатка та маршрутизація
│   ├── middlewares/   # Проміжне ПЗ (валідація, авторизація, логування)
│   ├── services/      # Сервісний шар для роботи з базой даних
│   ├── utils/         # Допоміжні функції та утиліти
│   └── server.js      # Точка входу в додаток (ініціалізація сервера)
├── .env.example       # Зразок конфігурації оточення
├── package.json       # Залежності та скрипти проекту
└── README.md          # Ця документація
```

---

## 📝 Скрипти та Команди

Усі команди запускаються через `npm run <назва_скрипта>`:
* `npm run dev` — Запуск локального сервера для розробки. Автоматично відслідковує зміни у файлах.
* `npm start` — Продакшн запуск додатка (`node src/server.js`).
* `npm test` — Запуск тестів (наразі заглушка).

---

## 📖 API Документація (Swagger)

Після запуску сервера повна документація до всіх доступних ендпоінтів (User Auth, Locations, Reviews тощо) доступна за адресою:
🔗 **[http://localhost:3000/api-docs/](http://localhost:3000/api-docs/)** *(якщо порт за замовчуванням 3000)*

У продакшн середовищі документація доступна на Render:  
🔗 **[://onrender.com](https://://onrender.com)**

---

## 📄 Ліцензія

Цей проект поширюється під ліцензією **ISC License**. Ви можете вільно використовувати його для власних потреб.