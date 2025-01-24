# qBraid Lab で Qiskit を使う手順
[qBraid Lab](https://www.qbraid.com/)でQiskitを使う場合の手順です。旧IBM Quantum LabのようにWebブラウザー上からインストールなしでQiskitを使うことができます。

**ご注意**：[公式には、ご自身のパソコンにQiskitをインストール](https://docs.quantum.ibm.com/guides/install-qiskit)して使うことをおすすめしています。インストールの手順はこちら（[macOS版](install_mac.md)、[Windows版](install_win.md)）をご覧ください。

## 1. qBraid環境へのログイン
ブラウザーを開き、 https://www.qbraid.com/ のサイトに入り、右上の「START NOW」をクリックします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/288986d0-f689-802f-6d2e-4479a32a07c9.png)

GoogleのID(gmail)かまたは、Emailアドレスでログインできます。Emailアドレスの場合は、下の方の「Create An Account」でアカウントを作ってログインします。

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/d8d9a778-20ca-51be-7445-4cf350e0fc8a.png)

Googleでログインする場合を紹介します。アカウントを選択します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/26f3e914-586b-043e-5c7d-d0e09715425c.png)

書かれていることに問題がなければ「次へ」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/2c38f21a-f1c1-add9-b40d-830c3cf3b7e9.png)

アンケートに答えない場合は「Skip」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/d3733b37-e4f6-179e-e298-91a22859cbd1.png)


## 2. qBraid Labでの最初の操作手順
上側中央の紫色の「Launch Lab>」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/29799381-b8ad-09f4-ec19-f6e96abc453d.png)

右側一番上のFreeのタブの「Start」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/739bda57-6df6-747c-22ae-6ebdda223adf.png)

以下のようにLab環境に入れます。真ん中の紫の「Start Tour」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/b67cbb25-473d-3b5f-3ebd-0d2ddae89b16.png)


使い方のツアーを見たい方は「Next」を押していきます。見なくてもいい人は右上の「x」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/d39a4eb0-2430-c38e-5d89-7ce53453e5fc.png)

Qiskitを使って、IBM Quantumの実機の量子コンピューターを使うのであれば、課金は必要ないので、左の「Not Now」をクリックします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/f28e62af-776d-a831-1f78-a9d91e580505.png)

右側の「ENVIRONMENTS」枠から「＋ADD」をクリックして、
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/931af54c-092c-678f-4d7d-29f70fb19de6.png)

たくさんの環境が出てきますので、「Qiskit」と名前のつく環境を探します。
検索バーで「qiskit」を検索した結果、以下のように様々なバージョンのQiskitカーネル環境が出てきますので、この中から最新のものを選びましょう。2025年1月現在、最新は「QDC 2024」なので、今回はこちらを選びます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/3bc6063c-495f-d3e7-7b9a-9287a22ab1e7.png)

「Install」をクリックするとインストールが始まり、インストール終了までしばらく時間がかかります。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/9db02c64-2342-9fdf-17cb-2b00a8955d1b.png)

インストールが終了すると真ん中の「Launcher」タブに、Qiskit印の「Python 3[QGSS-24]」のアイコンが増えているので、こちらをクリックすると、
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/7245d828-3b80-4ec1-4515-81e01dcea8f2.png)

新しいjupyter ノートブックが開きます。この環境には、Qiskitがインストールされているため、そのままコーディングをすることができます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/b6e31ea8-7a3f-f77e-0ccd-814d6631e994.png)

**ファイルをアップロードして開いたノートブックは、デフォルトのPython 3 のカーネルが使われ、そのままではQiskitが使えないので、右上の「Python 3 [Default]」をクリックして、インストールしたQiskitの入っているカーネルを選んで実行してください。**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/87369347-4987-6259-9b3d-2563a8f03138.png)

## 3. Qiskit で Hello world
続けて、QiskitのHello worldを実行して、Qiskitが正しく動くか確認してみましょう。
[Qiskit公式ドキュメントのHello world](https://docs.quantum.ibm.com/start/hello-world) から最初のセルのコードをコピーします。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/2ed9083d-715a-b365-6b0d-6548eb739a14.png)

ノートブックの最初のセルに貼り付け、「Shift」+「Enter」で実行します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/5a0f0fb5-a95b-7628-18c9-a65930e9fd7b.png)

正しくQiskitが動いている場合は、以下の回路図が出力されます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151117/49937210-b757-9638-e800-89f4a042fb3e.png)

以上です！

