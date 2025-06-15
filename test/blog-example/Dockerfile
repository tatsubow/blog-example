# 公式 Node.js イメージを使用
FROM node:18

# 作業ディレクトリを作成
WORKDIR /app

# 依存関係をコピー
COPY package*.json ./

# 依存関係をインストール
RUN npm install

# アプリのコードをコピー
COPY . .

# ビルド（Next.jsの場合は事前ビルドするか、devモードで実行）
RUN npm run build

# ポート3000を公開（Next.jsの場合）
EXPOSE 3000

# アプリを起動（開発モードなら `dev`、本番なら `start`）
CMD ["npm", "start"]
