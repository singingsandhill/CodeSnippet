
docker compose -f docker-compose.dev.yml up -d --build

docker ps 

docker restart tod-ai-be   

docker logs -f tod-ai-be

docker compose -f docker-compose.dev.yml down

======== 정리 ========
# 1. 실행 중인 컨테이너 확인
docker ps

# 2. 특정 이미지로 실행 중인 컨테이너 모두 정지
docker ps -q --filter ancestor=<이미지이름> | xargs -r docker stop

# 3. 해당 이미지 기반의 모든 컨테이너 삭제
docker ps -a -q --filter ancestor=<이미지이름> | xargs -r docker rm

# 4. 이미지 삭제 (강제 삭제 옵션 포함)
docker rmi -f <이미지이름>
