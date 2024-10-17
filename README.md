# Apache Nutch Docker Setup

This repository contains a simple setup for running Apache Nutch using Docker and Docker Compose.

## Prerequisites

- Docker installed on your machine.
- Docker Compose installed.

## Setup Instructions

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/azmisahin-test/apache-nutch-docker-setup.git
    cd apache-nutch-docker-setup
    ```

2. Start the Docker containers using Docker Compose:

    ```bash
    docker-compose up -d
    ```

3. Check the status of the containers:

    ```bash
    docker-compose ps
    ```

4. Access the Nutch container to run commands:

    ```bash
    docker exec -it nutch /bin/bash
    ```

5. To crawl a website, run the following command inside the Nutch container:

    ```bash
    /opt/nutch/runtime/local/bin/nutch crawl urls -depth 3 -topN 50
    ```

6. To stop the containers, run:

    ```bash
    docker-compose down
    ```

## Additional Notes

- You can customize the `docker-compose.yml` file to add more services or modify configurations as needed.
- The crawled data will be stored in the mounted volume.

Enjoy using Apache Nutch!
