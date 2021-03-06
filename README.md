## Як встановити проект

Якщо ви користуєтесь Vagrant, то ви вже знаєте, що вам робити:

```shell
vagrant up
```

В іншому разі, окрім стандартних процедур, для запуску проекту вам знадобиться оновити версію PHP до 5.6 та імпортувати схему бази даних із теки migration:

```shell
add-apt-repository ppa:ondrej/php5-5.6
apt-get update
apt-get install php5
mysql -u root -p hryvna < migration/database_structure.sql
mysql -u root -p hryvna < migration/database_data.sql
```

Після налаштування серверу не забудьте завантажити ліби за допомогою Composer:

```shell
vagrant ssh
cd /vagrant/engine
composer install
```

## API

Гривня Тудей має власне API, у якому можна отримати історію курсів за останній рік. Також, із запуском API тепер доступні курси багатьох валют. 

Документація та доступ знаходиться на Mashape за цим посиланням:

https://market.mashape.com/dontgiveafish/hryvna-today

## Telegram

Напишіть боту Гривні у Telegram! Бот навчений декільком командам, що дають інформацію про поточний курс валют:

https://telegram.me/HryvnaTodayBot

Код боту також відкритий і знаходиться в іншому проекті:

https://github.com/dontgiveafish/hryvna-today-telegram

## Багато дяк

[Dmytro Bagaiev](https://github.com/dbagaev) for code revision

## Таке інше

Якщо ви хочете долучитись до розробки чи маєте питання щодо API, пишіть на tony@dontgiveafish.com

І гуд тріп, як той казав Едіп!
