# Open Source Team Contribution – ENTR

## 관련 저장소
- 원본 프로젝트 (저작자): https://github.com/eradman/entr
- 팀 Fork 저장소 (Organization): https://github.com/OPS-entr/entr

## 프로젝트 개요
본 프로젝트는 Linux 파일 변경 감지 도구 **entr** 오픈소스를 기반으로 한  
**팀 단위 기여 프로젝트**입니다.

기존 entr 프로젝트를 분석한 후, Linux 환경에 특화된 기능을 확장하였으며  
inotify API를 활용한 파일 감시, 데몬 모드, 로그 시스템 등을 구현했습니다.

## 팀 협업 방식
- 팀 구성: 3명
- 협업 방식:
  - GitHub Issue 기반 작업 분담
  - Pull Request 중심 개발
  - 코드 리뷰 및 기능 토의

### 팀원별 기여
- 권오준: inotify 기반 watch loop 구현 및 모듈화
- 이원재: 데몬 모드 구현
- **정채윤**: 로그 시스템 설계 및 구현

## 나의 기여
본 프로젝트에서 **로그 시스템 전반을 설계하고 구현**하였습니다.  
데몬 모드 환경에서도 안정적으로 동작할 수 있도록 로그의 구조와 흐름을 설계하는 데 집중했습니다.

### 주요 작업 내용
- 로그 전용 모듈 구현 (`project/log.c`, `log.h`)
- Plain / JSON 로그 포맷 지원
- 로그 레벨 필터링 기능 구현 (EVENT, INFO, WARN, ERROR)
- 타임스탬프 포맷 커스터마이징 기능 추가
- SIGHUP 시그널을 이용한 로그 파일 재오픈 기능 구현
- 데몬 모드에서 표준 출력이 없는 환경을 고려한 로그 처리

### 관련 작업
- 로그 모듈 소스: `project/log.c`
- 관련 Pull Request:
  - (PR 링크 추가)

## 사용 기술
- C
- Linux / POSIX
- inotify API
- Git / GitHub

## 배운 점
- 기존 오픈소스 코드베이스를 분석하고 기능을 확장하는 방법
- C 언어 기반 모듈 설계 경험
- 시그널 처리 및 파일 디스크립터 관리에 대한 이해
- GitHub 기반 팀 협업 및 코드 리뷰 경험

