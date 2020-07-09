# Daily 

Uses Clockify api to fetch yesterday timers and print them to terminal.  
Can send the recap as SMS on your phone if you're a Free Mobile user.  

## Requirements

* PHP 7.4
* Composer
* Clockify Api token

### Install

```
cd daily
cp .env.example .env
composer install
chmod u+x daily
```

## Usage
Fetch yesterday timers and send it as SMS
```
#PHP
./daily -s
#DOCKER
docker container run --rm -v $(pwd):/daily/ php:7.4-cli /bin/bash -c "curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer; cd daily; /usr/local/bin/composer install; chmod u+x /daily/daily; php /daily/daily -s;"
```

## Improvements
- Allow for date
- On Monday use last Friday instead of Yesterday
