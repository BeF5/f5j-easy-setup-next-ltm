設定マイグレーションの実行
======================================

UCSからインポートしたアプリケーションをNextインスタンスへデプロイします。

|
ステータスがグリーンのApplicationを選択して **"Add"** をクリックします。

.. figure:: images/c10-m3-1.png
   :scale: 60%
   :align: center


|
**"Next"** をクリックします。

.. figure:: images/c10-m3-2.png
   :scale: 60%
   :align: center


|
“Shared Objects”(iRule、証明書等の共通項目)の **"import"** をすべてクリックしてCMに取り込んだ後、 **”Deploy”** をクリックします。
Deploy Locationは"Save as Draft"のままとしておきます。ここで任意のNextインスタンスを選択することも可能です。

.. figure:: images/c10-m3-3.png
   :scale: 60%
   :align: center


|
正常にSuccessfulでDeployされたら **”Finish”** をクリックして閉じます。

.. figure:: images/c10-m3-4.png
   :scale: 60%
   :align: center


|
My Application Servicesを見ると、Draftとして(instanceへの割り当てなし)Applicationが作成されています。

.. figure:: images/c10-m3-5.png
   :scale: 50%
   :align: center


|
（参考）実運用では、通信切り替え前にアドレス重複を避けるために、既存TMOSのVirtual Serverを先にDisableします。

.. figure:: images/c10-m3-6.png
   :scale: 35%
   :align: center


|
DeployするApplication **"application_1"** をクリックします。

.. figure:: images/c10-m3-7.png
   :scale: 50%
   :align: center


|
**“Review & Deploy”** をクリックします。

.. figure:: images/c10-m3-8.png
   :scale: 50%
   :align: center


|
アプリケーションをデプロイするNextインスタンスを選択します。 **“Start Adding”** をクリックし、 **big01.f5lab.local** を選択して **"+ Add to List"** をクリックします。

.. figure:: images/c10-m3-9.png
   :scale: 50%
   :align: center

- **"big01.f5lab.local(10.1.1.7)"** を選択
- **"+ Add to List"** をクリック
- **“Deploy”** をクリック


|
Instance/Locationsが "1"と表示されるようになり、1インスタンスにデプロイされていることを示しています。

.. figure:: images/c10-m3-10.png
   :scale: 50%
   :align: center


|
デプロイしたApplicationをクリックすると、指定したInstanceで正常に動作していることが確認できます。

.. figure:: images/c10-m3-11.png
   :scale: 50%
   :align: center


