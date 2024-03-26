HAクラスタのセットアップ
======================================

HAクラスタを設定していきます。
HA Active機とするBIG-IP Nextインスタンス#1(10.1.1.7)のMode “Standalone”をクリックします。

.. figure:: images/c11-m2-1.png
   :scale: 40%
   :align: center


|
左メニューからHAを選択し、 **”Enable HA”** をクリックします。

.. figure:: images/c11-m2-2.png
   :scale: 50%
   :align: center


|
ドロップダウンからStandbyノードを選択します。

.. figure:: images/c11-m2-3.png
   :scale: 50%
   :align: center

- Available Standalone Instances:
   - **big02.f5lab.local**
- **”Next”** をクリック




|
**HA Control Plane VLAN** を設定します。
Control Plane VLAN新規作成のための **”Create VLAN”** をクリックします。

.. figure:: images/c11-m2-4.png
   :scale: 50%
   :align: center

|
VLANの設定情報を入力します。

.. figure:: images/c11-m2-5.png
   :scale: 50%
   :align: center

- Name:
   - **control-plane-vlan**
- Tag:
   - **3999**
- **”Done”** をクリック


|
**HA Data Plane VLAN** を設定します。
Data Plane VLAN新規作成のための **”Create VLAN”** をクリックします。

.. figure:: images/c11-m2-6.png
   :scale: 50%
   :align: center

|
VLANの設定情報を入力します。

.. figure:: images/c11-m2-7.png
   :scale: 50%
   :align: center

- Name:
   - **data-plane-vlan**
- Network Interface:
   - **1.3**
- **”Done”** をクリック
- 次画面の **”Next”** をクリック


|
HA Propertiesを設定します。

.. figure:: images/c11-m2-8.png
   :scale: 65%
   :align: center

- HA Name:
   - **ha1**
- HA Management(Floating) IP Address:
   - **10.1.1.9**

*Active Node*

- Control Plane Address:
   - **10.1.1.77/24**
- Data Plane Primary Address:
   - **10.1.30.7/24**

*Standby Node*

- Control Plane Address:
   - **10.1.1.88/24**
- Data Plane Primary Address:
   - **10.1.30.8/24**
|
- **”Next”** をクリック
