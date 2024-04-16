Central ManagerへUCSファイルをインポート
======================================

前ページ手順で取得済みのUCSファイルは、Windows clientのデスクトップ上のフォルダに格納されています。

**デスクトップ > Handson Files > Backup UCS > udf-tmos-bigip.ucs**

.. note::

Windows client上のブラウザからCMへアクセスするか、ファイルを自身のPCへコピーしてから次の手順へ進んでください。


**"Applications"** 画面を開き、
My Application Servicesの画面から **”+ Add Application”** をクリックし、次画面で **”New Migration”** を選択します。

.. figure:: images/c10-m2-1.png
   :scale: 40%
   :align: center

.. figure:: images/c10-m2-2.png
   :scale: 50%
   :align: center

|
General Properties画面で、Migration Session名とDescriptionを設定します。

.. figure:: images/c10-m2-3.png
   :scale: 50%
   :align: center

- Session Name:
   - **my-1st-migration** (任意の名前)
- **"Next"** をクリック


|
CMへアップロードするUCSファイルを選択します。

.. figure:: images/c10-m2-4.png
   :scale: 50%
   :align: center

- 赤枠部分をクリックし、UCSファイルを選択します。
- Master keyをDisable
- **“Group by IP Addresses”** を選択
- **"Next"** をクリック


|
**Add Application** をクリックします。

.. figure:: images/c10-m2-5.png
   :scale: 70%
   :align: center


|
インポートされたApplicationのリストが確認できます。“Group by IP Addresses”を選択したため、同一IPで複数Portのものが同一Applicationにソートされて表示されています。

.. figure:: images/c10-m2-6.png
   :scale: 50%
   :align: center


|
それぞれのアプリケーションの移行可否のアセスメント結果が確認できます。（参考）

.. figure:: images/c10-m2-7.png
   :scale: 30%
   :align: center

.. figure:: images/c10-m2-8.png
   :scale: 40%
   :align: center
