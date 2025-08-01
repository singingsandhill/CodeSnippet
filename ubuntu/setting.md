# Install
## Docker
### ✅ 1단계: 기존 Docker 제거 (이미 설치된 경우)
```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

### ✅ 2단계: 패키지 업데이트 및 필수 패키지 설치

```bash
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

### ✅ 3단계: Docker 공식 GPG 키 추가

```bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

### ✅ 4단계: Docker 저장소 등록

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) \
  signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### ✅ 5단계: 패키지 목록 업데이트 및 Docker 설치

```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### ✅ 6단계: Docker 설치 확인

```bash
sudo docker --version
```

예시 출력:

```
Docker version 24.0.5, build ced0996
```

### ✅ 7단계: (선택) sudo 없이 Docker 명령어 사용

```bash
sudo usermod -aG docker $USER
newgrp docker
```

### ✅ 8단계: 설치 테스트

```bash
docker run hello-world
```
