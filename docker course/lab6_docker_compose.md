**1. Создай экземпляр базы данных postgres в контейнере с названием db, образ postgres, переменные окружения POSTGRES_PASSWORD=mysecretpassword**  
  
![](images/20230127120208.png)   

**2. Теперь создай простой контейнер с wordpress, он должен называться wordpress, образ: wordpress, сделай link этому контейнеру к контейнеру с именем db выставь 30085 порт на докер-хост**  
  
![](images/20230127120505.png)  

**3. Сначала надо прибрать за собой, давай удалим все, что осталось от предыдущих шагов.**  
Удали все контейнеры - db и wordpress  

![](images/20230127121350.png)  

**4. Создай файл docker-compose.yml в размещении /root/wordpress. Обрати внимание, размещение должно быть /root/wordpress/docker-compose.yml, иначе система не сможет правильно проверить результат. Сделай sudo -i, пароль selena. После этого запусти стек с помощью docker-compose в detached mode.**  
Важно, чтобы в файле спецификация была такой же, как и раньше, т.е. контейнеры были wordpress и db и не забудь прокинуть нужные порты

![](images/20230127123215.png)   

**5. Мы что-то поменяли, сколько реплик контейнеров в службе wordpress?**  
  
![](images/20230127123419.png)    

**6. Увеличь количество реплик wordpress до 2.**  
Пользуйся средствами docker-compose
  
![](images/20230127123557.png)  

**7. Останови стек docker-compose.**
Убедись, что Docker Compose корректно положил стек  
  
![](images/20230127123730.png)  