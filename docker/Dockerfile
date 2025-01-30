# ベースイメージとして NVIDIA PyTorch を使用
FROM pytorch/pytorch:2.1.0-cuda11.8-cudnn8-runtime

# 必要な依存関係をインストール
RUN apt-get update && apt-get install -y \
    curl \
    git \
    gpg \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリを作成
WORKDIR /workspace
RUN mkdir -p /workspace


# requirements.txt をコンテナにコピー
COPY requirements.txt .

# Pythonライブラリをインストール
RUN pip install --no-cache-dir -r requirements.txt

# デフォルトの作業ディレクトリを設定
CMD ["/bin/bash"]
