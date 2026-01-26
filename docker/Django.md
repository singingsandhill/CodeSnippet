### DRF Swagger 유효성 검사
```
docker exec ksox-ai-be-local python manage.py spectacular --validate
```
### DRF Swagger 문서 저장
```
docker exec ksox-ai-be-local python manage.py spectacular --format openapi-json --file schema.json
```
