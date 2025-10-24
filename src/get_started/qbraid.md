# qBraid Lab で Qiskit を使う手順
[qBraid Lab](https://www.qbraid.com/)でQiskitを使う場合の手順です。はじめに 1 回 Qiskit をインストールすれば、次回からインストールなしで Qiskit を使うことができます。

**ご注意**：公式には、ご自身のパソコンにQiskitをインストールして使うことをおすすめしています。インストールの手順はこちら（[macOS版](https://qiita.com/kifumi/items/8f3617051635f986cc5f)、[Windows版](https://qiita.com/kifumi/items/d36d0601d963a17bcf93)）をご覧ください。

# 1. qBraid環境へのログイン
ブラウザーを開き、 https://www.qbraid.com/ のサイトに入り、右上の「START NOW」をクリックします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/58016fd4-2238-4751-98d0-65c353a8b6d6.png)


GoogleのID(gmail)かまたは、Emailアドレスでログインできます。Emailアドレスの場合は、下の方の「Create An Account」でアカウントを作ってログインします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/d8d9a778-20ca-51be-7445-4cf350e0fc8a.png)

Googleでログインする場合を紹介します。アカウントを選択します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/26f3e914-586b-043e-5c7d-d0e09715425c.png)

書かれていることに問題がなければ「次へ」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/2c38f21a-f1c1-add9-b40d-830c3cf3b7e9.png)

アンケートに答えない場合は「Skip」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/d3733b37-e4f6-179e-e298-91a22859cbd1.png)


# 2. qBraid Labでの最初の操作手順
上側中央のブロックの「Default Workspace」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/4718a0d0-ed32-455a-8dda-ec2717e8d05c.png)


引き続き、中央のブロックから一つラボイメージを選び、「Launch Lab」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/37b5fc82-a93c-47e1-8a74-cb4dbe78760e.png)

しばらくすると、以下のようにLab環境に入れます。使い方のツアーを見たくない人は「Stop Tour」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/c91753fd-70b1-47b0-b804-cf0ab2c68d22.png)

Qiskitを使って、IBM Quantumの実機の量子コンピューターを使うのであれば、課金は必要ないので、左の「Not Now」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/9e0c47ac-5537-42ef-9247-765372560297.png)

右側の「ENVIRONMENTS」枠から「＋ADD」をクリックすると、
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/931af54c-092c-678f-4d7d-29f70fb19de6.png)

たくさんの環境が出てきますので、「Qiskit」と名前のつく環境を探します。
検索バーで「qiskit」を検索して、さらに「Qiskit」をクリックすると、
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/6d06aea7-2776-4a27-8e57-81ae30d880f7.png)


以下のように様々なバージョンのQiskitカーネル環境が出てきますので、この中から最新のものを選びましょう。**注：2025年10月現在、最新は「Qiskit (V2.2.1)」ですがこちらは調子が悪いようなので「Qiksit(v2.0.2)」を選びます。** 
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/6b78fa11-3565-4908-b0f5-2dd945816006.png)

「Install」をクリックするとインストールが始まり、完了までしばらく時間がかかります。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/ab4eb341-c0a3-459c-8589-a30281c644d0.png)

インストールが終了すると真ん中の「Launcher」タブに、Qiskit印の「Python3[qiksit(v2.0.2)]」のアイコンが増えているので、こちらをクリックすると、
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/f721e44d-0010-48cf-bc03-0945d258f8dc.png)



新しいjupyter ノートブックが開きます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/b6e31ea8-7a3f-f77e-0ccd-814d6631e994.png)
不足している可能性のあるライブラリーをインストールしておきます。以下のコマンドをコピーして、最初のセルに貼り付け、「Shift」+「Enter」で実行します。
```
!pip install qiskit-ibm-runtime qiskit-aer
```

# 補足：ファイルアップロード時には Qiskit カーネルを選択
ファイルをアップロードして開いたノートブックは、デフォルトのPython 3 のカーネルが使われ、そのままではQiskitが使えないので、右上の「Python 3 [Default]」をクリックして、インストールしたQiskitの入っているカーネルを選んで実行してください。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/87369347-4987-6259-9b3d-2563a8f03138.png)



# 3. Qiskitで回路を作成
続けて、ベル状態(2量子ビットのエンタングルメント)の回路を作成して実行してみましょう。

以下のコードをノートブックの最初のセルに貼り付け、「Shift」+「Enter」で実行します。
```
from qiskit import QuantumCircuit
from qiskit_aer import AerSimulator
from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager
from qiskit_ibm_runtime import SamplerV2 as Sampler
from qiskit.visualization import plot_histogram

qc = QuantumCircuit(2,2)
qc.h(0) 
qc.cx(0,1) 
qc.measure(0, 0)
qc.measure(1, 1)
qc.draw(output="mpl")
```
注：`ModuleNotFoundError: No module named 'qiskit_aer'`のエラーが出て qiskit-aer がインストールされていなかった場合には、以下のコマンドで qiskit-aer をインストールし、再度上のコードを実行します。

```
!pip install qiskit_aer
```
問題ない場合には、以下のようにベル状態を作る量子回路が表示されるでしょう。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/fccb71fa-e014-4ab8-a585-ad97c4348257.png)

以下のコードでQiskit Aer シミュレーターを使って実行します。
```
# シミュレーターで実験
backend = AerSimulator()
sampler = Sampler(backend)
job = sampler.run([qc])
result = job.result()

#  測定された回数を表示
counts = result[0].data.c.get_counts()
print(counts)

# ヒストグラムで測定された確率をプロット
plot_histogram( counts )
```
以下のような結果が出てきたら成功です。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/a61a6e15-987c-48ec-b529-615251672d29.png)


IBMの実機の量子コンピューターで実行する手法はこちらをご確認ください：https://quantum-tokyo.github.io/introduction/get_started/bell.html


お疲れ様でした！

