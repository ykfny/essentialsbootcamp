.. _prism_central_dashboards_reports:

-------------------------------------
Prism Central: Dashboards and Reports
Prism Central: ダッシュボードとレポート
-------------------------------------

Overview
概要
++++++++

This lab will introduce Prism Central’s Dashboards and Reporting features.
Prism Centralのダッシュボードとレポート機能について説明します。


Prism Central Dashboards
Prism Central ダッシュボード
++++++++++++++++++++++++

Prism Central dashboards allow you to quickly view the current state of the systems registered under that Prism Central instance.
Prism Central のダッシュボードから、そのPrism Centralインスタンスに登録されているシステムの現在の状態を素早く確認することができます。

The kind of information that you can obtain from a dashboard depends upon your interests.
ダッシュボードには管理者ユーザーの関心に合わせた情報を掲載できます。

It can include alerts about anything related to the health of a cluster, all the way to performance information.
クラスタの健全性に関連したパフォーマンス情報をアラートに含めることができます。

.. figure:: images/510PC1.png

Create a Custom Dashboard
カスタムダッシュボードの作成
.........................

Dashboards can also be customized.
ダッシュボードはカスタマイズ可能です。

#. In **Prism Central >** :fa:`bars` **> Dashboard**, or click the **Home X**
#. **Prism Central 左上メニュー > ダッシュボード**をクリックします。 もしくは画面中央のPrismアイコン**Home X**をクリックします。

The main dashboard is the first dashboard presented when the system first installed.
メイン ダッシュボードはシステムで初期構成されたダッシュボードです。

#. This dashboard can be customized as well, but instead we will each create new dashboard.
#. このメインダッシュボードをカスタマイズ出来ますが、新たにダッシュボードを作成可能です。

#. Click on :fa:`cog` **Manage Dashboards** to open the Manage Dashboards window.
#. [ダッシュボードを管理]をクリックし、ダッシュボードの管理画面を開きます。

#. Once there click on **+ New Dashboard**
#. [+ 新規ダッシュボード]をクリックします。

#. Enter "Dashboard-*intials*" for the name and click **Save**.
#. **Dashboard-席番号** を入力し、**保存** をクリックします。

.. figure:: images/510PC2.png

#. Now let’s add some Widgets.
#. 次はウィジェットを追加します

.. note::

  Widgets refer to the different sections of a dashboard.
　ウィジェットは、ダッシュボードの様々なセクションを参照します。
  A widget can be a graph, an alert board, or simply an information table showing nuggets of information.
  ウィジェットには、グラフ、アラート、価値ある情報を表示する情報テーブルがあります。
  You can choose to have widgets informing you on whatever piece of information you are interested, simply choose from the available entities.
  利用可能なエンティティから選ぶことで様々な情報を表示するウィジェットを配置できます。

#. Click **Add Widgets**.
#. 右上の **+ウィジェットを追加** をクリックします

#. From the list of available Widgets on the left hand side, notice there are three types of Widgets:
#. サイドバーに6種のカテゴリに分かれたウィジェットが表示されます

- CUSTOM WIDGETS
- CLUSTER WIDGETS
- APP WIDGETS

- CUSTOM WIDGETS（独自ウィジェット）
- 仮想インフラウィジェット
- ハードウェアウィジェット
- アクティビティウィジェット
- 運用ウィジェット
- アプリウィジェット

#. Choose any widget that may interest you in the **CUSTOM WIDGETS** section, and note that a custom set of parameters appears on the right hand side to specify.
#. **CUSTOM WIDGETS**から、関心のあるウィジェットを選択します。右側にカスタムパラメータセットが表示されますので適宜値を入力します。

#. Select amongst the options as desired and click **Add to Dashboard**.
#. 値を入力後、**ダッシュボードに追加** をクリックします。

.. figure:: images/510PC4.png

#. Next select another widget, now from the **CLUSTER WIDGETS** list. This time click on **Or, Add & Return to Dashboard.** to return to your newly created dashboard.
#. 次に、 **CUSTOM WIDGETS** の一覧から別のウィジェットを選択し、値を追加します。

#. 値を入力後、今回は **または、追加してダッシュボードに戻る** をクリックして、ダッシュボード画面に戻ります。


.. note::
.. ノート::


  There is a **+ Add Widgets** button in the top right corner of Prism Central that can be used to add more widgets at any time.
  Prism Centalの右上にある **+ウィジェットを追加** ボタンを使用して、いつでもウィジェットを追加できます。

  Also, note that hovering over any widget on the dashboard will show a little gray X on the top right corner that can be used to delete the widget.
  ウィジェットを削除する場合は、ウィジェットの右上に表示される**×**をクリックすると削除できます。

.. figure:: images/510PC5.png


Prism Central Reports
Prism Central レポート
+++++++++++++++++++++

Prism Central allows you to generate historical reports about your cluster environment that can be used to aid administrators in monitoring the health and performance of the clusters they manage.
Prism Central を使用して、クラスタ環境に関する履歴レポートを生成し、管理者が管理するクラスタの健全性とパフォーマンスの監視に役立てることができます。

Such reports can include resource consumption, abnormal behavior, and other valuable operational insights.
このようなレポートには、リソース消費、異常な動作、および運用に関するその他の有益なインサイト情報を含めることができます。

These reports can be manually generated or they can be automated from Prism Central to be sent out via email when it’s most convenient.
これらのレポートを手動で生成したり、生成を自動化して最適なタイミングで Prism Central から メール送信したりできます。

#. In **Prism Central >** :fa:`fa-navicon` **> Operations > Reports**.
#. **Prism Central 左上メニュー > オペレーション と進み、レポート**をクリックします


#. There you will see the two pre-defined reports available for you to use immediately:
#. 定義済みの2つのレポートが表示されます。

- Cluster Efficiency Summary
- Environment Summary

.. figure:: images/510reports1.png

#. レポートの作成と確認
#. Lets run the **Cluster Efficiency Summary** report.
#. **Cluster Efficiency Summary** レポートを実行します。

#. Select **Cluster Efficiency Summary**, then click **Run** from the **Actions** drop-down menu.
#. **Cluster Efficiency Summary**のチェックボックスにチェックを入れ、上部の**アクション**から**実行**をクリックします。

.. figure:: images/monitoring_01.png

#. Next, fill out the following fields and click **Run** from the **Actions** dropdown:
#.次に、以下のフィールドに値を入力し［実行］をクリックします

- **Report instance Name** - *initials* - Cluster Efficiency
- **レポートインスタンス名** - *席番号*_Cluster Efficiency
- **Time Period for Report** - Last 24 Hours
- **レポートの期間**  - Last 24 Hours（直近 24 時間）

#. Click **Run**.


#. Now lets run the **Environment Summary** report.
#. 今度は**Environment Summary**レポートを実行します。

#. Select **Environment Summary**, then click **Run** from the **Actions** drop-down menu.
#. **Environment Summary**のチェックボックスにチェックを入れ、上部の**アクション**から**実行**をクリックします。

#. Next, fill out the following fields and click **Run**:

- **Report instance Name** - *initials* - Environment Summary
- **レポートインスタンス名** - *席番号*_Environment Summary
- **Time Period for Report** - Last 24 Hours
- **レポートの期間**  - Last 24 Hours（直近 24 時間）

#. Click **Run**.

#. Once the reports are complete, select each report, and do the following:

#. Click **View Instances.** from the **Actions** drop-down menu.

- To view the report in a separate tab, click the name of the report.
- To download the report, select its check box, then click **Download** at the upper right of the screen.

#. Review the contents of the reports you created in this exercise.


#. レポートの確認
- レポート作成を実行後、各レポート名(Cluster Efficiency Summary, Environment Summary)をクリックし、各レポート画面へ移動します。
- ダウンロードの**PDF**をクリックしレポートの内容を確認します。



Create a Custom Report
カスタムレポートの作成
......................

#. To create a new custom report, click **+ New Report**.
#. カスタムレポートを作成するためにレポート画面上部の**+新規レポート**をクリックします。

#. Change the name of the report from **New Report** to *initials*-**Report**
#. **New Report**横のペンアイコンをクリックし、**席番号-Report** に変更します

.. figure:: images/510reports3.png

#. From the **CUSTOM VIEWS** menu on the left, click **Line Chart** and fill in the following:

- **Entity Type** - Cluster
- **Metric** - Memory Usage
- **Tittle** - *initials* - Cluster Memory Usage
- **Number of Entities** – 10
- **Sort Order** - Ascending

#. 左側の［カスタムビュー ］ メニューで ［線グラフ］をクリックし、以下のフィールドに入力します:
- **エンティティタイプ** - クラスタ
- **指標** - Memory Usage（メモリー使用率）
- **Tittle（タイトル）** - 席番号 – クラスタ メモリー使用率
- **Number of Entities（エンティティ数）** – 10
- **Sort Order（ソート順）** - 昇順
- **エンティティ** – すべて クラスタ

#. Click **Add**
#. **追加**をクリックします。

.. figure:: images/510reports2.png

#. From the **PRE-DEFINED VIEWS**, click on any entities that look interesting to you.
#. 同様に**事前に設定されたビュー** で関心のあるエンティティをクリックし、追加します。

.. note::
.. ノート::

  Since these are pre-defined, there are no extra configuration steps needed and they get added to the report immediately.
  これらのビューは定義済みなので、特別な設定手寿jンは不要で、すぐさまレポートに追加されます

#. Click on the **Add Schedule** button in the top right corner to add an automatic schedule to process the reports.
#. 右上の **スケジュールの追加** をクリックし、レポートの定期実行の設定を行います

#. Select any desired frequency, time, and duration to run the report.
#. レポートの頻度、時間、期間を任意で設定し[追加]をクリックします。

.. figure:: images/510reports4.png

.. note::
.. ノート::

  If SMTP is configured appropriately in Prism Central, this automated report can also get sent to any valid email address entered.
　Prism Central で SMTP が適切に設定されている場合、この自動生成されたレポートを、入力済みの有効なメールアドレスに送信することもできます

#. Click **Save** when done customizing your report.
#. レポートのカスタマイズが完了後、**保存** をクリックします。

#. Now your report has been saved, but note that there are no instances of it. This is because we have not run the report yet.
#. レポートは保存されましたが、そのインスタンスは存在していないことに注意してください。これは、まだレポートを実行されていないためです。

#. To run the report, click on **Run** from the top right corner.
#. レポート名をクリックし、右上の **実行**をクリックします。


.. figure:: images/510reports5.png

.. note::
.. ノート::

  Cloning a report is useful to leverage an existing report and edit it to customize it further.
  レポートのクローニングは、既存のレポートを利用して編集するため、詳細にカスタマイズするのに役立ちます

#. When the report finishes, you will see the first instance of this reported available for viewing by clicking **PDF** under Download.
#. レポートが完成、実行したら、［ダウンロード］ の［PDF］をクリックすると、このレポートが取得できます。

#. Then click on the X on the top right corner to exit.
#. 右上にある X をクリックして、レポートの作成画面に戻ります。

#. If you leave the report as is, it will get automatically run and sent to a provided email address at the specific frequency and time set.
#. レポートは設定した固有の頻度と時間で自動的に実行され、指定されたメールアドレスに送信されます。

#. The reports themselves can also be customized under **Report Settings** if different colors or logos are desired.
#. 別の色やロゴを設定したい場合は、［ レポート設定］ でレポート自体をカスタマイズ可能です。


Takeaways
ポイント
+++++++++

- The Prism Central Customizable Dashboards allow you to setup user and team specific dashboards with the information they care about.
-	Prism Central のカスタマイズ可能なダッシュボードを使用して、ユーザーやチームが関心のある情報を表示する固有のダッシュボードを設定できます。
- The Prism Central report management feature provides you with an ability to configure and deliver the historical reports containing information about the infrastructure resources straight into your mailbox according to the schedules configured.
- Prism Central のレポート管理機能では、設定済みのスケジュールに従って、インフラストラクチャーのリソースに関する情報を記載した履歴レポートを設定し、メールボックスに直接配信することができます。
