# Google Colab で Qiskit を使う手順

Google Colaboratory でQiskitを使いたい場合の手順です。

**ご注意**：Google Colabでは、毎回、Qiskitのインストールが必要になってしまうので、公式にはご自身のパソコンにQiskitをインストールして使うことをおすすめしています。インストールの手順はこちら（[macOS版](install_mac.md)、[Windows版](install_win.md)）をご覧ください。
また、qBraidの場合は、はじめに1回インストールするのみで毎回のインストールは必要ありません。[「qBraid LabでQiskitを使う手順」](qbraid.md)をご参照ください。

## 1. クラウド環境へのログイン
ブラウザーを開き、 https://colab.research.google.com/ のサイトに入り、右上の「ログイン」からログインします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/b25ea38f-e18d-8c5b-0220-0af4ed1cf4e8.png)

## 2. ノートブックを開く
以下のいずれかの方法で、ノートブックを開きます。
- 左下の「＋ノートブックを新規作成」をクリック。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/5929f457-cdb1-6127-6102-d01f9bcaa247.png)
- 上記のウィンドウが出てこなかった場合、左上の「ファイル」→「ノートブックを新規作成」をクリック。

## 3. Qiskit をインストール
以下のコマンドを最初のセルに入れて、「Shift」+「Enter」で実行します。Qiskitと関連ライブラリーがインストールされます。
```
!pip install qiskit qiskit-ibm-runtime jupyter qiskit-aer qiskit[visualization]
```

## 4. Qiskit で Hello world
続けて、QiskitのHello worldを実行して、Qiskitが正しく動くか確認してみましょう。
[Qiskit公式ドキュメントのHello world](https://docs.quantum.ibm.com/start/hello-world) から最初のセルのコードをコピーします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/2ed9083d-715a-b365-6b0d-6548eb739a14.png)

ノートブックの次のセルに貼り付け、「Shift」+「Enter」で実行します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/5a0f0fb5-a95b-7628-18c9-a65930e9fd7b.png)

正しくQiskitが動いている場合は、以下の回路図が出力されます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/49937210-b757-9638-e800-89f4a042fb3e.png)

## 5. 次にQiskitを使う場合
次にQiskitを使う場合や、新しいノートブックを立ち上げた場合、上記の3の手順を毎回行います。

以上です！





