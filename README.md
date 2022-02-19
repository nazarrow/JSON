### JSON

1. Создать внешний репозиторий c названием JSON:

    + войти <https://github.com/nazarrow?tab=repositories>

    + нажать `"New"`

    + ввести `"JSON"` в поле `"Repository name"` --> выбрать `"Public"` и `"Add a README file"`

    + нажать `"Create repository"`

2. Клонировать репозиторий JSON на локальный компьютер:

    + нажать `"Code"` --> выбрать `"HTTPS"` --> `скопировать ссылку на репозиторий`

    + в gitbash зайти в папку(в которой будет размещен репозиторий)

    + клонировать репозиторий на локальный компьютер --> `git clone` <https://github.com/nazarrow/JSON.git>

    + войти в папку "JSON" --> `cd JSON` (в конце адреса расположения отображается "main")

3. Внутри локальной папки JSON создать файл “new.json”:

    + `touch new.json`

    + `git status` - "new.json" отображается красным (изменения в файле не отслеживаются)

4. Добавить файл под гит:

    + `git add new.json`

    + `git status` - "new.json" отображается зеленым (изменения в файле отслеживаются)

5. Закоммитить файл:

    + `git commit -m "add new.json"` - создает снимок текущего состояния файла с комментарием add new.json

6. Отправить файл на внешний GitHub репозиторий:

    + `git push`

7. Отредактировать содержимое файла “new.json” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате JSON:

    + `vim new.json`

    + `"i"`

````json
{
 "full_name":"Nazarov_Aleksei_Olegovich",
 "age":28,
 "pets":"I don`t have any pets",
 "desired_salary":"500$"
}
````

+ `"Esc"`  

+ `":wq"`

8. Отправить изменения на внешний репозиторий:

    + `git add new.json`

    + `git commit -m "modified new.json"`

    + `git push`

9. Создать файл preferences.json:

    + `cat > preferences.json`

10. В файл preferences.json добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате JSON:

```` json
{
 "favorite_movie":"The Social Network",
 "favorite_series":"Silicon Valley",
 "favorite_food":"Meat",
 "favorite_season":"Summer",
 "country_i_would_like_to_visit":"Switzerland"
}
````

+ `"Enter"`

+ `"Ctrl + D"`

11. Создать файл skills.json добавить информацию о скиллах которые будут изучены на курсе в формате JSON:

    + `cat > skills.json`

````json
{
"skills":[
 "software testing theory",
 "client-server architecture",
 "HTTP Server Request Methods",
 "HTTP server Response codes",
 "Structures of HTTP requests and responses",
 "What is JSON, XML. Their structure",
 "API testing via Postman JS, API autotests",
 "Removing and reading logs from an external server",
 "Sniffing http web traffic through Charles and Fiddler",
 "Dev Tools of web browsers Google Chrome, FireFox",
 "VPN. How it works, why you need it, how to use it, tool options",
 "Mobile testing",
 "Feature of iOS, Android, guidelines",
 "Build iOS applications on Xcode",
 "Build Android applications on Android Studio",
 "ADB management of android devices",
 "Setting up proxy and vpn on iOS and Android",
 "Interception (sniffing) of mobile traffic through Charles and Fiddler on iOS and Android",
 "Command line (terminal) Linux copy, create, view, move files on servers without a graphical interface",
 "Basics of bash scripting, automation of routine tasks on the server",
 "Access to remote servers",
 "Basics of SQL Create, Delete, Drop, Insert Into, Select, From, Where, Join",
 "Postgres database installation, configuration and use",
 "Non-relational database Redis installation, configuration and use",
 "Load testing in Jmeter",
 "Scrum development methodology",
 "Python. Learning the basics. Building a client-server application"
 ]
}
````

+ `"Enter"`

+ `"Ctrl + D"`

12. Отправить сразу 2 файла на внешний репозиторий:

    + `git add ._`

    + `git commit -m "add preferences.json and skills.json"`

    + `git push`

13. На веб интерфейсе создать файл bug_report.json:

    + войти в `репозиторий "JSON"`

    + нажать кнопку `"Add file"`

    + выбрать `"Create new file"`

    + в поле `"Name your file"` ввести `"bug_report.json"`

14. Сделать "Commit changes" (сохранить) изменения на веб интерфейсе:

    + нажать кнопку `"Commit new file"`

15. На веб интерфейсе модифицировать файл bug_report.json, добавить баг репорт в формате JSON:

    + открыть файл `"bug_report.json"`

    + выбрать редактирование и ввести текст

````json
{
"bugReport":[
   {
   "summary": "Information dosn't provide if have more than 7 characters from WS",
   "descriprion": "WS dosen't provide information if response containes more than 8 characters",
   "actualResult": "information gets",
   "expectedResult": "information doesen't get",
   "requirementId": "requirement",
   "reproducedOn": "Win 10",
   "reproducibility": "always",
   "workaround": "no",
   "stepsTOreproduce":[
        {"one": "1. Open FireFox browser",
        "two": "2. Click [RESTClient] icon",
        "three": "3. Request method: POST",
        "four": "4. URL: <http://178.124.206.52/app/ws/>",
        "five": "5. type in Body: {user:rangarad, strict:false}"
                                }
                                ],
   "severity": "minor",
   "priority": "low"
   }  
   ]
}
````

16. Сделать "Commit changes" (сохранить) изменения на веб интерфейсе:

    + нажать кнопку `"Commit changes"`

17. Синхронизировать внешний и локальный репозиторий JSON:

    + `git pull`
