access2json
===========

Преобразователь mdb файлов в json по правилам описанным в структуре

Требования:
----------

- wscript (встроен в Windows)

Конфиг файл должен находится в одной папке с app.js и представляет из себя json файл со структурой:

    {
      query: "select ...",
      template:
      {
        "имя_поля": "{{name}}",
        "форматированная_дата": "{{data}}     2014 года",
        "привязки": 
        {
          query: "select ...",
          template:
          {
            ...
          }
        },
        "прочие": "asdasd"
      }
    }

На выходе получится json примерно такого содержания:

    {
        "имя_поля": "Вася",
        "форматированная_дата": "12.03   2014 года",
        "привязки": 
        {
            "волосы": "...",
            "рост": {
            ...
            }
        },
        "прочие": "asdasd"
    }



Использование:
------------

Первый вариант для оконного, второй для консольного запуска
wscript app
cscript app
