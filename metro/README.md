# 서울 지하철 — 홈 화면 앱 설치

폴더 안의 파일 전체를 GitHub 저장소 `dreroica/tide` 의 `metro` 폴더에 올린 뒤,
휴대폰 브라우저로 열어 홈 화면에 추가하면 아이콘이 생깁니다.

## 1. 파일 올리기

저장소에 `metro` 폴더를 만들고 아래 파일을 그대로 넣습니다.

```
metro/
  index.html
  manifest.webmanifest
  sw.js
  icon-180.png
  icon-192.png
  icon-512.png
  icon-maskable-512.png
  favicon-32.png
```

GitHub 웹에서 하는 방법: 저장소 → **Add file → Upload files** → 파일 8개를 끌어다 놓고,
파일 이름 칸 맨 앞에 `metro/` 를 붙인 뒤 **Commit changes**.

## 2. GitHub Pages 켜기

저장소 → **Settings → Pages** → Source 를 `Deploy from a branch`,
Branch 를 `main` / `/(root)` 으로 두고 저장합니다.
1~2분 뒤 아래 주소가 열립니다.

```
https://dreroica.github.io/tide/metro/
```

## 3. 홈 화면에 추가

**아이폰 (Safari)**
1. Safari 로 위 주소를 엽니다 (크롬 아님 — Safari 여야 합니다)
2. 아래쪽 **공유** 버튼 → **홈 화면에 추가**
3. 이름이 `서울 지하철` 로 나오는지 확인하고 **추가**

**안드로이드 (Chrome)**
1. Chrome 으로 위 주소를 엽니다
2. 우측 상단 **⋮** → **홈 화면에 추가** (또는 화면에 뜨는 설치 배너)
3. **설치**

주소창 없이 전체 화면으로 열리고, 한 번 연 뒤에는 인터넷이 끊겨도 동작합니다.

## 내용 수정 후

`index.html` 을 고쳐 올렸는데 앱에 반영되지 않으면 `sw.js` 의
`const CACHE = "seoul-metro-v1"` 을 `v2`, `v3` … 으로 올려 주세요.
