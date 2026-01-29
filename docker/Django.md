<img width="426" height="23" alt="image" src="https://github.com/user-attachments/assets/586af212-fded-4652-839d-239aec9545f6" />### DRF Swagger 유효성 검사
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
```
