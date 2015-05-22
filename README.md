# flipendo-env

Use this repository for development and test of Flipendo.  
It uses docker compose to set up the whole architecture of flipendo on your machine.

# Dependencies

You will need to install docker and docker-compose.

# Install

Run these commands:

```bash
git clone git@github.com:flipendo/flipendo-env
cd flipendo-env
git submodule init ; git submodule update
docker-compose up
```

docker-compose will run every component in a docker container and will link them together.
Here are the containers that will be run:

  - **flipendo-api**: The API of Flipendo.
  - **flipendo-website**: The website of Flipendo.
  - **flipendo-worker**: The worker that will split and transcode your video files.
  - **rabbitmq**: The message broker used by the API and the worker to communicate.
