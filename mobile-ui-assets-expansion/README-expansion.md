# 인챈트 인 차트 리소스 추가팩

이 ZIP은 앞서 만든 모바일 UI 추가팩에 이어 사용할 신규 PNG와 모녀 교체 PNG를 담고 있습니다. 기존 프로젝트 폴더에는 파일을 직접 덮어쓰지 않았습니다.

| 경로 | 용도 |
|---|---|
| `illustrations/prologue/` | 추운 연구실, 서리 낀 테라리움, 결심하는 캐시 순으로 재생합니다. 대사·건너뛰기는 웹 UI에서 표시합니다. |
| `illustrations/ending/` | 모닥불가 모녀와 안도하는 캐시의 후일담입니다. 모녀는 불을 보고 있으며 캐시는 들키지 않습니다. |
| `ui/mobile/result-panel.png`, `decor/mobile/result-topper.png`, `logos/clear-ko.png` | 9-slice 결과 패널, 상단 장식, 클리어 타이틀입니다. 별·코인·기존 축하 삽화를 별도 레이어로 얹습니다. |
| `ui/mobile/action-leaf.png` | 좌우 잎을 넣은 청록 버튼 9-slice입니다. 잎을 따로 배치할 때는 기존 청록 버튼 위에 `decor/mobile/button-leaf.png`를 놓고 오른쪽을 좌우 반전합니다. |
| `guides/` | 탭·드래그 손가락, 가로·세로·네 방향 화살표와 시작점·촉, 노란 워드 배지, 반복 절단선입니다. |
| `ui/mobile/use-count-badge.png` | 빈 횟수 배지입니다. 숫자는 HTML로 겹쳐 표시합니다. |
| `fx/` | 불꽃·눈송이·반짝이, 화상·화재·따뜻함·수증기 소멸, 막힘·힌트·코인 연출입니다. `sparkle.png`는 원하는 위치에서 여러 번 생성할 수 있습니다. 복제 반짝이와 점화는 각 3프레임입니다. |
| `ui/mobile/stage-*.png`, `stage-thumbnails/` | 열림·잠김·준비 중 카드와 첫 번째 불 썸네일입니다. 비와 강 썸네일은 앞선 팩에서 재사용합니다. |
| `ui/mobile/common-popup.png`, `hint-row.png`, `toast.png` | 공용 팝업, 힌트 행, 토스트의 9-slice입니다. |
| `branding/` | 기존 캐시, 온실, 테라리움을 활용한 앱 아이콘, 파비콘, 공유 썸네일입니다. |
| `tiles/mother.png`, `tiles/daughter.png` | 추운 스프라이트 모녀의 교체 이미지입니다. 기존 동명 파일을 이 두 파일로 교체할 수 있습니다. |
| `tiles/mother-warm.png`, `tiles/daughter-warm.png` | 각각 따뜻한 상태입니다. 추위가 해제되면 이 파일로 전환합니다. |

엄마는 256×512px, 딸은 256×256px입니다. 각 인물의 상태 전환에 같은 확대율과 발 기준선을 적용했습니다. 팔 포즈와 머리 폭이 달라지는 경우 파일에 투명 여백이 남습니다. 모든 PNG는 72 DPI이고 가로·세로가 4px의 배수입니다. 파일별 크기와 9-slice 인셋은 `mobile-ui-expansion-manifest.json`에서 확인할 수 있습니다.

시작·로딩 일러스트와 클리어 팝업의 기존 축하 삽화는 원래 파일을 사용합니다. 공용 닫기·자물쇠·언어 선택 칩과 캡슐 가격 버튼은 첫 모바일 UI 추가팩을, 되돌리기·화살표·별과 코인은 기존 세트를 사용합니다. 대사창·이름표는 기존 speech-body 및 category-tag 위에 텍스트를 표시합니다. 모닥불·나뭇가지 연결 타일, 선택 컷, 2·3스테이지 확정 후 항목은 이 팩 범위 밖입니다.

```css
.clear-panel { border: 0 solid transparent; border-image: url("../assets/ui/mobile/result-panel.png") 79 fill / 25px; }
.leaf-action { border: 0 solid transparent; border-image: url("../assets/ui/mobile/action-leaf.png") 65 48 34 48 fill / 23px 28px 12px; }
```
