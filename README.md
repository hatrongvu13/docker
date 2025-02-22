** jax tony
redis
https://github.com/bitnami/bitnami-docker-redis/blob/master/docker-compose-replicaset.yml

* using existing network

``` dockerfile
version: '3'
services:
    image: jenkins/jenkins:lts
    container_name: jenkins_lts
    restart: always
    ports:
        - "8080:8080"
        - "50000:50000"
    volumes:
        - "jenkins_homes:/var/jenkins_home"
    networks:
        - exist_network
volumes:
    jenkins_home:
    driver: local
networks:
    exist_network:
        external: true
```

* Bind mounts volumes

``` dockerfile
version: '3'
volumes:
    data_volumes:
        driver: local
        driver_opts:
            type: none
            device: /home/user/data_volumes
            o: bind
```