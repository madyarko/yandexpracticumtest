# yandexpracticumtest
# Git

### git config --global user.name madyarko

Изменение имени пользователя в глобальном конфиге

### cat .gitconfig

Просмотр локального файла конфигурации

### git init

Инициализация репозитория

### git status

Проверка статуса репозитория

### git add readme.txt

Добавление файла **readme.txt** в "корзину" будущего коммита, можно заменить название файла на флаг **--all**, тогда, добавятся все файлы которые есть в папке но нету в репозитории, или можно добавить папку, указав её название, так-же можно указать на текущую папку, так: **git add .**

### git commit -m 'my first commit'

Создает новый коммит в репозитории и присваивает ему сообщение **my first commit** 

### git log

Просмотр истории коммитов.


# GitHub

### Создать новый репозиторий

```bash
echo "# Git-Basics" >> README.md // Создаст файл README.md с содержимым "# Git-Basics"
git init // Инициализация локального репозитория
git add README.md // Подготовка файла README.md к будущему коммиту(добавление в корзину)
git commit -m "first commit" // Создаст коммит на локальном репозитории с сообщением "first commit"
git branch -M main // Переименовать ветку в main
git remote add origin git@github.com:madyarko/Git-Basics.git // Привязать локальный репозиторий к удалённому на GitHub
git push -u origin main // Отправить локальный репозиторий на удалённый
```



### Сохранить локальный репозиторий на удалённый

```bash
git remote add origin git@github.com:madyarko/Git-Basics.git // Привязать локальный репозиторий к удалённому на GitHub
git branch -M main // Переименовать ветку в main
git push -u origin main // Отправить локальный репозиторий на удалённый
```



### Убедится что всё работает

```bash
git remote -v
```

Покажет информацию о репозитории, должно быть так:

```bash
$ git remote -v
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push)
```



### Редактирование

```bash
git add -all // сохранить измения репозитория в "корзину" будущего коммита
git commit -m // создать коммит, пока только локальный
git push // отправить изменения локального репозитория на удалённый
```

# SSH-keys

### Папка с ssh-ключами

```bash
cd ~ // переход в домашнюю дерикторию
ls -a ./ssh // проверить, есть ли папка с ssh-ключами
```

### Генерация ssh-ключей

```bash
 ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" 
```

Если есть ошибки, используйте другой тип шифрования, вместо `ed25519` - используйте этот `4096`

### Укажите место хранение ключей

Укажите путь как в примере или нажмите **ENTER** - чтобы использовать стандартный путь - **домашний каталог**.

```bash
(C:\Users\<имя_пользователя>\.ssh\):[Press enter] // Windows
```

```bash
(/Users/you/.ssh/id_rsa): [Press enter] // Mac or Linux
```

### GitHub

Для работы ssh-ключей с **GitHub** нужно указать их в профиле: `Settings >> SSH and GPG keys >> New SSH key`.

### Ссылка на гайд по ssh-ключам

[[вот она]](https://code.s3.yandex.net/git_Basic/SSH_Screencast.mp4)


