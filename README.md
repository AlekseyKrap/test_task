# Тестовое задание

    Нужно создать две страници используя https://material-ui.com/ru/, json-server (команда "startServ") для роутинга https://reactrouter.com/web/guides/quick-start :
    1.  Главная страница 
        ![alt text](https://gyazo.com/ee2a35b4ba32fceaea24659893e49e5d)
        состоит из меню список юзеров и таблица с данными по юзеру
        
        список юзеров-получаем по запросу /users.logins
        Данные по юзеру
         -если в списке юзеров не выбранно юзера получаем данные по запросу /users.page 
         -если выбран юзер получаем данные по запросу /users.page/?usrId={usrId}
         
         нужно использовать redux и redux-saga
         
        также нужно написать функцию дженерик<[тип данных который хотим получить],[тип данных которые хотим передать(не обязательный)]>  которая будет принемать адрес запроса и возврощать промис
        
        выглядет следующем образом:
        `export const APIGetlistUsers = genFetchData<TAPIlistUsersResp>('/users.logins');
         export const APIGetAllUsersPage = genFetchData<TAPIUsersPage>('/users.page');
         export const APIGetUsersPageById = genFetchData<TAPIUsersPage, TPUsersPageById>(
           '/users.page',
         );`
        
        так чтобы в воркере саги можно было вызывать сгенерированные промисы `const res = yeld call(APIGetlistUsers)`    

    2. Станица с формой 
            адрес страници /form
            поля:
                логин - строковое поле 60 символов, состоящее из латинских заглавные и строчных букв знаков _ - 
                email 
                кнопка "отправить" если не запоненно/заполненно не корректно хоть одно поле кнопка не активна
            при нажатии на кнопку данные с формы отправляются в сагу воркер и там просто выводятся в консоль
            для формы использовать https://github.com/formium/formik
            

### Удачи !!! 🚀       


