# 안나 카레니나 · 한국어 읽기 배치 작업본

![안나 카레니나 표지](cover.jpg)

레프 톨스토이의 러시아어 원문을 바탕으로 만든 **AI 보조 한국어 번역·읽기 배치 초안**입니다. 전권 8부, 239장의 장별 원고와 HTML 미리보기, 삽화가 들어 있는 EPUB을 보관합니다. 전권 분량은 갖추었지만 전문 번역 교열과 인쇄용 검수는 완료되지 않았습니다. 정확한 인용이나 판매용 판본으로 쓰기 전에는 원문 대조와 교열이 필요합니다.

러시아어 대조 교열자, 한국어 시험 독자, 전자책 편집자와 삽화 검수자의 의견을 받기 위한 작업 공간입니다. 참여 방법은 [CONTRIBUTING.md](CONTRIBUTING.md)에 적었습니다.

## GitHub에서 받기

| 파일 | 내용 |
|---|---|
| [전권 EPUB](안나_카레니나_전권_읽기배치.epub) | 선택한 표지, 239장, 본문 삽화 46장 |
| [전권 원고·제작 자료 ZIP](anna-karenina-sources-2026-10-08.zip) | 8부 239장의 한국어 원고와 HTML, 러시아어 대조본 239장, 제작 코드·기록, 표지 원본 |
| [삽화 JPEG ZIP](anna-karenina-illustrations-jpeg-2026-10-08.zip) | 본문 삽화 46개와 추가 초안 1개 |
| [표지 JPG](cover.jpg) | 사용자가 선택한 그림에 제목과 저자를 조판한 표지 |

GitHub 루트에는 1부 장별 원고와 HTML도 따로 펼쳐 두었습니다. 아래 표의 나머지 상대 경로는 ZIP을 푼 폴더에서 찾을 수 있습니다. 과거 EPUB과 큰 PNG 원본까지 포함한 전체 작업 스냅샷은 로컬 백업으로 보존했습니다.

## 현재 작업물

| 종류 | 위치 | 상태 |
|---|---|---|
| 장별 한국어 편집 원고 | `제*부_제*장.md` | 239장 |
| 장별 웹 미리보기 | `제*부_제*장.html` | 239장 |
| 러시아어 대조 원문 | `russian_chapters/`, `original_manifest.json` | 239장 |
| 삽화 | `illustrations/`, `illustrations.json` | EPUB 반영 46장, 그중 주요 장면 전면 배치 14장 |
| 전권 전자책 | `안나_카레니나_전권_읽기배치.epub` | 239장과 새 표지 수록 |
| 표지 | `cover-art.png`, `cover.jpg` | 원본 그림과 제목을 조판한 완성본 |
| 제작 도구 | `make_cover.py`, `make_preview.py`, `build_sample_epub.py` | 재생성 가능 |
| 이전 작업 기록과 스크립트 | `work-history/` | 이전 기록을 수정 없이 보존 |

이전 시제품과 작업본 EPUB도 로컬 전체 백업에 보관했습니다. 작품명과 저자명은 각 부의 첫 장에만 표시합니다.
삽화는 장의 본문 묶음 사이에 배치하지만 분포는 고르지 않습니다. 1부 35장, 2부 2장, 3부 1장, 4부 2장, 5부 5장, 6부 1장이며 7·8부에는 아직 삽화가 없습니다.

## 재생성

```bash
python3 make_cover.py
python3 make_preview.py
python3 build_sample_epub.py
```

원고·제작 자료 ZIP과 삽화 ZIP을 같은 폴더에 압축 해제한 뒤 실행합니다. `make_cover.py`는 Pillow와 macOS의 AppleMyungjo 글꼴을 사용합니다. 다른 환경에서는 `FONT` 경로를 사용 가능한 한글 명조체로 바꾸어야 합니다. 원고와 삽화 변경 후 EPUB을 다시 빌드하세요.

## 출처와 작업 기록

- 러시아어 원문 목록: https://rvb.ru/tolstoy/anna-karenina.htm
- 제1부부터 제4부: https://rvb.ru/tolstoy/01text/vol_8/0031_1-full.htm
- 제5부부터 제8부: https://rvb.ru/tolstoy/01text/vol_9/0031_2-full.htm
- 삽화의 장면 배치와 검수 원칙: 원고·제작 자료 ZIP 안의 `삽화_작업지침.md`
- 기존 수정 로그: 원고·제작 자료 ZIP 안의 `work-history/README_before_github_2026-10-08.md`, `work-history/초기_작업기록.md`

## 남은 작업

- 주요 장면 20개 계획 중 현재 14개가 전면 삽화로 등록되어 있습니다.
- 장면과 인물 표현, 전체 번역, 실제 전자책 뷰어의 화면 배치를 계속 검수해야 합니다.
- 인쇄용 본문 PDF와 펼친 표지는 아직 제작하지 않았습니다.

2026-10-08 정리: 표지 생성 및 EPUB 반영, 기존 작업 폴더와 기록의 저장소용 사본 구성.
