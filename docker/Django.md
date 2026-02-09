### DRF Swagger 유효성 검사
```
docker exec ksox-ai-be-local python manage.py spectacular --validate
```
### DRF Swagger 문서 저장
```
docker exec ksox-ai-be-local python manage.py spectacular --format openapi-json --file schema.json
```
### 주입된 환경변수 확인
```
docker exec -it ksox-ai-be printenv DB_ENGINE
docker exec ksox-ai-be-local env | sort
```
### test 코드 실행
```
 docker exec ksox-ai-be-local python manage.py test --verbosity=2
```
### 문법 검사
```
docker exec -it ksox-ai-be-local python -m compileall -q .
```
