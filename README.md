# Git

## **Git이란?**

**(= Version Control System)**

Git 외 버전 관리 시스템에는 여러 종류가 있다.

- **CVS** : 예전에 유행
- **SVN** : 예전에도, 현재도 많이 사용
- **Git** : 오늘날 가장 많은 사람들이 사용

## Git 설치

[Git](https://git-scm.com/)

무지성 **Next** 누르기

## **Git Bash**

Linux나 unix 같은 운영체제에서 사용하는 명령어 형태를 Window에서도 명령어를 통해 제어할 수 있게 해줌

`git`을 입력했을 때 다음과 같은 메세지들이 뜨면 설치 완료

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled.png)

### 명령어

- `git` : 사용할 수 있는 명령어들을 볼 수 있음
- `pwd` : 현재 폴더 위치를 알려줌
- `cd (이동할 폴더명)` : **C**hange **D**irectory
- `ls -al` : 현재 디렉토리에 있는 파일 목록
- `git status` : 파일의 상태 확인하기

- `init` : .git 폴더 안에 Git의 저장소 초기화 , 현재 디렉토리에다 작업할 것을 Git에게 알림

<aside>
💡 **.git 폴더** 안에는 버전 관리를 하며 생성되는 정보들이 저장됨, 지우면 **버전에 대한 정보** 날라가니 조심!

</aside>

- `git add (파일명)` : Git에게 관리해야 할 파일에 대한 추적을 명확하게 명령, 불편하지만 정확함
    
    새로운 파일의 버전 관리를 Git에게 명령할 때도 쓰지만, 이미 버전 관리가 되고 있는 파일을 수정하고 난 후 새로운 버전을 생성할 때도 사용
    

<aside>
💡 **Git을 처음 사용한다면**, 자신이 작성한 버전에 포함될 자신의 이름을 입력 => 작성자를 알 수 있음

</aside>

- `git config --global user.name (자신의 이름)`
- `git config --global user.email (자신의 이메일)`

## **Version**

버전이란 **의미있는 변화가 완결된 상태**

## **Commit (=Version Message)**

파일의 변화 내용이나 변경된 이유를 적음

[누구나 쉽게 이해할 수 있는 Git 입문~버전 관리를 완벽하게 이용해보자~ | Backlog](https://backlog.com/git-tutorial/kr/)

## Repository

- **원격 저장소(Remote Repository)** : 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소
- **로컬 저장소(Local Repository)** : 내 PC에 파일이 저장되는 개인 전용 저장소

## Commit

## Branch

브랜치란 독립적으로 어떤 작업을 진행하기 위한 개념입니다. 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있습니다.

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%201.png)

## 용어

- 버전관리 = **형상관리**
- **Commit :** 작업물을 업로드 대기 상태로 바꾸는 것
- **Push :** 업로드 대기 상태의 파일들을 한번에 Git(웹하드)에 올리는 것
- **Pull :** Git(웹하드)에서 내려받는 것
- 폴더 = **디렉토리**

## 명령 프롬프트

**[방법 1] 홈 폴더 열기**

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%202.png)

`Win + R` 후 `cmd` 입력

**[방법 2-1] 원하는 경로에서 열기**

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%203.png)

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%204.png)

원하는 폴더 주소창에 `cmd` 입력

맥은 C드라이브, D드라이브 나눠쓰는 경우가 없기 때문에 홈 폴더에 생성하는게 깔끔함

**[방법 2-2] 원하는 폴더가 홈 폴더 안에 있는 경우**

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%205.png)

**C**hange **D**irectory

C:\Users\사용자명>`cd` 내가 이동하고자 하는 폴더명

## ssh 인증서(키 파일) 생성

맥은 터미널 열고 `git` 입력

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%206.png)

명령 프롬프트에 `ssh-keygen` 입력

- **Enter file in which save the key** = 파일이 생성되는 경로, 바꿀거면 경로 입력 (바꾸는 거 비추)
- **Overwrite** = 덮어쓰기
- **Enter passphrase** = 비밀번호 입력, 깃에 뭔가 할 때마다 비밀번호 입력해야함 (비추)
- **Enter same passphase again** = 비밀번호 확인

### C:\Users\사용자\.ssh (사용자 홈 폴더)

**[맥의 사용자 홈 폴더]**

- Users/아이디/.ssh
- ~/.ssh (Users/아이디를 ‘~’로 축약)

터미널 열고 `open Users/아이디/.ssh` 또는 `open ~/.ssh` 입력

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%207.png)

- **id_rsa** = 서버 키
- **id_rsa.pub** = 공개 키

<aside>
💡 파일 중 하나를 Git에 등록시켜, Git에 명령어를 내릴 때마다 쟈킷에 등록되어 있는 내용과 내 컴퓨터 속 파일을 대조해서 인증

</aside>

1. 메모장이나 VScode를 이용해 **id_rsa.pub** 파일 열기
2. `우측 상단 프로필 아이콘 > Settings > SSH and GPG keys > New SSH key`
3. **Title**엔 아무거나, **key**에 **id_rsa.pub** 소스 복붙

[https://github.com/settings/keys](https://github.com/settings/keys)

## 저장소 생성

[](https://github.com/new)

- **Repository name :** 저장소 이름, 주소로 만들어질 부분이니 무조건 **영문**으로, 띄어쓰기도 안됨
- **Description : 설명**
- **Add a README file :** 작업에 대한 설명을 작성하기 위한 파일 (무조건 체크하는게 좋음)
- **Add .gitignore :** 깃허브에는 등록하지 않을 파일을 명시하는 파일, **javascript**는 `Node`

## 클론 생성

<aside>
💡 깃허브의 저장소를 내 컴퓨터에 최초로 복사하는 행위를 **클론**이라고 함

</aside>

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%208.png)

`Code`에서 SSH 주소 복사 (**반드시 SSH!** HTTPS는 속도가 느림)

`git@github.com:아이디/저장소이름.git` (.git은 생략가능)

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%209.png)

`git clone git@github.com:아이디/저장소명`

## Commit (업로드 대기) / Push (업로드)

**[방법 1] 명령 프롬프트**

1. 클론 폴더에서 명령 프롬프트 열기
2. `git add -A` or `git add —-all` : ‘A’는 all, 내가 변경한 모든 것을 추려내는 명령어
3. `git commit -m ”간단한 코멘트”`
4. `git push origin main` : **origin**은 내 컴퓨터 속 파일, **main**은 git

git clone -b (branch name) url: 브런치 클론받기

git remote add origin: 내 레포지토리

git remote add (upstream): 내 원본의 원본

git merge main

git merge~?

- git에 업로드 한 순간, **git에 있는 파일이 원본**이 되고 내 컴퓨터 속 파일은 복사본이 됨
- 파일 하나가 **50MB**가 넘지 않는 이상, 용량은 **무제한**

<aside>
💡 최초로 commit을 한 경우, 누가 등록했는지 기록하기 위해 환경설정 값(이메일과 이름)을 추가하라는 메세지가 뜸

</aside>

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2010.png)

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2011.png)

`git config —global [user.email](http://user.email) “이메일@주소”`

`git config —global [user.name](http://user.name) “이름”` 입력 후 다시 commit

**[방법 2] VS Code**

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2012.png)

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2013.png)

**[방법 3] VS Code 명령어**

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2014.png)

`Ctrl + Shift + P` or `F1` 을 열어 `commit`

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2015.png)

**COMMIT_EDITMSG** 파일 **첫 줄**에 코멘트 적고 저장

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2016.png)

`Ctrl + Shift + P` or `F1` 을 열어 `push`

![Untitled](Git%20Github%20521e2cc6802240b2bbe7e079787c2a85/Untitled%2017.png)

저장소 선택하면 끝!

## Pull (다운로드)

`git pull origin main` : 변경사항만 다운로드
