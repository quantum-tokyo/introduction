# Qiskit のインストール手順 (Windows版)
[Qiskit](https://www.ibm.com/quantum/qiskit) をWindowsにインストールします。（macOS版は[こちら](install_mac.md)です。）
[公式インストール手順](docs.quantum.ibm.com/start/install)をもとに行います。

注意点：Qiskit 0.x をご自身の環境にインストールしたことがある方は、上書きアップグレードをしないでください。エラーが発生しやすくなります。


## 0. 「Python」のインストール
こちらのページ[「Windows版Pythonのインストール」](https://www.python.jp/install/windows/install.html)を参考に、Pythonをインストールします。

## 1. 「PowerShell」を起動
以下の操作で、「Windows PowerShell」を起動します。
- 画面左下の[スタート] メニューを開き、「Windows PowerShell」と入力し、[Windows PowerShell] を選択した後、[開く] を選択します。

## 2. Pythonの新しい仮想環境を作成する
以下のコマンドで `qiskit_env` の部分にご自分の使いたい仮想環境名（ディレクトリー名）と必要であればそのパスを入れ、実行します。

```
python -m venv qiskit_env
```

## 3. 仮想環境をActivateする
以下のコマンドで `qiskit_env` に作成した仮想環境名を入れて実行します。
```
qiskit_env\Scripts\Activate.ps1
```
正しく仮想環境に入れていれば、以下の図のように、PowerShellのコマンドラインの左端に作った仮想環境名が `(仮想環境名)` という状態で現れます。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/2894e5a6-e6b0-19ad-29e0-609489c3bb5c.png)


## 4. pip のインストール
[pip](https://pip.pypa.io/en/stable/installation/)がインストールされているか確認します。
```
pip --version
```
インストールされている場合は、以下のようなメッセージが出ます。

```pip 24.0 from C:\Users\...\qiskit_env\Lib\site-packages\pip (python 3.12)```

インストールされていない場合は、以下のようなメッセージが出ます。

```'pip' is not recognized as an internal or external command, operable program or batch file.```

インストールされていなかった場合は、以下のコマンドでpipをインストールします。
```
py -m ensurepip --upgrade
```

## 5. Qiskit のインストール
以下のコマンドでQiskitをインストールします。
```
pip install qiskit
```
## 6. 必要なライブラリーをインストール
Qiskit本体以外に必要となるライブラリーをインストールします。
```
pip install qiskit-ibm-runtime jupyter qiskit-aer qiskit[visualization]
```

## 7. Qiskit で Hello world
続けて、QiskitのHello worldを実行して、Qiskitが正しく動くか確認してみましょう。
以下のコマンドで、Jupyter notebookを立ち上げます。
```
jupyter notebook
```
以下のようにEdgeなどのウェブブラウザーが起動します。右上の「New」をクリックし、「Python 3」を選んで、新しいNotebookを起動します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/ede8f62f-ce17-95b1-c774-48b720567093.png)


[IBM Quantum Platform 資料のハローワールド](https://quantum.cloud.ibm.com/docs/ja/tutorials/hello-world) から最初のセルのコードをコピーします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/f28ca8d6-99ac-e749-2fa6-daaaf1632445.png)

自分のNotebookのセルに貼り付けます。「Shift」+「Enter」かまたは、上の方にある右向き三角アイコンで実行できます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/7ceccdb1-66eb-80ee-3a35-d1dffbab177f.png)

正しくQiskitが動いている場合、以下の回路図が表示されます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/ff7df460-6907-9956-fb16-27f7c22a79df.png)

ファイルを閉じるには、左上の「File」→「Close and Shut Down Notebook」→「Ok」で終了できます。
Jupyter notebookの環境を修了するには、PowerShellに戻り「Ctrl」+「c」を押します。
PowerShellで以下のコマンドを実行すると、仮想環境から抜けることができます。
```
deactivate
```

## 8. インストール後、再度、Qiskitを使う時
次にQiskitを使う時は、以下のようにしてください。
### 1. PowerShellから仮想環境の立ち上げ
```
qiskit_env\Scripts\Activate.ps1
```
### 2. Jupyter notebookの立ち上げ
```
jupyter notebook
```
ここで新しいPython3のNotebookを立ち上げて、Qiskitを使うことができます。

### 3. Jupyter notebookの終了
必要なNotebookをSaveした後、PowerShellで「Ctrl」+「c」。
### 4. 仮想環境の終了
```
deactivate
```

以上です。お疲れ様でした！

