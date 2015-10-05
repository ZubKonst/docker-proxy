### Hello

Run via docker-compose:
```
docker-compose build && docker-compose up -d
```

Run web container manually:
```
docker pull zubkonst/simple_rack:latest
docker run -d --expose=8080 -e WEB_CONCURRENCY=2 -e VIRTUAL_HOST=simple_rack zubkonst/simple_rack:latest unicorn -c config/unicorn.rb
docker stop -t=60 adoring_blackwell
```
