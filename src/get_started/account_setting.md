# IBM Cloud アカウント設定〜一般向け

IBM Cloud のトライアルアカウントの作成を行います。トライアルアカウントの期限は30日です。（延長するにはクレジットカードが必要です。）

1. https://quantum.cloud.ibm.com/registration を開き、Eメールとパスワードを設定し、「次のステップ」をクリックします。
![image.png](./images/account_1.jpg)

2. メールを確認し、IBM Cloud (no-reply@cloud.ibm.com) からの「Your IBM Cloud verification code」というタイトルのメールにある7桁の認証コードをコピペして、「次のステップ」をクリックします。
![image.png](./images/account_2.jpg)

3. 個人情報欄を全て埋めて「次のステップ」をクリックします。
![image.png](./images/account_3.jpg)

4. 「契約条件」を読み、よろしければチェックをして「続行」をクリックします。
![image.png](./images/account_4.jpg)

5. IBM Quantum Platform に自動的にログインします。「Terms」を読み、よろしければチェックして「Create instance」をクリックします。
![image.png](./images/account_5.jpg)

6. この画面になれば完了です。30日間のみ使えるアカウントで実機計算を合計10分試すことができます。
![image.png](./images/account_6.jpg)

以上で、IBM Cloud のアカウント設定は終了です。お疲れ様でした。


## API key と CRN の取得

実量子コンピューターで実験するため次の手順で、API keyとCRNを取得します。

1) https://quantum.cloud.ibm.com/ にサインインし、左側 「API key」の横にある「Create +」をクリックします。
![image.png](./images/apikey_1.png)

2) API keyの名前（例：my API など）を自由に入力し、「Create」をクリックします。
![image.png](./images/apikey_2.png)

3) 「Download」をクリックして「apikey.json」ファイルを保存します。
![image.png](./images/apikey_3.png)

4) 先ほど保存した「apikey.json」ファイルから、apikeyをコピーできます。
![image.png](./images/apikey_4.png)

5) CRNはこちらからコピーできます。
![image.png](./images/crn_image.png)

次は、[量子コンピューターの使い方〜量子回路の作成から実機実行までの手順](https://quantum-tokyo.github.io/introduction/get_started/bell.html) を参考に実際に使ってみましょう。
