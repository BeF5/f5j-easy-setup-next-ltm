デバッグ・ユーティリティの利用方法 (Central Manager GUI)
=====================================================

デバッグ・ユーティリティは、以下の方法で利用可能です。

クライアントでSSH公開鍵を作成
--------------------------------------

クライアント端末で、SSH公開鍵を取得もしくは作成します (例: ~/.ssh/id_rsa.pub)。各OSにおける詳細な手順につきましては、以下のドキュメントをご参照ください。
https://clouddocs.f5.com/bigip-next/latest/support/debug_utility.html#retrieve-client-ssh-public-key

.. note::
   F5 UDFラボのWindows 10 ClientにはSSH公開鍵には含まれていないため、上記ドキュメントの手順に従って、ssh-keygenコマンド (PowerShell)でSSH公開鍵を生成してください。


BIG-IP Central Managerでデバッグ・セッションを設定
--------------------------------------

My instancesから、デバッグ・セッションを行うBIG-IP Nextインスタンスを選択します。

.. figure:: images/c14-m1-1.png
   :scale: 25%
   :align: center


|
“Debug”を選択し、“Proceed”をクリックします。

.. figure:: images/c14-m1-2.png
   :scale: 35%
   :align: center


|
クライアント端末で作成したSSH公開鍵をコピーして、"Start Debug Session"をクリックします。

.. figure:: images/c14-m1-3.png
   :scale: 25%
   :align: center


|
Central Manager GUIに表示されたSSHコマンドを、ターミナルソフトで実行します。

.. figure:: images/c14-m1-4.png
   :scale: 35%
   :align: center


|
NextインスタンスにSSH接続できることを確認します。

.. figure:: images/c14-m1-5.png
   :scale: 60%
   :align: center


|
デバッグ・セッション中にNextインスタンス上で利用可能なコマンドの詳細については、以下のドキュメントをご参照ください。

https://clouddocs.f5.com/bigip-next/latest/support/debug_utility.html#f5-custom-tools

|
デバッグ・セッションの終了
--------------------------------------

Central Manager GUIで、"Stop Debug Session"をクリックします。

.. figure:: images/c14-m1-6.png
   :scale: 60%
   :align: center


|
ターミナルのセッションが終了したことを確認します。

.. figure:: images/c14-m1-7.png
   :scale: 30%
   :align: center

|
