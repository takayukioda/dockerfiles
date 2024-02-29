FROM ubuntu:latest

RUN apt update && \
	apt install -y \
		language-pack-ja-base \
		language-pack-ja \
		locales \
		vim \
		sudo && \
	rm -rf /var/lib/apt/lists/* && \
	apt clean
RUN locale-gen ja_JP.UTF-8

RUN useradd -ms /bin/bash me && adduser me sudo && echo 'me ALL=(ALL) NOPASSWD: ALL' >/etc/sudoers.d/me
USER me
WORKDIR /home/me
ENV LANG ja_JP.UTF-8
ENV TZ Asia/Tokyo
