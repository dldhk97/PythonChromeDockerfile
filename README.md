# python-chrome-kor-docker
[Python](https://hub.docker.com/_/python) 이미지에 크롬/크로니움(+드라이버)을 설치하고,  한글 폰트([나눔 글꼴](https://hangeul.naver.com/font))를 설치 및 로케일 설정한 이미지입니다.

이외에도 서울 타임존 설정, 크롬 크래시 방지를 위한 디스플레이 설정이 되어있습니다.

# How to build
```
docker build -t dldhk97/python-chrome-kor-docker:3.8_amd64 .
```

# Dockerhub
https://hub.docker.com/r/dldhk97/python-chrome-kor-docker
