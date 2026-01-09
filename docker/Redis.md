### 특정값 존재 여부 확인
```
 docker exec tod-redis redis-cli EXISTS ":1:django.contrib.sessions.cacheegn1o1p6pt2mj1irwytnwsi8bunbwtgp"
```
### 특정 값 조회
```
docker exec ksox-redis redis-cli -n 1 GET ':1:django.contrib.sessions.cachev2rofsnuctuf86rduwirbsvsqds3tmuq'
```
