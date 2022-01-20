# [Redis](https://redis.io/ "Redis")

##### Before

To use the following project first make sure you have installed [Docker](https://docs.docker.com/get-docker/ "Docker").

##### Verify Installation

In a terminal type the following command `docker --version`, then enter. The result should be like the following example `Docker version 20.10.10, build b485636`.

Note: The result will be the same or different depending on the version you have installed.

##### Setting

To not lose the data every time the container is started **[Redis](https://redis.io/ "Redis")** it is recommended to configure the file `docker-compose.yml` as follows:

    version: '3'
    
    services:
      rs01:
        image: redis
        ports:
          - "6379:6379"
        volumes:
          - folder_path/redis.conf:/usr/local/etc/redis/redis.conf
          - folder_path/data:/data

Note: The value of **"folder_path"** should be the path where the **[Redis](https://redis.io/ "Redis")** **"configuration"**and**"data"**files will be stored.

##### Execution commands
- To run the container:

`docker-compose up --build -d`

- To stop the container: 

`docker-compose down`

## Authors

- [@dj.pablo.ac](https://gitlab.com/dj.pablo.ac)

## Licencia

[MIT](https://choosealicense.com/licenses/mit/)