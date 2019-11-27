.. _prism_central_overview:

-----------------------
Prism Central: 概要
-----------------------

概要
++++++++
Prism Central UI のレイアウトやナビゲーション方法の概要を説明します。


Prism Central
+++++++++++++

#. Open https://<*Prism-Central-IP*>:9440

#. Fill out the following fields and click **Enter**:
#. 以下の項目を入力し **Enter** をクリックします。:

- **Username** - admin
- **Password** - *HPOC Password*

#. After you log in to Prism Central, familiarize yourself with the Prism UI.
#. Prism Centralへログイン後、Prism UI を操作します。

#. Explore the information on the **Home** screen:
#. **ダッシュボード**画面で以下の情報を確認します。

- Cluster Runway
- クラスタ ランウエイ
- Cluster Quick Access
- クラスタ クイックアクセス
- Impacted Cluster | Alerts
- 影響を受けたクラスタ | アラート
- tasks
- タスク

#. Review the **Explore** screen:
#. 左上の**ハンバーガーボタン**をクリックし、以下の項目で参照可能な内容を確認します。

-仮想インフラ
　- 仮想マシン
　- イメージ
  - ストレージコンテナ
  - VMs
- Images
- Storage Containers

- ハードウェア
 - クラスタ
 - ホスト
 - ディスク
- Clusters
- Hosts
- Disks

.. figure:: images/nutanix_tech_overview_10.png

#. Review the other sections, and do a quick walk through:
#. 以下の項目も参照できる内容を確認してください。

- Planning
- Analysis
- Apps (We will configure this later in the workshop)
- Alerts
- Tasks :fa:`circle-o`
- Search :fa:`search`
- Help :fa:`question`
- Configuration :fa:`cog`
- User :fa:`user`

.......................
Prism Central UI Review
Prism Central UIの確認
.......................

How would you find the screen that shows you a table of all the hosts managed by an instance of Prism Central?
以下の様に、Prism Centralの管理対象である、全てのホスト情報を一覧で表示するためにはどこから確認すれば良いでしょうか？

.. figure:: images/nutanix_tech_overview_11.png

..確認方法
#. In **Prism Central > Explore**, click **Hosts** on left-hand menu.
#. Prism Centralの左上メニュー > ハードウェア > ホスト** をクリックします

.. note::
.. ノート::

  If this Prism Central instance was managing multiple clusters, this screen would show the hosts for all of the clusters being managed.
　Prism Central で複数のクラスタを管理している場合は、この一覧画面で管理対象クラスタの全てのホストが表示されます。


How would you find the screen that lists all of the VMs currently deployed. This screen looks similar to the figure below?
以下の様に、現在デプロイされている全てのVMを一覧表示させるためにはどこから確認すれば良いでしょうか？

.. figure:: images/nutanix_tech_overview_12.png

..確認方法
#. In **Prism Central > Explore**, click **VMs** on left-hand menu.
#. Prism Centralの左上メニュー > 仮想インフラ > 仮想マシン** をクリックします


What page would show you the latest activity in the system?
On this page, you can monitor the progress of any task and keep track of what has been done in the past using time stamps. Can you figure out two different ways to get there?

システムにおける直近のアクティビティを表示するページはどこでしょうか？
このページでは、全てのタスクの進行状況を確認でき、タイムスタンプを使って過去に発生した事象を追跡することができます。


#. First Way, In **Prism Central > Home**, click **View All Tasks**. Second Way, click :fa:`circle-o`
#. **Prism Central 左上メニュー > アクティビティ と進み、タスク **をクリックします
#. **Prism Centralのメイン ダッシュボード** > 右上の:fa:`circle-o`をクリックします


.. note::
.. ノート::

  In ESXi:
  ESXiの場合
  - vCenter Server instances can be registered to Prism via Prism's :fa:`cog` icon.
  - vCenter Server インスタンスの登録は、Prism上の**設定**:fa:`cog` > vCenter Registration から行います。
  - Registering a Nutanix Cluster running ESXi with vCenter allows to perform core VM management operations directly from Prism without switching to vCenter Server.
  - vCenter ServerをPrismに登録するとESXiで構成されたNutanixクラスタ上の仮想マシン管理操作をvCenterへ切り替えることなく、Prismから直接操作できます。
  - The vCenter Server that is managing the hosts in the cluster is auto-discovered and its IP address is auto-populated in the Address field as shown in the example below.
  - 以下の図の様に、Nutanixクラスタ内のホストを管理しているvCenterはPrismから自動検出されます。

  Example view of vCenter registration to Prism:
  PrismのvCenter登録画面：

  .. figure:: images/nutanix_tech_overview_15.png


Takeaways
ポイント
+++++++++

- Prism is thoughtfully laid out UI
- Prism は シンプルでわかりやすいUI です
- Critical information is displayed front and center
- 重要な情報は前面や中央部に表示されます
- Prism Central can manage multiple clusters
- Prism Central は複数のクラスターを管理することができます
