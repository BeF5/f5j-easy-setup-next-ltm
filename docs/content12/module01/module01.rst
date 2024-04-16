Nextインスタンスのバックアップ
======================================

CMのMy Instances画面から、バックアップするインスタンスを選択し、右上の“Actions”メニューから”Back UP & Schedule”をクリックします。

.. figure:: images/c12-m1-1.png
   :scale: 50%
   :align: center

|
Backup Credentialsで、リストア時に使用するPasswordを設定します。

.. figure:: images/c12-m1-2.png
   :scale: 50%
   :align: center

- Encryption Password/Confirm Password:
   - **backup123**
- **“Schedule Backup →”** をクリック


|
Schedule Propertiesを設定します。今すぐOne timeでバックアップさせるようなオプションが現時点ないため、デイリー（日次実行）でバックアップを取る時刻と、このスケジュールタスクの終了日時の設定をします。

.. figure:: images/c12-m1-3.png
   :scale: 50%
   :align: center

- Frequency:
   - **Daily**
- Start:
   - (現在から5分後くらいの時刻を指定します)
- End:
   - End on: (適当に翌日等に設定します)
- **“Next →”** をクリック


|
サマリー画面を確認して、 **“Save Schedule”** をクリックします。

.. figure:: images/c12-m1-4.png
   :scale: 50%
   :align: center


|
Backup & Restore画面の“View Schedules”をクリックすると、スケジュールされた設定が確認可能です。
スケジュール日時を経過すると、バックアップファイルが作成され表示されます。

.. figure:: images/c12-m1-5.png
   :scale: 35%
   :align: center




