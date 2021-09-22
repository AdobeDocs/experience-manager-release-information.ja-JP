---
title: 累積修正パックの AEM Forms JEE へのインストール
description: AEM Forms JEE での累積修正パック（CFP）のインストールおよび設定手順の概要
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 69f4db4e2ef94c370ed590ec7e9859781a909270
workflow-type: ht
source-wordcount: '1044'
ht-degree: 100%

---

# AEM [!DNL  Forms] JEE への累積修正パックのインストール {#installing-cumulative-fix-packs-on-aem-forms-jee}

## AEM 6.3 [!DNL Forms JEE] に CFP をインストールする  {#install-cfp-forms-6-3}

指定した順序で次の手順を実行し、累積修正パックを AEM 6.3 [!DNL Forms JEE] にインストールします。

1. [Adobe サポート](https://www.adobe.com/account/sign-in.supportportal.html)に連絡して、CFP の AEM 6.3 [!DNL Forms JEE] インストーラーを入手します。
1. [AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee) のインストールと設定の説明に従って、CFP インストーラーを実行し、AEM [!DNL Forms JEE] を設定します。
1. 最新の AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md) をインストールします。
1. AEM CFP [6.3.3.x ](aem-forms-releases.md)用の[!DNL Forms]アドオンパッケージをインストールします。

### AEM [!DNL Forms JEE] バンドルパッケージのインストール {#install-aem-forms-jee-bundles-package}

AEM [!DNL  Forms JEE] パッケージ（aemfd-jee-bundles-package-6.3CFP1、バージョン 1.0.2）は、AEM [!DNL Forms] 上の [!DNL Forms JEE] ユーザーに、AEM [!DNL Forms OSGi] 上と同じ権限および機能を提供します。パッケージマネージャーでインストール済みのパッケージを確認し、パッケージがまだインストールされていない場合はインストールします。

### CQ-4208044 の追加手順 {#additional-instructions-for-cq}

AEM 6.3 [!DNL Forms JEE] サーバーと Oracle データベースを使用している場合は、CFP1 のデプロイ後、つまり Configuration Manager の実行後に、以下の設定を設定します。この設定は、エンタープライズドメインの同期が実行されるときに、ユーザー、グループ、グループメンバーを同期するために必要です。[AEM 6.3 リリースノート](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205)で問題 CQ-4208044 を参照してください。

1. **管理者** UI にログインします。
1. **[!UICONTROL 設定]**／**[!UICONTROL User Management]**／**[!UICONTROL 設定]**／**[!UICONTROL 設定ファイルの読み込みと書き出し]**&#x200B;に移動します
1. Config.xml ファイルを書き出します。
1. *Config.xml* のドメイン設定で、「`groupMemberDBQueryBatchSize`」のエントリを変更します。エントリ例：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. 変更したファイルを再度読み込んでから、同期を再実行してください。

## AEM 6.2 [!DNL  Forms JEE] に CFP をインストールする  {#install-cfp-on-aem-62-forms-jee}

指定した順序で次の手順を実行し、累積修正パックを AEM 6.2 [!DNL Forms JEE] にインストールします。

>[!NOTE]
>
>AEM 6.2 [!DNL Forms OSGi] を使用している場合は、[AEM 6.2 CFP リリースノート](release-notes-aem-6-2-cumulative-fix-pack.md)のインストール手順に従ってください。

1. [Adobe サポート](https://www.adobe.com/account/sign-in.supportportal.html)に連絡して、CFP の AEM 6.2 [!DNL Forms JEE] インストーラーを入手します。
1. [AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee) のインストールと設定の説明に従って、CFP インストーラーを実行し、AEM [!DNL Forms JEE] を設定します。
1. AEM Hotfix 12785 バージョン 7.0 をインストールします。
1. [AEM 6.2 サービスパック 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) をインストールします。
1. 最新の [AEM 6.2 サービスパック 1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md) をインストールします。
1. [AEM 6.2 サービスパック 1 CFP ](aem-forms-releases.md)用 [!DNL Forms] アドオンパッケージをインストールします。

### AEM [!DNL Forms JEE] バンドルパッケージのインストール {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE パッケージ （aemfd-jee-bundles-package-6.2CFP5、バージョン 1.0.2）は、AEM [!DNL Forms] 上の [!DNL Forms JEE] ユーザーに、AEM [!DNL Forms OSGi] 上と同じ権限および機能を提供します。パッケージマネージャーでインストール済みのパッケージを確認し、パッケージがまだインストールされていない場合はインストールします。

### コンポーネントレベルでの操作のタイムアウトの設定（NPR-16774）  {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>AEM 6.2 CFP4 の後は、次の手順で、アップグレードプロセス中にタイムアウトが原因で問題が発生した場合に DSC 操作のタイムアウトを設定できます。（[AEM 6.2 CFP4 リリースノート](release-notes-aem-6-2-cumulative-fix-pack.md)の NPR-16774 を参照）。

DSC のデプロイメントには、失敗する可能性があるため、変数の時間がかかります。インストール、読み込み、開始、停止などの DSC 操作のタイムアウトを変更するには、JVM 引数に -D オプションで使用して `adobe.component.registry.timeout` を設定する必要があります。

キーの値を秒単位で指定します。例：`-Dadobe.component.registry.timeout=300`

また、次の 3 つのプロパティを使用して、コンポーネントレベルでタイムアウトを変更することもできます。

1. `adobe.all-component.timeout`：製品のすべてのサービスのタイムアウトを上書きします。
1. `adobe.<serviceName>.timeout`：キーに指定されたサービス（&lt;サービス名>）のタイムアウトのみを上書きします。サービスレベルの値が設定されている場合、このコマンドを使用すると、指定したサービスがアプリケーションレベルに設定されている場合に、そのサービスのタイムアウト値だけが上書きされます。
1. `adobe.<serviceName>.<operationName>.timeout`：キーで言及されている特定のサービスの操作のタイムアウトのみを上書きします（&lt;サービス名>.&lt;操作名>）。値が操作レベルで設定されている場合、このコマンドを使用すると、指定したサービスがアプリケーションレベルまたはサービスレベルで設定されている場合に、そのサービスのタイムアウト値だけが上書きされます。

**例：**

次のコマンドを使用して、コンポーネントレベルでタイムアウトを設定します。

1. すべてのサービス操作のタイムアウトを 600 秒に設定するには、次を使用します。

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. `DesigntimeService` 操作値のタイムアウトを 500 秒に設定するには、次を使用します。

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. `DesigntimeService's previewLCA` 操作値のタイムアウトを 700 秒に設定するには、次を使用します。

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. 読み込み、インストールなどの `DSC operations` を 600 秒に設定するには、次を使用します。

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## AEM [!DNL Forms JEE] のインストールと設定  {#install-and-configure-aem-forms-jee}

1. /deploy フォルダーのバックアップを作成します。Quick Fix をアンインストールする場合は必須です。
1. アプリケーションサーバーを停止します。
1. パッチインストーラーアーカイブファイルをハードディスクに展開します。
1. 使用しているオペレーティングシステムに従って名前が付けられたディレクトリで、次の操作を実行します。

   **Windows**

   インストールメディア上、またはインストーラーをコピーしたハードディスク上のフォルダーの適切なディレクトリに移動します。

   * （Windows 32 ビット版）：Disk1\InstData\Windows\VM
   * （Windows 64 ビット版）：Disk1\InstData\Windows_64bit\VM

   次に、次の名前のファイルをダブルクリックします。

   * aemforms63_cfp_install.exe **（AEM [!DNL Forms] 6.3**）
   * aemforms62_cfp_install.exe **（AEM [!DNL Forms] 6.2**）
   * aemforms61_cfp_install.exe（**AEM [!DNL Forms] 6.1**）

   **Linux、Solaris、 AIX**

   適切なディレクトリに移動します。

   * （Linux）：Disk1/InstData/Linux/NoVM
   * （Solaris）：Disk1/InstData/Solaris/NoVM
   * （AIX）：Disk1/InstData/AIX/VM

   コマンドプロンプトで、次のように入力します。

   * ./aemforms63_cfp_install.bin（**AEM [!DNL Forms] 6.3**）
   * ./aemforms62_cfp_install.bin（**AEM [!DNL Forms] 6.2**）
   * ./aemforms61_cfp_install.bin（**AEM [!DNL Forms] 6.1**）

   インストールの手順を示すインストールウィザードが起動します。

1. 概要パネルで「**[!UICONTROL 次へ]**」をクリックします。
1. インストールフォルダーを選択画面で、表示されるデフォルトの場所が既存のインストール場所であることを確認するか、または「**[!UICONTROL 参照]**」をクリックして AEM [!DNL Forms] がインストールされている別のフォルダーを選択してから、「**[!UICONTROL 次へ]**」をクリックします。
1. Quick Fix パッチの概要の情報を読み、「**[!UICONTROL 次へ]**」をクリックします。
1. プリインストールの概要情報を読み、「**[!UICONTROL インストール]**」をクリックします。
1. インストールが完了したら、「**[!UICONTROL 次へ]**」をクリックして、インストールされたファイルに対して Quick Fix アップデートを適用します。
1. 「Configuration Manager を起動」チェックボックスはデフォルトで選択されています。「**[!UICONTROL 完了]**」をクリックして Configuration Manager を実行します。

   Configuration Manager を後で実行するには、「**[!UICONTROL 完了]**」をクリックする前に、「**[!UICONTROL Configuration Manager を起動]**」オプションの選択を解除します。*`[AEM_forms_root]`/configurationManager/bin* ディレクトリにある該当するスクリプトを使用して、Configuration Manager を後で起動することができます。

1. アプリケーションサーバーに応じて、以下のいずれかのドキュメントを選択し、「*AEM [!DNL Forms]* の設定とデプロイ」節の指示に従ってください。

   AEM [!DNL Forms] 6.3 の場合は、次を参照してください。

   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（JBoss 版）](https://helpx.adobe.com/jp/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebSphere 版）](https://helpx.adobe.com/jp/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebLogic 版）](https://helpx.adobe.com/jp/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   AEM [!DNL Forms] 6.2 の場合は、次を参照してください。

   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（JBoss 版）](http://www.adobe.com/go/learn_aemforms_installJBoss_62_jp)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebSphere 版）](http://www.adobe.com/go/learn_aemforms_installWebSphere_62_jp)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebLogic 版）](http://www.adobe.com/go/learn_aemforms_installWebLogic_62_jp)

   AEM Forms 6.1 については、次を参照してください。

   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（JBoss 版）](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebSphere 版）](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [ [!DNL Forms]  AEM のインストールおよびデプロイ（WebLogic 版）](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. AEM [!DNL Forms] JEE サーバーを再起動します。
