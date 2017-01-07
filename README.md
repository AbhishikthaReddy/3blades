[![slack in](https://slackin-tkscnxhpky.now.sh/badge.svg)](https://slackin-tkscnxhpky.now.sh/)

# 3Blades

## Overview

3Blades was born to **accelerate modern data science**. Import data, use Notebook servers for exploratory data analysis, create visualizations and publish trained machine learning models as RESTful endpoints in their native languages. All from one location!

This repository is the main entry point for all 3Blades application resources.

## Features

- A quick way to manage Notebook servers among team members.
- Connect to a variety of data source containers, including Spark, either as local containers or via SSH.
- Automate common tasks with cron jobs, such as train/test splits.
- Publish trained models as RESTful APIs, secured with user API tokens, in their native language.
- Create and share visualization dashboards to tell your data story.

## Repos

Main frontend and backend will be merged into one repo, once rewrite has been completed. For now, they are maintained independently:

- [RESTful service](https://github.com/3blades/app-backend): based on Flask, Celery, SQLAlchemy, RESTplus.
- [Frontend](https://github.com/3blades/react-frontend): ReactJs front end.

Other software artifacts:

- [Reverse proxy](https://github.com/3blades/openresty): used to route traffice correctly to each micro service and user server environments.
- [Notifications service](https://github.com/3blades/notifications-server): updates service and container statuses.
- [Statistics service](https://github.com/3blades/docker-stats): used to log basic run stats for user services (stop/start datetimes, file outputs, etc).
- [Log service](https://github.com/3blades/logspout): obtaines and optionally exports syslogs from docker containers. Also used for log streams in UI.
- [NBViewer](https://github.com/3blades/nbviewer): for `.ipynb` shares.

## Infrastructure elements:

- Docker Swarm
- NFS
- PosgreSQL
- Redis
- RabbitMQ
- SMTP

Currently we are using [AWS](https://aws.amazon.com/) to manage as many of the above services as possible.

- Compute: EC2
- Networking: VPC
- PosgreSQL: RDS
- Redis: Elasticache
- Storage: EBS, S3, EFS
- SMTP: SES

Other services:

RabbitMQ: [CloudAMQP](https://www.cloudamqp.com/)

## DevOps

- Code quality: [Code Climate](https://travis-ci.org/) and [Landscape](https://travis-ci.org/)
- Continuous Integration: [Travis-CI](https://travis-ci.org/)
- Coverage: [Codecov](https://codecov.io/)
- Version control: [GitHub](https://github.com)

## Resources

- [WIP] [Documentation](https://support.3blades.io)
- [WIP] [Community (Bugs, feature requests, general questions)](https://github.com/3blades/3blades/issues)
