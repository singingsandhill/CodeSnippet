
## nginx 설정 관련 명령어

```bash
# 설정 파일 문법 검사만 (오류만 표시)
nginx -t

# 설정 파일 문법 검사 + 전체 설정 내용 출력
nginx -T
```

**차이점:**
- `nginx -t`: 문법 오류가 있으면 오류 메시지만 표시
- `nginx -T`: 문법 검사 + 모든 설정 파일 내용을 합쳐서 출력 (디버깅용)

## nginx 서비스 관리 명령어

```bash
# nginx 상태 확인
systemctl status nginx
systemctl status nginx -l ## 생략없이 전체 출력

# nginx 시작
systemctl start nginx

# nginx 중지
systemctl stop nginx

# nginx 재시작 (완전 중지 후 시작)
systemctl restart nginx

# nginx 설정 재로드 (무중단, 권장)
systemctl reload nginx
```

## 추가 유용한 명령어

```bash
# nginx 활성화 (부팅 시 자동 시작)
systemctl enable nginx

# nginx 비활성화
systemctl disable nginx

# nginx 실행 여부만 확인
systemctl is-active nginx

# nginx 자동시작 설정 여부 확인
systemctl is-enabled nginx

# 전체 설정 파일 경로 확인
nginx -T | grep "# configuration file"

# nginx 버전 확인
nginx -v
nginx -V  # 상세 정보 포함
```

## 실무에서 자주 사용하는 조합

```bash
# 1. 설정 변경 후 안전하게 적용
nginx -t && systemctl reload nginx

# 2. 문제 발생 시 재시작
nginx -t && systemctl restart nginx

# 3. 현재 로드된 전체 설정 확인 (디버깅)
nginx -T | less

# 4. 설정 파일 위치와 문법 확인
nginx -t -c /etc/nginx/nginx.conf
```

**권장사항:** 설정 변경 후에는 항상 `nginx -t`로 문법 검사를 먼저 하고, `reload`를 사용하는 것이 안전합니다.

### 실패 로그 확인 명령어
```
tail -f /var/log/nginx/error.log
```
