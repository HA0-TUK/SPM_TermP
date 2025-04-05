## 🎮 게임 컨셉

- **High Concept**: 솜을 잃어버린 인형이 달리면서 장애물을 피해 솜을 모으는 게임
- **핵심 메카닉**:
  - 자동 달리기 (가로 배경 스크롤)
  - **점프**: 1회 누를 시 1단 점프, 공중에서 한번 더 누르면 2단점프
  - **스윙**: 점프 중 스윙 키 누를 시 실을 타고 앞으로 스윙
  - 솜 획득 시 점수 상승
  - 장애물 충돌 시 체력 감소 → 체력 0이면 게임 종료

## 🔧 개발 범위

| 항목 | 수량/범위 |
|------|-----------|
| CustomView | 배경/캐릭터 레이어, 아이템 및 장애물 레이어 |
| UI 컴포넌트 | 점수/체력 표시용 TextView & 게이지(가능하다면) 2개, 점프, 스윙 용 Button 2개 |
| 애니메이션 | 프레임 애니메이션 3개 (달리기, 점프, 스윙) |
| 충돌 판정 | 캐릭터 vs 장애물, 캐릭터 vs 아이템 |
| 점수 시스템 | 실시간 점수 갱신 |
| 체력 시스템 | 장애물 충돌마다 감소, 0되면 게임 종료 |
| 이벤트 처리 | 점프, 스윙 버튼 → 인터페이스 방식 처리 |
| 배경 스크롤 | 시간 기반 스크롤 (Handler/postDelayed) |
| 게임 루프 | 초당 n프레임 처리 (FPS 기반 진행)


## 📱 예상 게임 실행 흐름

1. **시작 화면**
   - 캐릭터 & 배경 이미지 표시
   - "게임 시작" 버튼
2. **게임 화면**
   - 캐릭터 자동 이동 (스크롤 배경)
   - 점프/스윙 조작
   - 목화솜 모으면 점수 증가
   - 장애물 충돌 → 체력 감소
3. **게임 오버 화면**
   - 최종 점수 표시
   - 다시 시작 or 종료 선택
  
## 🖼️ 게임 화면 예시

- 시작 화면  
 ![image](https://github.com/user-attachments/assets/a1f9c5ef-18b3-4f38-b19e-c174364284c6)


- 게임 진행 중  
  ![image](https://github.com/user-attachments/assets/1c268fd9-d10c-4865-8df3-c3fcbf1b5476)
  ![image](https://github.com/user-attachments/assets/c91f72d5-f266-4d2e-8271-f9b59996fdcf)


- 게임 오버 화면  
  ![image](https://github.com/user-attachments/assets/96ec680a-400a-4881-be5d-353e2ace1891)

  


## 📆 개발 일정 (8주)

| 주차 | 주요 개발 내용 |
|------|----------------|
| 1주차 (4/8~) | 기획 정리, 게임 플로우 구성, UI 레이아웃 구상 |
| 2주차 | 리소스 제작 (배경, 캐릭터, 아이템, 장애물 이미지), CustomView 구성 |
| 3주차 | 배경 스크롤 구현, 캐릭터 애니메이션 구현 (달리기, 점프) |
| 4주차 | 캐릭터 애니메이션 구현 (스윙) |
| 5주차 | 충돌 판정, 젤리/장애물 생성 및 이동 |
| 6주차 | 점수/체력 시스템, UI 업데이트 |
| 7주차 | 게임 오버 처리, 다이얼로그, 버튼 이벤트 처리 |
| 8주차 | 발표 영상 제작, README 정리, 코드 정리 및 마무리

