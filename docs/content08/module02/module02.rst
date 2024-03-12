HTTPS Virtual Serverのカスタマイズ
======================================

Virtual Serverの各種デフォルトの設定値を変更します。
作成したクローン **clone_HTTPS-Service** をクリックします。

.. figure:: images/c8-m2-1.png
   :scale: 50%
   :align: center


|
Virtual Server Portを443から8443へ変更
--------------------------------------

Template Bodyの中の、defaultポート番号設定の箇所を **”443”** から **”8443”** へ変更します。

※ **virtualport** や **443** 等の文字列でブラウザ文字検索すると該当箇所を簡単に見つけることができます。


.. figure:: images/c8-m2-2.png
   :scale: 40%
   :align: center


|
default Monitor typeをhttpからhttpsへ変更
--------------------------------------

Template Bodyの中の、Monitor Typeを **”http”** から **”https”** へ変更します。

※ **pools** 等の文字列でブラウザ文字検索すると該当箇所を簡単に見つけることができます。


.. figure:: images/c8-m2-3.png
   :scale: 40%
   :align: center


|
default Monitor typeをhttpからhttpsへ変更
--------------------------------------

Template Bodyの中の、Server-Side-TLSを **default false** から **true** へ変更します。

※ **enable_TLS_Server ** 等の文字列でブラウザ文字検索すると該当箇所を簡単に見つけることができます。


.. figure:: images/c8-m2-4.png
   :scale: 40%
   :align: center

