### 방화벽 확인
```
timeout 5 bash -c '</dev/tcp/DB URL/포트 번호' && echo "연결 성공" || echo "연결 실패"
```
