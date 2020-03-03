REDUX. Концепция flux, общий store

Доп.инфа тут: https://blog.tylerbuchea.com/super-simple-react-redux-application-example/

ДЗ:
1) Установить редакс
npm install --save redux react-redux 
или
yarn add redux react-redux
2) Создать папку redux в проекте
3) Создать 4 файла:
-> action-types.js
-> actions.js
-> reducers.js
-> store.js
4) Файл store.js
```
import {
    createStore
} from 'redux';
import { reducers } from './reducers'

export function configureStore(initialState = {}) {
    const store = createStore(reducers, initialState);
    return store;
};

export const store = configureStore();
```
5) Сделать так чтобы по клику на кнопку "Заблокировать пользователя -> Да" менялся цвет строки и закрывалось модальное окно