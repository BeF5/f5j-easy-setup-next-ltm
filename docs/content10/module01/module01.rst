TMOSバックアップファイル(UCS)の準備
======================================

.. note::
   UDFハンズオンラボではUCSファイルは取得済みで準備してありますので、本手順は実施不要です。想定シナリオでの参考情報として掲載しています。

次のNW構成図のように稼働中のClassic BIG-IP(TMOS)が存在し、そこからBIG-IP Next#1へ移行するシナリオを想定しています。

.. figure:: images/c10-m1-1.png
   :scale: 40%
   :align: center


|
多数のVirtual Serverが設定されています。

.. figure:: images/c10-m1-2.png
   :scale: 50%
   :align: center


|
System> Archivesから、"big-ip-ucs"というファイル名でUCSバックアップを作成しています。

.. figure:: images/c10-m1-3.png
   :scale: 50%
   :align: center


|
Archivesリストから作成したUCSファイルをクリックし、DownloadしてローカルPCの任意の場所に保存します。これでUCSファイルの準備は完了です。

.. figure:: images/c10-m1-4.png
   :scale: 50%
   :align: center


