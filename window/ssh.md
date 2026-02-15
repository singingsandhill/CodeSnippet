### ssh 접속
```
ssh -p 2222 user@host                 # SSH 포트가 2222 등으로 바뀐 서버에 접속 (-p로 포트 지정)
```
### ssh 파일 전송
```
scp .\file.txt user@host:/tmp/        # 로컬 파일을 원격 /tmp/로 업로드 (윈도우 경로는 .\ 사용 가능)
```
