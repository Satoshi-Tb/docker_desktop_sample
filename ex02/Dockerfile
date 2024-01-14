FROM php:8.2-apache

# tzdata の インストール
RUN apt-get update -qq \
 && apt-get install -y --no-install-recommends \
    tzdata \
 && rm -rf /var/ lib/ apt/ lists/*

# タイム ゾーンを設定する環境変数
ENV TZ="Asia/Tokyo"

# 作業 ディレクトリ を 変更
WORKDIR /usr/local/etc/php

# ファイル の コピー
COPY php.ini ${PWD}

# 一時変数の定義
ARG wdir

# 以下のように設定も可能
#ARG wdir="/var/www/html"

# 作業ディレクトリを変更
WORKDIR $wdir
