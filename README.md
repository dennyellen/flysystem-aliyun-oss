# Flysystem Adapter for Aliyun OSS.

This is a Flysystem adapter for the Aliyun OSS ~2.0.4

inspire by [aobozhang/aliyun-oss-adapter](https://github.com/aobozhang/aliyun-oss-adapter)

## Installation

```bash
composer require apollopy/flysystem-aliyun-oss
```

## for Laravel

This service provider must be registered.

```php
// config/app.php

'providers' => [
    '...',
    ApolloPY\Flysystem\AliyunOss\AliyunOssServiceProvider::class,
];
```

edit the config file: config/filesystems.php

add config

```php
'oss' => [
    'driver'     => 'oss',
    'access_id'  =>  env('OSS_ACCESS_ID','your id'),
    'access_key' =>  env('OSS_ACCESS_KEY','your key'),
    'bucket'     =>  env('OSS_BUCKET','your bucket'),
    'endpoint'   =>  env('OSS_ENDPOINT','your endpoint'),  
],
```

change default to oss

```php
    'default' => 'oss'
```