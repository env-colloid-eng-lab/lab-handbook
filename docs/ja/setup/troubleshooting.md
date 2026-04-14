# トラブルシューティング

このページでは、よくある問題とその解決方法を紹介します。問題が解決しない場合は、このリポジトリに GitHub Issue を作成してください。

---

## conda: command not found

**原因：** Miniconda はインストールされているが、ターミナルを再起動していないか、conda が初期化されていない。

**解決方法：**

```bash
source ~/.bashrc   # Linux / WSL
source ~/.zshrc    # macOS（zsh）
```

それでも解決しない場合は、Miniconda インストーラーを再実行し、初期化のプロンプトに `yes` と答えてください。

---

## Python のバージョンが想定と異なる

**原因：** conda 環境の Python ではなく、システムの Python が使われている。

**解決方法：** 環境を有効にしてから確認します：

```bash
conda activate myenv
python --version
```

---

## VS Code が Python を認識しない

**解決方法：**
1. コマンドパレットを開きます（Ctrl+Shift+P / Cmd+Shift+P）。
2. `Python: Select Interpreter` と入力します。
3. 正しい Python パスを選択します（通常 `~/miniconda3/envs/...` の下にあります）。

---

## git push でパスワードを何度も求められる

**原因：** SSH の代わりに HTTPS が使われているか、認証情報がキャッシュされていない。

**解決方法：** SSH 認証に切り替えてください。設定手順は [Git と GitHub](git-github.md) を参照してください。

---

## WSL がインターネットに接続できない

**解決方法：**
```bash
# WSL の DNS 設定をリセット
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf
```

問題が続く場合は WSL を再起動します：
```powershell
wsl --shutdown
```
その後、Ubuntu ターミナルを再度開いてください。

---

## macOS で Homebrew のインストールが失敗する

**解決方法：** 先に Xcode コマンドラインツールをインストールしてください：

```bash
xcode-select --install
```

その後、Homebrew のインストールを再試行してください。

---

[← セットアップ概要へ戻る](index.md)
