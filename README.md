# 測試套件

這是一個測試用的套件

---

## 安裝方式

假如要使用 composer require galaxytw/galaxytw, 請使用以下語法:
```
$ composer require galaxytw/galaxytw:dev-master
```
假如開發時要使用本機的時候開發, 請使用以下的 composer.json
```
{
    "require":{
       "galaxytw/galaxytw":"*"  
    },
    "minimum-stability":"dev",
    "repositories": {
        "local":
        {
        "type": "path",
        "url": "/your_path/galaxytw"
        }
    }
}
```
假如是使用壓縮檔案,  請使用以下 composer.json
```
{
    "require":{
       "galaxytw/galaxytw":"*"   
    },
    "minimum-stability":"dev",
    "repositories": [
        {
            "type": "package",
            "package":{
                "name":"galaxytw/galaxytw",
                "version":"0.0.8",
                "dist":{
                "type":"zip",
                    "url": "/your_path/galaxytw.zip"
                },
                "autoload":{
                    "psr-4":{
                        "galaxytw\\galaxytw\\":"src/"
                    }
                }
            }
        }
    ]
}
```
假如要使用 http 並且是 zip 檔案時,  請使用以下 composer.json
```
{
    "require":{
       "galaxytw/galaxytw":"*"   
    },
    "config":{
        "secure-http": false
    },
    "minimum-stability":"dev",
    "repositories": [
        {
            "type": "package",
            "package":{
                "name":"galaxytw/galaxytw",
                "version":"0.0.8",
                "dist":{
                "type":"zip",
                    "url": "http://your_url/galaxytw.zip"
                },
                "autoload":{
                    "psr-4":{
                        "galaxytw\\galaxytw\\":"src/"
                    }
                }
            }
        }
    ]
}

```

## 測試

安裝完後, 產生 test.php 檔案, 並輸入以下測試程式:
```
<?php

require_once __DIR__.'/vendor/autoload.php';

use galaxytw\galaxytw\CMisc;

echo CMisc::world();
```

## 執行

產生出 test.php 檔案後, 請在 command line 下執行
```
$ php -f test.php
```
結果將會出現:
```
Hello World, Composer!
```

---

## 參考網址:

https://blog.jgrossi.com/2013/creating-your-first-composer-packagist-package/

https://stackoverflow.com/questions/40582788/install-composer-php-plugin-from-zip-file

https://webcache.googleusercontent.com/search?q=cache:OCJgr9PIt3wJ:https://idce.com/document/0b60%3Fv%3Dv1.0+&cd=36&hl=zh-TW&ct=clnk&gl=tw
