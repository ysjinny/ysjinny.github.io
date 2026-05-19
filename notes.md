# Notes
## 2026-05-19
claude cli api 에러는 해결되지 않았지만... 사이드 프로젝트 하면서 머리를 식혀본다.
naver blog를 쓰다가 자유도가 너무 낮아서 github을 써보기로 마음 먹었다.
거의 회사에서 업무기록 의식의 흐름대로 적는 거겠지만!

일단 claude cli 현상태는,
windows os -> wsl -> docker -> container
여기서 도커에 설치를 하고 컨테이너에서 실행을 시키고 있다.

해결하는 여러가지 방법이 있었는데
1. export ANTHROPIC_API_KEY
2. ~/.zshrc 또는 ~/.bashrc 파일 가장 아래에 export 구문 추가하고 source ~/.zshrc 실행하기
3. docker build 시에 -e로 api key 넘겨주기

다 안 통한다.

웃긴건 claude interactive는 잘 됨... 
또 windows host에서는  interactive, cli 둘다 잘 된다는 거.
이걸로 봐서는 키 문제가 아니라 cli 모드인 경우에 우분투에서 환경변수를 못 가져오는 듯 하다. 
이틀 째 이걸로 삽질 중인데 뭐가 문제일까?

## 2026-05-18
claude code cli가 도커 내 컨테이너에서 인증이 잘 안된다. 
윈도우 환경을 전제로 해서 그런지 우분투 환경에서 뭔가 잘 안되고 있음. 
이걸 빨리 해결을 하고 싶었는데 잘 안돼서 많이 조급했던 하루였다. 

오늘은 docker daemon, docker context, docker engine, container 등등의 차이점을 좀 알게 되었다. 
진짜 AI가 생기고 나서 나는 많은 것들이 편해졌다. 

원태가 git worktree 써보라던데 구경도 못했다. 
제욱님은 리눅스 환경 claude code with narrans 좀 써보셨을지도?

## 2026-05-15
docker라는걸 처음으로 세팅해보고 만져보는 중인데, 익숙하지 않고 중첩에 중첩이 되어있다보니 헷갈려서 토할 것 같다...

claude code cli 수행 시켰는데 plan 모드 진입함. 
이유는 아직 파악 못함. 

우분투 도커 위에다가 윈도우 환경을 테스트 해보려고 하는데 이거 꽤 미련한 짓으로 느껴진다.
옵션이 가능한게 많으니까 삽질도 더 많다.
윈도우 도커로 하면 안됨?

회사에 윈도우 도커 쓰는 사례가 잘 안보여서 걍 리눅스 기반으로 하되 윈도우에서 해야하는 것들이랑 분리 중인데 죽을맛...