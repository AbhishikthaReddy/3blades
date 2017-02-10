## Guidelines for App Backend(Dev) setup (Windows machine)

Fork the repo https://github.com/3Blades/app-backend and clone it to your machine

## Requirements

1. Docker version: '2'
2. Python version: '2.7'

## Installation

1. pip install -r requirements/base.txt
2. Copy & paste the docker-compose.yml file
   i. Change the volumes & environment
      volumes:
            - .:/srv/app
            - /workspaces:/workspaces
            - //c/Users/Abhishiktha/.docker/machine/machines/default:/certs (custom path)
      environment:
            DOCKER_HOST: tcp://<<local_ip>>:2375 (for api, celery)
            DOCKER_HOST: tcp://192.168.99.100:2376 (for logspout)
   ii. Go to your folder path and Run "docker-compose up -d" in your docker terminal
   iii. Run "docker-compose ps" to check all the services are running
   iv. Create a super user with extension hstore "docker-compose exec db psql postgres -c 'create extension hstore;' -U postgres"
   v. Migrate the data by running "docker-compose exec api //srv/env/bin/python manage.py migrate"
   vi. Go to http://192.168.99.100:5000/api/v0/swagger/#/users

## License

Copyright © 2016-2017 3Blades, LLC. All rights reserved, except as follows. Code
is released under the BSD 3.0 license. The README.md file, and files in the
"docs" folder are licensed under the Creative Commons Attribution 4.0
International License under the terms and conditions set forth in the file
"LICENSE.docs". You may obtain a duplicate copy of the same license, titled
CC-BY-SA-4.0, at http://creativecommons.org/licenses/by/4.0/.
