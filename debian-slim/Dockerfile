
##########################################################################
##
##    Arguments
##
##########################################################################

ARG BASE_IMAGE_TAG="11.4-slim"

ARG SCALA_VERSION="2.13.8"
ARG SBT_VERSION="1.6.2"
ARG USER_ID="1001"
ARG GROUP_ID="1001"

##########################################################################

# ベースイメージ
FROM debian:${BASE_IMAGE_TAG} AS builder

# 環境変数を設定
ENV SCALA_VERSION ${SCALA_VERSION}
ENV SBT_VERSION ${SBT_VERSION}
ENV USER_ID ${USER_ID}
ENV GROUP_ID ${GROUP_ID}

# 必要なパッケージをインストール

RUN : \
    && apt-get update \
    && apt-get install -y \
            curl \
            openjdk-17-jdk-headless \
    ;

##########################################################################

CMD [ "/bin/bash" ]
