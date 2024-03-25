設定マイグレーションの実行
======================================

UCSからインポートしたアプリケーションをNextインスタンスへデプロイします。

|
ステータスがグリーンのApplicationを選択して **"Add"** をクリックします。

.. figure:: images/c10-m3-1.png
   :scale: 80%
   :align: center


|
**"Next"** をクリックします。

.. figure:: images/c10-m3-2.png
   :scale: 80%
   :align: center


|
“Shared Objects”(iRule、証明書等の共通項目)の **"import"** をクリックしてCMに取り込んだ後、 **”Deploy”** をクリックします。

.. figure:: images/c10-m3-3.png
   :scale: 80%
   :align: center


|
正常にSuccessfulでDeployされたら **”Finish”** をクリックして閉じます。

.. figure:: images/c10-m3-4.png
   :scale: 50%
   :align: center


|
My Application Servicesを見ると、Draftとして(instanceへの割り当てなし)Applicationが作成されています。

.. figure:: images/c10-m3-5.png
   :scale: 50%
   :align: center


|
（参考）実運用では、通信切り替え前にアドレス重複を避けるために、既存TMOSのVirtual Serverを先にDisableします。

.. figure:: images/c10-m3-6.png
   :scale: 50%
   :align: center
