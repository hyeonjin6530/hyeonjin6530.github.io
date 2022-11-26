**20223158 황현진**    
# 유레카프로젝트 - 개인 GIT BLOG 과제

:pushpin: **gitblog 생성 및 테마 설정**   
    나는 http://jekyllthemes.org/ 라는 사이트에서 'Not Pure Poole' 이라는 테마의 원격 저장소를 나의 원격 저장소로 포크해왔다. 이렇게 포크를 하는 과정 속에서 나의 레포지토리의 이름을 hyeonjin6530.github.io로 바꾸었다. 그리고 git clone을 하여 쉽고 빠르게 내가 원하는 테마의 깃블로그를 생성하였다.

</br>

:pushpin: **favicon 추가**   
    먼저 favicon에 사용할 이미지를 제작하기 위해 아이패드에 있는 '굿노트'라는 어플을 사용하여 직접 이미지를 그렸다.    
    그리고 이를 favicon으로 등록하기 위해 이미지를 넣으면 자동으로 favicon icon의 형태로 변환해주는 온라인 사이트를 이용하였고, 이를 통해 얻은 favicon icon 모음집을 assets이라는 폴더 속에 새롭게 logo.ico라는 파일을 만들어 그 안에 저장했다.   
    그리고 _includes 폴더 속 custom-head.html이라는 파일에 favicon을 설정할 수 있는 코드를 작성하였다.

</br>

:pushpin: **disqus를 이용하여 댓글 기능 추가**   
    댓글 기능은 disqus를 활용하였다. disqus 홈페이지를 통해 댓글 기능을 만들기 위한 세팅을 하고 홈페이지에서 얻은 universal Code를 페이지에 맞게 수정하여 기존 코드에 반영하였다. 그리고 최종적으로 댓글을 허용하고 싶은 post에 'comment: true'라는 문구를 추가하여 댓글을 작성할 수 있도록 하였다.

</br>

:pushpin: **깃블로그 메인 화면 수정하기**   
- 프로필 사진과 프로필 배경 변경      
      '핀터레스트'라는 사진 공유 사이트에서 내가 원하는 이미지를 찾은 후 이미지의 주소를 복사하여 _config.yml 에서 이미지를 설정하는 부분에 붙여넣었다.   

- 블로그 주인 이름, 블로그 설명 변경       
       위와 마찬가지로 _config.yml 에서 해당하는 부분들의 코드를 모두 수정하였다.

- 블로그와 연결되어 있는 social link를 나와 관련된 link로 변경(email, twitter, github)       
       _data/social.yml에 들어가서 link들을 다 나와 관련된 link로 변경하였다. 그러나 나는 트위터를 하지 않기 때문에 코드 수정을 통해 트위터 로고 대신 인스타그램 로고로 변경하고 나의 인스타그램의 링크를 올리는 것으로 대체하였다.   

</br>

:pushpin: **포스팅하기**   
    _posts라는 파일에 markdown을 이용하여 글을 작성하였다.   
    이 과정 속에서 포스팅이 올라가지 않는 오류를 겪었었는데, 이 경우에는 포스팅의 제목에 yyyy-mm-dd의 형식으로 날짜를 정확하게 입력하였더니 해결되었다.  

</br>

:pushpin: **google analytics 기능 추가하기**    
    google analytics에 접속한 한 다음 '측정 시작'을 누른다. 그리고 3가지 단계를 진행하면서 자신의 gitblog 주소를 입력한다.   
    그 다음 _config.yml 파일에 아래의 코드를 입력하면 자동으로 연동이 되어 사용자, 사용 평균 시간 등을 확인할 수 있다.   
    

    analytics:    
    provider               : google    
                            # false (default), "google", "google-universal", "google-gtag", "custom"
    google:
        tracking_id          : G-GLECBP0BSM
        anonymize_ip         : false 

이외의 내가 겪은 오류와 같이 자세한 내용은 [깃블로그](https://hyeonjin6530.github.io/2022/11/26/post-4/)에서 확인해볼 수 있다.
</br>

:pushpin: **위와 같은 모든 bulid를 깃블로그 사이트에 적용하기**    
    위에서 설명한 모든 수정 내용을 사이트에 적용하기 위해서는 아래의 3단계를 거쳐야 한다.  

1.  vscode를 이용하여 코드를 수정하고 저장한다.    

2. cmd 창에서 bundle exec jekyll serve 라는 명령어를 입력하여 얻은 http://127.0.0.1:4000 라는 사이트에 접속해 수정된 내용이 올바르게 적용되어 있는지 확인한다.    

3. git status를 통해 아직 add 되지 못한 파일을 확인한 후 git add * 하였다. 
        그리고 변경 사항에 대한 메모를 하기 위해 git commit -m "(설명)" 명령어를 사용하여 커밋하고 마지막으로 git push를 하였다.    
    
이러한 과정을 거치면 변경사항과 커밋 내용을 모두 깃허브에 기록할 수 있다.  
     