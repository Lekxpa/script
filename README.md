Урок 8. Скрипты Bash


Задание:

Написать скрипт очистки директорий. На вход принимает путь к директории. Если директория существует, то удаляет в ней все файлы с расширениями .bak, .tmp, .backup. Если директории нет, то выводит ошибку.

#!/bin/bash

directory=$1

if [ -d $directory ]

    then
        cd $directory | ls -al $directory
                        rm  *.bak *.tmp *.backup | echo "Done. Files deleted"
                        echo "Result: "
                        ls -al $directory
                else
                        echo "There are not a directory like this - $directory"
fi
