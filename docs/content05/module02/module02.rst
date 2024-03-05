Nextインスタンス　ライセンスアクティベーション
======================================

ライセンスオーバービュー
--------------------------------------

.. figure:: images/c5-m2-1.png
   :scale: 50%
   :align: center
|
- BIG-IP Nextインスタンス用のライセンスは、Central ManagerにLoadし、Central Managerがライセンス管理を行う
- Central Managerが、F5のライセンスサーバと通信を行い利用状況等をチェック
- BIG-IP Next Central Manager自体には、ライセンスは不要 (無償製品)
- 参考URL
  - https://clouddocs.f5.com/bigip-next/latest/use_cm/cm_license_bigip_next.html 

|
ライセンスの入手
--------------------------------------

MyF5よりTrialライセンス(JWTキー)を入手します。

- https://my.f5.com/

.. note::
   MyF5アカウントをお持ちの場合は、自身のアカウントからライセンス発行いただいてご利用ください。あるいはUDFハンズオン環境のWindows ClientのDesktop上に準備済みの仮ライセンスをご利用ください。

"TRIALS"をクリックします。

.. figure:: images/c5-m2-2.png
   :scale: 50%
   :align: center


|
"BIG-IP Next"をクリックします。

.. figure:: images/c5-m2-3.png
   :scale: 50%
   :align: center


|
“Downloads and licenses”をクリックします。

.. figure:: images/c5-m2-4.png
   :scale: 50%
   :align: center


|
“Copy JSON Web Token”をクリックしてテキストエディタにペーストしておくか、Downloadして保存しておきます。

.. figure:: images/c5-m2-5.png
   :scale: 50%
   :align: center


|
ライセンスのインストール
--------------------------------------

BIG-IP Next CMにログインし、Infrastructure (Manage Instances)の画面で、ライセンスをアクティベーションするインスタンスをクリックします。

.. figure:: images/c5-m2-6.png
   :scale: 35%
   :align: center

|
左部メニューから **“License”** を選択し、 **“Activate License”**をクリックします。

.. figure:: images/c5-m2-7.png
   :scale: 35%
   :align: center

|
確認画面で **"Next"** をクリックします。

.. figure:: images/c5-m2-8.png
   :scale: 35%
   :align: center

|
