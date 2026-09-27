# 소닉 라이더즈 한국어 패치

GameCube 일본판 **Sonic Riders**의 한국어 패치입니다. 배포: **nonunsaram** · 최신 버전: **v1.0**

**[v1.0 패치 다운로드](https://github.com/nonunsaram/sonic-riders-korean/releases/tag/v1.0)**

게임 원본과 패치된 ISO는 제공하지 않습니다. 직접 준비한 일본판 원본 ISO에 `.xdelta` 파일을 적용해 주세요.

## 변경 내용

- 메뉴, 옵션, 저장·불러오기 및 시스템 안내를 한국어로 번역했습니다.
- 코스·기어 이름과 설명, 미션 안내, 스토리 자막을 번역했습니다.
- 튜토리얼을 영어판 영상으로 교체하고 아래에 한국어 자막 27개를 넣었습니다. 게임 내 음원은 유지했습니다.
- 작은 기어 이름 54개에 갈무리11 Bold를 사용해 가독성을 개선했습니다.
- 저장 카드, 일시 정지·종료 확인·결과 메뉴, 규칙 설정 등에서 글자 정렬과 줄바꿈을 조정했습니다.
- 저장 카드의 RING TOTAL을 ‘토탈 링’으로 바꾸고 원본 글자색을 반영했습니다.
- 충돌 말풍선에는 원본 영어판 그래픽을 적용했습니다.
- ‘챠오’, ‘Dr. 에그맨’ 표기를 반영하고 대사 표현을 검수했습니다.

원래 영어로 말하는 ‘All Right!’ 등의 감탄사와 일부 영문 디자인 그래픽은 그대로 유지했습니다. 게임 음성은 한국어 더빙으로 변경하지 않았습니다.

## 필요한 원본

| 항목 | 값 |
|---|---|
| 게임 | Sonic Riders (Japan), GameCube |
| 게임 ID | `GXEJ8P` |
| 파일 형식 | 패치하지 않은 ISO |
| 크기 | 1,459,978,240바이트 |
| MD5 | `7eb29658744208dd505227bd8d3d6126` |
| SHA-256 | `d6f3bf86128748fa710dfa299c8468792aed632fb2661854337eefa53bd33a05` |

미국판 및 기존 한국어 패치 ISO에는 적용하지 마세요. RVZ 파일은 ISO로 변환한 뒤 위 해시와 일치하는지 확인해 주세요.

## 적용 방법

1. Releases에서 **`SonicRiders_Korean_v1.0.xdelta`**를 받습니다. GitHub가 자동으로 표시하는 ‘Source code’ 압축파일은 게임 패치가 아닙니다.
2. xdelta 패처를 준비합니다. 이 패치는 **xdelta3 3.0.11**로 생성하고 복원 검증했습니다. [개발자의 공식 3.0.11 다운로드 페이지](https://github.com/jmacd/xdelta-gpl/releases/tag/v3.0.11)에서 운영체제에 맞는 파일을 받으세요.
3. GUI 패처를 사용한다면 Patch에 `.xdelta`, Source에 일본판 원본 ISO, Output에 새 ISO 경로를 지정합니다. 원본과 출력 경로는 다르게 지정해 주세요.
4. 적용 후 아래 결과 해시를 확인하고 실행합니다. 게임의 일본어 텍스트 설정이 한국어로 대체됩니다.

명령줄에서는 실행 파일 이름을 `xdelta3.exe`로 맞춘 뒤 다음처럼 적용할 수 있습니다.

```powershell
.\xdelta3.exe -d -s "Sonic Riders (Japan).iso" "SonicRiders_Korean_v1.0.xdelta" "Sonic Riders Korean v1.0.iso"
```

Windows에서 파일의 SHA-256을 확인하려면 다음 명령을 사용합니다.

```powershell
Get-FileHash "Sonic Riders (Japan).iso" -Algorithm SHA256
```

| 파일 | SHA-256 |
|---|---|
| v1.0 `.xdelta` | `02459121a45f9a1e8d5615e9d8ca2fbc8f0ea35981f6634f6feeaa2c3cdb9b1b` |
| 적용 후 ISO | `6bbeea3d0c2f0ea4fe279ca74b1790b98efc23daa90052315d00ef98d01d22d3` |

패치 파일은 **74,224,848바이트**, 적용 후 ISO는 **1,459,978,240바이트**입니다. 튜토리얼 영상 변경으로 패치에 영상 차이 데이터가 포함됩니다. 실제 원본 ISO에 패치를 적용해 결과 해시가 일치하는 것을 확인했습니다.

## 사용 글꼴과 라이선스

| 글꼴 | 주 사용처 | 이용 조건 |
|---|---|---|
| LINE Seed KR Regular / Bold | 설명문, 시스템 메시지, 대사 및 튜토리얼 자막 | SIL Open Font License 1.1 — [전문](licenses/LINE_Seed_OFL.txt) |
| 샌드박스 어그로체 | 메뉴·제목 등 그래픽 UI | 샌드박스네트워크 배포 이용 조건 — [원문 PDF](licenses/SB_Aggro_Font_license.pdf) |
| 갈무리11 Bold | 작은 기어 이름: 12px, 정체, 1px 외곽선 | SIL Open Font License 1.1 — [전문](licenses/Galmuri_OFL.md) |

LINE Seed의 권리는 LY Corporation, 샌드박스 어그로체의 권리는 샌드박스네트워크, 갈무리의 권리는 Lee Minseo에게 있습니다. 각 글꼴의 정확한 조건은 함께 게시한 라이선스 원문을 확인해 주세요. 어그로체는 개인·기업의 영리·비영리 사용과 수정 등을 허용하며, 글꼴 파일 자체의 유료 판매는 금지합니다.

이 저장소에는 글꼴 설치 파일을 포함하지 않습니다. 글꼴 라이선스가 게임 및 원본 그래픽·음원·영상에 적용되는 것은 아닙니다. Sonic Riders와 원본 콘텐츠의 권리는 SEGA 및 각 권리자에게 있습니다. 본 패치는 비공식 팬 번역입니다.

## 확인 범위 및 제보

Dolphin에서 메뉴와 스토리 전체 컷씬을 검수했습니다. 실제 GameCube 하드웨어에서의 동작은 별도로 검증하지 않았습니다.

문제를 발견하시면 [Issues](https://github.com/nonunsaram/sonic-riders-korean/issues)에 발생 화면, 재현 방법, 사용 환경을 남겨 주세요. 원본 ISO나 게임 파일은 첨부하지 마세요.
