### 개발용 Compose 실행 (백그라운드 + 빌드)
```
docker compose -f docker-compose.dev.yml up -d --build
```
### 컨테이너 목록 확인
```
docker ps 
```
### 컨테이너 상세(포트/볼륨/Env/네트워크)
```
docker inspect tod-ai-be
```
### 컨테이너 재시작
```
docker restart tod-ai-be   
```
### 실시간 로그 확인
```
docker logs -f tod-ai-be
```
### Compose 중단
```
docker compose -f docker-compose.dev.yml down
```
```
docker stop $(docker ps -q)
```
### 특정 이미지로 실행 중인 컨테이너 정지
```
docker ps -q --filter ancestor=<이미지이름> | xargs -r docker stop
```
### 해당 이미지 기반 컨테이너 삭제
```
docker ps -a -q --filter ancestor=<이미지이름> | xargs -r docker rm
```
### 이미지 삭제 (강제 삭제 포함)
```
docker rmi -f <이미지이름>
```
