# 제일한의원 (The First Clinic) 공식 웹사이트

GitHub Pages를 활용한 제일한의원 공식 웹사이트 저장소입니다. Jekyll 엔진을 사용하여 정적 사이트로 구성되었습니다.

* **공식 도메인**: [https://thefirst.clinic](https://thefirst.clinic)
* **테스트 URL**: [https://thefirstclinic.github.io](https://thefirstclinic.github.io)

## 로컬 개발 환경 설정 (Local Build)

이 프로젝트는 Ruby와 Jekyll을 기반으로 합니다. 로컬에서 수정 사항을 확인하려면 아래 과정을 따라주세요.

### 1. 사전 요구사항 (Prerequisites)

* **Ruby**: 3.0 이상 버전 설치 필수 (Windows는 Ruby+Devkit 권장)
* **Bundler**: Ruby 패키지 관리 도구

#### A. Ruby 설치 (Windows 기준)

1. [RubyInstaller 공식 사이트](https://rubyinstaller.org/downloads/)에 접속합니다.
2. **Ruby+Devkit 3.x (x64)** 버전을 다운로드하여 설치합니다.
3. 설치 중 **'Add Ruby executables to your PATH'** 옵션을 반드시 체크하세요.
4. 설치 마지막 단계에서 `ridk install` 창이 뜨면, **1, 2, 3**을 차례로 입력하여 필수 MSYS2 구성 요소를 설치합니다.

#### B. Bundler 및 Jekyll 설치

Ruby 설치가 끝났다면, 새 터미널(PowerShell 또는 CMD)을 열고 아래 명령어를 입력하여 빌드 도구들을 설치합니다.

```bash
# gem을 통해 bundler와 jekyll을 전역 설치합니다.
gem install jekyll bundler
```

### 2. 프로젝트 의존성 설치

프로젝트 루트 폴더(thefirstclinic.github.io)로 이동한 뒤, 프로젝트에 필요한 정확한 라이브러리 버전들을 설치합니다.

```bash
# Gemfile에 명시된 패키지들을 로컬에 설치합니다.
bundle install
```

만약 webrick 관련 에러가 발생한다면 bundle add webrick을 실행해 주세요.

### 3. 로컬 서버 실행 및 빌드

모든 설정이 완료되었습니다. 이제 아래 명령어로 사이트를 빌드하고 미리 볼 수 있습니다.

```bash
# 로컬 서버 구동
bundle exec jekyll serve
```

- 서버 실행 후 브라우저에서 http://127.0.0.1:4000 주소로 접속하세요.
- 파일 수정 시 자동으로 다시 빌드되며, 브라우저 새로고침을 통해 결과를 확인할 수 있습니다.

## 프로젝트 구조

- _includes/: Header, Footer, Kakao Map 등 공통 UI 컴포넌트
- _layouts/: 페이지 기본 템플릿
- _site/: 빌드된 최종 결과물 (Git 추적 제외)
- assets/: 이미지, 스타일시트(CSS), 자바스크립트(JS)
- index.html: 메인 랜딩 페이지 콘텐츠

## 주의사항

- .gitignore: _site, .jekyll-cache, .bundle 등 빌드 과정에서 생성되는 임시 파일들은 Git 저장소에 포함되지 않도록 설정되어 있습니다.
- 경로 문제: 배포 후 이미지나 CSS가 깨진다면 _config.yml의 url과 baseurl 값이 저장소 이름과 일치하는지 확인하세요.
- 포트 충돌: 만약 4000번 포트가 이미 사용 중이라면 bundle exec jekyll serve --port 4001과 같이 포트를 변경할 수 있습니다.

© 2026 The First Clinic of Korean Medicine 제일한의원


