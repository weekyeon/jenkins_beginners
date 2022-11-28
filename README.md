# jenkins_beginners
:fire: Getting Started Jenkins

## Overview
* Github로 관리하는 source 및 resource를 CI/CD 자동화 작업을 이용해 Build & Deploy하는 것이 목표이다.
* CI/CD Tool은 Jenkins이며 Build Script는 Ant를 사용해야 한다.
* 위와 같은 작업을 통해 개발자는 다음과 같은 효과를 기대할 수 있다.

  > **👍** 박자바 씨의 Build & Deploy Job
  > 
  > `1` 개발자인 박자바 씨가 A Project에서 A.java 파일을 수정했습니다.
  >
  > `2` 박자바 씨는 수정된 사항을 Remote Repo에 Push했습니다.
  >
  > `3` Github 변경 사항을 Jenkins가 감지합니다.
  >
  > `4` Jenkins의 trigger가 실행되어 변경 사항을 가져옵니다.
  >
  > `5` Jenkins가 A Project 내에 있는 Ant Build Script를 호출합니다.
  >
  > `6` 호출된 Ant Build Script가 Build 작업을 진행합니다.
  >
  > `7` Ant 및 Jenkins Job 설정을 통해 Build 결과물이 B Project의 적합한 위치에 이동됩니다.

## Problem
* 테스트를 하던 중 Github Webhook의 동작 원리(?)를 알게 되었다.
* Github와 Jenkins의 Webhook은 Github가 Jenkins에게 HTTP POST 요청을 날리는 것으로부터 시작된다.
* 인터넷망이 있다면 상관없지만 내 업무 환경은 인터넷망이 없기 때문에 Github의 Webhook을 통해 CI/CD를 진행하는 것이 어렵다고 판단했다.

## Concluding Remarks
* Jenkins Build Trigger를 Github Webhook이 아닌 Git hook으로 연결하여 인터넷망이 없을 때도 CI/CD 자동화가 되도록 해결했다.
* 그래서 이 Repository는 이제 쓰지 않아도 될 듯 하다!
