<img src="https://cloud.githubusercontent.com/assets/668093/12567089/0ac42774-c372-11e5-97eb-00baf0fccc37.jpg" alt="OpenMRS"/>

# OpenMRS Platform MySQL Docker

> Docker containers for [OpenMRS](http://openmrs.org) Platform MySQL

This repository contains the necessary code to create Docker containers that start an instance
of the OpenMRS Platform MySQL database.

For more information about the OpenMRS Platform visit [openmrs.org](http://www.openmrs.org/).

## Prerequisites

Make sure you have [Docker](https://docs.docker.com/) installed.

## Setup
You need to have the Docker image locally in order to run it.

You can either build it yourself or pull it from the :cloud:

Please follow the appropriate section below.

### Build
Start by cloning this repository:

```
git clone https://github.com/teleivo/docker-openmrs-platform-mysql.git
```

Enter the directory and build the image:

```
cd docker-openmrs-platform-mysql
docker build --tag openmrs-platform-mysql .
```

### Pull
The Docker image is hosted on [Docker Hub](https://hub.docker.com/r/teleivo/openmrs-platform-mysql/)

You can pull via
```
docker pull teleivo/openmrs-platform-mysql
```

### Run
Ensure you built or pulled the image first.

Run an instance of the image (OpenMRS Platform database):

```
docker run -d openmrs-platform-mysql -p 3306:3306 docker-openmrs-platform-mysql --name openmrsdb \
    -e MYSQL_ROOT_PASSWORD="root" \
    -e MYSQL_USER="openmrs" \
    -e MYSQL_PASSWORD="openmrs" \
    -e MYSQL_DATABASE="openmrs"
```

### List
If you want to find your image list all images and look for your tag:

```
docker images
```

## License

[MPL 2.0 w/ HD](http://openmrs.org/license/) © [OpenMRS Inc.](http://www.openmrs.org/)
