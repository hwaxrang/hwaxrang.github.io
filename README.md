# Hwarang Kwon Personal Site

`main_cv.pdf` 내용을 바탕으로 만든 정적 개인 페이지입니다. 레이아웃은 `https://kminsalgorithm.github.io/`의 좌측 프로필 패널 + 우측 스크롤 콘텐츠 구조를 참고했고, 연구자 포트폴리오에 맞게 타이포그래피와 카드형 섹션으로 재구성했습니다.

## 파일 구성

- `index.html`: 메인 페이지
- `styles.css`: 전체 스타일
- `assets/profile-mark.svg`: 프로필 이미지 대신 사용하는 모노그램 그래픽
- `main_cv.pdf`: 다운로드용 CV

## 로컬에서 확인

`personal-site` 디렉터리에서 아래 둘 중 하나를 실행하면 됩니다.

```bash
python3 -m http.server 8000
```

또는 VS Code Live Server를 사용해도 됩니다.

브라우저에서 `http://localhost:8000`으로 접속합니다.

## GitHub Pages로 배포하는 가장 쉬운 방법

참조 링크처럼 `https://사용자이름.github.io/` 형태로 배포하려면 **저장소 이름을 정확히 `사용자이름.github.io`로 만들어야 합니다.**

예시:

- GitHub 아이디가 `hwaxrang`이면 저장소 이름은 `hwaxrang.github.io`
- 배포 URL은 `https://hwaxrang.github.io/`

## 배포 절차

1. GitHub에서 새 public repository를 생성합니다.
   저장소 이름: `hwaxrang.github.io`

2. 새 저장소를 로컬에 clone 합니다.

```bash
git clone https://github.com/hwaxrang/hwaxrang.github.io.git
cd hwaxrang.github.io
```

3. 현재 작업물(`personal-site` 내부 파일들)을 저장소 루트로 복사합니다.

복사해야 하는 파일:

- `index.html`
- `styles.css`
- `assets/`
- `main_cv.pdf`

4. commit 후 push 합니다.

```bash
git add .
git commit -m "Add academic personal page"
git push origin main
```

5. GitHub 저장소에서 `Settings > Pages`로 이동합니다.

- `Build and deployment`
- `Source`: `Deploy from a branch`
- `Branch`: `main` / `/ (root)`

6. 잠시 기다리면 `https://hwaxrang.github.io/`에서 바로 열립니다.

## 이미 다른 저장소 이름을 쓰고 싶다면

예를 들어 저장소 이름이 `personal-page`라면 URL은 아래처럼 됩니다.

`https://hwaxrang.github.io/personal-page/`

이 경우 참조 링크와 같은 루트 URL 형태가 아니므로, 참조 링크처럼 보이게 하려면 `hwaxrang.github.io` 저장소 방식을 쓰는 것이 맞습니다.

## 배포 후 수정 포인트

- 프로필 사진을 쓰고 싶으면 `assets/profile-mark.svg` 대신 실제 이미지 파일로 교체
- 논문 링크가 생기면 `index.html`의 Research 카드에 DOI 또는 PDF 링크 추가
- 뉴스 섹션을 더 자주 갱신하고 싶으면 `Highlights`를 `News`로 바꿔 월별 업데이트 추가
- Google Search 노출을 원하면 `favicon`, `og:image`, `sitemap` 추가
