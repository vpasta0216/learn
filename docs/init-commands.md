# init 명령어 총정리

---

## 1. `git init`

**Git 저장소 초기화** - 버전 관리 시작

```bash
# 현재 폴더를 Git 저장소로 만들기
git init

# 결과: .git/ 폴더 생성
```

| 언제 사용 | 새 프로젝트에서 Git 버전 관리 시작할 때 |
|----------|----------------------------------------|
| 실행 위치 | 프로젝트 루트 폴더 |
| 결과물 | `.git/` 폴더 (숨김) |

---

## 2. `/starter init`

**bkit 스킬로 웹 프로젝트 생성** - Claude Code 전용

```bash
# Claude Code 실행 후
/starter init my-portfolio
```

| 언제 사용 | 정적 웹사이트 프로젝트 시작할 때 |
|----------|--------------------------------|
| 실행 위치 | Claude Code 안에서 |
| 결과물 | 폴더 구조, 기본 파일들 자동 생성 |

### 생성되는 구조 (HTML/CSS 선택 시)

```
my-portfolio/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
├── docs/
│   ├── 01-plan/
│   └── 02-design/
└── CLAUDE.md
```

---

## 3. `npm init`

**Node.js 프로젝트 초기화** - package.json 생성

```bash
# 대화형 (질문에 답하며 설정)
npm init

# 기본값으로 바로 생성
npm init -y
```

| 언제 사용 | JavaScript/TypeScript 프로젝트 시작할 때 |
|----------|----------------------------------------|
| 실행 위치 | 터미널 (프로젝트 폴더) |
| 결과물 | `package.json` 파일 |

### package.json 예시

```json
{
  "name": "my-project",
  "version": "1.0.0",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  }
}
```

---

## 4. 기타 init 명령어

| 명령어 | 용도 |
|--------|------|
| `npx create-next-app` | Next.js 프로젝트 생성 |
| `npx create-react-app` | React 프로젝트 생성 |
| `pnpm init` | pnpm으로 프로젝트 초기화 |
| `yarn init` | yarn으로 프로젝트 초기화 |

---

## 비교 요약

| 명령어 | 목적 | 결과물 |
|--------|------|--------|
| `git init` | 버전 관리 | `.git/` |
| `/starter init` | 웹 프로젝트 템플릿 | 전체 폴더 구조 |
| `npm init` | Node.js 설정 | `package.json` |

---

## 새 프로젝트 시작 순서 (권장)

```bash
# 1. 폴더 생성 & 이동
mkdir my-project
cd my-project

# 2. Claude Code 실행
claude

# 3. 프로젝트 초기화 (Claude 안에서)
/starter init

# 4. Git 초기화 (Claude 안에서 또는 터미널)
git init

# 5. 첫 커밋
git add .
git commit -m "초기화: 프로젝트 생성"
```
