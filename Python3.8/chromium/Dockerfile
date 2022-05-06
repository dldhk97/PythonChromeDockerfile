FROM python:3.8

LABEL maintainer="dldhk97@naver.com"

COPY . /workspace

WORKDIR /workspace

# Set timezone
ENV TZ=Asia/Seoul
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install korean locale
RUN apt-get update && apt-get install -y locales git
RUN localedef -f UTF-8 -i ko_KR ko_KR.UTF-8
ENV LC_ALL ko_KR.UTF-8
ENV PYTHONIOENCODING=utf-8
ENV LANG=ko_KR.UTF-8 \
    LANGUAGE=ko_KR.UTF-8

# Install korean font
RUN mkdir /usr/share/fonts/nanumfont
RUN wget http://cdn.naver.com/naver/NanumFont/fontfiles/NanumFont_TTF_ALL.zip
RUN unzip NanumFont_TTF_ALL.zip -d /usr/share/fonts/nanumfont
RUN fc-cache -f -v

# Install chromium & driver
RUN apt install -y chromium chromium-driver

# Set display port to avoid crash
ENV DISPLAY=:99

# Run bash
CMD ["bash"]
