## Django ToDo Project With Docker Compose and Docker Machine

Featuring:

- Docker v18.09.2
- Docker Compose v1.23.2
- Docker Machine v0.16.1
- Python 3.7.3
- VirtualBox

### OS X Instructions

1. Start new docker machine - 
```
docker-machine create -d virtualbox dev;`
```

2. Configure your shell to use the new machine environment -
```
eval $(docker-machine env dev)
```

3. Build images - 
```
docker-compose build
```

4. Start services - 
```
docker-compose up -d
```

5. Create migrations - 
```
docker-compose exec web /usr/local/bin/python manage.py makemigrations todo

docker-compose exec web /usr/local/bin/python manage.py migrate
```

6. Grab IP - 
```
docker-machine ip dev
``` 

7. View the URL in your browser -

## Reference
https://realpython.com/blog/python/django-development-with-docker-compose-and-machine/