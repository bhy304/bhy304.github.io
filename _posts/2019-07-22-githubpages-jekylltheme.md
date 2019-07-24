---
layout: post
title: "GitHub Pages with Jekyll Themes"
tags: [jekyll]
comments: true
---

Jekyll Theme을 적용한 블로그 만들기

---

## 준비물

* 1. Git 설치
  1. GitHub 가입 (GitHub 계정 필요!)
  2. Ruby for Windows 설치

## Windows에서 Jekyll Theme 적용한 블로그 만들기

##### 1. Ruby 설치
    
[RubyInstaller](https://rubyinstaller.org/) Ruby+Devkit 버전으로 다운로드 후 설치 진행
    

##### 2. GitHub에 유저명.github.io 이름으로 repository 만들기

새로 만든 Repository를 로컬에 git clone 하기 

```git clone https://github.com/bhy304/bhy304.github.io.git```


##### 3. RubyGems 를 통해 Jekyll과 Bundler 설치

```gem install jekyll bundler```


##### 4. 설치 확인
    
```jekyll -v```


##### 5. 기본 블로그 테마 설치

현재 디렉토리에 Jekyll 사이트를 만들려면 ```jekyll new .```을 실행한다.
만약 디렉토리가 비어있지 않는 경우에는 ```--force```옵션을 넣어  ```jekyll new . --force```로 실행한다. 


##### 6. 개발 환경 Server 실행

jekyll 서버를 실행해 개발 환경에서 기본 블로그 테마가 설정되었는 지 확인할 수 있다.

```jekyll serve```

브라우저로 http://127.0.0.1:4000 에 접속!

```jekyll build```

##### 7. 원하는 테마 적용하기

Jekyll Themes 중 원하는 테마를 정하고 git clone 을 통해 로컬 폴더에 다운로드한다. 

```git clone https://github.com/aweekj/kiko-now.git```


**※ 주 의 ※**

> git clone 했기 때문에 주의할 점!!<br>
배포자의 Git을 그대로 Clone 했기 때문에 폴더 속에 .git 폴더가 존재한다.<br>
.git 폴더를 제외한 파일을 자신의 local 폴더로 옮겨주어야 한다.<br>


##### 8. _config.yml 환경설정 변경

##### 9. GitHub에 올리기
    
```
git add * 

git commit -m "commit message"

git push origin master 
```

---
