# Git と GitHub

このガイドでは、バージョン管理のために Git と GitHub をセットアップする基本手順を説明します。

## 1. Git のインストール

- **Windows（WSL / Ubuntu）**：`sudo apt install -y git`
- **macOS**：`brew install git`（[macOS セットアップ](mac.md) を参照）
- **Linux**：`sudo apt install -y git`

確認：

```bash
git --version
```

## 2. Git の初期設定

コミット履歴に表示される名前とメールアドレスを設定します：

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

## 3. GitHub アカウントの作成

アカウントをまだ持っていない場合は、以下で無料アカウントを作成します：  
[https://github.com/](https://github.com/)

大学のメールアドレスまたは個人のメールアドレスを使用してください。

## 4. GitHub との認証設定

認証には **SSH キー** または **GitHub CLI** を推奨します。

### 方法 A：SSH キー

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
cat ~/.ssh/id_ed25519.pub
```

出力をコピーし、GitHub に追加します：**Settings → SSH and GPG keys → New SSH key**

### 方法 B：GitHub CLI

```bash
# macOS
brew install gh

# Ubuntu / WSL
sudo apt install gh

# 認証
gh auth login
```

## 5. リポジトリのクローン

```bash
git clone git@github.com:<ユーザー名>/<リポジトリ名>.git
```

## 6. 基本的な Git ワークフロー

```bash
git status           # 変更内容を確認
git add .            # すべての変更をステージ
git commit -m "msg"  # コミット
git push             # GitHub にプッシュ
git pull             # 最新の変更を取得
```

---

[← セットアップ概要へ戻る](index.md)
