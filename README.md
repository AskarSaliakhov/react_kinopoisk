# Приложение по поиску фильмов/сериалов с помощью API Kinopoiska

Обязательно в файле. env(в корне директории) необходимо прописать токен!

# Запуск приложения
```
в файле. env(в корне директории) прописать токен
docker build -t react_kinopoisk .
docker run -p 7070:7070 -d react_kinopoisk
```

или

```
npm install
npm start
```

# Авторизация
```
логин: test
пароль: test
```

# Приложение написано на React, Typescript

# Особенности приложения
- Когда пользователь пытается найти фильм, то происходит debounce(300мс)
- Можно перейти на отдельную страницы фильма/сериала
- Реализована адаптивная и мобильная вёрстка
- Изначально страница случайного фильма выдает один фильм, а если нажать выдать следующий, то она просит авторизацию. Т.к. API кинопоиска может выдавать случайный фильм без изображения, то делаются запросы до тех пор, пока не будет изображения у фильма
