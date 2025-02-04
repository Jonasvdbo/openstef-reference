
# Openstf-reference

Reference implementation of the **OpenSTEF** stack. It includes all key functionality, e.g. the forecast engine, data storage and -models, the expert user dashboard!
![screenshot](https://user-images.githubusercontent.com/60883372/146760483-29af3ac7-62af-4f13-98c7-982a79c517d1.jpg)
Screenshot of the operational dashboard showing the key functionality of OpenSTEF. 
Dashboard documentation can be found [here](https://github.com/OpenSTEF/.github/blob/main/profile/README.md).
# Installation

## Prerequisites

You will need to install both Docker and Docker Compose.

### Install Docker

Follow the instruction on the Get Docker page: https://docs.docker.com/get-docker/

### Install Docker Compose

Follow the instruction on the Install Docker Compose page: https://docs.docker.com/compose/install/

# Usage

To start using the **OpenSTEF** reference stack use Docker Compose to bring up the whole stack:

```shell
$ sudo docker-compose up
```

Note: if you're running docker on a windows machine, issues might be caused by windows line endings.
All line endings should be Unix!

## Grafana

Open on http://localhost:3000
Log in using username `admin` and password `admin`

## PhpMyAdmin

Open on http://localhost:8080
Log in using username `root` and password `root`

## Nginx

Open on http://localhost:8090

# Tips and tricks

## Enter running container

To enter the InfluxDB container run:

```shell
$ sudo docker exec -it openstf-influxdb /bin/bash
```

```shell
$ sudo docker exec -it openstf-nginx /bin/bash
```

## Clear the volumes

Docker will try using previous volumes on runs. But sometimes you want to start fresh. Docker-compose offers the `--renew-anon-volumes` option for this purpose:

```
$ docker-compose up --renew-anon-volumes
```

# TODO
Nice-to-haves
* icarus-openstf-api (not included yet)
  * add openstf-dbc (JM is working on it)
  * make icarus-openstf-api opensource
  * add icarus-openstf-api pod
* nginx
  * use a persistent volume to store and share .htmls, which icarus-forecasts later can use to store trained models and reports
* mysql
  * change 'tst_icarus' name of table

## License
This project is licensed under the Mozilla Public License, version 2.0 - see LICENSE for details.

## Licenses third-party libraries
This project includes third-party libraries, which are licensed under their own respective Open-Source licenses. SPDX-License-Identifier headers are used to show which license is applicable. The concerning license files can be found in the LICENSES directory.


## Contributing
Please read [CODE_OF_CONDUCT.md](https://github.com/OpenSTEF/.github/blob/main/CODE_OF_CONDUCT.md), [CONTRIBUTING.md](https://github.com/OpenSTEF/.github/blob/main/CONTRIBUTING.md) and [PROJECT_GOVERNANACE.md](https://github.com/OpenSTEF/.github/blob/main/PROJECT_GOVERNANCE.md) for details on the process for submitting pull requests to us.

## Contact
Please read [SUPPORT.md](https://github.com/OpenSTEF/.github/blob/main/SUPPORT.md) for how to connect and get into contact with the OpenSTEF project
