# 깃허브 페이지 생성하기

## 단계

* jekyll 로컬 환경 설정
  * homebrew 설치
    ```
    $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
  * rbenv 다운로드
    ```
    $ brew update
    $ brew install rbenv ruby-build
    ```
  * ruby 최신 버전 다운로드
    ```
    $ rbenv install --list
    $ rbenv install 2.4.4
    $ rbenv rehash
    ```
  * ruby 버전 변경
    ```
    $ rbenv global 2.4.4
    
    $ export PATH="$HOME/.rbenv/bin:$PATH"
    $ eval "$(rbenv init -)"
    ```
  * 테마 다운로드

* 깃허브 연동
  * _config.yml 설정


---
## 참조

https://maejinkim.github.io/%EB%B8%94%EB%A1%9C%EA%B7%B8/%EB%B8%94%EB%A1%9C%EA%B7%B8/  
https://medium.com/fabiancode/github-io-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-with-jekyll-a98c018249a9