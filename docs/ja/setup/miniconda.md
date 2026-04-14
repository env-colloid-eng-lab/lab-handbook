# Miniconda

Miniconda は `conda` パッケージマネージャーを含む軽量な Python ディストリビューションです。このラボでは Python 環境の管理に Miniconda を推奨しています。

## 1. Miniconda のダウンロード

公式ページから OS に合ったインストーラーをダウンロードします：  
[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

- **Windows**：`.exe` インストーラーをダウンロードして実行します（WSL 内では Linux インストーラーを使用）。
- **macOS / Linux**：`.sh` インストーラーをダウンロードします。

## 2. Miniconda のインストール（macOS / Linux / WSL）

ダウンロードした `.sh` インストーラーを実行します：

```bash
bash <ダウンロードした .sh ファイル名>
```

例：
- **Linux (x86_64)**：`bash Miniconda3-latest-Linux-x86_64.sh`
- **macOS (Intel)**：`bash Miniconda3-latest-MacOSX-x86_64.sh`
- **macOS (Apple Silicon)**：`bash Miniconda3-latest-MacOSX-arm64.sh`

プロンプトに従ってインストールします。conda を初期化するか聞かれたら `yes` と答えてください。

ターミナルを再起動し、以下で確認します：

```bash
conda --version
```

## 3. 新しい環境の作成

プロジェクトごとに専用の環境を作成することを推奨します：

```bash
conda create -n myenv python=3.11
conda activate myenv
```

## 4. よく使うパッケージのインストール

```bash
conda install numpy pandas matplotlib jupyter
```

## 5. よく使う conda コマンド

| コマンド | 説明 |
|----------|------|
| `conda activate myenv` | 環境を有効にする |
| `conda deactivate` | 現在の環境を無効にする |
| `conda env list` | 全環境の一覧を表示 |
| `conda install <パッケージ名>` | パッケージをインストール |
| `conda update conda` | conda 自体を更新 |

---

[← セットアップ概要へ戻る](index.md)
