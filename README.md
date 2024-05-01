# Go. Моё изучение языка

<img src="https://raw.githubusercontent.com/BeautifulDirt/golang-study/main/golang.jpg" alt="golang" height="320" />


**[Go](https://go.dev/)** - это компилируемый многопоточный язык системного программирования с открытым исходным кодом, над созданием которого в компании Google трудились Роберт Гриземер, Кен Томсон и Роб Пайк.

`go build <name_file>.go` - компиляция Go-кода. Запуск в терминале `./<name_file>` \
`go run <name_file>.go` - запуск кода, как скрипт

В данном репозитории будут размещаться мною выполненные упражнения, которые представлены в конце каждой главы.


<details>
  <summary><strong>Глава 1. Краткое введение в Go</strong></summary>
  
  ##### *Упражнения*
  1. Наша версия `which(1)` останавливается после нахождения первого вхождения нужного исполняемого файла. Внесите необходимые изменения в [which.go](/exercise_chapter_1/which.go), чтобы найти все возможные вхождения нужного исполняемого файла.
  2. Текущая версия [which.go](/exercise_chapter_1/which.go) обрабатывает только первый аргумент командной строки. Внесите необходимые изменения в [which.go](/exercise_chapter_1/which.go), чтобы принять переменную PATH и выполнить поиск несколько исполняемых двоичных файлов.

  ##### *Мои решения*
  1. Для того, чтобы программа [which.go](/exercise_chapter_1/which.go) вывела все возможные варианты вхождения нужного исполняемого файла, необходимо убрать оператор `return` в 26 строке.
  Код решения представлен в файле [which_remake_1.go](/exercise_chapter_1/which_remake_1.go).

  Вывод [which.go](/exercise_chapter_1/which.go):

  ```bash
  $ go run which.go which
    /usr/bin/which
  ```

  Вывод [which_remake_1.go](/exercise_chapter_1/which_remake_1.go):

  ```bash
  $ go run which.go which
    /usr/bin/which
    /bin/which
  ```

  2. Используем измененный код [which_remake_1.go](/exercise_chapter_1/which_remake_1.go) для решения данного задания. Здесь необходимо добавить новый цикл для поиска необходимых исполняемых файлов из заданного списка аргументов. Поэтому убираем присвоение аргумента к переменной `file` в 15 строке. И в 18 строке добавляем цикл `for` для перебора слайза с последующим присвоением к `file`, игнорируя первый элемент полученных программой аргументов. 
  Код решения представлен в файле [which_remake_2.go](/exercise_chapter_1/which_remake_2.go).

  Вывод [which.go](/exercise_chapter_1/which.go):

  ```bash
  $ go run which.go which
    /usr/bin/which
  ```

  Вывод [which_remake_2.go](/exercise_chapter_1/which_remake_2.go):

  ```bash
  $ go run which.go which discord
    /usr/bin/which
    /usr/bin/discord
    /bin/which
  ```

</details>

##### Литература:
Цукалос Михалис. Golang для профи: Создаем профессиональные утилиты, параллельные серверы и сервисы. 3-е изд. - СПб.: Питер, 2024. - 624 с.: ил. - (Серия "Для профессионалов")

⭐ Star me!
