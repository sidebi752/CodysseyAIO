# 네이토 모델 별 토큰 소모량 확인

## 비교 목적과 환경

### 목적: 네이토 모델 별 토큰 소모값 실험

### 실험 환경:
99% 소진 후 2020 토큰이 남았을 때
5번째 질문에서 어떤 메세지가 뜨는지와 토큰 소모량이 어떻게 되는 지 실험
첨부파일 없이 대화만으로 측정

## 소모값 정리

### 모델 별 정리
- Gemini 3 Flash: 3000
- Gemini 3.1 Flash Lite: 3000
- Gemini 3.1 Pro: 9001
- Claude Haiku 4.5: 5389
- Claude Sonnet 4.6: 10780
- GPT-5 Mini: 3137
- Upstage Solar Pro 4: 5926
- Upstage Solar Mini 4: 5926
- Claude Opus 4.7: 16311
- Claude Opus 4.8: 16255
- GPT-5.5: 12548
- GPT-5.4: 6274
- GPT-5.4 mini: 3137

### 추가 확인 사항: 5~6번 질문한 후에 새 대화를 열라는 요구가 뜸

## 세 줄 요약

최신모델일수록 토큰 소모량이 늘어나는 편이다.
제미나이 Pro, 클로드 Opus, 지피티 5.5가 토큰 사용량이 많다.
Mini, flash는 사용량이 적은 편이다.
