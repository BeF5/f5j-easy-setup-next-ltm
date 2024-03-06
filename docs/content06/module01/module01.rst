HTTPアプリケーションの設定
======================================

Standard(default “http” template)を利用したWebアプリケーションの作成
--------------------------------------

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
次ページの“Start Adding”をクリックし、デプロイするインスタンスを選択して”+Add to List”。

.. figure:: images/c6-m1-8.png
   :scale: 40%
   :align: center

- **“big01.f5lab.local”** をチェックボックスをチェックする



