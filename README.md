# dcOwnCloud

```bash


# default data stored within container


# remove data
docker-compose down --rmi all --volumes

# shutdown containers
docker-compose down

# for remote access .env.OWNCLOUD_DOMAIN must be replaced
OWNCLOUD_DOMAIN=google.com:80 # ej


```

### Remote
1. [optional](Enable SSL)
```bash
docker-compose exec owncloud bash # get cli to owncloud service
vi /var/www/owncloud/config/config.php # access apache config file


```

```php
$CONFIG = array (
  'trusted_domains' =>
  array (
    0 => 'localhost',
    1 => 'example.com', 
    2 => '93.184.216.34',
));
```

```bash 
docker-compose restart owncloud
```