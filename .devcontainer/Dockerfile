# ↓ 現時点のデフォルトイメージ
FROM mcr.microsoft.com/devcontainers/ruby:1.1-3.3-bullseye
# ↓ 詳細にリリースタグを指定する場合
# FROM mcr.microsoft.com/devcontainers/ruby:1.1.1-3.3-bullseye

RUN apt update && \
  apt-get install --no-install-recommends -y \
  build-essential \
  default-libmysqlclient-dev \
  mariadb-client \
  libvips \
  pkg-config \
  git

RUN su vscode -c "gem install rails:7.1.3"
RUN su vscode -c "/usr/local/rvm/bin/rvm fix-permissions"

WORKDIR "/devcontainer/ruby-devcontainer"
RUN bundle config set --local path vendor/bundle
