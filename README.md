NGINX é um servico de proxy reverso usando o nginx

nginx

sudo docker network ls
sudo docker network connect mod_network nginx-app-1
sudo docker exec -it nginx-app-1 /bin/bash



pccontainers    10.0.2.11 | 10.0.11.2
pcnuvem         10.0.2.12 | 10.0.12.2
pcremoto        10.0.2.13 | 10.0.13.2


========================

    networks:
      network:
        ipv4_address: 10.0.5.2
      nginx_network:
        ipv4_address: 10.0.2.3

networks:
  network:
    driver: bridge
    ipam:
      config:
        - subnet: 10.0.5.0/24
  nginx_network:
    external: true