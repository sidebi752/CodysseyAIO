<<<<<<< HEAD
# First Project

## 1. 프로젝트 개요
(절대 경로와 상대 경로의 차이를 예시를 들어 설명할 수 있다.
파일 권한의 의미(r/w/x)와 755, 644 같은 표기가 어떤 규칙으로 해석되는지 설명할 수 있다.
기존 Dockerfile을 기반으로 “커스텀 이미지”를 만들 수 있다.
포트 매핑이 필요한 이유를 설명할 수 있다.
Docker 볼륨(영속 데이터)을 설명할 수 있다.
Git과 GitHub의 역할 차이(로컬 버전관리 vs 원격 협업 플랫폼)를 설명할 수 있다.약)


## 2. 실행 환경

### 💻 OS
- macOS Sonoma 14.x (또는 Windows 11 / Ubuntu 22.04 등)

### 🐳 Docker
\`\`\`bash
$ docker --version
Docker version 29.9.2, build a82e528

\`\`\`bash
$ docker info
(Client:
 Version:    29.9.2
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  agent: Docker AI Agent Runner (Docker Inc.)
    Version:  v1.152.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-agent.exe
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.33.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-ai.exe
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.38.1
    Path:     C:\Users\User\.docker\cli-plugins\docker-buildx.exe
  compose: Docker Compose (Docker Inc.)
    Version:  v5.6.1
    Path:     C:\Users\User\.docker\cli-plugins\docker-compose.exe
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.49.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-debug.exe
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  4.97.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-desktop.exe
  dhi: CLI for managing Docker Hardened Images (Docker Inc.)
    Version:  v0.0.9
    Path:     C:\Users\User\.docker\cli-plugins\docker-dhi.exe
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.32
    Path:     C:\Users\User\.docker\cli-plugins\docker-extension.exe
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.1
    Path:     C:\Users\User\.docker\cli-plugins\docker-init.exe
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.44.2
    Path:     C:\Users\User\.docker\cli-plugins\docker-mcp.exe
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.2.9
    Path:     C:\Users\User\.docker\cli-plugins\docker-model.exe
  offload: Docker Offload (Docker Inc.)
    Version:  v0.7.21
    Path:     C:\Users\User\.docker\cli-plugins\docker-offload.exe
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.3.2
    Path:     C:\Users\User\.docker\cli-plugins\docker-pass.exe
  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)
    Version:  v0.13.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-sandbox.exe
  scout: Docker Scout (Docker Inc.)
    Version:  v1.27.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-scout.exe

Server:
 Containers: 0
  Running: 0
  Paused: 0
  Stopped: 0
 Images: 0
 Server Version: 29.9.2
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: local
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Discovered Devices:
  cdi: docker.com/gpu=webgpu
 Swarm: inactive
 Runtimes: runc io.containerd.runc.v2 nvidia
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: b7a25261e029d68978bbf290df0a62fc819b3c51
 runc version: v1.5.2-0-g29dd3dc2
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.18.54.1-microsoft-standard-WSL2
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64
 CPUs: 8
 Total Memory: 7.605GiB
 Name: docker-desktop
 ID: 639f6308-1387-4528-b98e-f6835b874f9e
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 HTTP Proxy: http.docker.internal:3128
 HTTPS Proxy: http.docker.internal:3128
 No Proxy: hubproxy.docker.internal
 Labels:
  com.docker.desktop.address=npipe://\\.\pipe\docker_cli
 Experimental: false
 Insecure Registries:
  hubproxy.docker.internal:5555
  127.0.0.0/8
  ::1/128
 Live Restore Enabled: false
 Firewall Backend: iptables)


### 🌿 Git
\`\`\`bash
$ git --version
git version 2.56.0.windows.4

$ git config --global user.name
si***

$ git config --global user.email
si***@gmail.com)

## 3. 수행 항목 체크리스트
### 🐳 Docker 환경
- [o] Docker Desktop 설치
- [o] Docker 버전 확인 (`docker --version`)
- [o] Docker 시스템 정보 확인 (`docker info`)

### 📦 웹서버 컨테이너
- [ ] 웹서버 소스코드 작성 (`app/index.html`)
- [ ] Dockerfile 작성
- [ ] 이미지 빌드 (`docker build`)
- [ ] 컨테이너 실행 (`docker run`)

### 🔌 포트 매핑
- [ ] `-p 8080:80` 옵션으로 실행
- [ ] 브라우저에서 `localhost:8080` 접속 확인
- [ ] 접속 화면 스크린샷 캡처

### 📁 바인드 마운트
- [ ] `-v` 옵션으로 호스트 폴더 마운트
- [ ] 호스트에서 파일 수정 → 컨테이너 반영 확인
- [ ] 변경 전/후 스크린샷

### 💾 볼륨 영속성
- [ ] Docker 볼륨 생성 (`docker volume create`)
- [ ] 컨테이너에 볼륨 연결
- [ ] 컨테이너 삭제 후 데이터 유지 확인

### 🌿 Git & GitHub
- [o] Git 사용자 정보 설정
- [o] 로컬 저장소 초기화 (`git init`)
- [o] GitHub 저장소 생성
- [o] 원격 저장소 연결 (`git remote add`)
- [o] VSCode에서 GitHub 로그인
- [ ] 첫 푸시 완료 (`git push`)

## 4. 검증 방법
(명령어와 결과)

## 5. 트러블슈팅
### 문제 1
**증상:**
\`\`\`
Docker Desktop requires the "Virtual Machine Platform" 
Windows feature, which is not enabled on this machine.
\`\`\`

**원인:**
- WSL2 실행에 필요한 "Virtual Machine Platform" 기능 비활성화
- 일반 사용자 권한으로는 활성화 불가

**해결:**
1. 관리자 PowerShell에서 `wsl --install` 실행
2. 컴퓨터 재부팅
3. Docker Desktop 재설치 (All-users installation 선택)

**교훈:**
- Docker는 WSL2 기반이라 Windows 시스템 설정 변경 필요
- 공용 PC에서는 관리자 승인 필수

### 문제 2

## 6. Git & GitHub 연동 과정

### 6-1. Git 사용자 설정

\```bash
$ git config --global user.name "si***"
$ git config --global user.email "si***@gmail.com"
\```

**설정 확인:**
\```bash
$ git config --global user.name
si***

$ git config --global user.email
si***@gmail.com
\```

### 6-2. 로컬 저장소 초기화

\```bash
$ cd si-docker-project
$ git init
Initialized empty Git repository in C:/.../si-docker-project/.git/

$ git branch -M main
\```

### 6-3. GitHub 저장소 생성

![GitHub 저장소 생성](images/github-create-repo.png)
> 📸 GitHub에서 "New repository" 버튼으로 생성한 화면

### 6-4. VSCode에서 GitHub 로그인

1. `Ctrl+Shift+P` → "Sign in to GitHub" 입력
2. 브라우저에서 인증 완료
3. VSCode 좌측 하단에 GitHub 계정명 표시 확인

![VSCode GitHub 로그인](images/vscode-github-login.png)

### 6-5. 원격 저장소 연결 & 첫 푸시

\```bash
$ git remote add origin https://github.com/si***/CodysseyAIO.git

$ git remote -v
origin  https://github.com/si***/CodysseyAIO.git (fetch)
origin  https://github.com/si***/CodysseyAIO.git (push)

$ git add .
$ git commit -m "Initial commit: README 작성 시작"
$ git push -u origin main
\```

### 6-6. GitHub에 반영 확인

![GitHub 푸시 완료](images/github-pushed.png)
> 📸 GitHub 저장소에 README가 올라온 화면
=======
# CodysseyAIO
codyssey rookie_mariner
>>>>>>> 2114af0be5a3b6a24c35ac46a863e6d3590533a3
