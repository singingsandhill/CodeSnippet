#### 1. 특정 디렉토리 내 SQL Anywhere 관련 폴더 검색 (/opt, /usr, /var 경로에서 'sqlany' 이름을 가진 디렉토리 검색 (최대 깊이 3))
find /opt /usr /var -maxdepth 3 -type d -iname 'sqlany'

#### 2. 설치된 패키지 확인 (dpkg 패키지 목록에서 'sqlany', 'sql anywhere', 'sybase' 관련 항목 검색)
dpkg -l | grep -i -E 'sqlany|sql anywhere|sybase'
