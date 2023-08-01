# Архиватор пользователей, сообществ, постов, лайков и комментариев с сайта vk.com через API ВКонтакте
[![Version](http://poser.pugx.org/kostyan-org/vk-archiver/version)](https://packagist.org/packages/kostyan-org/vk-archiver)
[![Total Downloads](http://poser.pugx.org/kostyan-org/vk-archiver/downloads)](https://packagist.org/packages/kostyan-org/vk-archiver)
[![License](http://poser.pugx.org/kostyan-org/vk-archiver/license)](https://packagist.org/packages/kostyan-org/vk-archiver)
[![PHP Version Require](http://poser.pugx.org/kostyan-org/vk-archiver/require/php)](https://packagist.org/packages/kostyan-org/vk-archiver)

![Image](https://github.com/kostyan-org/vk-archiver/raw/gh-pages/vk-archiver.PNG)

[Home page](https://kostyan-org.github.io/vk-archiver)

## Installation:

    composer create-project kostyan-org/vk-archiver
    cd .\vk-archiver\

edit the **.env** file

    VK_API_TOKEN=полученный токен от вк
    VK_API_USER=айди юзера токена
    DATABASE_URL="mysql://root:@127.0.0.1:3306/название новой БД?charset=utf8mb4"

create a new database

    php bin/console doctrine:database:create
    php bin/console doctrine:migrations:migrate

## Job
command list

    php bin/console app:

example of loading 3 latest posts with likes and comments from the vk group

    php bin/console app:download vk --likes --comments --limit 3

list of ready-made statistics methods

    php bin/console app:stat --methods

example of viewing group statistics - vk

    php bin/console app:stat --method statwall --source vk
