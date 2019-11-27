.. _prism_pro_effeciency_anomaly:

--------------------------------------------
Prism Pro: VM Efficiency & Anomaly Detection
Prism Pro: VM効率化および異常検出
--------------------------------------------

Overview
概要
++++++++

Prism Pro is a product designed to make our customer IT operations smarter and automated. Today, there is no solution that is specifically designed for IT operations for the data center built around HCI. The infrastructure in this type of data center is dynamic, scalable, and highly performed. The traditional performance monitoring and IT OPS tools are built for the static infrastructure. When the IT admins use the traditional tool to manage HCI environment, they are overwhelmed by the complexity and noisy signal the tool brings. This decreases the productivity of the operations and reduces the ROI from adopting the HCI.

Prism Pro はお客様による IT 運用をスマートかつ自動化するための製品です。現在、HCI を中心として構築されている、データセンターの IT 運用に特化したソリューションはありません。このタイプのデータセンターのインフラストラクチャーは動的で拡張性があり、パフォーマンスに優れています。従来のパフォーマンスモニタリングおよび IT 運用ツールは、静的なインフラストラクチャー向けに構築されています。IT 管理者が従来のツールを使用して HCI 環境を管理すると、その複雑さとツールが検知するシグナルの誤りの多さが負担になります。その結果、運用の生産性が低下し、HCI の導入から得られる ROI が減少します。

Prism Pro takes a unique approach that maximizes the operation efficiency of an HCI based data center. First, Prism Pro uses purpose-built machine learning (X-FIT) to extract the insights from the mass amount of operations data the HCI produces. The first three use cases Prism Pro shipped are capacity forecast and planning, VM right sizing, and anomaly detection. These use cases help our customer detect problems and waste with the actionable signal. Second, Prism Pro delivers an automation mechanism (X-Play) that enables customers to automate their operations tasks confidently to respond to the signal X-FIT detects.

Prism Pro は、独自のアプローチを採用して、HCI をベースとするデータセンターの運用効率を最大限に高めます。第一に、Prism Pro は専用の機械学習（X-FIT）を使用して、HCI が生み出す大量の運用データからインサイトを抽出します。Prism Pro には、キャパシティ予測およびプランニング、VM の適切なサイジング、異常検知という 3 つのユースケースが初めて搭載されました。お客様はこれらのユースケースを利用して、実用的なシグナルで問題点と無駄を検知することができます。第二に、Prism Pro が提供する自動化メカニズム（X-Play）によって、X-FIT が検知したシグナルに対応する運用タスクをお客様が確実に自動化できます。


Lab Setup
+++++++++

This lab requires a VM to be provisioned and will be stressed later in the lab to produce CPU and memory metrics.

Applications provisioned as part of the  :ref:`linux_tools_vm` will be used to accomplish this.

#. Please follow the instructions to deploy the :ref:`linux_tools_vm` before moving on with this lab.


#. Right click the following URL to open a new tab and navigate to the webpage at http://10.42.247.70 and enter the details in the Setup portion of the form. Then click 'Begin Setup' once you have filled in all the fields. This will get your environment ready for this lab. **Keep this tab open during entire Prism Pro lab to return to as directed in later portions.**

   .. figure:: images/ppro_08.png

#. After hitting continue, it will take a bit of time for the setup to complete. In the meantime, switch back to Prism Central and go through the labs.


VM Efficiency
仮想マシン効率
+++++++++++++++++++++++++++

Prism Pro uses X-Fit machine learning to detect the behaviors of VMs running within the managed clusters. Then applies a classification to VMs that are learned to be inefficient. The following are short descriptions of the different classifications:
Prism Pro では、X-Fit 機械学習機能を使用して、管理対象のクラスタ内で実行されている VM の動作を検知します。そして、学習によって非効率的と識別された VM に分類を適用します。様々な分類の簡単な説明を以下に示します：

* **Overprovisioned:** VMs identified as using minimal amounts of assigned resources.
* **Inactive:** VMs that have been powered off for a period of time or that are running VMs that do not consume any CPU, memory, or I/O resources.
* **Constrained:** VMs that could see improved performance with additional resources.
* **Bully:** VMs identified as using an abundance of resources and affecting other VMs.

* **オーバープロビジョニング**：割り当てられた必要最小限のリソースを使用している VM。
* **非アクティブ**：一定時間パワーオフになっている VM、または動作しているが CPU、メモリ、または I/O リソースをまったく消費していない VM。
* **制約**：リソースを追加すればパフォーマンスが向上する可能性がある VM。
* **ブリー**：大量のリソースを使用し、他の VM に影響を与えている VM

#. In **Prism Central**, select :fa:`bars` **> Dashboard** (if not already there).
#. **Prism Central** で **ダッシュボード** を選択します（まだダッシュボードが表示されていない場合）

#. From the Dashboard, take a look at the VM Efficiency widget. This widget gives a summary of inefficient VMs that Prism Pro’s X-FIT machine learning has detected in your environment. Click on the ‘View All Inefficeint VMs’ link at the bottom of the widget to take a closer look.
#. ダッシュボードで **仮想マシン効率** ウィジェットを参照します。このウィジェットには、Prism Pro の X-FIT 機械学習が環境内で検知した非効率的な VM のサマリーが表示されます。ウィジェット下部にある **View All Inefficeint VMs（非効率的な 仮想マシンを全て表示）** リンクをクリックして、詳細を確認します。

   .. figure:: images/ppro_58.png

#. You are now viewing the Efficiency focus in the VMs list view with more details about why Prism Pro flagged these VMs. You can hover the text in the Efficiency detail column to view the full description.
#. VM のリストビューに、Prism Pro がこれらの VM を分類した理由に関する詳細情報が表示されています。［ Efficiency Detail（効率の詳細） ］ 列の文字にマウスポインタを合わせると、説明を全て見ることができます。

   .. figure:: images/ppro_59.png

#. Once an admin has examined the list of VM on the efficiency list they can determine any that they wish to take action against. From VMs that have too many or too little resources they will require the individual VMs to be resized. This can be done in a number of ways with a few examples listed below:
#. 管理者が効率リストの VM を調べ、何らかのアクションを起こすかどうかを判断できます。リソースが多すぎる、または少なすぎる VM の場合は、個々の VM のサイズを変更する必要があります。VM のサイズは様々な方法で変更できます。いくつかの例を以下に示します：

* **Manually:** An admin edits the VM configuration via Prism or vCenter for ESXi VMs and changes the assigned resources.
* **X-Play:** Use X-Plays automated play books to resize VM(s) automatically via a trigger or admins direction. There will be a lab story example of this later in this lab.
* **Automation:** Use some other method of automation such as powershell or REST-API to resize a VM.

* **手動**：管理者が Prism または ESXi VM 用の vCenter から VM 構成を編集し、リソースの割り当てを変更します。
* **X-Play**：X-Play の自動化プレイブックを使用し、トリガーまたは管理者の指示によって自動的に VM のサイズを変更します。演習の後半で、この演習ストーリーを取り上げます。
* **自動**：PowerShell や REST-API など、他の自動化メソッドを使用して VM のサイズを変更します。


Anomaly Detection
異常検知
+++++++++++++++++++++++++++++++

In this lab story you will take a look at VMs with an anomaly. An anomaly is a deviation from the normal learned behavior of a VM. The X-FIT alogrithms learn the normal behavior of VMs and represent that as a baseline range on the different charts for each VM.
この演習ストーリーでは、異常のある VM を調べてみます。異常とは、VM の学習された正常動作からの逸脱です。X-FIT アルゴリズムが VM の正常動作を学習し、各 VM の様々なグラフ上にベースライン範囲として表します。

#. Now let's take a take a look at a VM by searching for ‘bootcamp_good’ and selecting ‘bootcamp_good_1’.
#. ‘bootcamp_good’を検索し、‘bootcamp_good_1’を選択して、VM を調べてみましょう。

   .. figure:: images/ppro_61.png

#. Go to Metrics > CPU Usage. Notice a dark blue line, and a lighter blue area around it. The dark blue line is the CPU Usage. The light blue area is the expected CPU Usage range for this VM. This range is calculated using Prism Pro’s X-FIT machine learning engine. In this case, an anomaly has been raised for this VM, because the Usage is far below the expected range. You can also reduce the time range “Last 24 hours” to examine the chart more closely.
#.［ Metrics（評価指標） ］ > ［ CPU Usage（CPU 使用量） ］ と進みます。濃い青色の線と、その周囲に薄い青色のエリアが表示されています。濃い青色の線は CPU 使用量です。薄い青色のエリアは、この VM に対して予測される CPU 使用量の範囲です。この範囲は、Prism Pro の X-FIT 機械学習エンジンを使用して計算されます。このケースでは、使用量が予測される範囲をはるかに下回っているので、この VM に関して異常が発生しています。時間範囲を ［ Last 24 hours（直近 24 時間） ］ に短縮して、グラフをより詳しく調べることもできます。

   .. figure:: images/ppro_60.png

#. Click **“Alert Setting”** to set an alert policy for this kind of situation.
#. **アラート設定**をクリックして、このような状況に関するアラートポリシーを設定します。

#. In the right hand side, you can change some of the configurations however you would like. In this example I have changed the Behavioral Anomaly threshold to ignore anomalies between 10% and 70%. All other anomalies will generate a Warning alert. I have also adjusted the Static threshold to Alert Critical if the CPU Usage on this VM exceeds 95%.
#. 右側で、任意の値に設定を変更出来ること確認します。今回は、10% ～ 70% の異常を無視するように ［ Behavioral Anomaly（動作の異常） ］ しきい値を変更します。それ以外の異常は全て、警告アラートを生成します。また、この VM の CPU 使用量が 95% を超えた場合に重大アラートを生成するように ［ Static Threshold（静的しきい値） ］ も調整しました。

   .. figure:: images/ppro_25.png

#. Hit **Cancel** to exit the policy creation workflow.
#. **キャンセル** をクリックして、ポリシー作成ワークフローを終了します。


Takeaways
ポイント
+++++++++

- Prism Pro is our solution to make IT OPS smarter and automated. It covers the IT OPS process ranging from intelligent detection to automated remediation.
- Prism Pro は IT 運用をスマートかつ自動化するためのソリューションです。インテリジェントな検知から自動修復までの IT 運用プロセスを対象とします。
- X-FIT is our machine learning engine to support smart IT OPS, including forecast, anomaly detection, and inefficiency detection.
- X-FIT は、予測、異常検知、非効率性検知など、スマートな IT 運用をサポートする機械学習エンジンです。
