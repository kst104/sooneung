# sooneung

2027학년도 수능 영어 독해 연습 세트 (D-23 달력, 날짜별 9문항 세트, 타이머·채점·해설).
서버나 빌드 없이 브라우저만으로 동작하는 정적 HTML입니다. 풀이 결과는 브라우저 localStorage에만 저장됩니다.

## 실행

**웹 (GitHub Pages)**: 저장소 Settings → Pages → Build and deployment에서 Source를 `Deploy from a branch`, Branch를 `main` / `/ (root)`로 저장합니다. 몇 분 뒤 `https://kst104.github.io/sooneung/` 에서 열립니다 (첫 화면이 `수능영어/index.html`로 이동합니다).

**내 컴퓨터**: `수능영어/index.html`을 브라우저로 바로 열면 됩니다. 로컬 서버로 열려면:

```sh
python3 -m http.server 8000
# http://localhost:8000/ 접속
```

## 세트 관리 도구 (Node.js 필요)

`수능영어` 폴더에서 실행합니다. 자세한 규칙은 `수능영어/NOTES.md`, `수능영어/assets/SET-FORMAT.md`.

```sh
node tools/validate.js --all     # 모든 세트 형식 검증
node tools/build-lessons.js      # assets/plan.js 기준으로 lessons/*.html 다시 생성
```
