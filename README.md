Project overview: Building a workstation using Docker and terminal
  - Workstation: high performance computer system that is basically designed for a single user

Execution Environment: <br>
    1. OS : macOS 15.7.4 <sw_vers>
    2. shell : zsh <echo $SHELL>
    3. 터미널 : Apple_Terminal <echo $TERM_PROGRAM>
    4. Docker : 28.5.2 <Docker --version>
    5. git : git version 2.53.0 <git --version>

Checklist of tasks : 
    Terminal O
    Permissions O
    Docker O 
    Dockerfile O
    Port Mapping O
    Volume O
    Git O
    Github O

Verification method: Refer to hyperlinks

Troubleshooting : 
    ### 1 - error after running docker logs

    문제:
    ```bash
    docker logs
    ```

    에러:
    ```text
    docker: 'docker logs' requires 1 argument
    ```

    원인 가설:
    - Docker logs is used to check logs of a container
    - Therefore, a the name or ID of a container must be provided

    확인:
    ```bash
    docker logs --help
    ```
    Confirmed that the command does require the name of the container

    해결:
    - Check running containers and then view logs of a container

    ```bash
    docker ps
    docker logs my-web
    ```

    Result: Successful display of logs of the container

    정리:
    - docker logs: require container name / container_ID

    
터미널 조작 로그 :
    pwd ,ls -a , mkdir , ls , cd , cp -r , mv , touch , rm , rmdir , vim , cat <br>
    [터미널 조작 로그 보기](docs/01_terminal_logs.md) <br>
    [권한실습 및 증거기록](docs/02_권한실습_및_증거기록.md)

Docker 운영 및 검증 로그 : 
    1. docker version , docker info
    2. dokcer images , docker ps -a , docker logs <br>
        [도커설치 및 기본점검](docs/03_Docker설치_및_기본점검.md) <br>
        [도커 기본운영 및 명령수행](docs/04_도커_기본운영_명령_수행.md)



Dockerfile 기반 웹 서버 컨테이너 :

    1. 웹 서버 소스코드 ( app/index.html )
    2. Dockerfile
    3. 빌드 및 실행 명령 결과 로그 
![index.html 실행 결과](img/web.png)
4. 포트 매핑 접속 성공 증거 (스크린샷 또는 로그)<br>
    [컨테이너 실행 실습](docs/05_컨테이너_실행_실습.md) <br>
    [도커파일 기반 커스텀이미지](docs/06_도커파일기반_커스텀이미지제작.md)<br>


포트 매핑 접속 증거 :
    1. p <host_port>:<container> 실행 후.  주소창 포함 브라우저 접속 화면 (스크린샷 폴더)
    ![포트 매핑 접속 증거](img/수정후.png) <br>
    [포트매핑 접속 증거](docs/07_포트매핑_접속증거.md)


바인드 마운트 반영 + 볼륨 영속성 증거 :
    1. 바인드 마운트 : 실행 명령 + 호스트 변경 전 후 비교

![수정전](img/수정전.png)
![수정후](img/수정후.png)<br>
[바운드마운트 증거](docs/08_바운드마운트_증거.md)


    2. docker 볼륨 : 생성 , 연결 , 검증 명령 + 컨테이너 삭제 전 후. 비교
[볼륨영속성 증거](docs/09_볼륨_영속성.md)

Git 설정 및 Github / VSCode 연동 증거 : 
1. 깃 사용자 정보 , 기본 브랜치 설정 후 , vscode 에서 깃허브 로그인 및 저장소 연동 완료
![git](img/git.png)
![git_log](img/git_log.png)<br>
