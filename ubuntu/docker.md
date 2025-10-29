
docker compose -f docker-compose.dev.yml up -d --build

docker ps 

docker restart tod-ai-be   

docker logs -f tod-ai-be

docker compose -f docker-compose.dev.yml down
