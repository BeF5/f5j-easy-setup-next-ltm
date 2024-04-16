HTTPアプリケーションの設定
======================================


Standard(default “http” template)を利用したWebアプリケーションの作成
----------------------------------------------------------

CM画面左上部のworkspaceから、”Applications”を選択します。

.. figure:: images/c6-m1-1.png
   :scale: 50%
   :align: center

|
”Start Adding Apps”をクリックします。

.. figure:: images/c6-m1-2.png
   :scale: 50%
   :align: center

|
新規アプリケーション作成を開始するにあたりアプリケーション名とテンプレート選択をおこないます。

.. figure:: images/c6-m1-3.png
   :scale: 50%
   :align: center

- Application Service Name:
   - **HTTP-Service**　（任意の名前）
- What kind of Application:
   - **Standard**　を選択
- **“Start Creating”** をクリック

|
次ページで表示される **“Start Creating”** をクリックします。

.. figure:: images/c6-m1-4.png
   :scale: 50%
   :align: center


|
Application Service Propertiesの設定画面で、Virtual Server、Pool、Protocol Profiles等の構成を定義します。

.. figure:: images/c6-m1-5.png
   :scale: 30%
   :align: center

- Virtual Server Name:
   - **HTTP-VS**
- **“Pools”** タブをクリック


|
Poolを作成します。　Pool memberのIPは後工程のアプリケーションDeploy時に設定します。

右の **"+ Create"** をクリックします。

.. figure:: images/c6-m1-6.png
   :scale: 35%
   :align: center

- Pool Name:
   - **http-pool**
- Server Port:
   - **80**
- Load-Balancing Mode:
   - **round-robin**
- Monitor Type:
   - **http**
- 上記設定後、再度 **”Virtual Server”** タブに戻る


|
再度Virtual Server設定で、作成したPoolを選択します。

.. figure:: images/c6-m1-7.png
   :scale: 30%
   :align: center

- Pool:
   - **http-pool**　を選択
- **“Review & Deploy”** をクリック


|
次ページの“Start Adding”をクリックし、設定をデプロイするインスタンスを選択して”+Add to List”をクリックします。

.. figure:: images/c6-m1-8.png
   :scale: 40%
   :align: center

- **“big01.f5lab.local”** のチェックボックスをチェックする
- **“+Add to List”** をクリック


|
次のDeploy画面で、Virtual ServerのIPとPool memberを設定します。

.. figure:: images/c6-m1-9.png
   :scale: 30%
   :align: center

- Virtual Address:
   - **10.1.10.100**
- Membersの下矢印を展開し、 **“+Pool Members”** をクリック


|
Pool memberを設定します。

.. figure:: images/c6-m1-10.png
   :scale: 30%
   :align: center

- **“+Add Row”** を２回クリックし2member分作成
- Pool Members:
   - Name: **web-server1** , IP Address: **10.1.20.101**
   - Name: **web-server2** , IP Address: **10.1.20.102**
- 入力後、 **”Save”** をクリック


|
設定内容に問題ないかを適用前に検証し、本番適用します。

.. figure:: images/c6-m1-11.png
   :scale: 30%
   :align: center

- **“Validate All”** をクリックして設定内容を検証、エラーがなく”Validated”の結果が表示されること
- **“View Results”** で設定反映されるAPI内容を確認可能です
- **“Deploy Changes”** をクリックし、次に表示される画面で **”Yes, Deploy”** をクリックします


|
作成したアプリケーションがリストに表示されます。

.. figure:: images/c6-m1-12.png
   :scale: 50%
   :align: center


|
作成したアプリケーションをクリックすると、設定オブジェクトと状態確認、設定編集が可能です。

.. figure:: images/c6-m1-13.png
   :scale: 35%
   :align: center





