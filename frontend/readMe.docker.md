READ ME FOR THE DOCKER STUFF

We have 2 docker files here, namely:
    Doeckerfile.dev => For the local development
    Dockerfile  => For production

Build the image and specify the file for local development
    docker build -f Dockerfile.dev .

USING VOLUME WITH DOCKER
    docker run -p 3001:3000 -v /app/node_modules -v $(pwd):/app 9f88979dcdbd

TEST A DOCKER IMAGE
    docker run -it 9f88979dcdbd npm run test


FOR THE DOCKERFILE (NOT THE DEV ONE)
    docker build .
    docker run -p 8080:80 b456c08b60

WHEN DOCKER COMPOSE FILE IS NOT docker-compose.yml,  you will need to pass the -f for the filename, see below
    docker-compose -f docker-compose-dev.yml up
    docker-compose -f docker-compose-dev.yml up --build
    docker-compose -f docker-compose-dev.yml down

