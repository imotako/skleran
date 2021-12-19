FROM python:3.9-slim

# パッケージのインストール
RUN apt-get update && apt-get install -y \
    tzdata \
 && rm -rf /var/lib/apt/lists/*

# モジュールインストール
WORKDIR /tmp/work
COPY requirements.txt ${PWD}
RUN pip install -r requirements.txt

# 環境変数の定義
ENV TZ=Asia/Tokyo
ENV USER user1
