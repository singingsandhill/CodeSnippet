### 특정 시간대의 특정 레벨의 로그만 보기
```
docker logs --since "2025-11-20T09:35:00" --until "2025-11-20T09:40:00" ksox-ai-be 2>&1 | grep -iE '\b(err(or)?|warn(ing)?)\b'
```
### 특정 문자열을 포함한 로그 검색
```
 docker logs tod-ai-be 2>&1 | grep "CID:b6a306d5"
```
### 특정 조건의 제한된 줄만 확인 (앞에서 50개)
```
docker logs tod-ai-be 2>&1 | grep -a "8ac9c551" | head -n 50
```
### Redis Docker 이미지 Session 조회
```
docker exec tod-redis redis-cli GET ":1:django.contrib.sessions.cacheegn1o1p6pt2mj1irwytnwsi8bunbwtgp"
```
### Redis Docker 이미지 키 검색
```
docker exec tod-redis redis-cli KEYS ":1:django.contrib.sessions.cache*"
```
