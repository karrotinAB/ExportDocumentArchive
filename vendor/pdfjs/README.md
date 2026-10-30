# pdf.js (로컬 복사본)

- 출처: `pdfjs-dist@3.11.174` (Mozilla, Apache-2.0 — `LICENSE` 참고)
- `pdf.min.js`, `pdf.worker.min.js`: `legacy/build`의 UMD 빌드. `<script>`로 불러와서
  워커 없이 메인 스레드에서 돌린다 (file://로 열어도 동작하게).
- `cmaps/*.js`: `cmaps/*.bcmap`을 base64로 감싼 파일. 한글·중국어·일본어 글꼴 PDF의 글자를 읽을 때
  필요한 것만 그때그때 `<script>`로 불러온다 (file://에서는 fetch가 막혀서 이렇게 함).
- 외부 네트워크 요청 없음. 버전을 바꾸면 4.x부터는 ES 모듈만 있어서 이 방식이 안 되니 3.x를 유지할 것.
