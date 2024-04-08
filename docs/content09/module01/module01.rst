iRuleの作成
======================================

「HTTPリクエストの特定のURI path(/test)の場合、任意のコンテンツを返す」 内容のiRuleを作成していきます。

iRule作成
--------------------------------------

CM画面左上部のworkspaceから、”Applications”を選択します。

.. figure:: images/c9-m1-1.png
   :scale: 50%
   :align: center


|
左メニューから **”iRules”** を選択し、右上の **”+ Create”** をクリックします。

.. figure:: images/c9-m1-2.png
   :scale: 50%
   :align: center


|
次のiRuleスクリプトを、iRule設定画面にコピー＆ペーストします。


.. code-block:: cmdin

    when HTTP_REQUEST {
        if { [HTTP::uri] eq "/test"} {
            set content "<!doctype html>\n
            <head lang=\"en\">\n
            <meta charset=\"utf-8\">\n
            <title>Test Page</title>\n
            </head>\n
            <body>\n
              <h3>Test Page</h3>\n
                <ul>\n
                  <li> Virtual server address: [IP::local_addr] </li>\n
                  <li> Client IP:port: [IP::client_addr]:[TCP::client_port]</li>\n
                </ul>\n</body>\n</html>"
            HTTP::respond 200 content $content
        }
    }

|

- 作成するiRuleのスクリプト内容

  - HTTP Requestイベント時
  - URI Path "/test" へのアクセスの場合、“Test Page”のhtmlコンテンツとステータスコード200をレスポンスする


|
.. figure:: images/c9-m1-3.png
   :scale: 40%
   :align: center

- Name:
   - **irule-test**
- 上記赤枠のフィールドに前ページのiRuleをコピーペーストし、 **”Save”** をクリック


|
アプリケーションへの適用
--------------------------------------

My Application Servicesから作成済みの”HTTP-Service”をクリックします。

.. figure:: images/c9-m1-4.png
   :scale: 60%
   :align: center


|
次画面右上の”Edit”をクリックします。

.. figure:: images/c9-m1-5.png
   :scale: 50%
   :align: center


|
iRuleの"Edit"ボタンをクリックします。

.. figure:: images/c9-m1-6.png
   :scale: 50%
   :align: center


|
“Use iRules”のトグルをEnableにし、”Add”をクリックします。

.. figure:: images/c9-m1-7.png
   :scale: 50%
   :align: center


|
作成した”irule-test”のチェックボックスをクリックし”Add”をクリックします。

.. figure:: images/c9-m1-8.png
   :scale: 50%
   :align: center

元画面で **"Save"** をクリックし、　**”Review & Deploy"** をクリックします。


|
次のDeploy画面で、 **"Deploy Changes"** をクリックします。

.. figure:: images/c9-m1-9.png
   :scale: 50%
   :align: center


|
 **"Yes, Deploy"** をクリックします。

.. figure:: images/c9-m1-10.png
   :scale: 50%
   :align: center


|
クライアントからサーバへの通信確認を行います。 Windows clientのブラウザから
 **http://10.1.10.100/test**　のURLへアクセスを試行します。

.. figure:: images/c9-m1-11.png
   :scale: 50%
   :align: center

"Test Page" の画面が表示されると、iRuleからコンテンツを返しています。

