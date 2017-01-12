[![slack in](https://slackin-pypmyuhqds.now.sh/badge.svg)](https://slackin-pypmyuhqds.now.sh/)

# 3Blades

- [Overview](https://github.com/3Blades/3blades/blob/master/README.md#overview)
- [Repos](https://github.com/3Blades/3blades/blob/master/README.md#repos)
- [Infrastructure elements](https://github.com/3Blades/3blades/blob/master/README.md#infrastructure-elements)
- [DevOps](https://github.com/3Blades/3blades/blob/master/README.md#devops)
- [Documentation](https://github.com/3Blades/3blades/blob/master/README.md#documentation)

## Overview

3Blades meta package for installation and docs.

3Blades was born to **accelerate modern data science**. Import data, use Notebook servers for exploratory data analysis, create visualizations and publish trained machine learning models as RESTful endpoints in their native languages. All from one location!

There are two options available:

- [Online](https://3blades.io): free signup and no credit card required.
- [On-premise](https://github.com/3blades/onpremise): free community version available. Pro version adds more goodies and support services.

And yes, 3Blades is open source, BSDv3 licensed!

#### Some features...more to come!

- A quick way to manage Notebook servers among team members.
- Connect to a variety of data source containers, including Spark, either as local containers or via SSH.
- Automate common tasks with cron jobs, such as train/test splits.
- Publish trained models as RESTful APIs, secured with user API tokens, in their native language.
- Create and share visualization dashboards to tell your data story.

We would love to hear from you if you have a feature request. If you have something in mind, feel free to open a feature request in our [roadmap repo](https://github.com/3blades/roadmap).

## Repos

Main frontend and backend will be merged into one repo, once rewrite has been completed. For now, they are maintained independently:

- [Frontend](https://github.com/3blades/react-frontend): ReactJs front end.
- [RESTful service](https://github.com/3blades/app-backend): based on Flask, Celery, SQLAlchemy, RESTplus.

Other software artifacts:

- [Log service](https://github.com/3blades/logspout): obtaines and optionally exports syslogs from docker containers. Also used for log streams in UI.
- [NBViewer](https://github.com/3blades/nbviewer): for `.ipynb` shares.
- [Notifications service](https://github.com/3blades/notifications-server): updates service and container statuses.
- [Reverse proxy](https://github.com/3blades/openresty): used to route traffic correctly to each micro service and user server environments.
- [Statistics service](https://github.com/3blades/docker-stats): used to log basic run stats for user services (stop/start datetimes, file outputs, etc).

User container servers:

- [Core server](core-server): parent server for job-server, model-server and notebook-server.
- [Job server](https://github.com/3blades/job-server): server to run scheduled jobs, useful for recurring and batch processes.
- [Model server](https://github.com/3blades/model-server): server to publish models as RESTful endpoints, in their native language.
- [Notebook server](https://github.com/3blades/notebook-server): notebook server used for exploratory data analysis.

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

- Analytics: [Mixpanel](https://mixpanel.com/)
- Code quality: [Code Climate](https://travis-ci.org/) and [Landscape](https://travis-ci.org/)
- Continuous Deployment: [Travis-CI](https://travis-ci.org/)
- Continuous Integration: [Travis-CI](https://travis-ci.org/)
- Configuration Management: [Ansible](https://www.ansible.com/)
- Coverage: [Codecov](https://codecov.io/)
- Exception tracking: [Sentry](https://getsentry.com)
- Infrastructure Deployment: [AWS CloudFormation](https://aws.amazon.com/cloudformation/)
- Monitoring: [Pingdom](https://www.pingdom.com/)
- Testing:
- Version control: [GitHub](https://github.com)

## Documentation

- [WIP] [Community](https://slackin-tkscnxhpky.now.sh)
- [WIP] [Issue tracking](https://github.com/3Blades/3blades/issues)
- [WIP] [Installation and configuration](https://github.com/3Blades/docs)
- [WIP] [Support](https://support.3blades.io)

## Copyright and license

Copyright © 2016-2017 3Blades, LLC. All rights reserved, except as follows. Code
is released under the BSD 3.0 license. The README.md file, and files in the
"docs" folder are licensed under the Creative Commons Attribution 4.0
International License under the terms and conditions set forth in the file
"LICENSE.docs". You may obtain a duplicate copy of the same license, titled
CC-BY-SA-4.0, at http://creativecommons.org/licenses/by/4.0/.
