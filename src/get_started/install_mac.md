---
title: Qiskit 1.0のインストール手順 (macOS版)
tags: QISKIT 量子コンピューター 量子コンピュータ
author: kifumi
slide: false
---
# Qiskit 1.x のインストール手順 (macOS版)
[Qiskit 1.x](https://www.ibm.com/quantum/qiskit) をmacOSにインストールします。（Windows版は[こちら](install_win.md)です。）
[公式インストール手順](https://docs.quantum.ibm.com/start/install)をもとに行います。

注意点：以前のバージョンのQiskitをご自身の環境にインストールしたことがある方は、上書きアップグレードをしないでください。エラーが発生しやすくなります。

## 1. 「ターミナル」を起動
以下のいずれかの操作で、「ターミナル」を起動します。
- DockでLaunchpadのアイコンをクリックして、検索フィールドに「ターミナル」と入力してから、「ターミナル」をクリックします。
- Finder で、「/アプリケーション/ユーティリティ」フォルダを開いてから、「ターミナル」をダブルクリックします。

## 2. Pythonの新しい仮想環境を作成する
以下のコマンドで `qiskit_env` の部分にご自分の使いたい仮想環境名（ディレクトリー名）と必要であればそのパスを入れ、実行します。

```
python3 -m venv qiskit_env
```

## 3. 仮想環境をActivateする
以下のコマンドで `qiskit_env` に作成した仮想環境名を入れて実行します。
```
source qiskit_env/bin/activate
```
正しく仮想環境に入れていれば、以下の図のように、ターミナルのコマンドラインの左端に作った仮想環境名が `(仮想環境名)` という状態で現れます。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/7525a607-c6c4-7b82-98b9-4fa785aae442.png)

## 4. pip のインストール
[pip](https://pip.pypa.io/en/stable/installation/)がインストールされているか確認します。
```
pip --version
```
インストールされている場合は、以下のようなメッセージが出ます。
```pip 24.0 from /Users/../../qiskit_env/lib/python3.12/site-packages/pip (python 3.12)```
インストールされていない場合は、以下のようなメッセージが出ます。
```zsh: command not found: pip```
インストールされていなかった場合は、以下のコマンドでpipをインストールします。
```
python3 -m ensurepip --upgrade
```

## 5. Qiskit のインストール
以下のコマンドでQiskitをインストールします。
```
pip install qiskit
```
## 6. 必要なライブラリーをインストール
Qiskit本体以外に必要となるライブラリーをインストールします。
```
pip install qiskit-ibm-runtime jupyter qiskit-aer
```
表示に必要なライブラリーをインストールします。以下のどちらかを実行してください。
- zshシェルの方：
```
pip install 'qiskit[visualization]'
```
- bashシェルの方：
```
pip install qiskit[visualization]
```
## 7. Qiskit で Hello world
続けて、QiskitのHello worldを実行して、Qiskitが正しく動くか確認してみましょう。
以下のコマンドで、Jupyter notebookを立ち上げます。
```
jupyter notebook
```
以下のようにChromeなどのウェブブラウザーが起動します。右上の「New」をクリックし、「Python 3」を選んで、新しいNotebookを起動します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/57f9b06c-d797-67f4-44d8-d61946521602.png)

[公式QiskitドキュメントのHello world](https://docs.quantum.ibm.com/start/hello-world) から最初のセルのコードをコピーします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/f28ca8d6-99ac-e749-2fa6-daaaf1632445.png)

自分のNotebookのセルに貼り付けます。「Shift」+「Enter」かまたは、上の方にある右向き三角アイコンで実行できます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/7ceccdb1-66eb-80ee-3a35-d1dffbab177f.png)

正しくQiskitが動いている場合、以下の回路図が表示されます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/ff7df460-6907-9956-fb16-27f7c22a79df.png)

ファイルを閉じるには、左上の「File」→「Close and Shut Down Notebook」→「Ok」で終了できます。
Jupyter notebookの環境を修了するには、ターミナルに戻り「Ctrl」+「c」のあと、「y」と入れて「Enter」キーを押します。
ターミナルで以下のコマンドを実行すると、仮想環境から抜けることができます。
```
deactivate
```

## 8. インストール後、再度、Qiskitを使う時
次にQiskitを使う時は、以下のようにしてください。
### 1. ターミナルから仮想環境の立ち上げ
```
source qiskit_env/bin/activate
```
### 2. Jupyter notebookの立ち上げ
```
jupyter notebook
```
ここで新しいPython3のNotebookを立ち上げて、Qiskitを使うことができます。

### 3. Jupyter notebookの終了
必要なNotebookをSaveした後、ターミナルで「Ctrl」+「c」のあと、「y」と入れて「Enter」キー。
### 4. 仮想環境の終了
```
deactivate
```

以上です。お疲れ様でした！

