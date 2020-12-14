---
title: 累積修正パックのAEM FormsJEEへのインストール
description: AEM FormsJEEでのCumulative Fix Pack(CFP)のインストールおよび設定手順の概要
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 23%

---


# AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}への累積修正パックのインストール

## AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}にCFPをインストール

指定した順序で次の手順を実行し、累積修正パックをAEM 6.3 [!DNL Forms JEE]にインストールします。

1. [Adobeサポート](https://www.adobe.com/jp/account/sign-in.supportportal.html)に連絡して、CFPのAEM 6.3 [!DNL Forms JEE]インストーラーを入手してください。
1. [AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee)のインストールと設定の説明に従って、CFPインストーラーを実行し、AEM [!DNL Forms JEE]を設定します。
1. 最新のAEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)をインストールします。
1. AEM CFP [6.3.3.x追加](aem-forms-releases.md)用の[!DNL Forms]-onパッケージをインストールします。

### AEM [!DNL Forms JEE]バンドルパッケージ{#install-aem-forms-jee-bundles-package}をインストールします

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1;バージョン1.0.2)は、AEM上の [!DNL Forms] ユーザーに、AEM上 [!DNL Forms JEE] と同じ権限および機能を提供 [!DNL Forms OSGi]します。パッケージマネージャーでインストール済みのパッケージを確認し、パッケージがまだインストールされていない場合はインストールします。

### CQ-4208044の追加手順{#additional-instructions-for-cq}

AEM 6.3 [!DNL Forms JEE]サーバーとOracleデータベースを使用している場合は、CFP1のデプロイ後、つまりConfiguration Managerの実行後に、以下の設定を設定します。 この設定は、エンタープライズドメインの同期が実行されるときに、ユーザー、グループおよびグループメンバーを同期するために必要です。 [AEM 6.3リリースノート](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205)のCQ-4208044の問題を参照してください。

1. **管理者** UIにログインします。
1. **[!UICONTROL 設定]**/**[!UICONTROL User Management]**/**[!UICONTROL 設定]**/**[!UICONTROL 設定ファイルの読み込みと書き出し]**&#x200B;に移動します
1. config.xmlファイルを書き出します。
1. *config.xml*&#x200B;のドメイン設定で、「`groupMemberDBQueryBatchSize`」のエントリを変更します。 サンプルエントリ：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. 変更したファイルを再度読み込んでから、同期を再実行してください。

## AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}にCFPをインストール

指定した順序で次の手順を実行して、累積修正パックをAEM 6.2 [!DNL Forms JEE]にインストールします。

>[!NOTE]
>
>AEM 6.2 [!DNL Forms OSGi]を使用している場合は、[AEM 6.2 CFPリリースノートのインストール手順に従ってください。](release-notes-aem-6-2-cumulative-fix-pack.md)

1. [Adobeサポート](https://www.adobe.com/account/sign-in.supportportal.html)に連絡して、CFP用のAEM 6.2 [!DNL Forms JEE]インストーラーを入手してください。
1. [AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee)のインストールと設定の説明に従って、CFPインストーラーを実行し、AEM [!DNL Forms JEE]を設定します。
1. [AEM Hotfix 12785 version 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785)をインストールします。
1. [AEM 6.2 Service Pack 1](https://helpx.adobe.com/jp/experience-manager/6-2/release-notes/sp1.html)をインストールします。
1. 最新の[AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md)をインストールします。
1. [AEM 6.2 Service Pack 1 CFP ](aem-forms-releases.md)用追加の[!DNL Forms]-onパッケージをインストールします。

### AEM [!DNL Forms JEE]バンドルパッケージ{#install-aem-forms-jee-bundles-package-1}をインストールします

[AEM FormsJEEパッケージ](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) (aemfd-jee-bundles-package-6.2CFP5;バージョン1.0.2)は、AEM上の [!DNL Forms] ユーザーに、AEM上 [!DNL Forms JEE] と同じ権限および機能を提供 [!DNL Forms OSGi]します。パッケージマネージャーでインストール済みのパッケージを確認し、パッケージがまだインストールされていない場合はインストールします。

### コンポーネントレベルでの操作のタイムアウトの設定(NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>AEM 6.2 CFP4の後は、次の手順で、アップグレードプロセス中にタイムアウトが原因で問題が発生した場合にDSC操作のタイムアウトを設定できます。 ([AEM 6.2 CFP4リリースノート](release-notes-aem-6-2-cumulative-fix-pack.md)のNPR-16774を参照)。

DSCのデプロイメントには、失敗する可能性があるため、変数の時間がかかります。 インストール、読み込み、開始、停止などのDSC操作のタイムアウトを変更するには、-Dオプションを指定してJVM引数を使用して`adobe.component.registry.timeout`を設定する必要があります。

キーの値を秒単位で指定します。 例：`-Dadobe.component.registry.timeout=300`

また、次の3つのプロパティを使用して、コンポーネントレベルでタイムアウトを変更することもできます。

1. `adobe.all-component.timeout`:は、製品のすべてのサービスのタイムアウトを上書きします。
1. `adobe.<serviceName>.timeout`:は、キーに指定されたサービス(&lt;servicename>)のタイムアウトのみを上書きします。サービスレベルの値が設定されている場合、このコマンドを使用すると、指定したサービスがアプリケーションレベルに設定されている場合に、そのサービスのタイムアウト値だけが上書きされます。
1. `adobe.<serviceName>.<operationName>.timeout`:特定のサービスの操作のタイムアウトのみを上書きします&lt;servicename>。&lt;operationname>)がキーで言及されている。値が操作レベルで設定されている場合、このコマンドを使用すると、指定したサービスがアプリケーションレベルまたはサービスレベルで設定されている場合に、そのサービスのタイムアウト値だけが上書きされます。

**例:**

次のコマンドを使用して、コンポーネントレベルでタイムアウトを設定します。

1. すべてのサービス操作のタイムアウトを600秒に設定するには：

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. `DesigntimeService`操作値のタイムアウトを500秒に設定するには、次を使用します。

   &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;を設定

1. `DesigntimeService's previewLCA`操作値のタイムアウトを700秒に設定するには、次を使用します。

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. load、installなどの`DSC operations`を600秒に設定するには、次を使用します。

   &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;を設定

## AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}のインストールと設定

1. /deployフォルダーのバックアップを作成します。 Quick Fix をアンインストールする場合は必須です。
1. アプリケーションサーバーを停止します。
1. パッチインストーラーのアーカイブファイルをハードドライブに展開します。
1. 使用しているオペレーティングシステムに従って名前が付けられたディレクトリで、次の操作を実行します。

   **Windows**

   インストールメディアまたはハードディスク上の、インストーラーをコピーしたフォルダーの適切なディレクトリに移動します。

   * （Windows 32ビット）:Disk1\InstData\Windows\VM
   * （Windows 64ビット）:Disk1\InstData\Windows_64bit\VM

   次に、次の名前のファイルを重複キーを押しながらクリックします。

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux、Solaris、AIX**

   適切なディレクトリに移動します。

   * (Linux):Disk1/InstData/Linux/NoVM
   * (Solaris):Disk1/InstData/Solaris/NoVM
   * (AIX):Disk1/InstData/AIX/VM

   コマンドプロンプトで、次のように入力します。

   * 。/aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * 。/aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * 。/aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   インストールの手順を示すインストールウィザードが起動します。

1. 概要パネルで「**[!UICONTROL 次へ]**」をクリックします。
1. インストールフォルダを選択画面で、表示されるデフォルトの場所が既存のインストールに適していることを確認するか、「**[!UICONTROL 参照]**」をクリックしてAEM [!DNL Forms]が現在インストールされている別のフォルダを選択し、「**[!UICONTROL 次へ]**」をクリックします。
1. Quick Fix パッチの概要の情報を読み、「**[!UICONTROL 次へ]**」をクリックします。
1. プリインストールの概要情報を読み、「**[!UICONTROL インストール]**」をクリックします。
1. インストールが完了したら、「**[!UICONTROL 次へ]**」をクリックして、インストールされたファイルに対して Quick Fix アップデートを適用します。
1. 「Configuration Manager を起動」チェックボックスはデフォルトで選択されています。「**[!UICONTROL 完了]**」をクリックして Configuration Manager を実行します。

   Configuration Manager を後で実行するには、「**[!UICONTROL 完了]**」をクリックする前に、「**[!UICONTROL Configuration Manager を起動]**」オプションの選択を解除します。Configuration Managerは、後で&#x200B;*`[AEM_forms_root]`/configurationManager/bin*&#x200B;ディレクトリの適切なスクリプトを使用して開始できます。

1. アプリケーションサーバーに応じて、以下のいずれかのドキュメントを選択し、「*AEM の設定とデプロイ[!DNL Forms]*」節の指示に従ってください。

   AEM [!DNL Forms] 6.3の場合は、次を参照してください。

   * [ [!DNL Forms] AEM のインストールおよびデプロイ（JBoss 版）](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebSphere 版）](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebLogic 版）](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   AEM [!DNL Forms] 6.2の場合は、次を参照してください。

   * [ [!DNL Forms] AEM のインストールおよびデプロイ（JBoss 版）](http://www.adobe.com/go/learn_aemforms_installJBoss_62_jp)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebSphere 版）](http://www.adobe.com/go/learn_aemforms_installWebSphere_62_jp)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebLogic 版）](http://www.adobe.com/go/learn_aemforms_installWebLogic_62_jp)

   AEM Forms6.1については、次を参照してください。

   * [ [!DNL Forms] AEM のインストールおよびデプロイ（JBoss 版）](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebSphere 版）](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [ [!DNL Forms] AEM のインストールおよびデプロイ（WebLogic 版）](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. AEM [!DNL Forms] JEEサーバーを再起動します。
