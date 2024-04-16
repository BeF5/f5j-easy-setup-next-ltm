Central ManagerへのNextインスタンス登録
======================================

UDF環境からCM GUIへのアクセス
--------------------------------------

UDF画面上部タブの"DEPLOYMENT"をクリックし、BIG-IP Next Central Managerインスタンスの"ACCESS" > "GUI" を選択します。

.. figure:: images/c5-m1-1.png
   :scale: 50%
   :align: center


|
|
BIG-IP Next CM GUIへのログイン
--------------------------------------

ログインプロンプトが表示されたら、ユーザ名/パスワードを入力してログインします。

.. figure:: images/c5-m1-2.png
   :scale: 50%
   :align: center

- ユーザー名/パスワード:
   - **admin/Welcome123!**


ログインすると次のようなホーム画面が確認できます。

.. figure:: images/c5-m1-3.png
   :scale: 50%
   :align: center


|
|
BIG-IP Next Instance1 をCMへ登録
--------------------------------------

ホーム画面の"Manage Instances"をクリックします。

.. figure:: images/c5-m1-4.png
   :scale: 50%
   :align: center


|
“Start Adding Instances”をクリックします。

.. figure:: images/c5-m1-5.png
   :scale: 50%
   :align: center

|
NEXTインスタンスのIPアドレスを入力します。

.. figure:: images/c5-m1-6.png
   :scale: 50%
   :align: center

- IP Address/FQDN:
   - **10.1.1.7**
- **"Connect"** をクリック


|
NEXTインスタンスのCredentialを入力します。

.. figure:: images/c5-m1-7.png
   :scale: 50%
   :align: center

- Username:
   - **admin**
- Password:
   - **Welcome123!**
- **"Next"** をクリック


|
BIG-IP Next CMからNextインスタンスを管理するためのCredentialを設定し、”Add Instance”クリックします。

.. figure:: images/c5-m1-8.png
   :scale: 50%
   :align: center

- Username:
   - **admin-cm**
- Password/Confirm Password:
   - **Welcome123!**
- **"Add Instance"** をクリック


|
確認画面が表れますので、”Add”クリックします。

.. figure:: images/c5-m1-9.png
   :scale: 50%
   :align: center

- **"Add"** をクリック


|
すると、以下のようにBIG-IP Nextインスタンスが管理インスタンスリストに追加されます。

.. figure:: images/c5-m1-10.png
   :scale: 30%
   :align: center
