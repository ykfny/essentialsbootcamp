.. _prism_pro_xplay:

--------------------------------------------
Prism Pro: X-Play
--------------------------------------------

Overview
概要
++++++++



Increase Constrained VM Memory with X-Play
制約されている VM のメモリを X-Playを用いて増加させる
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

In this lab story we will now use X-Play to create a Playbook to automatically add memory to the lab VM that was created earlier, when a memory constraint is detected.
この演習ストーリーでX-Play を使用して、メモリの制約が検知されたときに作成済みの演習用 VM に自動的にメモリを追加するプレイブックを作成します。

#. Use the search bar to navigate to the **Playbooks** page.
#. 検索を使用して、**プレイブック** ページに移動します。

   .. figure:: images/ppro_26.png

#. We will start by creating a Playbook. Click **Create Playbook** at the top of the table view
#. プレイブックの作成から始めます。画面中央の[はじめに]クリックし、テーブルビューの上部にある ［プレイブックの作成］ をクリックします。

   .. figure:: images/ppro_27.png

#. Select Alert as a trigger
#. トリガーとして ［アラート］ を選択します。

   .. figure:: images/ppro_28.png

#. Search and select **VM {vm_name} Memory Constrained** as the alert policy, since this is the issue we are looking to take automated steps to remediate.
#. 検索に、［ VM {vm_name} Memory Constrained］ をアラートポリシーとして選択します。このアラートをPlaybookにて自動修復します。

   .. figure:: images/ppro_29.png

#. Select the *Specify VMs* radio button and choose the VM you created for the lab. This will make it so only alerts raised on your VM will trigger this Playbook.
#. *VMs を指定* のラジオボタンを選択し、*Linux-toolsVM* を選びます。これによって、指定した VM に対して発生したアラートのみがこのプレイブックをトリガーするようになります。

   .. figure:: images/ppro_29b.png

#. We will first need to snapshot the VM. Click **Add Action** on the left side and select the **VM Snapshot** action.
#. VM のスナップショットを取得します。左側にある **アクションの追加** をクリックし、**VM スナップショット**アクションを選択します。

   .. figure:: images/ppro_30.png

#. The Target VM is auto filled with the source entity from the Alert trigger. To finish filling the details for this action, enter a value, such as **1**, in the Time to Live field.
#. ターゲット VM には、アラートトリガーのソースエンティティが自動設定されます。**存続時間** フィールドに 1 などの値を入力します。

   .. figure:: images/ppro_32.png

#. Next we would like to remediate the constrained memory by adding more memory to the VM. Click **Add Action** to add the **VM Add Memory** action
#. 次に、VM にメモリ追加を登録します。**アクションの追加** をクリックして、**VM メモリを追加** アクションを追加します。

   .. figure:: images/ppro_33.png

#. Set the empty fields according to the screen below.
#. 空のフィールドに設定します。

   .. figure:: images/ppro_34.png


#. Next we would like to notify someone that an automated action was taken. Click **Add Action** to add the email action
#. 次に、自動化アクションが実施されたことを通知しするアクションを設定します。**アクションの追加** をクリックして、メールアクションを追加します。

   .. figure:: images/ppro_35.png

#. Fill in the field in the email action. Here are the examples
#. 11.	メールアクションのフィールドに入力します。以下に例を示します。

**Recipient:** Fill in your email address.
**Subject :**
``Playbook {{playbook.playbook_name}} addressed alert {{trigger[0].alert_entity_info.name}}``
**Message:**
``Prism Pro X-FIT detected  {{trigger[0].alert_entity_info.name}} in {{trigger[0].source_entity_info.name}}.  Prism Pro X-Play has run the playbook of "{{playbook.playbook_name}}". As a result, Prism Pro increased 1GB memory in {{trigger[0].source_entity_info.name}}.``

**受信者:** メールアドレス
**件名:** Playbook {{playbook.playbook_name}} addressed alert {{trigger[0].alert_entity_info.name}}（プレイブック {{playbook.playbook_name}} がアラート {{trigger[0].alert_entity_info.name}} に対処しました）
**メッセージ:** Prism Pro X-FIT detected  {{trigger[0].alert_entity_info.name}} in {{trigger[0].source_entity_info.name}}.（Prism Pro X-FIT が {{trigger[0].source_entity_info.name}} で  {{trigger[0].alert_entity_info.name}} を検知しました。）  Prism Pro X-Play has run the playbook of "{{playbook.playbook_name}}".（Prism Pro X-Play がプレイブック "{{playbook.playbook_name}}" を実行しました。）As a result, Prism Pro increased 1GB memory in {{trigger[0].source_entity_info.name}}.（その結果、{{trigger[0].source_entity_info.name}} のメモリが 1GB 増加しました。）


You are welcome to compose your own subject message. The above is just an example. You could use the “parameters” to enrich the message.
独自の件名とメッセージを自由に作成することができます。上記は一例です。[パラメータ］を使用してメッセージを編集させることができます。

   .. figure:: images/ppro_36.png

#. Click **Add Action** to add the **Acknowledge Alert** action
#. **アクションの追加**をクリックして、**アラートを確認**アクションを追加します。

   .. figure:: images/ppro_37.png

#. Click **Save & Close** button and save it with a name “*Initials* - Auto Increase Constrained VM Memory”. **Be sure to enable the ‘Enabled’ toggle.**
#. **保存して閉じる** ボタンをクリックし、*"席番号 - Auto Increase Constrained VM Memory"* という名前で保存します。**有効**のトグルボタンを必ず有効にしてください。

   .. figure:: images/ppro_39.png

#. You should see a new playbook in the “Playbooks” list page.
#. プレイブックリストページに新しいプレイブックが表示されます

   .. figure:: images/ppro_40.png

#. Search for your VM and record the current memory capacity. You can scroll down in the properties widget to see the configured memory.
#. VM を検索して現在のメモリキャパシティを確認します。プロパティウィジェットをスクロールダウンして、構成済みのメモリを確認します。

   .. figure:: images/ppro_41.png

#. **Switch tabs back to** the http://10.42.247.70 page and press Continue from the Story 1-3 Step, if you have not already.
#. 開いておいたhttp://10.42.247.70 ページにタブを切り替え、ストーリー 1 ～ 3 の手順を続けます。

   .. figure:: images/ppro_08b.png

#. Now we will simulate an alert for ‘VM Memory Constrained’ which will trigger the Playbook we just created. Click the ‘Simulate Alert’ button to create the alert.
#. 6.	今度は、作成したプレイブックをトリガーする「VM のメモリが制約されている」アラートをシミュレートします。Select your VMでLinux-toolsVMを選択し［アラートのシミュレート］ ボタンをクリックして、アラートを作成します。

   .. figure:: images/ppro_64.png

#. Go back to Prism page and check your VMs page again, you should now see the memory capacity is increased by 1GB. If the memory does not show updated you can refresh the browser page to speedup the process.
#. Prismに戻り、VM ページを再度確認します。プレイブックのシナリオが実施され メモリキャパシティが 1GB 増加しているはずです。メモリが更新されていない場合は、ブラウザページを更新し再度確認します。

#. You should also receive an email. Check the email to see that its subject and email body have filled the real value for the parameters you set up.
#. プレイブックで設定したメールをチェックして、設定したパラメータの実際の値が件名とメール本文に挿入されていることを確認します。

#. Go to the **Playbook** page, click the playbook you just created.
#. プレイブック ページに移動して、作成したプレイブックをクリックします。

   .. figure:: images/ppro_44.png

#. Click the **Plays** tab, you should see that a play has just completed.
#. *プレイ* タブをクリックします。Statusを確認しプレイが実施されたことが確認できます

   .. figure:: images/ppro_45.png

#. Click the “Play” to examine the details
#. *プレイブック*をクリックして、詳細を確認します。

   .. figure:: images/ppro_46.png

Takeaways
ポイント
+++++++++

- X-Play, the IFTTT for the enterprise, is our engine to enable the automation of daily operations tasks.
- X-Play enables admins to confidently automate their daily tasks within minutes.
- X-Play is extensive that can use customer’s existing APIs and scripts as part of its playbooks.
- 企業向けの IFTTT である X-Play は、日々の運用タスクの自動化を可能にするためのエンジンです。
- 管理者は X-Play を使用して、日々のタスクを数分以内に確実に自動化することができます。
- X-Play は強力で、お客様の既存 API やスクリプトをプレイブックの一部として利用できます。
