# opensamguk-images

[opensamguk](https://github.com/peppone-choi/opensamguk) 게임이 실제로 쓰는 이미지만 둔다.
원화·생성기·검수 자료는 두지 않는다 (필요하면 이 저장소의 Git 히스토리에서 찾는다).

## 경로

| 경로 | 형식 | 크기 | 쓰는 곳 |
| ---- | ---- | ---- | ------- |
| `portraits/portrait/<id>.png` | PNG | 148×210 | 장수 정보 |
| `portraits/icon/<id>.webp` | WebP | 96×96 | 목록·지도 |
| `portraits/thumb/<id>.webp` | WebP | 48×68 | 작은 표시 |
| `portraits/registry.tsv` | TSV | — | ID ↔ 한자 이름 ↔ 읽기 |

- `<id>`는 장수 초상 ID(10001~11000)다. **한 번 정한 ID와 경로는 바꾸지 않는다.** 게임 데이터가 이 숫자만 저장한다.
- 게임은 `<이미지 서버>/portraits/<변형>/<id>.<확장자>`로 읽는다. 이미지 서버 주소는 게임 설정(`VITE_IMAGE_BASE_URL`)이 정한다.
- 시나리오 장수 이름 ↔ ID 대응은 게임 저장소의 `resources/portraits/rtk14-map.json`이 맡는다.

## 라이선스

`public/`에는 게임 화면의 생성 그림·Natural Earth 지도·기본 실루엣을 별도로 보관한다. 원본 경로·바이트 해시·공개 승인 여부는 [public/manifest.json](public/manifest.json), 출처는 [public/NOTICE.md](public/NOTICE.md)를 따른다. 두 게임 버전은 전체 커밋 SHA로 고정한 같은 파일을 읽는다. 아래 원작 초상 설명은 `portraits/`에만 적용한다.

**이 저장소의 그림은 오픈 라이선스가 아니다.** 「삼국지 14」(Koei Tecmo Games Co., Ltd.) 인물 일러스트에서 가공한 것이며,
이 저장소는 저작권을 주장하지 않고 누구에게도 사용·복제·재배포 권리를 주지 않는다.
저장소 소유자(peppone-choi)는 자기 게임에서 쓰는 책임을 직접 진다 (2026-09-06 결정).
공개 서비스에서 계속 쓸지는 게임의 공개 전 라이선스 관문(AC-M3-06)에서 다시 정한다.

이전 판의 다른 이미지(와룡전 타일, UI 아이콘, 계책 카드, 자작 초상 등)는 2026-10-20에 정리했다. 새 이미지는 생성해서 다시 만든다.
