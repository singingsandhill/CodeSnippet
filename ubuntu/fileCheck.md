#### 특정 파일 경로 찾기
```
find / -name "prometheus.yml" 2>/dev/null
grep -R "server_name ksoxai-sandbox.pwc.kr" -n /etc/nginx
```
#### 용량이 큰 파일 찾기 (100M 이상)
```
find / -type f -size +100M 2>/dev/null
```
