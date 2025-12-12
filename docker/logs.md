### 특정 시간대의 특정 레벨의 로그만 보기
```
docker logs --since "2025-11-20T09:35:00" --until "2025-11-20T09:40:00" ksox-ai-be 2>&1 | grep -iE '\b(err(or)?|warn(ing)?)\b'
```
### 문자열 검색
```
 docker logs tod-ai-be 2>&1 | grep "CID:b6a306d5"
```
