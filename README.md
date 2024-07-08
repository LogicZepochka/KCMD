### KCMD
Хакерский инструмент для игры GreyHack
#Подготовка окружения
Потребуется **greybel** расширение для **VS Code** и настройка самой игры
## Настройка игры
В игре необходимо создать папку `KCMD` по адресу `/home`
greybell будет импортировать исходный код в папку по адресу
> /home/KCMD

После его нужно подготовить саму игру к работе с greybell
- Далее нужно установить BepInEx [здесь](https://github.com/BepInEx/BepInEx/releases/tag/v5.4.23.1 "здесь") и установить в игре ([Подробная инструкция по установке](https://docs.bepinex.dev/articles/user_guide/installation/index.html "Подробная инструкция по установке"))
- Запустить игру, чтобы BepInEx создал необходимые файлы
- Скачать [GreyHackMessageHook5.dll](https://gist.github.com/ayecue/b45998fa9a8869e4bbfff0f448ac98f9/raw/ada96de7fae26d6aca85b1e6aba6873799cd37e6/GreyHackMessageHook5.dll "GreyHackMessageHook5.dll")
- Поместить GreyHackMessageHook5.dll в папку plugins BepInEx
- (Для Linux) Изменить параметры запуска в Steam на `"/path/to/Steam/steamapps/common/Grey Hack/run_bepinex.sh" %command%`

## Настройка VS Code
- Устанавливаем **Greybell**
- Открываем настройки расширения Greybell
- Устанавливаем:
`Сreate Ingame -> Mode -> Public`
`Create Ingame -> Agent -> message-hook`
`Transpiler -> Ingame Directory -> /home/KCMD`
- Сохраняем настройки

## Проверка правильности настройки
- Запускаем игру (В мультиплеере, либо в одиночной)
- *В VS Code*: Нажимаем ПКМ по папке src -> Greybell: Import file in to game
Если файлы успешно скопировались в игру - настройка завершена

## Тестирование
Для теста необходимо скомпилировать файл main.src в игре и запустить исполняемый файл
