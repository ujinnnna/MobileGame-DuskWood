# DuskWood

모바일(iOS) 3D 액션 RPG 개인 프로젝트입니다.  

<p align="center">
  <a href="https://youtu.be/acB6vXXTcko?si=a6tCo8J469wg3b8Y">
    <img src="https://img.youtube.com/vi/acB6vXXTcko/maxresdefault.jpg" alt="Demo Video" width="100%" />
  </a>
  <br />
  <a href="https://youtu.be/acB6vXXTcko?si=a6tCo8J469wg3b8Y"> 시연 영상 </a>
</p>

## 개요
- 플랫폼: Mobile(iOS)
- 장르: 3D Action RPG
- 개발: 1인 개발
- 기간: 2025.09 ~ 2026.03 (6개월)
- 엔진: Unity 6.0 (URP), C#

## Keys
- **계층 분리**: Game / Infrastructure / Data & Shared로 책임 분리, asmdef로 참조 범위 제한
- **전투 구조**: 무기 로직은 인터페이스 기반으로 분리하고, 입력/애니메이션 이벤트는 공통 진입점으로 모아 무기 추가 시 수정 범위를 줄임
- **콤보 설계**: 애니 타이밍 + 입력 버퍼로 콤보
- **보스 AI**: Behavior Tree 기반으로 패턴 확장, 필요 노드는 커스텀 Task/Composite 생성
- **연출**: 보스 처치 순간에 BGM/슬로우모션/UI 페이드/SFX를 연결
- **리소스 관리**: Addressables 프리웜으로 시작 시점에 다운로드/캐싱하고, 풀링으로 전투 중 생성/파괴 비용을 줄임
- **세이브/로드**: JSON 저장/복원, 동시 저장 호출은 순차 처리로 파일 충돌 방지
