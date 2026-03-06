### 형상관리 되고 있는 파일 추적 중지
```
# .gitignore에 먼저 추가

# Git 인덱스에서만 제거(=로컬 파일은 남김)
git rm --cached path/to/file
git rm -r --cached path/to/dir/

# 커밋 & 푸시
git add .gitignore
git commit -m "Stop tracking ignored files"
git push
```
