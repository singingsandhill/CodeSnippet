
### 이미지 삭제 (강제 삭제 포함)
```
docker rmi -f <이미지이름>
```

### 특정 시간 로그 검색
```
 docker logs --since "2025-11-03T04:40:00" --until "2025-11-03T04:59:00" ksox-ai-be
```

 ### 특정 이미지 빌드, 생성 시간 확인
 ```
docker image inspect 이미지명 --format='{{.Created}}'
```

### 웹 어플리케이션 스웨거 문서 추출
```
docker exec ksox-ai-be-local python manage.py spectacular --file schema.json
```
