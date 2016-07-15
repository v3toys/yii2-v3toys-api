V3toys yii2 api
===================================

http://www.v3toys.ru/index.php?nid=api

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist v3toys/yii2-api "*"
```

or add

```
"v3toys/yii2-api": "*"
```

How to use
----------

```php
//App config
[
    'components'    =>
    [
    //....
        'v3toys' =>
        [
            'class'         => '\v3toys\yii2\api\ApiV04',
        ],
    //....
    ]
]

```

Examples
----------

```php

$response = \Yii::$app->v3toys->send('getProductsDataByIds', [
    'products_ids' => 217070
]);

if ($response->isError)
{
    echo $response->error_code;
    echo $response->error_message;
}

if ($response->isOk)
{
    print_r($response->data);
}

```
___

> [![skeeks!](https://gravatar.com/userimage/74431132/13d04d83218593564422770b616e5622.jpg)](http://skeeks.com)  
<i>SkeekS CMS (Yii2) — fast, simple, effective!</i>  
[skeeks.com](http://skeeks.com) | [cms.skeeks.com](http://cms.skeeks.com) | [marketplace.cms.skeeks.com](http://marketplace.cms.skeeks.com)
