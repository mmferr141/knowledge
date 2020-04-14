# Docker composer template

{% code title="docker-compose.yml" %}
```text
version: "3"
services:
    redis-server:
        image: "redis"
    node-app:
        restart: on-failure
        build: .
        ports:
            - "4081:8081"
```
{% endcode %}

### Restart policies

* no: never attempot to restart this container if stops or craches
* always: if this container stops for any reason always attemp to restart it
* on failure: Only restart if the container stops with an error code 
* unless-stopped: Always restart unless we \(the developers\) forcibily stop it



