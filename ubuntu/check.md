### 방화벽 확인
```
sudo ufw status                        # UFW 방화벽 상태/허용 규칙 확인

timeout 5 bash -c '</dev/tcp/DB URL/포트 번호' && echo "연결 성공" || echo "연결 실패"
```

### IP 확인
```
hostname -I
```

### 네트워크 확인
```
ip a                                   # 네트워크 인터페이스/주소 상세 확인
```

### 서비스/로그(systemd)
```
sudo systemctl status <service>        # 서비스 현재 상태 확인(실행 중/중지, 최근 로그 일부, PID, 활성화 여부)

sudo systemctl enable <service>        # 부팅 시 자동 시작 설정(즉시 시작은 아님)
```

### 로그
```
sudo journalctl -u <service> -n 200 --no-pager  # 해당 서비스 로그 최근 200줄 출력(페이지 없이)
```
