.. _prism_pro_resource_planning:

--------------------------------
Prism Pro: Resource Planning
Prism Pro: リソース プランニング
--------------------------------

Overview
概要
++++++++

This lab will introduce Prism Central’s resource planning features that help you stay on top of cluster utilization and more accurately predict cluster expansions.
この演習では、クラスタの利用を完全に把握し、クラスタの拡張をより正確に予測できるようにする Prism Central のリソースプランニング機能をご紹介します。

Lab Setup
+++++++++

This lab requires a VM to be provisioned and will be stressed later in the lab to produce CPU and memory metrics.

Applications provisioned as part of the  :ref:`linux_tools_vm` will be used to accomplish this.

#. Please follow the instructions to deploy the :ref:`linux_tools_vm` before moving on with this lab.


#. Right click the following URL to open a new tab and navigate to the webpage at http://10.42.247.70 and enter the details in the Setup portion of the form. Then click 'Begin Setup' once you have filled in all the fields. This will get your environment ready for this lab. **Keep this tab open during entire Prism Pro lab to return to as directed in later portions.**

   .. figure:: images/ppro_08.png

#. After hitting continue, it will take a bit of time for the setup to complete. In the meantime, switch back to Prism Central and go through the labs.

Prism Central Resource Planning
Prism Centralのリソースプランニング
+++++++++++++++++++++++++++++++

Nutanix utilizes our X-Fit machine learning and data analytics as part of Prism Pro. We utilize that machine learning and data analytics to provide Cluster Runway and just in time forecasting (What If Planning).
Nutanix は、X-Fit 機械学習機能とデータ分析機能を Prism Pro の一部として利用します。これらの機能を利用して、クラスタのランウェイとジャストインタイム フォーキャスト（What If プランニング）を提供します。

Capacity Runway
キャパシティ ランウェイ
...............

Use Prism Central’s Capacity Runway feature to learn about cluster resource planning and recommendations.
Prism Central のキャパシティランウェイ機能を使用して、クラスタのリソースプランニングと推奨について学習します。

Lets view the Capacity Runway of your lab cluster.
演習に使用するクラスタのキャパシティランウェイを見てみましょう。

#. In **Prism Central > Planning > Capacity Runway**.
#. 演習に使用するクラスタのキャパシティランウェイを見てみましょう。


- Note the runway summaries showing the days left for each cluster.
- How long does the current cluster has before it runs out of memory, CPU, and storage?

- 各クラスタの残り日数を示すランウェイサマリーに注目してください。
- 現在のクラスタがメモリ、CPU、ストレージを使い切るまでの残り時間は？


#. Click on the **Prism-Pro-Cluster** cluster.
#. Prism-Pro-Clusterをクリックします。

. You can now take a look at the Runway for Storage, CPU, and Memory.
. ストレージ、CPU、メモリのランウェイを調べることができます。

   .. figure:: images/ppro_12.png

#. When selecting the Memory tab, you can see a Red Exclamation mark, indicating where this cluster will run out of Memory. You can hover the chart at this point to see on which day this will occur.
#. ［ Memory（メモリ） ］ タブを選択すると、このクラスタがメモリを使い切ることを示す[赤い感嘆符 ”!” ] を確認することができます。この点でグラフにマウスポインタを合わせると、メモリを使い切る日が表示されます。

   .. figure:: images/ppro_13.png

#. Click on the **‘Optimize Resources’** button on left. This is where you can see the inefficient VMs in the environment with suggestions on how you can optimize these resources to be as efficient as possible.
#. 左側にある ［リソースの最適化］ ボタンをクリックします。環境内の非効率的な VM と、これらのリソースをできる限り効率的に最適化する方法に関する提案が表示されます。

   .. figure:: images/ppro_14.png

#. Close the optimize resources popup.
#. リソースの最適化ポップアップを閉じます。


What If Planning
What If プランニング
................

#. Under the **‘Adjust Resources’** section in the left side of this page, click the **‘Get Started’** button. We can now use this to start planning for new workloads and see how runway will need to be extended in the future.
#. このページの左側にある **リソースの調整** セクションの下にある **はじめに** ボタンをクリックします。この方法で新しいワークロードのプランニングを開始し、将来的にランウェイをどれくらい延長する必要があるかを確認できます.


#. Click the **add/adjust** button in the left side underneath the ‘Workloads’ item.
#. 左側の **ワークロード** 項目の下にある **追加/調整** ボタンをクリックします。

   .. figure:: images/ppro_15.png

#. Add one for VDI and select 1000 Users. You can also set a date for when this workload should be added to the system. Save this workload when you are done.
#. VDI 用のワークロードを追加して、1000 ユーザーを選択します。このワークロードをシステムに追加する日付を設定することが出来ます。完了したら、このワークロードを保存します。

   .. figure:: images/ppro_16.png

   .. figure:: images/ppro_17.png

#. Add another workload of your choice.
#. 自分で選んだワークロードをもう 1 つ追加します。


#. Now click the **‘Recommend’** button on the right side of the page.
#. 今度はページの右側にある**推奨**ボタンをクリックします。

   .. figure:: images/ppro_18.png

#. Once the Recommendation is available, toggle between list and chart view to get a better overview of your Scenario.
#. 推奨が利用可能になったら、シナリオの概要を把握しやすいように、*リストビュー*と*グラフビュー*を切り替えます。

   .. figure:: images/ppro_19.png

#. Click the **Generate PDF** button in the upper right hand corner. This will open a new tab with a PDF report for the scenario/workloads you have created.
#. 右上にある ［PDF の生成］ボタンをクリックします。新しいタブが開き、作成したシナリオ/ワークロードの PDF レポートが表示されます。

   .. figure:: images/ppro_19b.png

#. View your report.
#. レポートを確認します。

   .. figure:: images/ppro_20.png

Takeaways
ポイント
+++++++++

- The Capacity Runway view in the Planning dashboard allows you to view summary resource runway information for the registered clusters and access detailed runway information about each cluster.
- The Scenarios view in the Planning dashboard allows you to create "what if" scenarios to assess the future resource requirements for potential work loads that you specify.
- You must have a Prism Pro license to use the resource planning tools.
- プランニングダッシュボードのキャパシティビューを使用して、登録済みクラスタのリソースランウェイ情報のサマリーを表示し、各クラスタに関する詳細なランウェイ情報にアクセスすることができます。
- プランニングダッシュボードのシナリオビューを使用して、What If シナリオを作成し、指定した潜在的ワークロードに将来的に必要になるリソースを評価することができます。
- リソースプランニングツールを使用するには、Prism Pro ライセンスが必要です。
