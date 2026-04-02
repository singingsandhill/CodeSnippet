<img width="518" height="19" alt="image" src="https://github.com/user-attachments/assets/8e03e250-87aa-4708-b903-4708b0f6bf05" />### 특정값 존재 여부 확인
```
 docker exec tod-redis redis-cli EXISTS ":1:django.contrib.sessions.cacheegn1o1p6pt2mj1irwytnwsi8bunbwtgp"
```
### 특정 값 조회
```
docker exec ksox-redis redis-cli -n 1 GET ':1:django.contrib.sessions.cachev2rofsnuctuf86rduwirbsvsqds3tmuq'
```
### 영구저장 옵션 활성화 확인
```
docker exec ksox-redis-local redis-cli CONFIG GET save
```
