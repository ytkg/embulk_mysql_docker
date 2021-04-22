FROM openjdk:8

RUN apt-get -y update && apt-get -y upgrade && \
    apt-get -y install vim

ENV TZ Asia/Tokyo

RUN curl --create-dirs -o ~/.embulk/bin/embulk -L "https://dl.embulk.org/embulk-latest.jar" && \
    chmod +x ~/.embulk/bin/embulk && \
    echo 'export PATH="$HOME/.embulk/bin:$PATH"' >> ~/.bashrc && \
    . ~/.bashrc

WORKDIR app
