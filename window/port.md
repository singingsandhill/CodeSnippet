윈도우에서 **특정 포트**를 사용 중인 **프로세스(PID)** 를 확인하고 종료하는 명령어

---

### 특정 포트의 PID 확인

```bash
netstat -ano | findstr :8080
```

---

### 해당 PID 종료 (프로세스 강제 종료)

```bash
taskkill /PID 12345 /F
```

* `/F` 옵션은 **강제 종료(Force)** 의미.

---

###  한 줄로 확인 & 종료 (파이프 활용)

```bash
for /f "tokens=5" %a in ('netstat -ano ^| findstr :8080') do taskkill /PID %a /F
```

