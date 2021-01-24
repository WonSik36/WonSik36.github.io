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
    $ rbenv install 2.7.2
    $ rbenv rehash
    ```
  * ruby 버전 변경
    ```
    $ rbenv global 2.7.2
    
    $ export PATH="$HOME/.rbenv/bin:$PATH"
    $ eval "$(rbenv init -)"
    ```
  * 테마 다운로드
    minimal-mistakes 테마 다운로드
    ```
    $ git clone https://github.com/mmistakes/minimal-mistakes.git
    $ git remote remove origin
    $ git remote add origin "본인 리포지터리 주소" 
    ```

* 깃허브 연동
  * _config.yml 설정
  ```
  # _config.yml
  url : "https://wonsik36.github.io/" # 본인 블로그 주소
  ```

* 글 올리기
```
# _posts 폴더 생성
$ vi ./_posts/2020-01-18-hello-world.md
$ git add .
$ git commit -m "First posts"
$ git push origin main
```

* 페이스북 댓글 플러그인 더하기

```
# _config.yml
comments:
  provider               : "facebook"
  facebook:
    appid                : {YOUR_APP_ID}    # https://developers.facebook.com/apps/
    num_posts            : 5
    colorscheme          : "light"

defaults:
  ...
      comments: true
```

로컬에서는 `JEKYLL_ENV=production` 이 설정되어 있어야한다.

---
## 참조

[Jekyll 연동1](https://maejinkim.github.io/%EB%B8%94%EB%A1%9C%EA%B7%B8/%EB%B8%94%EB%A1%9C%EA%B7%B8/)  
[Jekyll 연동2](https://medium.com/fabiancode/github-io-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-with-jekyll-a98c018249a9)  
[페이스북 댓글 연동](https://github.com/mmistakes/minimal-mistakes/issues/2527)