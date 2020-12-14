---
title: AEM 6.2 累積修正パック
description: 'null'
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '19954'
ht-degree: 21%

---


# AEM 6.2累積Fix Packリリースノート{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## リリース情報 {#release-information}

| **製品** | Adobe Experience Manager |
|---|---|
| **バージョン** | 6.2 |
| **リリース** | [累積修正パック6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **前提条件** | [AEM 6.2 Service Pack 1](https://helpx.adobe.com/jp/experience-manager/6-2/release-notes/sp1.html) |
| **一般リリース** | 2019年6月06日 |

### 累積修正パック {#cumulative-fix-pack}

アドビは、複数の修正を一度にリリースする配信モデルを導入しました。Adobeでは、個々の問題に対してホットフィックスをリリースする代わりに、Cumulative Fix Pack (CFP)を毎月リリースするようになりました（品質チェックに合格した場合）。 CFP は複数の修正を集約したコンテンツパッケージです。CFP には主にバグ修正が含まれていますが、機能パックも含まれる場合があります。CFP には個別ホットフィックスリリースと比較して、次の利点があります。

* 累積的な性質（例えば、ある CFP には以前の CFP で配信された修正が含まれます）
* 品質保証の向上
* インストールの単純化（最新のサービスパック以外には依存しない、単一パッケージとして CFP をインストールできます）。

CFPと他のタイプのリリースについて詳しくは、[メンテナンスリリースの車両](https://docs.adobe.com/content/docs/ja-JP/aem/6-2/deploy/maintenance-release-vehicle-definitions.html)を参照してください。

## リリースについて {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20は、AEM 6.2用の最後の累積Fix Packで、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

>[!CAUTION]
>
>インストールされた機能パック間の互換性を検証せずに CFP を適用すると、システム障害またはカスタム設定の損失が発生する恐れがあります。その場合、解決するためにバックアップから復元する必要が出ることがあります。

>[!NOTE]
>
>* AEM Cumulative Fix Pack 6.2 SP1-CFP10には、新しいSling `discovery-  api`バンドルJohnzon 1.0.0が含まれています。 さらに、サービスユーザーsling-discoveryには、CRXリポジトリのノード&#x200B;*/var/discovery*&#x200B;に対する読み取りおよび書き込み権限が追加されます。
   >
   >
* **org.apache.commons/commons-email/1.5**&#x200B;の電子メールバンドルが追加され、**com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**&#x200B;に置き換えられました。
   >
   >
* Adobeでは、AEMインスタンスに多数のユーザーを置いている場合に、installフォルダーを介してCFPをデプロイすることをお勧めします。

>



## {#issues-included}を含む問題

このセクションでは、現在の CFP に含まれるすべての問題とホットフィックスについて説明します。

さらに、このCFPには、以前の累積修正パック](#previous)で提供されたホットフィックスが含まれます。[

### 統合 {#integration}

* 複数のキャンペーンターゲット設定のパーソナライゼーションのバックポートが改善されました。 NPR-29163：CQ-4264126 のホットフィックス
* com.day.cq.personalization.impl.TeaserResourceEventHandler が無限ループに入り、パブリッシュインスタンスのノードをアップデートする原因になる。NPR-28561：CQ-4263096 のホットフィックス

### DAM - 一般 {#dam-general}

* 特定のDamフォルダーの管理者以外のユーザーに対して、レプリケーションボタンを表示/非表示にできません。 NPR-29026：CQ-4265361 のホットフィックス

### 脆弱性 {#vulnerability}

* CSRF 保護フレームワークが、AEM 基盤フォームで機能しない。NPR-28612：GRANITE-22231 のホットフィックス

### フォーム {#forms}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms ユーザーは、AEM サービスパック、累積修正パック、機能パックのいずれかをインストールした後で、AEM Forms アドオンパッケージをインストールすることが不可欠です。

>[!NOTE]
>
>AEM Forms アドオンパッケージは、AEM サービスパックおよび累積修正パックとのフォーム機能の整合性を確保するために役立ちます。そのため、AEM Service Pack、累積Fix Pack、または機能パックをインストールした後に、AEM Formsアドオンパッケージをインストールする必要があります。

#### アダプティブフォーム {#adaptive-forms}

* iOS 12.1デバイス用の手書きメモコンポーネントの使い勝手の問題。 NPR-29082：CQ-4261765 のホットフィックス

#### Forms - Document Security {#forms-document-security}

* PDF Advanced Electronic Signatures(PAdES)を使用してPDF内のすべての署名を検証すると、InvalidOperationExceptionがスローされます。 NPR-27848：CQ-4244837 のホットフィックス

#### Forms — 通信{#forms-correspondence}

* レターをPDFとしてプレビューする場合、マスターページに配置されたテキストフィールドは、データタブまたは指定されたデータリンケージに従って入力された値を使用しません。 NPR-29239：CQ-4266856 のホットフィックス.

#### Forms - インタラクティブコミュニケーション {#forms-interactive-communication}

* アポストロフィ文字を追加すると、レター内の事前入力されたフィールドは、通常のアルファベットではなく、ASCII文字で表示されます。 NPR-28863：CQ-4262900 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer}

* Forms JEE インストーラーには、新しい AEM Forms の修正はありません。

## 以前の累積修正パックに含まれていたホットフィックスと機能パック {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### 累積修正パック 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19は重要なアップデートで、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* AEM 6.2へのMS Translator API v3.0のサポートを有効にしました。
* すべてのSP、CFP、およびHF用のパッケージが正常にインストールされた後に追加されたログメッセージ。

### Assets {#assets}

* 権限「ACLを編集」がない場合は、DAMフォルダーの名前を変更できません。 NPR-27555：CQ-104652 のホットフィックス
* 6.2.1 CFP 17以降では、画像プリセットエディタツールがレスポンシブではありません。 NPR-28147：CQ-4261041 のホットフィックス

### Sites {#sites}

* リンクチェッカーはジョブを完了せず、応答のないリンクで停止します。 NPR-27373：CQ-4256030 のホットフィックス
* セグメントのパスを壊す追加のルートパスが原因で、セグメントファイルが正しく読み込まれません。 NPR-28014：CQ-4260332 のホットフィックス

### 統合 {#integration-1}

* LiveCopy継承のキャンセルが、対象コンテナで正しく機能しません。 NPR-28129：CQ-4259813 のホットフィックス
* cq :actionsは、対象のコンポーネントに対しては考慮されません。 NPR-27616：CQ-4257497 のホットフィックス

* 継承を無効にするアイコンの表示は一貫していません。 NPR-27671：CQ-4257779 のホットフィックス

### Felix {#felix}

* AEM 6.2 SP1インスタンスにCFP 18をインストールした後、Webコンソールコンポーネントの詳細が500で失敗する。 NPR-28350：CQ-4261095 のホットフィックス

### 翻訳 {#translation}

* MS TranslatorをAPI v3.0にアップグレードした後、AEM 6.3でMS Translatorサービスのサポートを有効にします。NPR-28123:CQ-4259096の修正プログラム

### UI - 基盤 {#ui-foundation}

* OOTBサイトカレンダーに正しくない日付が表示される。 NPR-28392

### Granite {#granite}

* sling :basenameを使用してリソースバンドルのディクショナリが無効になりません。 NPR-27624

### 維持 {#sustenance}

* パッケージマネージャーのアクティビティログは、別のログファイルに抽出する必要がある。NPR-27323：Granite-14866 のホットフィックス
* インストールが完了したときに表示されるerror.log内の標準化されたフレーズ/単語/ログ行です。 NPR-27835
* Graniteパッケージプラグインは、org.apache.sling.i18nの下位バージョンの依存関係を選択しています。 CQ-4263245 のホットフィックス
* 6.2SP1-CFP15の後で最新のCFPをインストールすると、com.adobe.cq.com.adobe.cq.ui.commonsバンドルが削除される。 CQ-4258808 のホットフィックス

### フォーム {#forms-1}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-1}

#### アダプティブフォーム {#adaptive-forms-1}

* AEM Forms の XML インジェクションの脆弱性。NPR-27843：CQ-4257315 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-1}

* Forms JEE インストーラーには、新しい AEM Forms の修正はありません。

### {#osgi-bundles-and-content-packages-included}に含まれるOSGIバンドルとコンテンツパッケージ

次のテキストドキュメントには、CFPに含まれるOSGIバンドルとコンテンツパッケージのリストが示されています。

AEM 6.2 SP1-CFP19に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2SP1-CFP19に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/cfp19_content_packages.txt)

### 累積修正パック 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18は重要なアップデートで、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* DAM CommandLineProcessで、長時間実行中のプロセスを停止するサポートが追加されました。
* ReplicationEventListenerでのセッションリークを修正。
* コアページコンポーネントにリダイレクトのサポートを追加しました。

### アセット{#assets-1}

* 大量の取り込みが行われる間にCamera Rawプロセスが停止し、最終的にすべてのワークフロー処理がブロックされる。 NPR-26990：NPR-23860 のホットフィックス
* ダウンロード機能は、assetdownloadサーブレットを介してAEM Assetsを利用し、匿名ユーザーがすべてのアセットをダウンロードできるようにします。 NPR-27054、CQ-4254732用の修正プログラム
* AEMの電子メールテンプレートの件名行に、特殊文字が壊れて表示されます。 NPR-26470：CQ-4252368 のホットフィックス

### サイト{#sites-1}

* ConfigPostProcessorクラスの不正な動作により、親画像を中断するとcqが削除されます。子ページからのLiveRelationship混合タイプ。 NPR-26745：CQ-4254163 のホットフィックス
* コアページコンポーネントへ追加のリダイレクトのサポート。 NPR-26576：CQ-110529 のホットフィックス
* コンテキストハブをjquery 3に移行します。 NPR-26956：CQ-4255472 のホットフィックス
* アンカー入力フィールドは、ダイアログ上のブラウザー表示セクションの外に、最大化されるまで表示されます。 NPR-26852：CQ-4255019 のホットフィックス
* 不要な&lt;br>を挿入するテキストの貼り付けをコンテンツフラグメントにコピーします。 NPR-26660：CRTE-151 のホットフィックス
* 一部のページの右側のペインにリストが表示されない。 NPR-27247：CQ-4251621 のホットフィックス
* （クラシックUI）ページの移動/名前変更を試みると、「ページの移動中にエラーが発生しました」というエラーが発生します。 NPR-27179：CQ-4235907 のホットフィックス

### 統合 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever が、使用可能なブランドを収集するために、ツリー全体を調べる。NPR-27060：CQ-4255790 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components}

* Foundationリストコンポーネントに関する検索機能の問題。 NPR-26817：CQ-4250324 のホットフィックス

### プラットフォーム {#platform}

* 特殊文字のemダッシュが原因で、パブリッシャーでキャッシュをフラッシュ中に問題が発生しています。 NPR-27199：CQ-4242790 のホットフィックス

### 花崗岩{#granite-1}

* パッケージ検証ツールが、CFP/SP に含まれるパッケージを検証しない。NPR-26775：Granite-22825 のホットフィックス

### レプリケーション {#replication}

* ReplicationListenerでのJCRセッションリーク。 NPR-27063：CQ-4232088 のホットフィックス

### フォーム {#forms-2}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-2}

* Forms アドオンパッケージには、新しい AEM Forms の修正はありません。

### Forms JEE インストーラー {#forms-jee-installer-2}

* Forms JEE インストーラーには、新しい AEM Forms の修正はありません。

#### {#osgi-bundles-and-content-packages-included-1}に含まれるOSGIバンドルとコンテンツパッケージ

AEM 6.2 SP1-CFP18に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### 累積修正パック 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17は重要なアップデートで、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* at-integration.jsのサイト拡張なしURLのサポートを追加しました。
* S7ポーリングインポーターがS7クラウドサービス設定から削除されました。
* マルチテナント実装のオーディエンスー構造をサポートするために、フォルダー表示を変更しました。
* jqueryuiの更新   clientlib v1.12.1.

### アセット{#assets-2}

* アセットUIからワークフローを開始するには、ユーザーに書き込み/削除/変更権限が必要です。 NPR-25688：CQ-4250140 のホットフィックス
* 「公開」ボタンと「非公開」ボタンは、「複製」権限を持たないユーザーでも表示されます。 NPR-25094
* （ワークフロー）スマートタグアセットワークフローは、AEMプロキシ設定を通じて処理されません。 NPR-25915：CQ-4248202 のホットフィックス
* S7クラウドサービス設定からS7ポーリングインポーターを削除します。 NPR-25239：CQ-95236 のホットフィックス

### サイト{#sites-2}

* エディターから開始したワークフロー->ページ情報には、ペイロード内のコンテキストパスが含まれます。 NPR-26389：CQ-76804 のホットフィックス
* （外部リンクチェッカー）無効なhttpsリンクは有効なリンクとして表示されます。 NPR-25541：CQ-4201333 のホットフィックス
* （クラシックUI）ライブコピーの下にスタンドアロンページを作成する場合、そのページはライブコピーとして作成されます。 NPR-25610：CQ-4249801 のホットフィックス
* ページがアクティブ化されたときにデザインインポーターコンポーネントに関連付けられたリソースを発行する際の問題 NPR-25638：CQ-102532 のホットフィックス
* RTEリッチテキストツールバーは、選択したリストをカバーします。 NPR-25165：CQ-4248948 のホットフィックス
* ContextHubをjquery 3に移行します。 NPR-25059：Granite-19902 のホットフィックス
* ネストされたparsysコンポーネントの場合、デザインを満たす最初の（ネストされたパスが最も少ない）部分が、複数の使用可能なコンポーネントから常に適用されます。 詳しくは、[デザインパスの解像度](https://helpx.adobe.com/jp/experience-manager/6-3/sites/developing/using/page-templates-static.html)を参照してください。 NPR-25250：CQ-4246276 のホットフィックス

### 統合 {#integration-3}

* OOTBターゲット統合を使用して、コンポーネントをターゲット設定すると、空のターゲットコンポーネントではなく、ページ全体がレンダリングされます。 NPR-25273：CQ-4248003 のホットフィックス
* ターゲット設定モードで継承を無効にしても、継承を使用したターゲットコンポーネントが編集モードで壊れていないことが示されます。 NPR-25324：CQ-4248162 のホットフィックス
* ページでパーソナライゼーションが定義され、オーディエンスが解決されると、対応するエクスペリエンスが編集モードで表示されます。 NPR-25731：CQ-4249465 のホットフィックス
* デフォルト以外のコンテキストパスでAEMを使用した場合に、誤ったティーザーURLが表示されます。 NPR-25971：CQ-4250953 のホットフィックス
* オプトアウトを使用した場合に空白のレンダリングが行われます。 NPR-25295：CQ-4246792 のホットフィックス
* 作成者環境から削除されたエクスペリエンスが、ページのアクティベーション時に発行サイトから削除されることはありません。 NPR-24869：CQ-4247832 のホットフィックス

### DAM - DM クライアント {#dam-dm-client}

* (Chrome、Firefox)タッチ対応デバイスでのマウスクリックは無視されます。 CQ-4247370 のホットフィックス

### プラットフォーム {#platform-1}

* パッケージの取得/解放時に最大再試行数を設定できます。 NPR-25328：Granite-22376 のホットフィックス
* レプリケーションエラーが発生した場合に正しくログに記録されません。 NPR-25308：CQ-4249402 のホットフィックス
* FormsAEM 6.2FormsCFP8をCFP14にインストールすると、Apache POIが失敗します。 NPR-25053：Granite-21771 のホットフィックス

### 花崗岩{#granite-2}

* OakConstraint0022例外が発生し、ユーザー同期プロセスが失敗しています。 NPR-25729:Oak-7428用修正プログラム

### Communities {#communities}

* cq -social-as-providerバンドルは、mongoドライバー3.xバージョンと開始しません。 NPR-26271：CQ-4252710 のホットフィックス

### UI - 基盤 {#ui-foundation-1}

* jqueryuiの更新   clientlib v1.12.1. NPR-25090:Granite-21981、CQ-4248897用修正プログラム

* (Omnisearch):&#39;Title&#39;プロパティは、Sitesのクロスサイト(XSS)スクリプティングに対して脆弱です。 NPR-24994：Granite-19933 のホットフィックス

### フォーム {#forms-3}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-3}

#### アダプティブフォーム {#adaptive-forms-2}

* アダプティブフォームからデータを送信する際に誤ったエンコーディングが発生する。 NPR-25539

#### Forms - 管理 {#forms-management}

* ページの発行時に参照としてレポートされた、関連のないフォームアセット。 NPR-26167：CQ-4251004 のホットフィックス

### Forms - JEE インストーラー {#forms-jee-installer-3}

#### Document Security {#document-security}

* 変数がデータタイプリストとして入力され、サブタイプが文字列ですが、「オブジェクトを強制できません」というエラーが発生します。 NPR-26194：CQ-4252287 のホットフィックス
* 6.2-SP1-CFP15のインストール後、透かしの設定にアクセスできない。 NPR-26130：CQ-4250984 のホットフィックス

### {#osgi-bundles-and-content-packages-included-2}に含まれるOSGIバンドルとコンテンツパッケージ

AEM 6.2 SP1-CFP17に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2SP1-CFP17に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### 累積修正パック 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16は重要なアップデートで、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* Day CQ 電子メールサービスに STARTTLS サポートを追加。
* プロファイルポーバーでのContextHubアイコンの位置揃えを修正しました。
* ドロップダウンコンポーネントの表示／非表示機能を修正しました。
* 最新のJacksonバージョン2.8.11へのアップグレード

### アセット{#assets-3}

* リスト表示からワークフローを開始できません。 NPR-24393：CQ-4245788 のホットフィックス
* (Firefox/Chrome)アセット共有ページでアセットをダウンロードできません。 NPR-24523：CQ-4224408 のホットフィックス
* AEMのビデオプレビューのデフォルト画質が向上しました。 NPR-24148：CQ-4244310 のホットフィックス

### 統合 {#integration-4}

* コンポーネントが発行インスタンスをターゲットにすると、ターゲットに設定されたエクスペリエンスより前のデフォルトのエクスペリエンスがちらつきで表示されます。 NPR-23992：CQ-4242038 のホットフィックス
* 作成者環境から削除されたエクスペリエンスが、ページのアクティベーション時に発行サイトから削除されることはありません。 NPR-24869：CQ-4247832 のホットフィックス

### プラットフォーム {#platform-2}

* clientlib から jQuery 1.12.4 にパッチを適用して、セキュリティ修正を含める。NPR-24129：Granite-20058 のホットフィックス
* Day CQ 電子メールサービスに STARTTLS サポートを追加。NPR-23941：CQ-4240397 のホットフィックス
* デフォルトのMERGE_PRESERVE aclHandlingを削除します。 NPR-24593：Granite-21889 のホットフィックス
* リクエストに無効なクエリパラメーターが含まれている場合、LineCheckerはリンクを外部化できません。 NPR-24127：CQ-4241893 のホットフィックス

### MSM {#msm}

* クロスサイトスクリプティング攻撃(XSS)に対するプロアクティブなホットフィックス。 NPR-21893：CQ-4223385 のホットフィックス
* MSM LiveRelationship:BlueprintConfigがルートにある場合、有効なロールアウト設定が正しくありません。 NPR-23999：CQ-4243000 のホットフィックス

### サイト{#sites-3}

* ライブコピー領域で新しいエクスペリエンスを作成するには、継承が機能しないように設定する必要があります。 NPR-24995、CQ-4248209用の修正プログラム
* （タッチUI）ページのロックまたはロック解除を行うと、上部のツールバーのいくつかのアイコンが消えます。 NPR-23954：CQ-4243345 のホットフィックス
* contexthub内のフィールドの配置が正しくない。 NPR-23958
* ロックされた改ページのオーサリングに対する発行アクション。 NPR-23970：CQ-4243203 のホットフィックス
* /etc/reports/のOOTBレポートが正常に機能せず、履歴データグラフも表示されません。 NPR-20035：CQ-4220180 のホットフィックス
* プロジェクトで&#39;起動の要求&#39;ワークフローを開始中に、起動の作成に失敗しました。 NPR-24255：CQ-4245030 のホットフィックス
* CFP10のインストール後に電子メールを送信する際に無視されるHTMLタグと属性。 NPR-24287：CQ-4240028 のホットフィックス
* TagPicker:タグメタデータスキーマのタグフィールドクエリタグ可能なノード内のタグ提案。したがって、読み込みに時間がかかります。 NPR-24347：CQ-4244291 のホットフィックス
* Salesforce統合は、プロキシ設定では失敗します。 NPR-24418：CQ-4245300 のホットフィックス
* (WCM)PageManagerは、リビジョンの作成中、例外時にページをチェックインしたままにします。 NPR-24565：CQ-4246203 のホットフィックス
* CFP14を適用すると、「Device Emulator」ボタンが編集モードとプレビューモードから消えます。 NPR-24566：CQ-4247060 のホットフィックス
* （クラシックUI）ダイアログでオーサリングすると、タグ全体が空として表示されます。 NPR-24688、CQ-4246407用の修正プログラム
* 最初の試行でバージョンを作成できません。 NPR-24774：CQ-4232176 のホットフィックス
* /etc/reports/のOOTBレポートが正常に機能せず、履歴データグラフも表示されません。 NPR-24138：CQ-4220180 のホットフィックス

### 脆弱性 {#vulnerability-1}

* Salesforce 統合が、サーバーサイド要求偽造（SSRF）に対して脆弱。NPR-24289：CQ-4245277 のホットフィックス
* ReportingServicesProxyServletのサーバー側要求偽造(SSRF)の脆弱性。 NPR-24657：CQ-4246880 のホットフィックス

### 花崗岩{#granite-3}

* メタデータの読み取り操作を終了できません。 NPR-24240：Granite-19866 のホットフィックス
* 脆弱性を修正するために、Jettyを9.4.11.v20180605に更新しました。 NPR-25033：Granite-22120 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-1}

* ページの並べ替え中にClassCastExceptionをスローするPageComparator。 NPR-24123：CQ-4244048 のホットフィックス
* フォームドロップダウンコンポーネントの表示／非表示機能が期待どおりに機能しない。NPR-24562：CQ-4222853 のホットフィックス

### ユーザーインターフェイス {#user-interface}

* 管理者の検索機能のリクエストが多いため、CPU 使用率が高くなる。NPR-23588：Granite-21286 のホットフィックス
* （クラシックUI）関連付けられたフォームデータモデルサービスが空のフィールドに設定されている場合でも、コンポーネントはデフォルト値を表示します。 NPR-21903：GRANITE-19744 のホットフィックス
* 要求にFormDataが存在しない場合にNPEをスローするマルチフィールド。 NPR-24513：Granite-21055 のホットフィックス

## フォーム {#forms-4}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-4}

#### コア {#core}

* (OSGI)AEM FormsOSGIは、ジャクソンのデータバインディングセキュリティ警告の影響を受けている。 NPR-24274：CQ-4230245 のホットフィックス

#### Rights Management {#rights-management}

* Apache POIは、インストール後AEM 6.2 SP1-CFP14で失敗します。 NPR-25054、NPR-25052：CQ-4245898、CQ-4244778 のホットフィックス

#### HTML5 のフォーム {#html-forms}

* HTMLプレビューでの複数行のフィールドの事前入力に関する情報は、データに入力されません。 NPR-23357：CQ-4244212 のホットフィックス
* レターをデフォルトのプレビューでプレビューする場合、レイアウトフラグメントマッピングは表示されませんが、プレビューボタンをクリックしたときに同じマッピングが正しく表示されます。 NPR-22993：CQ-4237745 のホットフィックス
* テンプレートに社会保障番号パターンが適用された場合の、テキストフィールドのHTMLプレビューに関する問題が発生します。 NPR-23205

#### アダプティブフォーム {#adaptive-forms-3}

* AEMフォームをparsysコンポーネントに追加中に、「Guidelibが定義されていません」というエラーが発生する。 NPR-24269：CQ-4244546 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* シェルスクリプトファイルのウィンドウ行の終わりは、UNIXでLCMが実行されない原因となります。 NPR-22958

### {#osgi-bundles-and-content-packages-included-3}に含まれるOSGIバンドルとコンテンツパッケージ

AEM 6.2 SP1-CFP16に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2SP1-CFP16に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### 累積修正パック 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15は、[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* デザインの一貫性を維持するために、Foundationテーブルのプロアクティブなセキュリティ修正を行いました。
* 値を文字列として保存するためのtypeHintのサポートを追加しました。
* Forms事前入力サービスのセキュリティ強化を提供
* 最新のadobe-reader-extensions-dsc.jarファイルに更新し、Reader拡張機能の修正を確認します。
* 検証フックを調整し、ブースト値の入力で「:invalid」項目を考慮しました。

### アセット{#assets-4}

* EmbedXMP データが Ptiff 生成プロセスで常に「アクティブ」に設定される。NPR-22776：CQ-4234498 のホットフィックス
* 複数値フィールドに複数のデフォルト値を設定できません。 NPR-22900：CQ-4239000 のホットフィックス
* (Dynamic Media)「ダイナミックレンディション」チェックボックスを選択すると、ダウンロードしたzipファイルが、0バイトファイルの元のTIFF画像を生成する問題を修正しました。 NPR-22410：CQ-4198471 のホットフィックス
* （タッチ操作対応UI）列表示のアセットの初期設定のアップロード場所。 NPR-23475：CQ-4237057 のホットフィックス

### 統合 {#integration-5}

* ターゲットモードでは、作成者は継承をキャンセルすることなく、ブループリントから継承したコンポーネントを変更できます。 NPR-22751：CQ-4237907 のホットフィックス
* Path変数が適切にエンコードされていないため、非永続的なクロスサイトスクリプティング(XSS)が発生しません。 NPR-22851

### MSM {#msm-1}

* 複数のロールアウト設定を持つLiveCopyのロールアウト中に、ResourceNameConflictがルートの下に発生した場合、すべてのブランチを含めずにロールアウトフローが終了します。 NPR-22842：CQ-4236188 のホットフィックス

### プラットフォーム {#platform-3}

* 1回のリクエストで、逆引きのアプリケーションに対してポーリング制限を実装します。 NPR-23351：Granite-21135 のホットフィックス****
* メッセージパターンの変更は、カスタムロガーには反映されません。 NPR-23486：CQ-4241974 のホットフィックス

### サイト{#sites-4}

* リッチテキストエディターのテキスト内に、スペースや他の特殊文字を含むドキュメントへのリンクを作成しても、機能しません。 NPR-22289：CQ-4224321 のホットフィックス
* 大きな値(100000000000)でセグメントを保存すると、ブーストが0に設定され、エラーメッセージが表示されます。 NPR-22524：CQ-4237006 のホットフィックス
* マルチフィールドコンポーネントの追加項目をクリックできません。 NPR-22552：CQ-4237404 のホットフィックス
* 水平スクロールバーは、セグメントに長いタイトルが付いている場合は表示されません。 NPR-22615：CQ-4237001 のホットフィックス
* 空のオーディエンスを読み込むと、誤ったJavaScriptコードが生成されます。 NPR-22974：CQ-4238734 のホットフィックス
* アクティベーションをスケジュール設定または非アクティブ化する場合、ワークフロータイトルは必須なので、カスタムワークフロータイトルはタイムラインで翻訳されません。 NPR-23121：CQ-4237552 のホットフィックス
* サイトのターゲットセグメントに関する問題に対する修正のリクエストです。 NPR-23128
* (Firefox)選択した個人のチェックボックスが正しくありません。 NPR-23345
* 異なるモードのラベルは、アイコンと共に表示されます。 NPR-23275
* AEM 6.0からAEM 6.2にコンポーネントを移行中に、&#39;無効な再帰セレクター値&#39;エラーが発生しました。NPR-23503:CQ-4241258の修正プログラム

### コミュニティ{#communities-1}

* グループへのメッセージ失敗により、Web およびメール通知がトリガーされない。NPR-23447：CQ-4242880 のホットフィックス

### 翻訳 {#translation-1}

* 翻訳設定で「翻訳しない」アセットが設定されている場合、アセット言語コピーが作成されます。 NPR-22540：CQ-4237962 のホットフィックス

### ユーザーインターフェイス {#user-interface-1}

* Omnisearchでハイフンクエリを使用すると、サーバーエラーが返されます。 NPR-22999：Granite-19674 のホットフィックス
* DatePicker が、非表示フィールドによって設定された外部タイプヒントの手動設定をサポートしない。タイプヒントを変更すると、変換エラーが発生する。NPR-23333：Granite-21194 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-2}

* CAPTCHAコンポーネントは、セキュリティを強化するために廃止されました。CAPTCHAコンポーネントを使用している場合は、「Captchaコンポーネントは非推奨です。使用しないでください。」というメッセージが表示されます。 は、6.2 SP2-CFP15以降のリリースをインストールした後に表示されます。 AEMコンポーネントは、セキュリティを高めるために、reCAPTCHAを含めるようにカスタマイズできます。CQ-4220052用修正プログラム
* WCM Foundationコンポーネント&#39;Table&#39;は、格納されたクロスサイトスクリプティングに対して脆弱です。 NPR-23206：CQ-4240760 のホットフィックス

### 脆弱性 {#vulnerability-2}

* 管理 UI プロジェクトリンクのクロスサイトスクリプティング（XSS）。NPR-23272：CQ-4241795 のホットフィックス

## フォーム {#forms-5}

### Forms アドオンパッケージ {#forms-add-on-package-5}

#### Correspondence Management {#correspondence-management}

* レターをデフォルトのプレビューでプレビューする場合、レイアウトフラグメントマッピングは表示されませんが、プレビューボタンをクリックしたときに同じマッピングが正しく表示されます。 NPR-23335：CQ-4237745 のホットフィックス
* XDPで定義されている連結に対応するレター内のデータが、ダイレクトレターURLを使用して入力されない。 NPR-24145：CQ-4244290 のホットフィックス

#### モバイルForms{#mobile-forms}

* (Correspondence Management)ターゲットXMLでレターを読み込む際のデータのずれ。 NPR-22993：CQ-4237663 のホットフィックス

#### Reader Extensions サービス {#reader-extensions-service}

* Reader ExtensionをAdobe PDFに適用できません。 NPR-23067

#### Forms Manager {#forms-manager}

* サイトに埋め込まれたFormsは、サイトページの再公開時に公開されません。 NPR-23014：CQ-4236566 のホットフィックス

#### 脆弱性 {#vulnerability-3}

* クロスサイトスクリプティングに関するプロアクティブなホットフィックス。 NPR-20624：CQ-4206055 のホットフィックス
* Forms Manager の「メモ」タブに、保存されたクロスサイトスクリプティング（XSS）の脆弱性がある。NPR-27157：CQ-4255556 のホットフィックス

#### Encryption サービス {#encryption-service}

* (OSGI)[JEE]「PDFの検証プロセス」を使用して検証中に、添付ファイル付きのPDFの署名ステータスが正しくありません。 NPR-23269、NPR-23737

### Forms JEE インストーラー {#forms-jee-installer-5}

#### コア {#core-1}

* Core-extの静的コード分析で報告された問題を修正する必要があります。 NPR-13947

#### PDFG サービス {#pdfg-service}

* HTMLからPDFへの変換が機能しません。 NPR-21545

### {#osgi-bundles-and-content-packages-included-4}に含まれるOSGIバンドルとコンテンツパッケージ

次のテキストドキュメントには、CFPに含まれるOSGIバンドルとコンテンツパッケージのリストが示されています。

AEM 6.2 SP1-CFP15に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2SP1-CFP15に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### 累積修正パック 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14は重要なアップデートで、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* アセットのメタデータプロパティの編集性が向上しました。
* 既に期限切れの状態にあるアセットのパスワード有効期限通知ジョブを再設定しました。
* Touch UIコンソールをカスタマイズして、追加のロケールを拡張。
* 効率的なLivecopyindex同期のために、cq-msm-coreが更新されました。
* 様々なロールアウトへのレプリケーション機能を合理化。

### アセット{#assets-5}

* 免責事項を含み、長いファイル名が付いたアセットをダウンロードできない。NPR-22163：CQ-4235274 のホットフィックス
* 一重引用符文字を使用すると、一括表示でのメタデータの更新が防げ、クイックツールバーアクションを使用してアセットのプロパティを開くと、UIが完全に壊れます。 NPR-22317、NPR-22353：CQ-4236990、CQ-4236469 のホットフィックス
* アセット有効期限通知ジョブでは、期限切れのアセットは非アクティブ化されません。 NPR-22346：CQ-4237188 のホットフィックス
* Safari でアセットの Digital Rights Management を使用すると、アセットのダウンロードが失敗する。NPR-22378：CQ-4236460 のホットフィックス
* 小さい画像のWebレンディションのピクセルサイズが正しくありません。 NPR-22435：CQ-4236742 のホットフィックス

### サイト{#sites-5}

* （タッチUI）移動されたタグが、ページのプロパティの古い場所と新しい場所に表示されます。 NPR-21921、CQ-4238598用の修正プログラム
* （タッチ操作対応UI）リッチテキストエディターは、&lt;a>タグからid以外の属性をすべて削除します。 NPR-22045：CQ-4234133 のホットフィックス
* Ctrl + Vキーを押しながらリッチテキストエディターにコンテンツを直接貼り付けると、改行がスキップされます。 NPR-22117：CUI-5881 のホットフィックス
* （タッチ操作対応UI）名前空間の下に40個を超えるタグを表示できません。 NPR-22290：CQ-99114 のホットフィックス
* RSSフィードの問題、ポート —1 ～ AEM 6.2 NPR-22158:CQ-4233339の修正プログラム
* (IE)リッチテキストフィールド内の任意の文字を初めてオーサリングする場合、文字の末尾に空白が追加されます。 NPR-22443：CQ-4235343 のホットフィックス
* パッケージ名と一致しようとすると、Java Useオブジェクトは、パッケージ宣言の末尾に空白文字があるので、SightlyJavaCompilerServiceをフリーズします。 NPR-22557：Granite-20836 のホットフィックス
* タッチUIコンソールで、タグ付けに使用する新しい言語が取得されません。 NPR-22250：CQ-4239194 のホットフィックス

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite)FolioをDPSにアップロードする前に、Folioに対して発行日と表紙日の両方のフィールドを設定する必要がありました。 NPR-22484

### Commerce {#commerce}

* コマースでの複数のクロスサイトスクリプティング(XSS)脆弱性カタログの作成ウィザード。 NPR-22344：CQ-4237017 のホットフィックス

### MSM {#msm-2}

* LiveCopyIndexの同期により、長時間のインデックス更新中にスレッドが輻輳する。 NPR-22214：CQ-90667 のホットフィックス
* cq:cugEnabledプロパティは、livecopy内の別のフィールドが編集された場合に無効になり、ページが保護されなくなります。 NPR-22246：CQ-4236050 のホットフィックス
* ページのロールアウトアクションは、ページが中断されたときに子の更新に失敗します。 NPR-22483：CQ-4236956 のホットフィックス
* マスターで移動された構造をロールアウトすると、間違った cq:moveTarget が発生する。NPR-22373：CQ-4232536 のホットフィックス

### 統合 {#integration-6}

* オファーセレクターライブラリでオファーを並べ替えようとすると、異常な動作が発生します。 NPR-22208：CQ-4235439 のホットフィックス
* 長時間実行されるクエリで TargetContentImpl を使用すると、AEM の速度が低下する。NPR-22361：CQ-4236907 のホットフィックス
* ターゲットエンジン（mbox.js、at.js）が、マングリングされた URL を使用せず、特定のデプロイメントで失敗する可能性があるコロンを含む URL を使用する。NPR-22366：CQ-4237854 のホットフィックス
* ページのパーソナライゼーションには、ブランドノード上での投稿権限が必要です。 NPR-22370：CQ-4236895 のホットフィックス

### Foundation {#foundation}

* Apache SlingスクリプティングSightlyモデルは、プロバイダーバンドル&#x200B;**org.apache.sling.scripting.sightly.models.provider/1.0.18**&#x200B;を使用します。 NPR-22614:Sling-5944、Sling-6866用修正プログラム

### プロジェクト {#projects}

* ワークフロースターターは、文字列のTypeHint値を受け入れられません。 NPR-22436：CQ-4237855 のホットフィックス

### 翻訳 {#translation-2}

* プレビュー機能の問題を調査。NPR-22201：CQ-4223753 のホットフィックス

### ユーザーインターフェイス {#user-interface-2}

* （クラシックUI）関連付けられたフォームデータモデルサービスが空のフィールドに設定されている場合でも、コンポーネントはデフォルト値を表示します。 NPR-21903：GRANITE-19744 のホットフィックス

### WCM ‐ 基盤コンポーネント  {#wcm-foundation-components-3}

* Adobe Campaignのインポーターページを指すLive Copyページを公開する際にエラーが発生する。 NPR-22470：CQ-4237164 のホットフィックス
* エクスペリエンスフラグメントエディターを開くときにJavaScriptエラーが発生する。 NPR-22598：CQ-4238415 のホットフィックス

### ワークフロー {#workflow}

* Day CQワークフロー電子メール通知サービスは、WorkflowCompleted通知とWorkflowAborted通知用に、Mongoノードごとに1つの電子メールをトリガーします。 NPR-22486：CQ-4238172 のホットフィックス

## フォーム {#forms-6}

### Forms アドオンパッケージ {#forms-add-on-package-6}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

#### アダプティブフォーム {#adaptive-forms-4}

* IE11およびChromeでアダプティブフォームのドロップダウンプレースホルダー値に一貫性がない。 NPR-22405：CQ-4227096 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-6}

#### LCM のインストール {#install-lcm}

* インストーラーと LCM で Jsafe Jars を Cryptoj 6.1.3.1 に更新。NPR-22744

### 含まれている機能パック {#feature-packs-included}

#### プロセス管理 {#process-management}

* (HTML Workspace)ユーザーがタスクを要求すると、その特定のユーザーのキューの数は更新されますが、ページが更新されない限り、他のユーザーのキューの数は更新されません。 NPR-19778：CQ-4233665 のホットフィックス

### OSGIバンドルおよびコンテンツパッケージはCFP14に含まれています{#osgi-bundles-and-content-packages-included-in-cfp}

AEM 6.2 SP1-CFP14に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2SP1-CFP14に含まれるコンテンツパッケージのリスト

[Get ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* AT.jsをクライアントライブラリとして使用している間、ターゲットコンポーネント設定内で静的パラメーターフィールドの設定を有効にしました。
* ドロップダウンコンポーネントの表示／非表示機能を修正しました。
* ターゲット同期オーディエンスの使用に関する修正。
* Correspondence Managementの汎用性が向上し、特殊文字に対応できるようになりました。

### アセット{#assets-6}

* バージョンの削除で、古いバージョンのアセットを削除できません。 NPR-21682：CQ-4212996 のホットフィックス
* 順序を変更可能なフォルダーの下でのフォルダーの順序変更は維持されません。 NPR-21964：CQ-4231761 のホットフィックス

### サイト{#sites-6}

* (TouchUI)(ClassicUI)HTLおよびコアコンポーネントに複数のクロスサイトスクリプティング(XSS)脆弱性が存在する問題を修正しました。 NPR-21532：CQ-4232305 および CQ-4232511 のホットフィックス
* 選択したテキストのコンテンツの作成/書式設定(新しいリストスタイルの割り当て/削除など)は、Internet Explorer 11では正常に機能しません。 NPR-21533：CQ-4230689 のホットフィックス
* (Safari)アセットファインダーパネル内のすべてのアセットに表示を設定することはできません。 NPR-21981：CQ-4213720 のホットフィックス
* Time Warpは、ページが文字化けして「RecursionTooDeepException」エラーを返し、日付が変更された場合でも新しいバージョンは作成されません。 NPR-21707：CQ-4199536 のホットフィックス
* エディターでページを読み込むと、WorkflowStatusprovider(pageinfo.json)が3回読み込まれ、AEMインスタンスの動作が遅くなります。 NPR-21778：CQ-59232 のホットフィックス

### 統合 {#integration-7}

* オーサリングターゲットモードでのモバイルタイプとブラウザーのオーディエンスの作成が、AEMで動作していません。 NPR-21676、NPR-21681：CQ-4232100 のホットフィックス
* ターゲットコンポーネントの更新中に待ち時間が長い場合は、コンポーネントが完全に更新される前に、別のオファーを追加することができます。 NPR-21744：CQ-4233158／CQ-4234293 のホットフィックス
* クラウド設定でAT.jsをクライアントライブラリとしてテストすると、mbox呼び出しでテスト静的パラメーターの値が表示されません。 NPR-21930：CQ-4234520 のホットフィックス

### プラットフォーム {#platform-4}

* ユーザーまたはグループの数が多い場合に、ユーザー同期でパフォーマンスが低下する。 NPR-20431：CQ-4223282 のホットフィックス
* Sling配布を使用してユーザー同期と同期していないユーザー。 NPR-21911：Granite-20404 のホットフィックス
* (Geometrixxページの)検索抜粋で、停止ワードがハイライトされるのを防ぎます。 NPR-21835：Granite-21067 のホットフィックス\
   注意：この修正にはOak CFP 1.4.20以降が必要です。

### 翻訳 {#translation-3}

* 翻訳プロジェクトの作成中に、イニシエーターユーザーidにjcrプロパティが見つかりません。 NPR-21715：CQ-4230713 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-4}

* フォームドロップダウンコンポーネントの表示／非表示機能が期待どおりに機能しない。NPR-22164：CQ-4235288 のホットフィックス

## フォーム {#forms-7}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ  {#forms-add-on-package-7}

#### アダプティブフォーム {#adaptive-forms-5}

* アダプティブFormsでのXML External Entity Injection(XE)の挿入 NPR-21982：CQ-109878 のホットフィックス
* (iOS11)添付ファイルコンポーネントをクリックすると、添付ファイルは、デバイスのファイルブラウザーではなくカメラを開きます。 NPR-21926：CQ-4214348 のホットフィックス
* テーマ作成UIにタイトルが見つからない場合、例外が発生し、ダイアログのレンダリングに失敗します。 CQ-4236143 のホットフィックス

#### Correspondence Management {#correspondence-management-1}

* 特殊文字を含むxmlデータのレンダリングの問題。 NPR-21712：CQ-4229137 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-7}

#### Assembler サービス {#assembler-service}

* 6.2.0-ASM-1017-003を使用して生成されたPDFファイルは壊れます。 NPR-21427：CQ-4228046 のホットフィックス

#### PDFG サービス {#pdfg-service-1}

* PNG、JPEG、TIFFファイルの予期しないページサイズ(PDF)が原因でOCRに失敗しました。 NPR-19489：CQ-4209079 のホットフィックス

## OSGIバンドルおよびコンテンツパッケージはCFP13に含まれています{#osgi-bundles-and-content-packages-included-in-cfp-1}

AEM 6.2 SP1-CFP13に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2SP1-CFP13に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1は重要なアップデートで、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正が含まれています。

このCumulative Fix Packの主な特徴は次のとおりです。

* 複数値フィールドのメタデータ処理を改善。
* 翻訳ワークフローでの複数文字（2つ以上）の国コードのサポート。
* 複数のネストされたコンポーネントを含むページのレンダリングを改善。
* AEMとAdobe Digital Publishing Suiteの間でアセットの発行日の同期を改善。

### アセット{#assets-7}

* オムニサーチの文字が多すぎると、AEM サーバーがクラッシュする。NPR-21083：CQ-4223602 のホットフィックス
* メタデータスキーマの複数値フィールドの2番目のオプションで指定された値は、CRX-deで以前に指定された値に追加されません。 NPR-21220：CQ-4224526 のホットフィックス
* Safari でアセットの Digital Rights Management を使用すると、アセットのダウンロードが失敗する。NPR-21387：CQ-4230287 のホットフィックス

### サイト{#sites-7}

* (DAM)(ClassicUI)AEM CQ Author/Publishクイックスタートの一部のSWFファイルに、複数のクロスサイトスクリプティング(XSS)脆弱性が存在する。 NPR-21073、NPR-21074:NPR-20612用の修正プログラム
* 複数の言語で使用可能なタグは、タグピッカーで翻訳されません。NPR-21221:CQ-78855の修正プログラム
* 複数のネストされたコンポーネントを使用するとAEM記事コンソールでのレンダリングの問題が発生すると動作が遅くなります。 NPR-21271：CQ-4224158 のホットフィックス

### 統合 {#integration-8}

* ターゲットフレームワークを追加する場合、ターゲットモードはエディターの「モードを選択」リストでは使用できません。 NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite)AEMのFolioの公開日が、Folio Producerに表示される日付と一致しません。 NPR-21145

### MSM {#msm-3}

* LC内の最初のローカルページを削除すると、Live Copyのリセットプロセスが停止する。 NPR-21276：CQ-4229743 のホットフィックス

### プラットフォーム {#platform-5}

* スクリプトとして実装されたタグを参照するカスタムtaglibは、AEM 6.3にアップグレードした後に見つかりません。NPR-20149:Granite-18433用修正プログラム

### 翻訳 {#translation-4}

* 2文字を超えるlang_countryコードがある場合、変換ワークフローは失敗します。 NPR-21088：CQ-4197439 のホットフィックス
* プロジェクトが完了するまで、アセットページを再び翻訳プロジェクトに送信することはできません。 NPR-21219：CQ-4209908 のホットフィックス

### ユーザーインターフェイス {#user-interface-3}

* 「Select component」は、フォームの送信中にターゲットプロパティを削除しません。 NPR-21163：GRANITE-14125 のホットフィックス
* HTTP.encodePathOfURI展開重複エンコードはプラス記号「+」です。 NPR-21417：GRANITE-16340 のホットフィックス

### 脆弱性 {#vulnerability-4}

* DAMメタデータエディターのクロスサイトスクリプティング(XSS)。 NPR-21434：CQ-83472 のホットフィックス
* 複数のSWFファイルは、クロスサイトスクリプティング(XSS)に対して脆弱です。 NPR-20612：CQ-4213297 のホットフィックス

## フォーム {#forms-8}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ  {#forms-add-on-package-8}

#### Correspondence Management {#correspondence-management-2}

* (IE11)完全なUIが読み込まれた後、右側が断続的に読み込まれている間に、HTMLコンテンツの初期レンダリングが左側でのみ発生します。 NPR-21554
* AEM 6.2 SP1-CFP9のインストール後、レタープレビューの送信ボタンが無効になる。 NPR-21547
* アセットのリンケージタイプを選択すると、「アセットセレクター」ウィンドウがレターデータ連結の編集ウィザードで開きません。 NPR-21164：CQ-4194567 のホットフィックス
* インラインまたは編集可能なテキストモジュールを編集するには、関連する編集アイコンをタップするか、レタープレビュー内の関連するテキストモジュールを重複クリックします。 NPR-21402

#### アダプティブフォーム {#adaptive-forms-6}

* AEM Formsの送信ボタンコンポーネントには、type=&quot;submit&quot;ではなくtype=&quot;button&quot;と表示されます。 NPR-21007
* 繰り返し可能なパネルの新しいパネルを追加または削除しても、データは保持されます。 NPR-21408

### Forms JEE インストーラー {#forms-jee-installer-8}

#### コア {#core-2}

* 最新のJava 8 Update 131にアップグレードすると、次の例外がスローされます。&quot;JsafeJCEプロバイダーが無効です。FIPS 140で必要な自己整合性の確認に失敗しました。&quot; NPR-21355

   **注意：** このNPRでは、追加の設定が必要です。詳しくは、 [最新のJava 8アップデートを参照してください](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)。

* Core、Encryption、Signature、およびドキュメントセキュリティのjsafe jarをcryptoj 6.1.3.1に更新します。 NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### LCM のインストール {#install-lcm-1}

* インストーラーとLCMで、Jsafe JarsをCryptoj 6.1.3.1に更新します。 NPR-21362

#### PDFG サービス {#pdfg-service-2}

* PDFGのJsafe JarsをCryptoj 6.1.3.1に更新します。 NPR-21359

#### プロセス管理 {#process-management-1}

* (HTML Workspace)名前カテゴリーが切り捨てられて表示されないように列のサイズ変更を有効にする。 NPR-19770：CQ-4233668 のホットフィックス

#### Reader Extensions サービス {#reader-extensions-service-1}

* REでjsafe jarsをcryptoj 6.1.3.1に更新します。 NPR-21357

## OSGIバンドルおよびCFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}に含まれるコンテンツパッケージ

AEM 6.2 SP1-CFP12.1に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11は、AEM 6.2 SP1の一般リリース(GA)以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* 効率的なLivecopyindex同期のために、cq-msm-coreが更新されました。
* コンテンツフラグメントの編集効率が向上しました。
* ACL権限を検出するための検証オプションをパッケージマネージャーに提供します。
* 顧客対応の電子メールIDを含むキャンペーン機能が導入されました。
* Dynamic Mediaファイルのビデオエンコーディング機能を改善。
* SightlyコンポーネントとLiveCopiesの修正点です。

### アセット{#assets-8}

* 名前にスペースが含まれるファイルのDynamic Mediaビデオエンコーディングは失敗します。 NPR-20818：CQ-102469 のホットフィックス
* AEM CQ Author/Publishクイックスタートの一部のSWFファイルに、複数のクロスサイトスクリプティング(XSS)脆弱性が含まれている。 NPR-21071、NPR-21072
* 免責事項を含み、長いファイル名が付いたアセットをダウンロードできない。NPR-20255：CQ-4222139 のホットフィックス

### サイト{#sites-8}

* AEMとキャンペーンの統合：Adobe Campaignで特別なリンクが書き換えられるので、顧客は次のメールを送信できません。電子メールのハイパーリンク。 NPR-20787：CQ-4225760 のホットフィックス
* （タッチUI）言語がフランス語に設定されている場合、AEMのユーザビリティに関する問題とパフォーマンスの問題が発生します。 NPR-20854：CQ-4227628 のホットフィックス
* RTEでリンクプラグインを使用してエンコードされたアセットファイルをリンクすると、空のリンクが返されます。 NPR-20626、NPR-21059：CQ-4223011 のホットフィックス
* コンテンツフラグメントメタデータエディターを使用すると、コンテンツ作成者は変更をコンテンツフラグメントに保存できません。 NPR-20641：CQ-4224755 のホットフィックス
* ページプロパティのエイリアスは、「発行の要求/非公開の要求」に結び付きます。 NPR-20731：CQ-4226227 のホットフィックス
* RTE要素でのリンクのエンコードに関するテキストコンポーネントの問題。 NPR-20755：CQ-4224321 のホットフィックス

### プラットフォーム {#platform-6}

* ResourceResolverImpl.map()はResourceDecoratorを呼び出しません。 NPR-20788：GRANITE-19718 のホットフィックス
* org.apache.sling.i18n.DefaultLocaleResolverはorg.apache.sling.engine.SlingRequestProcessorを介して要求を処理できません。 NPR-20706：CQ-94880 のホットフィックス
* 特定のパッケージに対するACL権限や権限が変更されたかどうかを検出するために、Package Managerに検証オプションを追加するように要求します。 CQ-4229196 のホットフィックス

### 統合 {#integration-9}

* (Search&amp;Promote)コンテンツパッケージのフィルター定義があいまいな場合、インストール時に上書きされたパスが発生します。 NPR-20808：CQ-4227615 のホットフィックス

### ワークフロー {#workflow-1}

* AEM 実稼働サーバーのデプロイメントに関する安定性の問題。NPR-20979：Granite-19104 のホットフィックス

### プロジェクト {#projects-1}

* （タッチ操作対応UI）チームメンバーをプロジェクトに追加できません。 NPR-20990：CQ-4205375 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-5}

* Sightly画像コンポーネントの「リンク先」で、.html拡張子が見つからないため、403エラーが発生します。 NPR-20823：CQ-4195909 のホットフィックス
* LiveCopyを使用する設計図サイトで、フォームコンポーネントを削除しようとすると、NullPointerExceptionがスローされ、フォームコンポーネントを削除する代わりに追加し直します。 NPR-20855：CQ-4204628 のホットフィックス
* LiveCopyIndexの同期により、長時間のインデックス更新中にスレッドが輻輳する。 NPR-20634：CQ-90667 のホットフィックス

### セキュリティ {#security}

* XSSライブラリのプロアクティブな更新。 NPR-21174
* 電子メール送信用の簡易APIを表示するApache Commons Email 1.5にアップグレードします。 NPR-20509：Granite-18240 のホットフィックス
* XSSのバイパスの可能性を排除するために、Apache Sling XSS Protection APIに適用されたセキュリティパッチ。 NPR-21290：GRANITE-19924 のホットフィックス
* XSSAPI#getValidHref関数のXSSバイパス。 NPR-21174：Granite-19924 のホットフィックス

### モバイルアプリ {#mobile-apps}

* AEM の OOTB アセットに対する curl Head リクエストの問題を修正。NPR-20511：CQ-4221520 および CQ-103024 のホットフィックス

## フォーム {#forms-9}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

AEM Forms の主なハイライトは次のとおりです。

* Workbench ユーザーの証明書認証を有効化。
* Correspondence Management、HTML5フォーム、およびAEM FormsWorkspaceのユーザビリティが修正されました。

### Forms アドオンパッケージ {#forms-add-on-package-9}

#### HTML5 のフォーム {#html-forms-1}

* iOS 10および11デバイスでの手書きメモコンポーネントの使い勝手の問題。 NPR-21092

#### Correspondence Management {#correspondence-management-3}

* (Correspondence UI)1回のクリック後に送信ボタンを無効にします。 NPR-21078

### Forms JEE インストーラー {#forms-jee-installer-9}

#### Assembler サービス {#assembler-service-1}

* docConvertorは、「要素&quot;stEvt:action&quot;のプレフィックス&quot;stEvt&quot;がバインドされていません」というエラーが表示されてPDF/Aの生成に失敗する。 NPR-21032：CQ-4222540 のホットフィックス
* サービスOMPFSubmission/PDFA/PDFA/PDFtoPDFを呼び出す際に、java.lang.IllegalArgumentExceptionメッセージ：No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTUREというという名が付けられて例外が発生します。 これにより、サーバーが再起動されるまで、短時間のみ有効な署名の検証プロセスが完了しなくなります。 NPR-20792

#### Workbench {#workbench}

* Workbenchユーザーの証明書認証を有効にします。 NPR-17548：CQ-4214486 のホットフィックス

#### プロセス管理 {#process-management-2}

* データ準備プロセスは、モバイルフォームがdatarefパラメーターと共にレンダリングされると、複数回呼び出します。 NPR-19801：CQ-4230427：CQ-4230400 のホットフィックス

## OSGIバンドルおよびコンテンツパッケージはCFP11に含まれています{#osgi-bundles-and-content-packages-included-in-cfp-3}

AEM 6.2 SP1-CFP11に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10は、AEM 6.2 SP1の一般リリース(GA)以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* テスト用に新しいユーティリティ関数onDialogLoadedが追加されました。
* フロントエンドユニットテストと設定をClientLibraryProxyServletに追加。
* 複数のイメージインプレイスエディタコンポーネントのパフォーマンスが修正されました。
* Apache Sling JCR ResourceBundleProviderの設定の更新。

### アセット{#assets-9}

* アセットの更新ワークフローが無効になっていると、アセットプレビューが機能しません。 NPR-20543：CQ-4204986 のホットフィックス
* 花崗岩にクラスが追加されたレンダリングの問題：クラスプロパティ(cq-damadmin-admin-assets-upload) NPR-20514：CQ-4219238 のホットフィックス
* titleに特殊文字を含むサムネールアセットが、NPR-20347のalt属性にjavaオブジェクトとして表示される：CQ-4223620の修正プログラム
* ライセンスの問題により、バージョン比較コードをアドビ独自のコードに置換。NPR-20273：CQ-4223758 のホットフィックス
* 複数のアルファレイヤーを含むCMYK PSBファイルをアップロードすると処理の問題が発生する。 NPR-20251：CQ-4220869 のホットフィックス
* 国際標準化辞書は、org.apache.sling.i18n 2.5.6でサーバーを再起動しない限り、機能しません。NPR-20525:花崗岩用修正プログラム — 19490
* スケジューラー期間に従って、デフォルトのスレッドダンプコレクタの設定(デフォルトのAEM開始アップ)を使用してスレッドダンプが生成されません。 NPR-20288:GRANITE-19488/GRANITE-12741/CQ-90647用の修正プログラム。

### サイト{#sites-9}

* 保存済みの検索結果を開いた後に変更日付フィルタを変更した場合、結果に影響はなく、表示される結果は、変更日付フィルタの前に保存した値と同じになります。 NPR-19739：CQ-4219425 のホットフィックス
* ネストされたコンポーネントを含むページの読み込みに失敗しました。 NPR-20312
* ワークフローパッケージの削除時に、削除の要求ワークフローがトリガーされます。 NPR-20266：CQ-4221686 のホットフィックス
* （タッチ操作対応UI）OSクリップボードと内部AEMクリップボードでコピー/貼り付けを行った場合の問題。 NPR-20228：CQ-4220383 のホットフィックス
* 複数のアセット（100を超える）が読み込まれると、AEMインスタンスはリスト表示で遅くなります。 NPR-20034：CQ-4222695 のホットフィックス
* （タッチ UI）クラシック UI コンソールを介してローンチを削除すると、すべてのページが編集できなくなる。NPR-20520：CQ-4225074 のホットフィックス
* ターゲットドロップダウンは、ダイアログ内の複数のRTEコンポーネントでは機能しません。 NPR-20345：CQ-4220981 のホットフィックス

### プラットフォーム {#platform-7}

* 匿名セッションを使用してアクセスした場合、ClientLibraryProxyServletは、パブリッシュインスタンス上のクライアントライブラリにリクエストをプロキシせず、HTTP 404が見つかりませんエラーをスローします。 NPR-20195：Granite-14409 のホットフィックス

### 統合 {#integration-10}

* ターゲットエンジンをAdobe Targetとして選択すると、コンポーネントが読み込まれず、サーバーログでエラーがスローされます。 NPR-20058：CQ-88071、CQ-109698、CQ-4201600 のホットフィックス

### コマース{#commerce-1}

* 同じページの製品を作成する場合、確認またはリダイレクトポップアップメッセージは表示されません。 NPR-20257：CQ-4223414 のホットフィックス

### ユーザーインターフェイス {#user-interface-4}

* 日付選択が複数のフィールドに含まれるフィールドの場合、日付フィールドに保存された値は、コンポーネントの編集中に保持されません。 NPR-20077：GRANITE-19147 のホットフィックス
* 連続したクエリがトリガーされて誤った結果が生じても、以前のクエリが中止されない。NPR-20397：GRANITE-19306 のホットフィックス

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-6}

* ImageMapプロパティは、複数のイメージインプレイスエディタコンポーネントからイメージを削除した後も存在します。 NPR-20142：CQ-4222982 のホットフィックス

## フォーム {#forms-10}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ  {#forms-add-on-package-10}

#### アダプティブフォーム {#adaptive-forms-7}

* valueCommitスクリプトは、UIを通じて変更された場合にDropDownListに対して2回実行されます。 NPR-19989：CQ-110212 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-10}

**プロセス管理**

* CFPパッケージには、AEM FormsHTML Workspaceバージョン2.2.26が含まれています。NPR-20099
* モバイルフォームがPDFとして表示するように設定されている場合、事前入力されたフォームは機能しません。 NPR-20566

**Rights Management**

* CAC /相互認証証明書選択ダイアログに、拡張キー使用(EKU)を持つ証明書がクライアント認証またはスマートカードのログオンとして表示される必要があります。 NPR-20708
* Forms JEE が PKCS#11 相互認証をサポート。NPR-15001

## OSGIバンドルおよびコンテンツパッケージはCFP10に含まれています{#osgi-bundles-and-content-packages-included-in-cfp-4}

AEM CFP 6.2 SP1-CFP10に含まれるOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/bundle-list-cfp10.txt)

AEM CFP 6.2 SP1-CFP10に含まれるコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1～CFP9は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* シークレット入力用にAnalytics Classic UIの設定を変更。
* Contexthub用の独立永続性キャッシュの修正。
* アセットディメンションの正確な計算。
* Brand Portalにアセットを公開する際のAEMのパフォーマンスが最適化されました。
* キャンバスノードのResourcetype値を修正しました。
* ドキュメントフラグメントコンテンツで、大文字と小文字が区別され、特殊文字を検索できるようになりました。
* アダプティブFormsが強化され、Safariで添付ファイルとしてPDFを添付できるようになりました。\
   新しいDynamic Mediaパブリッシングインフラストラクチャに接続する新しいDynamic Mediaを提供し、高速で拡張性の高いレプリケーションを実現します。

### アセット{#assets-10}

* AEM Assetsは、InDesignアセットへの重複リンクを含むサブアセット参照を抽出できません。 NPR-19006：CQ-4204186 のホットフィックス
* コマースのコレクション内のアセットで並べ替えオプションが機能しない。 NPR-19508：CQ-4213622 のホットフィックス
* 既存のアセットと同じ名前を持つアセットが同じ場所に移動された場合、cqの値は次のようになります。アセットのlastReplicationActionがアセット間で入れ替わるので、誤ったメタデータが作成されます。 NPR-19531
* すべてのアセットが正しく発行されているにもかかわらず、大量のアセットを発行すると、エラーメッセージが表示されます。 NPR-19629：CQ-4219611 のホットフィックス
* 静的レンディションは固定サイズで表示され、実際のレンディションのサイズは反映されません。 NPR-20004
* 4 つを超える複数のアセットが Brand Portal に公開されているとき、AEM インスタンスの動作が遅くなる。NPR-20009

### サイト{#sites-10}

* AEMは、ユーザーが別のユーザーによってロックされたページの公開/非公開/バージョンの作成を試みると、予期しない動作を表示します。 NPR-19249;CQ-4215298およびCQ-4203856の修正プログラム
* ネストされた開始を手動でプロモートする間、子ページが削除されます。 NPR-19704
* ContextHub が初期化中にデフォルトの永続化レイヤーを上書き保存するときの永続化の問題。NPR-19979：CQ-4218399 のホットフィックス
* コンテンツフラグメントは他のボタンと重なっています。 NPR-19980：CQ-4221519 のホットフィックス
* SiteAdminでエイリアスを使用して表示した場合に、サイトページが表示されない。 NPR-20053：CQ-4221478 のホットフィックス
* Adobe Campaignのインポーターページを指すLive Copyページを公開する際にエラーが発生する。 NPR-20066：CQ-4220846 のホットフィックス

### プラットフォーム {#platform-8}

* Apache POIをバージョン3.16にアップグレードし、PPTスライドの背景画像をレンディションに含めることをサポートしました。 NPR-18286
* 同じフォルダー内の複数のアセットをアップロードする際に、Internet Browser 11およびEdgeでレンダリングの問題が発生する。 NPR-20062

### 統合 {#integration-11}

* 匿名ユーザーでアクセスすると、カスタム at.js ファイルが公開されない。NPR-19542：CQ-4219592 のホットフィックス
* Analyticsの既存の資格情報をWSSE認証に移行します。 NPR-19962

### Brand Portal {#brand-portal}

* tagadmin/tagging コンソールで AEM から Brand Portal にタグを公開できるようになりました。NPR-20271

## フォーム {#forms-11}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ  {#forms-add-on-package-11}

#### Correspondence Management {#correspondence-management-4}

* レターのプレビュー時に、ドキュメントフラグメント内の実際のテキストを検索する機能を有効にしました。 NPR-19712

#### アダプティブフォーム {#adaptive-forms-8}

* アダプティブFormsが強化され、Safariで添付ファイルとしてPDFを添付できるようになりました。 既存のフォームで同じ機能をサポートするには、添付ウィジェットの設定を変更し、「サポートされるファイルの種類」で値.pdfではなくapplication/pdfを更新する必要があります。 NPR-19623

#### Formsマネージャ{#forms-manager-1}

* アダプティブフォームのフィールドでvalidationStateが未定義でelementFocusChangedイベントが発生した場合、エラーイベント(errorState)がAdobe Analyticsサーバーに返されます。 NPR-19513

### Forms JEE インストーラー {#forms-jee-installer-11}

#### コア {#core-3}

* シャットダウン中は接続マネージャーを使用できません。 作成者EARがデプロイ解除される前に、JbossはJDBC依存関係を切り離し、破損の問題を引き起こします。 NPR-19703

## 含まれている機能パック {#feature-packs-included-1}

* Dynamic Mediaでのサムネールの補正と透明度の改善 NPR-15207

## OSGIバンドルおよびコンテンツパッケージはCFP9に含まれています{#osgi-bundles-and-content-packages-included-in-cfp-5}

AEM 6.2SP1 ～ CFP9で更新されたコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

AEM 6.2SP1 ～ CFP9で更新されたOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* Adobe電子メールテンプレートサービスのカスタムユーザーテンプレートにタグを導入します。
* デスクトップアプリケーションのTouchUIボタンの機能強化。
* クリック時に送信ボタンを無効にし、翻訳ページで複数のフォームが送信されないようにしました。
* ダイアログ内で複数のRTEコンポーネントを設定。
* 強化されたリファレンスのライブコピーの更新
* ドキュメントフラグメントコンテンツで、大文字と小文字が区別される検索機能を有効にしました。
* LinuxライブラリのリストをAEM Formsのインストールドキュメントに追加しました。

### アセット{#assets-11}

* SafariブラウザーのスマートコレクションにOmnisearchフィルターを適用する際に発生する問題を修正しました。 NPR-19511
* PDF アセットに複数のキーワードが関連付けられている場合、PDF キーワードメタデータが適切に抽出されず、誤って変更される。この問題を解決するために、PDF アセットのサブジェクトフィールドメタデータプロパティを削除。ただし、メタデータスキーマを編集して、サブジェクトフィールドに複数値のテキストフィールドを追加することは可能。NPR-19126
* ワークフロー通知サービスは、電子メール内のリンクをエンコードせず、ユーザーがリンクをクリックした後に読み込めません。 NPR-19490：CQ-4218055 のホットフィックス
* Chrome を使用して、列表示でページ／アセットの完全なリストをロードできない。NPR-19458：CQ-4214248 のホットフィックス
* 「アクティベーションの要求」ワークフローをアクティブ化すると、AEMインボックスに正しくないオフタイムアイコンが表示される。 NPR-19365：CQ-4216174
* リスト表示での並べ替えに関する問題があります。 NPR-19217：CQ-95602
* アセットフォルダーの設定でタイトルまたはサムネール画像を変更すると、フォルダーの元のグループと権限が上書きされる。NPR-19283：CQ-4216080 のホットフィックス
* Windows 10ワークステーションは、タッチモードに自動的に切り替わり、一部のボタンが機能しなくなります。 NPR-19183

### サイト{#sites-11}

* ダイアログ内に複数のRTEコンポーネントがある場合の問題 NPR-19311：NPR-19587
* VersionManagerImplの初期化後、vanilla AEM 6.2での自動バージョン削除が1回だけ機能します。 NPR-19315：CQ-4217175 のホットフィックス
* ワークフローインスタンスが「Salesforce.comエクスポート」ワークフローステップで停止する。 NPR-19222：CQ-4212976 のホットフィックス
* ライブコピーから作成された言語コピーページは編集できません。 NPR-18967
* 階層の変更に伴い、ReferencesUpdateActionは、ネストされたLiveCopyへのリンクの更新に失敗します。 NPR-18715：CQ-4214105 のホットフィックス

### プラットフォーム {#platform-9}

* Adobe 電子メールテンプレートサービスが、カスタムユーザーテンプレートにタグを追加する。NPR-19190：CQ-4217113 のホットフィックス

### プロジェクト {#projects-2}

* プロジェクトエディターが、プロジェクトアセットフォルダーにアセットをコピー／貼り付けできない。NPR-19619
* 6.2 SP1-CFP1をインストールした後、翻訳プロジェクトのプレビューを生成できません。 NPR-16481：CQ-4204655

### 統合 {#integration-12}

* Classic UI の Adobe Digital Publishing Solution で誤って設定されている記事のプロパティにアクセスする。NPR-19366
* AEM記事コンソールでの記事のサイズが最大になるため、サムネールのレンダリングが遅くなる。 NPR-19086：CQ-4217148
* ユーザーが複数の領域にアクセスできる場合、キャンペーンを介してオファーをパーソナライズするときの、自動フォールドの不正な動作。NPR-19290：CQ-4218029 のホットフィックス
* ターゲットモジュールを編集して複数回保存すると、ターゲットモードでターゲティングダイアログが表示されない。NPR-19144：CQ-4216708 のホットフィックス

### ワークフロー {#workflow-2}

* インボックスクラシックUIのユーザー/グループで、インボックス内の通知をフィルターできない。 NPR-19122：CQ-4215374 のホットフィックス
* 画像マップは、HTL画像コンポーネントで選択された座標を保持しません。 NPR-18911：CQ-4211584

## フォーム {#forms-12}

* AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-12}

* Microsoft WordまたはWebブラウザーからCorrespondence Managerのテキストエディターにコンテンツをコピーすると、スタイルが失われます。 NPR-19530
* 改行を含まないコンテンツは、テキストエディタで折り返されません。 NPR-19481
* レターのプレビュー時に、ドキュメントフラグメント内の実際のテキストを検索する機能を有効にしました。 NPR-17792：CQ-4214501 のホットフィックス

#### Correspondence Management {#correspondence-management-5}

>[!NOTE]
>
>テキストフラグメントの検索機能には、いくつかの制約があります。
>
>* ドキュメントフラグメントのコンテンツでは大文字と小文字が区別され、タイトルでは大文字と小文字が区別されません。
>* 検索した単語の一部のスタイルが異なる場合や、「」、「」、「\」などの特殊文字が含まれている場合、検索結果はハイライトされません。
>* ドキュメントフラグメント内の動的コンテンツ（データディクショナリ要素の値や変数の値など）に対しては検索が機能しません。


#### Formsマネージャ{#forms-manager-2}

* CQ-4219684の修正プログラムで、アダプティブFormsのXMLスキーマプロパティをAEM 6.2でCFP6を適用した後に編集できない
* サーバーの再起動時に、AEM Formsマネージャーコアバンドルのすべてのサービスが開始されません。 CQ-4217014 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-12}

#### LCM のインストール {#install-lcm-2}

* Microsoft Windowsの管理者画面に、CFP6のインストール後にバージョン番号6.0が表示される。 CQ-4217573 のホットフィックス

## 含まれている機能パック {#feature-packs-included-2}

* デスクトップアプリケーションのTouchUIボタンの機能強化。 NPR-18676

## CFP 8 {#osgi-bundles-included-in-cfp}に含まれるOSGiバンドル

AEM 6.2SP1-CFP8で更新されたOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/updated-bundles-list-cfp8.txt)

AEM 6.2SP1 ～ CFP8で更新されたコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* dcを持つ画像の画像カード上のタイトルの表示に関する動作の変更：titleプロパティがString [] (multifield)に設定されている。
* Dynamic MediaCloud Services、タッチ操作対応UI、およびセキュリティUIインターフェイスのパフォーマンスの問題を修正しました。
* Apache Felix Http Bridge 3.0.8の修正点
* 作成者と発行環境間のバイナリレスレプリケーション(BLR)を解決しました。
* 一般的なWeb実装とシングルページアプリケーションの両方のために設計された、Adobe Targetとのクライアント側統合のための実装ライブラリ、AT.JSターゲットライブラリファイルのサポート。
* ユーザーが設定可能なMarketing Cloudソリューション(Analytics、DTM、ターゲットおよびS&amp;P)の接続タイムアウト時間を導入することで、AEMのパフォーマンスが向上しました。

### アセット{#assets-12}

* Dynamic MediaCloud Servicesで設定されたAEM 6.3でビデオ取り込みをテストする際に、「開いているファイルが多すぎます」という例外が発生する。 NPR-18734;CQ-4211407の修正プログラム
* AEMインスタンスを再起動した後、ページ上のアセットのバニティURL設定が機能しない。 NPR-18634;Granite-18085用修正プログラム
* TouchUIでは、アセットを公開する権限を持たないユーザーに対しては、「公開」ボタンが表示されます。 NPR-18620;CQ-4214042の修正プログラム
* ライセンス契約が設定されると、アセットのダウンロードダイアログボックスに動的レンディションオプションが表示されなくなります。 NPR-18607;CQ-4212342の修正プログラム
* 名前にスペースが含まれるアセットのダイナミックレンディションがダウンロードできない。NPR-18571;CQ-4211738の修正プログラム
* Creative Cloudでアセットフォルダーを共有する際に、複数のユーザーを保存できません。 NPR-18489;CQ-103297用修正プログラム
* dc:title &amp; dc:説明は、crx/deの複数フィールドの値に変更されません。 NPR-18474;CQ-4209086の修正プログラム
* アセットの移動操作は、パフォーマンスの低下を引き起こします。 NPR-18346
* デフォルトの「すべてを表示」オプションを設定して開いた場合、タイムラインに項目は表示されません。 NPR-18302;CQ-4211957用修正プログラム
* ASCII／UTF-8 エンコードされたテキストファイルが AEM Assets にアップロードされ、サムネールの生成に失敗すると、エラーが発生する。NPR-18006：CQ-4209345 の CFP
* 「発行」アクションボタンは、複製アクセス権を持たないユーザーでも表示されます。 NPR-17353;CQ-4209269の修正プログラム
* min:gcc;obfuscate=trueを使用して縮小が有効になっている場合、サイト管理者とミスカドミンはどちらも機能しません。 NPR-18593;CQ-4209220の修正プログラム
* カスタムメニュー項目は、毎回画面が更新されるまで表示されません。 NPR-18500;CQ-4213581の修正プログラム
* moment.jsを2.10.6にアップグレードします。NPR-18596;Granite-11881用修正プログラム
* DMマクロに権限を適用すると、管理者ユーザーの表示が壊れる。 NPR-18544;CQ-4211729の修正プログラム
* アセットの「後で発行」で、不正なArgumentExceptionが発生する。 CQ-4214532

### サイト{#sites-12}

* MongoDBを使用するアクティブ — アクティブ作成者クラスターでは、時間がコンテンツに対して設定されたオンタイムに達すると、両方の作成者が同じコンテンツのレプリケーションをトリガーしようとします。 NPR-18708;CQ-4210982の修正プログラム
* jcrのない参照を持つリソースを移動する場合のNPE:コンテンツノード。 NPR-18664
* プレースホルダーが複数の parsys コンポーネントを含むページに表示されない。NPR-18645;CQ-110253の修正プログラム
* AbstractCopyMoveCommandの並行性の問題。 NPR-18591
* テキストを別のAEMインスタンスからparsysコンポーネントにコピーする場合、parsysはresourceTypeが設定されていない状態で作成されます。 NPR-18511;CQ-4212306の修正プログラム

### プラットフォーム {#platform-10}

* JCRインストーラーで、パッケージのインストール後にバンドルバージョンが更新されない。 NPR-18728;NPR-15135用の修正プログラム
* バイナリレスレプリケーション(BLR)は、作成者と発行の環境を含むバイナリで失敗します。 NPR-18704
* AEM環境でのApache Felix Http Bridge解決リクエスト。 NPR-18297
* 同じ構造を持つ複数のページがSlingコンテンツ配信と同時に複製される場合、レプリケーションは失敗します。 NPR-18665;Granite-13712用修正プログラム
* Sling配布パッケージは構築され、自動クリーニングは行われません。 NPR-18601;Granite-16183用修正プログラム

### 統合 {#integration-13}

* ライブラリフォルダーから発行されたオファーを表示すると、NPEが発生します。 NPR-18732;CQ-4214593の修正プログラム
* アクティビティの開始/終了日がJCRで更新されず、ターゲットが特定の日付から「アクティブ/非アクティブの場合」に変更された場合にも更新されません。 NPR-18612;CQ-104831の修正プログラム
* AEMとのAnalytics統合では、httpclient接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。 NPR-18497
* AEMとのDTM統合では、httpclient接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。 NPR-18495
* AEMとのターゲット統合では、httpclient接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。 NPR-18494
* AEMとのSearch &amp; Promoteの統合では、httpclient接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。 NPR-18493
* 追加のエクスペリエンスを追加した後、ターゲットアクティビティが無効化される。NPR-18227;CQ-4201895の修正プログラム

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-7}

* 画像マップは、HTL画像コンポーネントで選択した座標を保持しません。 NPR-18530;CQ-4211584の修正プログラム

### 翻訳 {#translation-5}

* 翻訳の検索結果に翻訳プロジェクト名が含まれない。NPR-18224;CQ-4210658の修正プログラム

### ブランドポータル{#brand-portal-1}

* tagadmin/tagging コンソールで AEM から Brand Portal にタグを公開できるようになりました。CQ-4212165

## フォーム {#forms-13}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-13}

#### Correspondence Management {#correspondence-management-6}

* 正しいデータは、フラグメントが保存されるまで編集パネルに表示されません。 NPR-19092
* ドキュメントフラグメントをレターに追加するには、かなり時間がかかります。 NPR-18958
* XML 宣言がデータ xml ファイルに存在し、レターのレンダリングが POST リクエストによって開始されると、対応するレターでデータを表示できない。NPR-18870
* CM アセットに実行されたアクションの監査ログが生成されない。NPR-16618

>[!NOTE]
>
>次の2つの問題の影響を受ける場合は、このCFP追加オンパッケージをインストールしないでください。
>
>* Word / WebからCM Text Editorにコピーして貼り付けを実行すると、改行の内容が表示されます。 NPR-19530
>* CM Text Editorで改行のないコンテンツは折り返されません。 NPR-19449

>
>
これらは、将来のCFPで対応される予定です。

#### アダプティブフォーム {#adaptive-forms-9}

* 繰り返し可能なパネルに新しいパネルを追加すると、前のパネルのドロップダウンフィールドの値が削除されます。 NPR-18772
* 整数のみを受け入れるようにマークされたアダプティブフォームフィールドでは、数値パッドからの特殊文字も受け入れます。 NPR-18680
* guiderootパネルの初期化イベント時にボタンタイトルを変更するスクリプトが動作しません。 NPR-18476
* ルールエディターで作成されたルールの右パネルには、スクロールバーが表示されません。 NPR-18716

#### AEM Forms アプリケーション {#aem-forms-app}

* AEM Formsアプリがオフラインモードの場合、またはネットワークに接続されていない場合、Formsはアプリで正しくレンダリングされません。 CQ-4218368

### Forms JEE インストーラー  {#forms-jee-installer-13}

#### PDFG サービス {#pdfg-service-3}

* 指定されたブックマークレベルで PPDF Generator がDF ドキュメントを生成できない。CQ-4211102 のホットフィックス

## CFP7 {#osgi-bundles-included-in-cfp-1}に含まれるOSGiバンドル

AEM 6.2SP1-CFP7で更新されたOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

AEM 6.2SP1-CFP7で更新されたコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* タブレットでのレイアウトモードでの非表示のコンポーネントの効率的な管理。
* ハイブリッドデバイスでのQuickactionsの概要を参照してください。
* ライブコピーに関するコンポーネントレベルの同期の問題を解決します。

### アセット{#assets-13}

* 必要な権限を持たないユーザーがアセットの操作を移動しようとすると、顧客がブロックされます。 NPR-18330;CQ-4212560の修正プログラム
* 複数のスマートコンテンツサービスの設定を結合すると、ユーザビリティの問題が発生します。 NPR-18273;CQ-4201557の修正プログラム
* チェックアウトアクション/ワークフローは、約1回はタイムラインコンソールから使用できません。 80個のフラグメントがアセットフォルダーに追加されます。 NPR-18257;CQ-4211214およびNPR-18251用の修正プログラム。CQ-4211216の修正プログラム。
* メモリ不足でシステムがクラッシュし、アセットレポート中にページネーションが表示されない。 NPR-17865;CQ-4209759の修正プログラム
* 公開したビデオは、エンコードされたビデオアセットでの再生に失敗します。 NPR-17849;CQ-4210739の修正プログラム
* PDFのサムネールは生成されません。 NPR-17831、NPR-17750;CQ-4210547の修正プログラム
* 期限切れのアセットは、Adobe CQDAM有効期限通知ジョブによって非アクティブ化されません。 NPR-17666;CQ-107766の修正プログラム
* アセットに所有者が割り当てられていない場合、アセットの有効期限アクティビティは停止します。 NPR-17665;CQ-4197946の修正プログラム
* 150 を超える参照先を持つアセットフォルダーを移動すると、ヌルポインター例外が発生する。CQ-4200981

### サイト{#sites-13}

* パーソナライゼーションは、IP範囲に対してセグメントルールが設定されている場合、最初のIPに対してのみ機能します。 NPR-18121;CQ-83767の修正プログラム
* historyShowプロパティが有効な場合、NumberFormatExceptionが原因でログインに失敗します。 NPR-18073;CQ-101965の修正プログラム
* タッチ操作対応UIで、マークが付いた削除済みページが表示されます。 NPR-18025;CQ-86694の修正プログラム
* 多数（2000 以上）のオーディエンスを持つページをロードする場合のパフォーマンスの問題。NPR-17884;CQ-4209567の修正プログラム
* ページ上の別の画像を削除した後は、画像を選択できません。 NPR-17711;CQ-4201323の修正プログラム

### プラットフォーム {#platform-11}

* タッチUIコントロールは、必要な権限を持たないユーザーに対しては非表示になりません。 NPR-17945;CQ-4211231の修正プログラム
* タグピッカーフィールドに日本語タグがありません。 NPR-17768;CQ-4210456の修正プログラム
* FastQuerySizeが有効な場合、getsize()クエリは誤った結果を返します。 NPR-18018
* スタンバイインスタンスのWebコンソールにアクセスできません。 NPR-17861;Granite-14582用修正プログラム

### コマース{#commerce-2}

* クエリトラバーサルは、カタログのブループリントにセクションに対して条件が定義されていない場合に発生します。 NPR-18229;CQ-4211924の修正プログラム

### コミュニティ{#communities-2}

* PollingImporterImpl. aemのシャットダウンを遅らせます。 NPR-18298;CQ-96133用修正プログラム

### 統合 {#integrations}

* AEM Day HTTP Client 3.1 OSGI がダイジェスト認証を必要とするプロキシで設定されている場合に発生する可能性がある AEM Search コンポーネントエラーを解決。NPR 18128
* 継承を元に戻すチェックボックスがありません。 NPR-17753;CQ-4210139の修正プログラムのリクエスト
* 1つのコンポーネントを複数のアクティビティでターゲット設定する場合、優先順位を設定できません。 NPR-18658;CQ-4210727の修正プログラム
* /etc/segmentation/group1フォルダーの下に作成されたオーディエンスーを選択するために、/etc/segmentationフォルダーを参照することはできません。 NPR-18522

### セキュリティ {#security-1}

* アセットの移動ウィザードは、ターゲットフォルダーに対する書き込み権限がない場合にハングします。 NPR-18300
* XSS脆弱性を事前にエンプトするために、Apache Sling APIでorg.apache.sling.servlets.postサーブレット(2.3.22)のアップグレードバージョンを使用するようにリクエストします。 NPR-18963

### 翻訳 {#translation-6}

* プロジェクトが完了するまで、アセットページを再び翻訳プロジェクトに送信することはできません。 NPR-18249;CQ-4209908用修正プログラム

### WCM ‐ 基盤コンポーネント {#wcm-foundation-components-8}

* WCM 基盤の iparsys コンポーネントを編集可能なテンプレートで使用できない。NPR-18223;CQ-4210384の修正プログラム
* 画像マップは、HTL画像コンポーネントで選択された座標を保持しません。 NPR-18032;CQ-4211584の修正プログラム
* HTL画像コンポーネントがレンダリングされると、URL内のファイル名が変更され、URLが壊れます。 NPR-17908;CQ-4211587の修正プログラム
* 変更を加えた後、ページプロパティを終了できません。 NPR-17832;CQ-96110の修正プログラム

## フォーム {#forms-14}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Formsリリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-14}

**Correspondence Management**

* レターのレンダリング中に、データディクショナリが繰り返し読み取られます。 NPR-18482、CQ-4210805用の修正プログラム
* com.adobe.livecycle.content クラスの JavaDocs を追加。NPR-18467
*  レターの作成時に、レターの説明が保存されない。NPR-18039
* テキストモジュールが保存され、テキストモジュールの式に開始または終了の式タグが含まれていない場合、エラーメッセージが表示されない。テキストモジュールがエラーメッセージを表示し、レターのレンダリングに失敗する。NPR-17798
* アドオンパッケージのインストール時にログに予期しないエラーが表示される。 NPR-18295

**Forms Manager**

* AEM Forms UI ですべてのアセットが古い順にリスト表示される。ユーザーはアセットを新しい順に並べ替えることができない。NPR-18451

### Forms JEE インストーラー  {#forms-jee-installer-14}

**Output サービス**

* AEM forms 6.2のOutputサービスのパフォーマンスの問題が改善されました。NPR-18033

**Signature サービス**

* リモートハードウェアセキュリティモジュールでPDFドキュメントに署名できません。 NPR-18017

## CFP6に含まれるOSGiバンドル{#osgi-bundles-included-in-cfp-2}

AEM 6.2SP1-CFP6で更新されたOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

AEM 6.2SP1-CFP6で更新されたコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* アセットの共有、移動、公開、ダウンロードに関するUIの問題がいくつか解決しました。
* 参照アセットを表示する際の[移動]ダイアログの容量が増加しました。
* 非公開やバージョンの削除など、WCMのコンポーネントとワークフローに関するいくつかの問題を解決しました。
* ツールバーアクションおよびCoralコンポーネントの表示に関するアクションバーの応答性が改善されました。

### アセット{#assets-14}

* ブランドポータルへの公開機能のパフォーマンスが向上しました。 NPR-17189;CQ-4204150の修正プログラム
* 「リンクを共有」オプションを使用してアセットを共有しても、フラットフォルダー構造を持つzipファイルはダウンロード用に作成されません。 NPR-17513;CQ-4209381用修正プログラム
* DAMでアセットを選択して「発行」をクリックしても、アセットの詳細ページに「Brand Portalに発行」オプションは表示されません。 NPR-17351;CQ-94905の修正プログラム
* DAMワークフロー手順では、SessionまたはResourceResolverから取得したバイナリストリームを、リソースリークが発生しないように、最終ブロック内で閉じる必要があります。 NPR-17385;CQ-4209452の修正プログラム
* DAMでWordドキュメントをアップロードすると、nullポインター例外が発生し、ワークフローインスタンスが実行中の状態のままになります。 NPR-17160;CQ-4207358の修正プログラム
* 管理者以外のユーザーのメタデータエディターページには、期限切れのアセットに対して、「共有」、「移動」、「公開」、「ダウンロード」ボタンが表示されます。 NPR-16903;CQ-101440/CQ-104535の修正プログラム
* 共有、移動、公開、コピーなどのアクションは、アセットコンソールの管理者ユーザーに対して表示されます。 NPR-16902;CQ-4207111用修正プログラム

### サイト{#sites-14}

* クラシックUIとタッチUIのいずれかを使用してページを移動する場合、移動ダイアログに150を超える参照が表示されないので、ユーザーはこれらの参照を更新してページを再公開できません。 この問題は、クラシックUIのプロパティを導入することで修正されました。「maxRefNo」（siteadminノードで設定可能）&#39;/libs/wcm/core/content/siteadmin&#39;が追加されました。 このプロパティでは、移動が多い操作の前に表示される参照の最大数（デフォルト値150）を指定します。また、ページに参照数が多い場合は、movePageダイアログに表示されません。 この設定は、ノードに設定を適用することにより、damadminとmiscadminにも適用されます。それぞれ`'/libs/wcm/core/content/damadmin'`と`'/libs/wcm/core/content/miscadmin'`です。 NPR-17222;CQ-85878の修正プログラム

* WCMコンポーネントを使用する場合、タッチUIリッチテキストエディターで、スペースを含むハイパーリンクが削除されます。 NPR-17698、NPR-17570;CQ-4206768の修正プログラム
* ページのプロパティから非公開の要求ワークフローをトリガーすると、レプリケーション権限のないユーザーに対してJavaScriptエラーが表示されます。 NPR-17294;CQ-102064の修正プログラム
* HTL画像コンポーネントのレンダリングまたは書き出しを行うと、URLが数値に変更され、ファイル名が変更されるので、リンクが壊れます。 NPR-17245;CQ-59616の修正プログラム
* ネストされたローンチで、ローンチを削除するとサブローンチが孤立する。NPR-17228;CQ-4202639の修正プログラム
* AEM 6.2でOak 1.4.13を適用してVersion Purgeを実行すると、ログで常に警告が繰り返し表示されます。 NPR-17391;CQ-4206870の修正プログラム
* ContextHubコンポーネント用の修正プログラムまたはアップグレードをインストールした後、コンテンツパッケージは/etc/segmentation/contexthub内のすべてのセグメントを上書きするので、すべてのカスタムContextHubセグメントが失われます。 NPR-17250;CQ-79958用修正プログラム
* ワークフローユーザーとしてネストされたグループを含むワークフローを実行する場合、WorkflowStatusProvider(pageinfo.json)によってワークフローインスタンスがロックアップされます。 NPR-17555;CQ-4202056用修正プログラム
* WCMページエディターコンポーネントを使用する場合、オーサーインスタンスのタッチUI編集モードでは、ページの最後に膨大な空き領域が存在します。 NPR-17510;CQ-4205441の修正プログラム
* HTL画像コンポーネントのレンダリングまたは書き出しを行うと、URLが数値に変更され、リンクが壊れます。 NPR-17245;CQ-59616の修正プログラム

### UI {#ui}

* アセットを選択して開発ツールをクリックした場合、遅い接続ではツールバーのアクションがアクションバーに表示されない場合があり、ページを再読み込みする必要があります。 NPR-17568;CQ-108365の修正プログラム
* アクションバーが更新され、次の2つのコンテナが使用されます。coral-actionbar-primaryとcoral-actionbar-secondaryです。coral-actionbar-commandaryの代わりに、coral-actionbar-primaryとcoral-actionbar-secondaryが使用されます。 NPR-17591;GRANITE-15225用修正プログラム

### Mobile-on-demand {#mobile-on-demand-2}

* AEM Mobileアプリに対する「読み取り専用」権限を持つユーザーは、AEM Mobileコンテンツ管理ページからコンテンツをプレビューできません。 NPR-17390;CQ-4209690の修正プログラム

### セキュリティ {#security-2}

* HTMLRendererServletによって生成された出力のXSS脆弱性。 NPR-17136
* AEM Web SyndicationフィードページでのAEMバージョンの公開を防ぐためのリクエストです。 NPR-16219

### フォーム {#forms-15}

#### Forms アドオンパッケージ {#forms-add-on-package-15}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳細については、AEM Forms リリースを参照してください。

**アダプティブフォーム**

* 添付ファイルを持つアダプティブフォームの場合、フォームが2回目に送信されると、送信済みXMLにafSubmissionInfoタグの重複エントリが作成されます。 NPR-17364
* Google Chromeブラウザーを使用中に、フォームから添付ファイルを削除した後に、同じ添付ファイルを再度添付しようとすると、エラーが発生します。 NPR-17297
* ネストされた繰り返し可能な遅延読み込みパネルがXSDベースまたはNo-Form-modelベースのアダプティブFormsにある場合、フォームに入力された値はレコードのドキュメント(DOR)に保持されません。 NPR-17176
* ルールエディタのエラーログに表示されるエラーは、try/catchブロックのJavaScriptコードのcatchブロックに追加する必要があります。 NPR-16757
* フォーム内の添付ファイルをクリックすると、ブラウザーコンソールエラーがスローされ、添付ファイルプレビューは表示されません。 NPR-17174

**Correspondence Management**

* 通信を作成のUI機能は、UIにインラインテキストまたは空白行が追加された場合に壊れます。 NPR-17748
* レターを編集用に開くと、ブラウザーが点滅します。 NPR-17576
* 計算済みデータディクショナリ要素にリモート関数を追加する際に、関数の数がリモート関数を示すタブの長さより長い場合、タブにスクロールバーは表示されません。 NPR-17359
* APIメソッドの読み込みcom.adobe.icc.services.api.LetterInstanceServiceが機能しません。 NPR-17922、NPR-16008
* テキストモジュールに追加された変数は、レターの編集中、データ連結パネルに表示されません。 NPR-17940
* HTML送信アクションがPOST方式を使用している場合に、Correspondence Management UIが起動しない。 NPR-17595

**Forms支配人**

* ABテスト用に設定されたアダプティブフォームでは、「開始ABテスト」をクリックしてもテストが開始されず、ブラウザコンソールエラーがスローされます。 NPR-17838

**Forms サービス**

* OSGIフォームのスタティックコード分析で報告された問題を修正する必要があります。 NPR-13951

#### Forms JEE インストーラー {#forms-jee-installer-15}

**Output サービス**

* AEM forms 6.2 Output Serviceを使用して特定のフォームをデータXMLとマージする場合、同じ操作に対してLiveCycleES4 SP1サーバーがとる時間に比べて、20倍の時間がかかります。 WindowsおよびLinux環境で修正されました。 NPR-17501

**LCM のインストール**

* AEM Forms6.2 GMのビルドをインストールし、AEM 6.2 CFPを適用した後、LiveCycleConfiguration Managerを実行すると、不要なセミコロンが「Version Information」に表示され、パッチのインストール日は更新されません。 NPR-14322

**プロセス管理**

* TaskContext 変数が AEM Forms プロセスに入力されない。CQ-4211857

#### AEM FormsJEEバンドルパッケージ{#aem-forms-jee-bundles-package}

* JEE管理UIコンソールとOSGiコンソールのどちらを使用しているかに関係なく、フォームユーザーの機能は同じにする必要があります。 NPR-17670

### CFP5に含まれる機能パック{#feature-packs-included-in-cfp}

**FormsJEEパッケージ**

Process Management - HTML Workspace

* ワークスペース手順を割り当てる際、添付ファイルまたはメモが複数ある場合に、「ワークスペースの添付ファイル」タブに添付ファイルまたはメモのカウンターが表示される必要があります。 NPR-17771
* AEM JEEFormsのOffice 365をサポートし、フォームワークフローでの電子メール機能を要求します。 NPR-13866

**Forms追加オンパッケージ**

Correspondence Management

* レタープレビュー中にテキストエディターでフラグメントを編集する場合は、フラグメントで使用されるインライン条件の代わりに、処理済みのテキストが編集用に表示されます。 NPR-15748、NPR-17504

### CFP5に含まれるOSGiバンドル{#osgi-bundles-included-in-cfp-3}

AEM6.2 SP1 ～ CFP5間で更新されたOSGiバンドルのリスト

[ファイルを入手](assets/do-not-localize/cfp5_osgi_bundles.txt)

AEM6.2 SP1 ～ CFP5間で更新されたコンテンツパッケージのリスト

[ファイルを入手](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4は、AEM 6.2 SP1の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

このCumulative Fix Packの主な特徴は次のとおりです。

* ファイルレンディション、タイムラインCamera Raw表示、画像の向きに関するアセットの修正
* 改善点

   * サイトでのWCM起動
   * プロジェクトワークフロー
   * ContextHubコンポーネント

* キャンペーン、Mobile On-Demandおよび翻訳に関する修正
* アダプティブフォームのルールエディターでの操作性の向上
* フォームのCorrespondence Management用のインライン条件エディターの強化
* JEE上のAEM formsのプロセス管理と出力サービスに関する修正
* Formsデザイナースクリプトエディター関連の修正

### プラットフォーム {#platform-12}

* Search&amp;Promote検索フォームでは、クラウドサービスの設定時に`environment`設定が無視され、作成者インスタンスで使用できなくなります。 NPR-16594：CQ-4206076 のホットフィックス
* /appsでオーバーレイして&#x200B;**Assets OmniSearch**&#x200B;結果に列を追加またはカスタマイズすることはできません。 NPR-16737：CQ-4206785 のホットフィックス
* AEM 6.1 SP2からAEM 6.2 SP1へのインプレースアップグレード後、**Deagnosis tool **pageが機能しなくなる。 NPR-17121;CQ-4196786の修正プログラム
* HTL:フォーラムを選択し、トピックと投稿を作成する際に、`Sightly SightlyCompiledScript`によって、`RequestDispatcherOption`に誤った`addSelectors`プロパティが追加されます。 NPR-17008：GRANITE-16384 のホットフィックス

* `ReportImporter`で使用される`ManagedPollConfigs`に`CRON expressions`のサポートを追加しました。 NPR-16608：CQ-4206066 のホットフィックス要求

* LDAPユーザーのアバター画像のアップロードに失敗しました。 NPR-16561;Granite-17013用修正プログラム
* User Management画面に表示される結果の数は、カードとリストの表示で異なります。 NPR-16241;GRANITE-16914用修正プログラム
* Google Chromeブラウザーでフルスクリーンモードで表示中に、ワークフロー通知の遅延読み込みが失敗する。 NPR-17013：CQ-4207567 のホットフィックス

### アセット{#assets-15}

* 定義された方向を持つ画像を読み込む際に、画像の方向が正しく適用されません。 NPR-16750：CQ-4204356 のホットフィックス
* 初期設定で「すべてを表示」が設定されている場合でも、アセットタイムライン表示にアセットは表示されません。 NPR-16957：CQ-98780 のホットフィックス
* アセットにレンディションとして追加されたCamera Rawファイル（ARW、CR2、NEF、DNG、EPSなど）は、選択または削除できません。 このようなファイルは、ユーザーがクリックすると自動的にダウンロードされます。 NPR-16949：CQ-4206846 のホットフィックス
* アセットUIで別のpdf内にpdfを作成しても、作成したpdfはDAM UIに表示されませんが、CRXリポジトリには表示されます。 NPR-16833：CQ-4206501 のホットフィックス
* タッチ UI を使用して、アセットをそれ自体の直接の子ノードとしてアップロードすると、問題が発生する。アセットは、前に選択したアセットの直接の子としてアップロードされます。 NPR-16534：CQ-4204287 のホットフィックス
* DAM UIで、アセットにコメントし、コメント内のユーザーにタグを付けても、電子メール通知は生成されません。 NPR-16589：CQ-102318 のホットフィックス

### プロジェクト {#projects-3}

ワークフローが削除されると、プロジェクトワークフローコンソールにNullPointerExceptionがページに表示されます。 NPR-17017：CQ-4194269 のホットフィックス

### サイト{#sites-15}

* `ContextHub`内のファイルは、作成者インスタンス上で最小化されません。 NPR-17022：CQ-79456 のホットフィックス
* WCM起動のローンチプロモーションは、ページの大きなツリーで構成される起動のプロモーションに長い時間がかかります。 NPR-16480：CQ-82731 のホットフィックス
* `ClientContext` セグメント条件レンダラーは、未完了または未完了のルールを使用してセグメント(またはオーディエンス)が作成された場合にクラッシュします。NPR-16759：CQ-4205104 のホットフィックス
* WCM起動で、タッチUIのページプロパティ内からアクションが開始された場合、起動に関連付けられたページは非公開になりません。 NPR-16560：CQ-4204681 のホットフィックス
* リンクリライタは、コロン「:」がJCR名前空間を定義していると仮定し、コロンを含むhref値を誤って書き換えます。 NPR-16753：CQ-4203762 のホットフィックス
* WCM-Design Importerで、テストインポーターページを開き、zipファイルをアップロードしようとすると、以前にアップロードおよび削除されている場合に問題が発生します。 NPR-16486：CQ-90962 のホットフィックス
* Firefox SafariとGoogle Chromeブラウザーを使用して&#x200B;**[!UICONTROL グローバルナビゲーション]**&#x200B;ペインに移動すると、ユーザーの操作感が異なります。 Firefoxブラウザーには&#x200B;**[!UICONTROL ツール]**&#x200B;メニューが表示され、Google Chromeブラウザーには&#x200B;**[!UICONTROL ナビゲーション]**&#x200B;メニューが表示されます。 NPR-16770;CQ-4200456の修正プログラム

### Campaign {#campaign}

* AEMキャンペーンテンプレートをテストし、シードアドレスを変更して「追加データ」を含めると、タッチUIコンテキストハブでAdobe Campaignのドロップダウンが消えます。 NPR-16771：CQ-105748 のホットフィックス

### モバイルオンデマンド{#mobile-on-demand-3}

* AEM作成者環境からパブリケーションをプリフライトする場合、5秒以上かかるプリフライトアクションは、AEMM - AEM PECS Integration splunkダッシュボードで、1秒あたりのステータス要求数が多い異常なスパイクを引き起こします。 NPR-16908：CQ-4207055 のホットフィックス
* AEM-6.2-SP1-CFP1-1.0アップデートのインストール後、AEM Mobileの設定管理が失敗する。 NPR-16909：CQ-4204892 のホットフィックス

### 翻訳 {#translation-7}

* 6.2 SP1 - CFP1のインストール後、翻訳ジョブのプレビューが動作しない。 NPR-16481;CQ-4204655の修正プログラム
* 翻訳を使用して作成された言語コピーは、ローカルの国のlivecopyではなく、ルートマスターを指します。 NPR-17257;CQ-4208287の修正プログラム

### セキュリティ {#security-3}

* ファイルのバイナリがAEMにアップロードされる場合、MIMEタイプの検証は実行されません。 NPR-16617
* LDAP ユーザーのアバター画像のアップロードに関する問題。NPR-16561

### フォーム {#forms-16}

#### Forms アドオンパッケージ {#forms-add-on-package-16}

**アダプティブフォーム**

* アダプティブFormsエディタでは、head.jspのターゲット設定コメントを新しいContext Hub文に置き換える必要があります。 NPR-17173
* アダプティブFormsルールエディタで、**[!UICONTROL アイテムを選択]**&#x200B;にイベントが「null」と表示されます。 NPR-17139
* 送信されたフォームは、進む矢印(>)を使用して進むと再送信されます。 NPR-17080
* AJAX経由でアダプティブフォームを送信する場合、エラーが発生した場合に&#39;error&#39;コールバック関数は呼び出されません。 NPR-17034
* 実行時にルールエディターで「**[!UICONTROL フォームを保存]**」ボタンをクリックしても、フォームは保存されません。 NPR-16905
* スタティックテキストは、アダプティブフォームではタブ順序から除外する必要があります。 NPR-16749
* 十進数フィールドの計算値が正しく表示されません。 NPR-16596
* ヘルプコンテンツを表示するアイコンは、アダプティブフォームのタブ順序に含める必要があります。 NPR-16484
* アダプティブFormsのデータの事前入力用に、&#39;**[!UICONTROL デフォルトの事前入力サービスの設定]**&#39;でタイプ`dataRef=C:/Users/`の正規式の使用をサポートします。 NPR-16425

* ネストされた遅延読み込みシナリオがある場合、検証はすべてのパネルで正しくトリガーされません。 NPR-15821

**Correspondence Management**

* レターに空白のテキストモジュール（テキストのないモジュール）が含まれる場合、レターのレンダリングは失敗します。 NPR-17054
* 改行とタブスペースは、テキストエディタに貼り付けた後で、コンテンツから削除されます。 NPR-17039
* テキストモジュールが多数のレターで参照されている場合、テキストモジュールの参照の表示には時間がかかります。 NPR-17035
* ドキュメントフラグメントの参照の編集、保存、削除および設定には時間がかかります。 NPR-17033
* 均等揃えされたテキストは、レターをプレビューする際に、異なるフォントでレンダリングされます。 NPR-16976
* 検索されたテキストに複数の語句が含まれる場合、検索機能は正しく動作しません。 NPR-16920
* ブラウザにテキストエディタツールバーが断続的に表示されます。 NPR-16919
* ルールエディターの&#x200B;**[!UICONTROL 「フォームを保存]**」構文が機能しません。 NPR-16905
* Internet Explorerを使用してデータディクショナリに基づくテキストモジュールを作成する場合、フォントドロップダウンはフォントファミリーに入力されません。 NPR-16944
* テキストフラグメントを作成すると、レターのプレビュー時にレターのフォントが変更されます。 NPR-16830
* ドキュメントフラグメントの先頭または式の間にタブスペースがあるレターは、レンダリングまたはプレビューできません。 NPR-16769

**モバイルForms**

* Mobile Formプレビューでは重なり合うコンテンツが表示されますが、フォームはPDFレンダリングに対して正しく表示されます。 NPR-17105

**フォームポータル**

* 送信されたフォームの「**[!UICONTROL ダウンロード]**」リンクをクリックすると、PDFフォームではなくHTMLページが開きます。 NPR-17082

* `Upload Comments` の添付ファイルは、crxリポジトリに格納されたXMLには存在しますが、送信済みインスタンスのUIには表示されません。NPR-17075

**Reader Extensions サービス**

* 特定のファイルは、AEM forms OSGIのインストールでReader拡張されていません。 NPR-16625

#### Forms JEE インストーラー  {#forms-jee-installer-16}

**コア**

* アップグレードプロセス中に、Configuration Managerがタイムアウトで失敗します。 NPR-16774（[コンポーネントレベルでの操作のタイムアウトの設定](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)を参照）。

**Process Management - HTML Workspace**

* 開始タスクからのスタートポイントは、スタートポイントの送信時に送信されたデータで始まりません。 NPR-16917
* HTML Workspace内のフォームの「**[!UICONTROL Return]**」ボタンをクリックしても、フォームは閉じられませんが、グループキューに戻ります。\
   NPR-16352

**プロセス管理**

* ユーザーは、以前のタスクの表示名をプロセスインスタンス内の次のタスクのいずれかに設定できます。 NPR-15382

**Output サービス**

* Outputサービスは、`date-time format`メタデータに追加の&#39;milli-sec&#39;フィールドが含まれるように変更されたPDFの処理に失敗します。 NPR-16838

#### Forms - Designer {#forms-designer}

* AEM Designerのスクリプトエディターでは、フォームのプロパティのデフォルト値が`Calculate Event`および`Validate Event`に適用されません。 NPR-15921

### CFP4に含まれる機能パック{#feature-packs-included-in-cfp-1}

**Forms追加オンパッケージ**

* Correspondence Management用のインライン条件エディターの機能強化。 NPR-10981

### CFP4に含まれるOSGiバンドル{#osgi-bundles-included-in-cfp-4}

AEM 6.2 SP1 と CFP4 の間で更新された OSGi バンドルのリスト

CFP3の主なハイライトは次のとおりです。

* ダイジェスト認証を使用したプロキシを使用した、クラシックUIおよびAEM検索コンポーネントの検索機能の効率化
* アセットのアップロードとアセットメタデータの表示の問題を修正
* タイトルに特殊文字が含まれる場合の、フォルダーの作成時やページの移動時の問題を修正しました。
* ターゲット設定 —オーディエンスの同期、キャンペーンの公開、タッチUIでの目標指標の選択の使用に関する修正
* 翻訳ジョブの同期の問題を解決します。
* Forms事前入力サービスのセキュリティ強化を提供
* フォームポータルのドラフトと送信コンポーネントおよびBarcoded Serviceでの改善点
* ファイル添付ウィジェットまたは遅延読み込みフラグメントを含むアダプティブフォームの使い勝手を向上しました。
* 検索機能の強化、削除されたアセットのログ、データディクショナリの読み込みなど、Correspondence Managementでの操作性が向上しました。

### プラットフォーム {#platform-13}

* **ModelAdapterFactory**&#x200B;の競合状態。2つのスレッドが同じフィールドを挿入しようとすると、モデルの構築に失敗する可能性があります。 NPR-16443：SLING-6584 のホットフィックス。
* /appsの下のオーバーレイされたファイル（JSPまたはJavaScriptファイル）と/libsの下の修正プログラムに含まれるファイルとの間の競合を検出するための、パッケージマネージャーの検証オプション。 影響を受けるオーバーレイは、/libsの下のファイルの変更を含むように再ベースできます。 NPR-16216：CQ-81729 のホットフィックス
* パブリッシャーの起動後、error.logにログインすると、数秒後に停止し、再度実行するためにクリアする必要がある場合があります。 ログフレームワークを更新し、Slingログを提供する要求です。 NPR-15913：Granite-15452 のホットフィックス
* HTL JavaScript Use API実装の失敗を回避するために、JavaScript &quot; `use"` APIの更新を求めます。 NPR-16461：SLING-6780 のホットフィックス。

### サイト{#sites-16}

* AEM 6.0からAEM 6.2にアップグレードした後、多数のクエリが原因でタグを検索する際に、クラシックUIのパフォーマンスが遅くなります。 この問題を解決するには、[タグ付けコンソール（クラシックUI）のレプリケーションステータスを無効にする](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr)に記載されている手順に従います。 NPR-15842：CQ-4201748 のホットフィックス.

* タッチUIでページを作成する場合、「名前」フィールドの入力チェックでは、（クラシックUIと同様に）特殊文字「アポストロフィ」はチェックされません。 したがって、ページを移動できません。 NPR-16404：CQ-4205321 のホットフィックス.
* リッチテキストエディターで2つの行に異なるスタイルを適用して結合すると、2つ目の行に適用されたスタイルが削除されます。 NPR-16389：CQ-4203835 のホットフィックス.
* タッチ操作対応UIサイト画面で、サブページのないページ内にページを貼り付けようとしても、「貼り付け」ボタンが表示されないので、機能しません。 NPR-15894：CQ-4201696 のホットフィックス.
* コンテンツファインダーパネルの「ページ」タブをスクロールすると、クラシックUIではページの一部が無制限に表示されますが、タッチUIでは繰り返しないページの数が限られて表示されます。 NPR-16271：CQ-4202371 のホットフィックス
* LiveCopyのページプロパティをタッチ操作対応UIで開き、変更せずに「保存」をクリックすると、LiveCopyタブが書き出され、LiveSync Configノードが作成されます。 NPR-16327：CQ-108562 のホットフィックス
* フォーム制約は`ConstraintMessage`プロパティを読み取れません。 NPR-16388：CQ-101330 のホットフィックス
* `wcm/foundation/components/parsys`コンポーネントは&#x200B;**[!UICONTROL &#39;コンポーネントをここにドラッグ]**&#39;プレースホルダーを表示しません。 NPR:16748:CQ-4205187の修正プログラム

### アセット{#assets-16}

* pdfラスタライザーが動作を停止し、6.2 SP1またはHotfix 12430のインストール後にメモリ不足の問題が発生します。 NPR-15991
* 文字列プロパティ`documentNumber`のメタデータは日付として表示されますが、数値である必要があります。 NPR-16134：GRANITE-16916 のホットフィックス
* タイムラインイベントのバルーンのテキスト切り捨て NPR-16226：CQ-85226 のホットフィックス
* タイトルに特殊文字を含むコンテンツ階層下のフォルダを作成すると、その特殊文字のエンコードされた形式が表示される。 NPR-15935：CQ-4202987 のホットフィックス
* 「作成」ボタンの使用時に表示される動作が一貫しないため、ユーザーはアセットのアップロードやフォルダの作成を実行できません。 NPR-16410：CQ-4204793 のホットフィックス
* AEMオーサリングの記事表示から共有HTMLリソースをアップロード中に予期しないエラーが発生しました。 NPR-16133:AEMM 4155970用修正プログラム

### 統合 {#integration-14}

* ダイジェスト認証でプロキシ認証を有効にする場合、AEM検索コンポーネントはConcurrentModificationExceptionをスローします。 NPR-15309：CQ-4199191 のホットフィックス
* AEMでターゲットA/Bテストアクティビティを作成すると、オーディエンスはターゲットと同期せず、「オーディエンスなし」と表示されます。 NPR-16229：CQ-4204210 のホットフィックス
* SP1+NPR-11577 v1.2をインストールした後、TouchUIでターゲット設定を行っているときに、目標指標に「Analytics指標を使用」を選択した場合、指標のドロップダウンリストが読み込まれなくなりました。 NPR-16129：CQ-4204316 のホットフィックス
* ターゲット設定を使用している場合、キャンペーンを公開しても、ブランドやマスターを含むツリー全体は自動的に公開されません。 NPR-15855：CQ-94630 のホットフィックス

### 翻訳 {#translation-8}

* 同期翻訳ジョブは自動的にはトリガされず、翻訳プロジェクトをポーキングしない限りAEMのポーリングは行われません。 NPR-15163：CQ-90856 のホットフィックス

### フォーム {#forms-17}

#### Forms アドオンパッケージ {#forms-add-on-package-17}

**アダプティブフォーム**

* 添付ファイルを含むアダプティブフォームを保存する際、添付ファイルのフルパスが、添付ファイルの名前ではなく、生成されたXMLの`fileAttachment`タグに追加されます。 NPR-16529
* XDPベースのアダプティブフォームでは、事前入力XMLに`afData/afBoundData`ラッパーがなくても、送信済みXMLに`afData/afBoundData`ラッパーが存在します。 NPR-16118

* 数値フィールドの指数表記：アダプティブフォームを使用する際に、合計10文字を超える小数の数値を入力すると、送信されたXMLでその数値は指数表記に変わります。 NPR-16106
* 添付ファイルコンポーネントと遅延読み込みフラグメントの両方を含むフォームの場合、送信されたデータxmlには添付ファイルコンポーネントの情報が含まれません。 NPR-16022
* 遅延読み込みが有効な繰り返し可能パネルで、繰り返し可能な親要素がない場合、パネルの2番目のインスタンス内の繰り返し可能な子要素は繰り返しに失敗します。 NPR-15944
* フォームエディターでフラグメント内にフラグメントを保存しようとすると、フラグメントモデルのルートに子フラグメントの値が入力されなくなります。 NPR-15943
* 項目が1つだけのチェックボックスを作成し、項目のタイトルを非表示にしたままチェックボックスのタイトルを表示しようとすると、項目のテキストが空の場合、辞書の作成アクションは`ArrayIndexOutOfBoundException`をスローします。 ディクショナリは作成されず、エラー応答は画面に生成されません。 NPR-15816
* 添付ファイルウィジェットを含むアダプティブフォームの場合、添付ファイルをプレビューした後、フォームの一部が無効になります。\
   NPR:16611

* 複数の添付ファイルを許可する添付ファイルウィジェットの場合、添付ファイルを含む新しいフォームインスタンスが以前の添付ファイルを持つウィジェットで送信されると、エラーコードが表示され、実際のコンテンツは表示されません。 NPR-16258
* `file://`、`http://`、`ftp://`などのプロトコルを使用して、フォームの事前入力サービスを不正アクセスから保護します。 「[Configuration Managerを使用した事前入力サービスの設定](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)」を参照してください。 NPR-15414

* 検証手順では、アダプティブフォームをHTMLではなくPDF形式でレンダリングし、PDFにすべての添付ファイルを追加して、印刷結果にフォーム全体が表示されるように要求します。 NPR-9011

**Correspondence Management**

* プレビュー/編集モードでレター内のテキストフラグメントを操作中に、テキストがリストに変換されると、レターの機能全体が壊れ、JavaScriptエラーが生成されます。 NPR-16460
* XSDがアップロードされ、ルートノードが選択されるたびにブラウザーが応答しなくなるので、Correspondence Managementノードにデータディクショナリを作成するXSDファイルの読み込みは失敗します。 この問題はブラウザーに依存せず、サーバーログには表示されません。 NPR-16452
* Internet Explorerブラウザーを使用してレターをプレビューし、コンテンツのフォントサイズを編集しようとすると、フォントサイズドロップダウンに重複の値が8 ～ 72の間で表示されます。 NPR-16387
* XDPフラグメントからの入力フィールドとしてフローティングフィールドが表示される場合、Internet Explorerブラウザーの使用中にレタープレビューでそのフィールドが拡大されません。 NPR-16367
* プレビューから直接レターを送信しようとすると、レター名のポップアップが非表示になっているので、正しく表示されません。 NPR-16353
* レターの編集中に追加された行スペースは、プレビューーウィンドウに反映されません。 テキストフラグメント内のリストの場合、PDF出力で正しい間隔が表示されません。 NPR-16267
* Internet Explorerブラウザーを使用してテキストドキュメントフラグメントを操作中に、テキストにインデントを設定しようとすると、カーソルでテキストのインデントが許可されないので、テキストにインデントを設定できません。 NPR-16128
* 既存のテキストドキュメントフラグメントへのデータディクショナリの追加または変更には時間がかかり、ユーザーには常に通知されません。 NPR-16102
* Internet Explorerブラウザーを使用してスクロール可能コンテンツを含むレターをプレビューする場合、ブラウザーのスクロールバーはレターのスクロールバーと重なり、右側のフラグメントについてはコンテンツ全体を表示できません。 NPR-16068
* Google Chromeブラウザーを使用してテキストドキュメントフラグメントを作成または編集中に、色選択ドロップダウンが自動的にポップアップ表示され、削除できません。 フラグメントを編集するには、リストをデータエントリの種類として選択する必要があります。 NPR-16067
* レターインスタンスAPIを使用している間は、メソッド`import com.adobe.icc.services.api.LetterInstanceService`は機能しません。 NPR-16008
* Asset Composer設定で日付の表示形式を`locale=en_US; dateFormat=MMM dd,yyyy;`に変更すると、期待どおりに動作せず、日付の形式が無効な文字として表示されます。 NPR-16007
* 再オーサリング時のレターのデータリンケージタイプは、以前に異なる設定があった場合でも「ユーザー」として表示されます。 NPR-16619

**フォームポータル**

* ドラフトコンポーネントと送信コンポーネントのアップグレードシナリオは、データベースサンプルの実装では動作しません。 NPR:16752

**Barcoded Service(BCF)**

* Barcoded Digital Service(BCF)の静的コード分析は、問題を報告します。 NPR-13855

#### Forms JEE インストーラー  {#forms-jee-installer-17}

**Process Management - HTML Workspace**

* 「file://」、「http://」、「ftp://」などのプロトコルを使用して、フォームの事前入力サービスを不正アクセスから保護します。 詳しくは、[Configuration Managerを使用した事前入力サービスの設定](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)を参照してください。 NPR-15434

**ユーザー管理 **

* SAMLログイン画面に、AEM 6.2サーバー上の不適切なバージョン(6.1.0)が表示される。 NPR-13825
* AEM Formsがシングルサインオン(Kerberos)認証を設定している場合、ログイン試行中にユーザー認証に失敗すると、エラーコード「404」が返されます。 ページを更新した後でのみ、ユーザーはログインサイトにリダイレクトされます。 NPR-15015

#### Forms - Designer {#forms-designer-1}

* 辞書のスペルチェックでフォームロケールをフランス語（カナダ）に変更しても、AEM Formsデザイナーでは機能しません。\
   NPR-15896

### CFP3に含まれる機能パック{#feature-packs-included-in-cfp-2}

**Forms追加オンパッケージ**

* Correspondence Managementでアセットを削除する場合、警告メッセージがerror.logファイルに記録されます。 NPR-13225
* Correspondence Managementでレターをプレビューする際の検索機能を強化し、レタータイトルやラベルだけを検索するのではなく、テキストフラグメントコンテンツ内のテキストを検索できるようにします。 NPR-16103

### CFP3に含まれるOSGiバンドル{#osgi-bundles-included-in-cfp-5}

AEM 6.2 SP1 と CFP3 の間で更新された OSGi バンドルのリスト

[Get ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
FileCumulative Fix Pack 2の主な特徴は次のとおりです。

* Slingフレームワークや操作を含むAEMプラットフォームの安定性の修正とパフォーマンスの向上
* アセット管理が改善され、アセットのアクセス、移動、検索、アップロードおよび公開に関するいくつかの修正が行われました。
* コンテンツフラグメント、アンカープラグイン、スライドショー、Context Hubコンポーネントの修正により、サイトのオーサリングと管理が改善されました。
* テキストエディター、Omnisearch、バリアント作成プロセスなど、タッチUIに関するいくつかの修正
* 翻訳ワークフローの改善Azureポータル用の新しい変換APIを使用するためのMicrosoftコネクタの強化
* プロジェクトとキャンペーンの修正点
* アダプティブフォーム、Correspondence Management、およびフォームポータルの機能が修正され、オーサリングと管理が強化されました。
* FormsのJEEコア、XTG、およびHTML Workspaceコンポーネントの修正点

### プラットフォーム {#platform-14}

* Slingフレームワークを直接参照するページが編集された場合に`SlingPostProcessor`がトリガーされます。 NPR-15754：CQ-104153 のホットフィックス

* `tagBasePath`プロパティを持つタグの値は、ページコンポーネントへの移動中にクラシックUIダイアログで取得されません。 NPR-15543：CQ-4199950 のホットフィックス

* Sling処理の実行中に、&#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk`という名前のチャンクが空のチャンクを持つ永久ループに巻き込まれます。 NPR-15455：SLING-5701 のホットフィックス。

* インターフェイスが別のインターフェイスを拡張する場合、スーパーインターフェイス上のインジェクト可能なメソッドは正しく挿入されません。 NPR-15202：SLING-5710 のホットフィックス。
* `com.adobe.granite.infocollector.impl.FilesTraversal`関数呼び出しを使用する場合、潜在的なnullポインタの例外を防ぐことはできません。 NPR-15169 CQ-4197640用の修正プログラム
* 一部の二次ノードではワークフローの状態が一貫しておらず、そのノードの監視イベントをディスパッチ中にエラーが表示されます。 NPR-15701：GRANITE-13786 のホットフィックス
* ユーザーがCRXDEでノード（/content/dam/など）を選択し、「アクセス制御」タブをクリックしてアクセス制御リストが存在することを確認すると、一部の要素をドラッグ&amp;ドロップすると、選択した要素以外の要素が移動します。 NPR-15696 GRANITE-16300用修正プログラム
* 偽装を試行する際に、ドロップダウンリストからユーザーを選択すると、ユーザー全体がポップアップ表示されなくなります。 NPR-15774:HotFix for CQ-4201738/GRANITE-11895
* Omnisearchでは、自動入力された提案を含むタグでの検索は機能しません。 NPR-15088：GRANITE-14426 のホットフィックス.\
   注意：この修正には、Oak CFP 1.4.11以降が必要です。

### Mobile AEM Author {#mobile-aem-author}

* ハイブリッドアプリケーションでAEM MobileとContentSyncパッケージを使用する場合、AEMは、アプリケーションが要求したものの代わりに、最も古いパッケージを使用して、アプリケーションが作成したフェッチ要求（タイムスタンプ付き）に応答します。 NPR-15749：CQ-104153 のホットフィックス

### サイト{#sites-17}

* ワークフローをアクティブ化した後にユーザーがページを変更した場合、WCMコアのワークフローインボックスの変更ステータスは変更されません。 NPR-15684:CQ-4196974のホットフィックス
* タッチUI用リッチテキストエディターのアンカープラグインは、ユーザーがアンカーアイコンをクリックして名前を追加した場合、非準拠のHTML5を生成します。 アンカー要素のHTML5タグに、「name」属性の代わりに「id」属性を追加する必要があります。 NPR-15650：CQ-89782 のホットフィックス
* 多数のフィールドを持つメタデータスキーマを作成し、コンテンツフラグメントメタデータに適用した場合、コンテンツフラグメントメタデータ画面にはスクロールバーが作成されず、フィールドを編集できなくなります。 NPR-15478：CQ-4202622 のホットフィックス
* `TagInput`フィールドコンポーネントの編集時に、以前に設定した値がダイアログフィールドに表示されません。 NPR-15464:CQ-4200360のホットフィックス

* コンテンツフラグメントエディターUIでは、コンテンツフラグメントの多くのバリエーションが作成された場合、サイドパネルにスクロールバーが表示されず、すべてのバリエーションを操作できます。 NPR-15445:CQ-4199444のホットフィックス
* ユーザーを直接グループから削除すると、継承されたグループに追加されます。 NPR-15400：CQ-98758 のホットフィックス
* WCMオーサリング：タッチUI作成者は、名前にコンマが含まれるページを編集できません。 NPR-15396：CQ-4199723 のホットフィックス
* オーサリングにタッチUIを使用している場合、関数`Granite.author.editableHelper.doSelectParent`が引数を誤った順序で渡すと、JavaScriptエラーが発生します。 NPR-15349：CQ-4198594 のホットフィックス
* ContextHubセグメントは、オプトアウトCookieが存在する場合でもエクスペリエンスを表示します。 NPR-15293：CQ-4198024 のホットフィックス
* クラシックUIのスライドショーコンポーネントでは、スライドを作成したり、画像をドラッグ&amp;ドロップして新しいスライドを作成することはできません。 NPR-15281：CQ-4194164 のホットフィックス
* ユーザーは、権限に関係なく、サイト管理コンソールに「ページを作成」、「サイトを作成」、「ライブコピーを作成」、「起動を作成」、「カタログを作成」の各メニュー項目など、「作成」オプションを表示します。 NPR-15278：CQ-94436 のホットフィックス
* AEM 6.2 Service Pack 1のインストール後、「サブページを含める」スライダーがページ起動時に機能しなくなります。 NPR-15230：CQ-4198449 のホットフィックス
* バージョンの削除を拡張して、ブロック内のバージョンを取得して処理し、指定されたパスをXPathクエリに使用できるようにする要求です。 NPR-15186：CQ-109205 のホットフィックス
* サイトコンポーネントの「ページプロパティ」サムネールタブに「クリア」ボタンが表示されない。 NPR-15143 CQ-4196997用の修正プログラム
* ライブコピーを使用するサイトでは、サイト管理コンソールの列パネルで「ライブコピー」チェックボックスを選択すると、ライブコピーのステータスが正しく表示されず、HTMLマークアップのみが表示されます。 NPR-15108：CQ-97086 のホットフィックス
* コンテンツフラグメントを編集する際に、ユーザーが投稿の応答を取得する前に「完了」（「暗号」）をクリックして編集をクリックすると、編集したコンテンツが正しく保存されません。 NPR-15014：CQ-4194095 のホットフィックス
* Timewarpモードで編集ページを閉じ、Siteadminから再度開こうとすると、ページを再び開く代わりにステータスが「500」のエラーが発生します。 NPR-14965：CQ-109647 のホットフィックス:
* Digital Asset Manager(DAM)UIで、「ユーザーピッカー」の「認証可能な項目を検索」を使用すると、「メモリ不足」の例外が発生します。 NPR:15307:CQ-98542のホットフィックス

### アセット{#assets-17}

* Omnisearchでアセットを検索した後、アセットを選択し、「表示のプロパティ」をクリックしてプロパティを編集しようとすると、「保存」ボタンによって空白のページにリダイレクトされます。 NPR-15900：CQ-4202372 のホットフィックス
* アセットユーザーインターフェイスがイベントに応答しない。 アセットを選択して「公開」または「レンディション」をクリックしても、アクティビティは発生しません。 NPR-15828：CQ-4202247 のホットフィックス
* カード表示からアセットを発行する場合、ページが更新されない限り、カードは発行済み状態を反映するように更新されません。 NPR-15826:CQ-102732のホットフィックス
* アセットのホットフィックスを含む累積的な修正プログラム。 NPR-15225
* アセットフォルダーの名前にアンパサンド(&#39;&amp;&#39;)文字が含まれている場合、アセットに移動する際にフォルダー名が正しく表示されません。 NPR-15775：CQ-4201735 のホットフィックス
* アセットファイルの名前にアンパサンド(&amp;)文字を使用すると、そのプロパティにアクセスする際に問題が発生します。 NPR-15770：CQ-4201737 のホットフィックス
* アセット内を移動し、「列表示」表示モードを使用している間、アセットを選択してクリックした後にページを更新すると、アセットの詳細が表示され、更新されたコンテンツは表示されません。 NPR-15768：CQ-4201727 のホットフィックス
* PDS取り込みでは、PDFサービス用のライブラリの山により、CPU使用率が100%増加します。 NPR-15606 HotFix for GRANITE-12929
* Firefoxブラウザーを使用して「リンクの共有」UIにアクセスしても、共有アイテムまたはユーザーが表示されず、画面が使用できない。 NPR-15539:CQ-4200992のホットフィックス
* Digital Asset Managerの使用時、ページが画像のセットに関連付けられている場合、画像を新しいフォルダーに移動すると、ページの関連付けが解除され、関連付けられたページで一部の画像が失われます。 NPR-15538：CQ-111479 のホットフィックス
* Dam Viewerコンポーネントで、「nosamplecontent」実行モードを使用すると、ダイナミックメディアでエラーが発生します。 NPR-15449：CQ-4195425 のホットフィックス
* ビデオプロファイルの作成時に、高品質と中品質の両方のビデオエンコーディングプリセットが選択されている場合、行われた変更は保存されません。 NPR-15447：CQ-4195482 のホットフィックス
* サーバーエラーの応答が原因でBrand Portalへのアセットのアップロードに失敗した場合でも、Brand Portal UIのステータスが「発行済み」に更新され、見逃したファイルを追跡しにくくなります。 NPR-15442：CQ-4197968 のホットフィックス
* アセットフォルダーをBrand Portalに公開する際に、公開に1時間以上かかる場合、一部のファイルが公開に失敗することがあります。 NPR-15441：CQ-4199493 のホットフィックス
* 列表示でアセットファインダーコンソールを使用している場合、フォルダーの作成を試みると、再試行に成功しても失敗します。 NPR-15370：CQ-4199448 のホットフィックス
* DAM UIで選択したアセットまたはフォルダーの名前にコンマが含まれている場合、「参照」タブは使用できず、「参照のリストは複数選択に対して使用できません」というメッセージが表示されます。 NPR-15362：CQ-4199721 のホットフィックス
* Brand Portalにフォルダーを公開しても、フォルダーの下のアセットが正常に公開されても、フォルダーの公開状態は変更されません。 NPR-15292：CQ-4197667 のホットフィックス
* タッチ操作対応UIでアセットコンソールに移動する際に、特定のアセットをアクティブ化する際に表示される例外があります。 NPR-15217:CQ-108779のホットフィックス
* プロキシサーバー経由の接続時にビデオをYouTubeに公開する。 NPR-15109:CQ-110332のホットフィックス
* 名前にピリオド(.)を含むアセットの使用 の値は、データを含まないリソースが同じアセットに解決されず、出力パスがドットで終了します。 NPR-15069：CQ-4195914 のホットフィックス
* AEM 6.2をService Pack1にアップグレードした後、アセットのScene7への同期に失敗します。 dam:Scene7ファイルステータスプロパティは、発行済みアセットでも&#39; `UploadFailed`&#39;ステータスを表示します。 NPR-15269：CQ-4197708 のホットフィックス

### ユーザーインターフェイス {#user-interface-5}

* **[!UICONTROL Touch UI]**&#x200B;では、Internet Chromeブラウザーバージョン56.0.2924.87を使用している場合、type=&#39;datetime&#39;を持たない日付フィールドには保存済みの日付が表示されません。NPR-15383:GRANITE-16481用修正プログラム
* **[!UICONTROL タッチUI]**&#x200B;では、リッチテキストエディターは、HTMLテーブルのレンダリング中にスレッドとキャプション要素をHTMLテーブルから削除します。 NPR-15267：CRTE-41 のホットフィックス
* `FileUpload Validator` は、autostartがtrueの場合や、が手動で呼び出され、このような場合に無効な検証レポートが生成さ `uploadFile()` れる場合には処理しません。NPR-15295：GRANITE-13499 のホットフィックス

* 場所の設定が&#x200B;*/libs/granite/omnisearch/content/metadata/*&#x200B;に一覧表示されると想定しているので、Omnisearchでは/appsを使用するお客様は列データソースを追加できません。 NPR-13188 GRANITE-16479用修正プログラム
* **[!UICONTROL タッチ操作対応UI]**&#x200B;を使用する場合、製品のバリアントは、製品と同じレベルで作成されません。 バリアント作成プロセスの状態はユーザーに通知されません。 NPR-15345:CQ-4198948のホットフィックス

**Scene7**

* Scene7ワークフローを実行すると、開いているファイルが閉じられません。 AEM-S7サービスを改善し、共有プーリング設定の単一のHttpClientインスタンスを維持して再利用できるようにする要求です。 NPR-15357:HotFix for CQ-109958

### 翻訳 {#translation-9}

* 翻訳プロジェクトを使用する場合、英語のマスターから言語コピーを更新すると、は11個の異なる起動を行い、すべて同じ名前とソースルートで起動しますが、ページ名が設定パターンに従う場合は、起動ルートがわずかに異なります。 NPR-15605：CQ-4200699 のホットフィックス
* 言語ルートの名前にハイフンやダッシュが含まれている場合、ページの翻訳プロジェクトは作成されません。 NPR-15171:CQ-96286のホットフィックス
* MicrosoftがAzureポータルで利用できるMicrosoft Translator APIを使用できるようにMicrosoftコネクタを更新するように要求します。 NPR-15320：CQ-101010 のホットフィックス

### プロジェクト {#projects-4}

* 20個を超える非アクティブなプロジェクトがリポジトリに存在しているにもかかわらず、プロジェクト画面に表示されるのは20個の非アクティブなプロジェクトのみです。 NPR-15656：CQ-4200903 のホットフィックス

### キャンペーン{#campaign-1}

* キャンペーン — ターゲット設定およびMAC — テストとターゲットの統合コンポーネントを使用している場合、アクティビティのパブリケーション解除によってマスターUIのアクティビティステータスが更新されない。 NPR-15401:CQ-4199839のホットフィックス
* AEMコマースで製品を移動する際、製品の移動ウィザードでは、製品名、タイトル、参照先ページ、作成者、作成日に対する事前入力済みの値が見つかりません。 NPR-15228：CQ-98617 のホットフィックス

### セキュリティ {#security-4}

* GETメソッドを使用してフォームに追加されたCSRFトークンパラメーター。 NPR-15229

### フォーム {#forms-18}

#### Forms アドオンパッケージ {#forms-add-on-package-18}

`**Adaptive Forms**`

* アダプティブフォームに入力XMLを事前に埋め込むと、デフォルト値はxml内の空の値によって上書きされます。 NPR-15721
* `afData/afBoundData`ラッパーは、送信済みXMLに存在します。ただし、事前入力XMLでも、XMLスキーマベースのアダプティブフォームでは`afData/afBoundData`ラッパーを持ちません。 NPR-15541

* アコーディオンバーのタイトルは、「a」タグではなく、HTMLの「h2」見出しで編集可能にする必要があります。 NPR-15475
* フォームパネルのアコーディオンレイアウトは、スクリーンリーダーユーザーはアクセスできません。 ユーザーは、JAWSやNVDAなどのスクリーンリーダーソフトウェアを使用して、キーボードだけでアコーディオンタブに移動することはできません。 NPR-15474

`**Correspondence Management**`

* ドキュメントフラグメントの参照の保存、削除、設定にかなりの時間がかかります。 NPR-15939
* CCR UIで、複数のヘッダーの区切りを含むテキストの「アセットを管理」で設定されたタブの整列。 NPR-15818
* テキストモジュールのサムネールには、Google Chromeのタブで作成された整列コンテンツが含まれていても、整列コンテンツは表示されません。 NPR-15819

`**Forms Portal**`

* 事前入力サービスは、XDPFormsでは機能しません。 NPR-15466
* アダプティブフォームのドラフトと送信をデータベースに保存する場合、何らかの理由（例えば、長い間無操作状態が続いた後など）でデータベース接続が失敗すると、アダプティブフォームの状態が破損します。 NPR-15297

#### Forms JEE インストーラー  {#forms-jee-installer-18}

`**Core**`

* 最新バージョンのJava 1.8.0_121-b13にアップグレードした後は、管理者ユーザーインターフェイスはAEM Formsでアクセスできません。 NPR-15330

`**XTG**`

* Outputサービスを使用して特定のフォームとdataxmlをマージする場合、応答時間は、ES4 SP1サーバーが同じ操作に費やした時間と比較して20倍になります。 NPR-15283

#### AEM Forms アプリケーション {#aem-forms-app-1}

* 未保存のタスクを回復する場合は、未保存のタスクの回復時に表示されるメッセージを明確にして、ユーザーエラーを減らす必要があります。 NPR-15377
* AEM Formsアプリは、カスタムテンプレートから作成されたフォームをレンダリングしません。 NPR-15892
* ユーザーは、AEM Formsアプリにログインできません。 NPR-15891

AEM 6.2 SP2-CFP1の主なハイライトは次のとおりです。

* サイトのレプリケーション機能を合理化：

   * ロールアウト、LiveCopy、書き込み障害の問題の修正

* 次の場合にタッチ操作対応UIの応答性が向上します。

   * アセットの検索
   * サイズベースの並べ替え

* スマートコレクションのタグ管理を強化
* フォルダに対するCRUD操作中のアクセス制御の厳密さ

### プラットフォーム {#previous}

* レプリケーションエージェントの起動中に`ReplicationQueue#forceRetry` API呼び出しを削除するように要求する。この呼び出しは、特に多数のレプリケーションエージェントを持つ場合に、インスタンスの速度を大幅に低下させるからです。 NPR-14032：GRANITE-13095 のホットフィックス
* `DurboImportConfigurationProviderService` OSGi設定に対して、値の配列を格納できるフィールドをサポートするよう要求します。 NPR-14570：CQ-108684 のホットフィックス
* AEM 6.2への移行後にページでSightlyコンポーネントを使用すると、ページのプロパティダイアログが動作を停止します。 NPR-14328：CQ-108355 のホットフィックス
* 以前にスケジュールされたジョブのスケジュールを解除しても、*/var/eventing/scheduled-jobs*&#x200B;の下の対応するノードは削除されません。 NPR-14253：SLING-5666 のホットフィックス。
* 管理者が削除されたユーザーとして動作しようとすると、ユーザーインターフェイスの更新に失敗します。 NPR-14247：CQ-107446 のホットフィックス
* XSS保護チェックを行うと、Sightlyコンポーネントで誤ったエンコードが発生する。 NPR-14004：CQ-93821 のホットフィックス
* 複数の問題を解決するために、Jackrabbit Filevaultを3.1.30にアップグレードするように要求します。 NPR-13454
* Sling配布で作成者から発行への配布パッケージが同期されると、キャッシュエラーが発生します。 NPR-13034：GRANITE-13970 のホットフィックス

### サイト{#sites-18}

* VersionManagerImplで、バージョン履歴から正しくないバージョンを削除するという問題が発生します。 NPR-14372
* WCM Sightly Foundation parsysコンポーネントは、コンポーネント宣言タグ名`cq:htmlTag / cq:tagName`を無視します。 NPR-14225
* Touch UIでJavaScriptを介して挿入されたコンポーネントをSightly Parsysを使用してレンダリングする場合、ページが更新された後、カスタムデコレーションは無視されます。 NPR-14122
* 複数のリッチテキストフィールド（リンクなど）が作成されている場合、タッチUIダイアログでターゲットドロップダウンリストは機能しません。 NPR-13911
* ダイアログ（タッチUI）で複数のリッチテキストエディター(RTE)プロパティを使用してテキストフィールドを編集する場合、フォーカスはランダムに特定のRTEプロパティに移動します。 NPR-13703
* 初期設定の初期設定のビデオコンポーネントは、ビデオサムネールをレンダリングしません。 NPR-14976
* 情報がテンプレートエディターの「ライブ使用状況」タブにゆっくり読み込まれる。 NPR-14880：CQ-83417 のホットフィックス
* AEM 6.2インスタンスにHotfix-10936をインストールすると、iparsysコンポーネントが無効になります。 NPR-14330：CQ-106982 のホットフィックス
* AEM 6.1 SP1への移行後、複数のロールアウトコンポーネントの問題とライブコピーの問題が発生する。 NPR-15256
* ページロールアウトアクションは、複数のロールアウト設定でも、最初のレベルを超える子の作成に失敗します。 NPR-15055
* エディターからPagePropertiesダイアログを送信する場合、LiveCopyタブ内の変更されていないデータが書き換えられます。 NPR-14693
* エディターからページプロパティダイアログが送信されると、MSMポストプロセッサーは、`msm:writeLiveCopyConfig`パラメーターの代わりに、リクエストから一部のパラメーターを書き込みます。 NPR-14434
* ロールアウトコンポーネント、ライブコピー、およびMSMのその他の側面に関する複数の問題 NPR-12235

### アセット{#assets-18}

* UnPackワークフローは、イメージファイル名に特殊文字を含むイメージを処理できません。 NPR-15227：CQ-103887 のホットフィックス
* 「条件を指定して繰り返し」式を持つアセットが正しく表示されません。 ユーザーが`*CDN3835RLCEN*`レターテンプレートをプレビューすると、Bodyターゲット領域にあるアセットは表示されません。 オプションのアセットである`*VIPReassement*`（事前選択）が選択されていない場合、事前選択されている他のアセットがレターに表示されます。 NPR-14844

* スマートコレクションの作成時に、スマートコレクションを保存する際にスタイルタグが保持されません。 NPR-15081：CQ-4195494 のホットフィックス
* 複数のユーザーによる同時検索中に、タッチ操作対応UIで動作が遅いアセット検索クエリ。 NPR-15019:Hotifx for CQ-4195405
* タイプ`Long[]`のプロパティに対して抽出されたメタデータは、元のアセットを別の場所に再アップロードすると、タイプ`String[]`に変換されます。 NPR-15016:CQ-4195005の修正プログラム

* 保存済みの検索またはスマートコレクションを削除できないユーザー。 NPR-14924：CQ-108494 のホットフィックス
* 基になるメタデータスキーマのドロップダウンフィールドでTypeHintのブール値を使用して、アセットのメタデータを一括（追加モード）で編集するとエラーが発生します。 NPR-14529：CQ-106876 のホットフィックス
* レプリケーション権限を持たないユーザーは、アセットフォルダーを削除できません。 NPR-14321：CQ-88271 のホットフィックス
* チャネルエディターでビデオのビデオプロファイルを編集しようとすると、デザインダイアログが開かず、エラーログでNull Pointer Exceptionが発生します。 NPR-14144：CQ-81101 のホットフィックス
* アセットのプロパティページに表示されるシステム生成の「作成済み」タイムスタンププロパティが正しくありません。 NPR-13992：CQ-95029 のホットフィックス
* AEM AssetsNPR-13851で、「読み取り」アクセスを持たないユーザーの重複アセットの検出を有効にする要求：CQ-102281用修正プログラム
* プロパティページからアセットのメタデータを一括して編集できない。 NPR-13721：CQ-100703 のホットフィックス
* 重複アセットがアップロードされたときに、クラシックUIに正しくないエラーメッセージが表示される。 エラーメッセージには、アップロードが失敗した理由が示されません。 NPR-13691：CQ-99272 のホットフィックス
* フォルダーに多数のアセットが含まれる場合、AEM Assetsはリスト表示で一度に50個を超えるアセットをサイズ別に並べ替えることができません。 CQ-100588
* 複数のアセットを選択すると、アセット/フォルダーのURIが長すぎる場合、応答コード — 414（要求 —URIが長すぎる）でエラーが発生します。 NPR-13516：CQ-76076 のホットフィックス
* 列の設定ダイアログですべての選択肢を選択すると、アセットレポートページが応答しなくなります。 NPR-13187：CQ-95589 のホットフィックス
* SafariおよびInternet Explorerでのタグ選択の予期しない動作。 NPR-13134
* アセット管理者の検索パネルで保存済みの検索を編集すると、保存した検索をネストされたスマート選択として保存できるので、環境の安定性に問題が生じます。 NPR-13119：CQ-99460 のホットフィックス
* ファイル（またはフォルダー）を移動してから名前を変更した後、&#39;cq:name&#39;メタデータには新しいファイル名（フォルダー名）が反映されません。 NPR-13036：CQ-99141 のホットフィックス
* 特殊文字を含む名前のアセットは、電子メールで共有されるダウンロードリンクからダウンロードできません。 NPR-12872：CQ-95795 のホットフィックス
* 大量のアセットが存在する場合に生成される、あらかじめ用意されたアセットレポートは、検索がインデックスやCPU使用率のスパイクにヒットしない場合に、大量のトラバルを引き起こします。 NPR-12811：CQ-84409 のホットフィックス
* AMSAEM Assets作成者インスタンスが異なるネットワークからアクセスした場合、フォルダの削除権限がないと、チャンクアップロードを使用してアセットをアップロードできません。 NPR-12768：CQ-82715 のホットフィックス
* アセット検索レールを使用したタグベースのアセット検索では、先読み入力機能では、自体がルートパスに制限されず、すべての名前空間のタグが表示されます。 NPR-12666
* StaticRenditionsコンポーネントはnullポインターの例外を発生させます。 NPR-12665
* バッジ通知UIで、「入力をスキャンできません」というランタイム例外が発生し、ページが区切られる原因となるので、MissingMetadataNotificationJobを無効にする要求です。 NPR-12500：CQ-93573 のホットフィックス
* タグフィールドの「編集を無効にする」オプションは、TouchUIのアセットプロパティページでは機能しません。 NPR-12429：CQ-88835 のホットフィックス
* Companion App SMB実装のAEM Assets6.2でのAPI修正。 NPR-11099
* Jqueryが更新されたので、ユーザーはアセットコレクションを選択できず、コンテンツフラグメントのコンテンツを関連付けパネルで選択を確認できません。 NPR-14847:CQ-4194209のバックポート
* クライアント側で無限の並べ替えを呼び出した場合でも、UIに現在表示されている記事/バナー/コレクションのみが並べ替えられます。 NPR-14493：CQ-109926 のホットフィックス
* AEM mobile-on-demandサービス用のOmnisearch機能の実装のリクエストです。 記事、コレクション、バナーのキーワード検索では一致は返されません。 NPR-14093：CQ-101394 のホットフィックス
* ダイアログでCoral-selectコンポーネント(*granite/ui/components/coral/foundation/form/select*)を使用する場合、選択された値に単一の項目が含まれると、Internet Explorer（IE11またはEdgeブラウザ）で値の初期化が正しく機能しません。 NPR-13395：CQ-101013 のホットフィックス

### プロジェクト {#projects-5}

* 翻訳メソッドを「人」、翻訳プロバイダーを「なし」として作成した翻訳プロジェクトを書き出す場合、GUIDマッピングファイルがないため、translation_export_summary.xmlファイルは生成されません。 NPR-13137：CQ-91976 のホットフィックス
* AEMプロジェクトでは、due-dateプロパティが設定されたプロジェクトを作成すると、サーバーとクライアントのタイムゾーンの違いが原因で、日付変換によって時間が正しく設定されません。 NPR-13003：CQ-98288 のホットフィックス
* 翻訳プロジェクトが更新されたときに、「サイトで表示」オプションが翻訳ジョブに含まれていません。 NPR-12966：CQ-93740 のホットフィックス
* 書き出したサイトページ用に翻訳プロジェクトを作成すると、プレビューでは正しくレンダリングされません。 NPR-12964：CQ-84627 のホットフィックス

### ワークフロー {#workflow-3}

* ワークフローコンソールの「アーカイブ」タブにあるペイロードリンクは、クリック時に応答コード「404」のエラーを返します。 NPR-14993：CQ-4194977 のホットフィックス
* AEMのデフォルトのワークフローを使用する場合、CQメーラーは、1人のメンバーの電子メールアドレスを見逃す電子メール通知をグループに送信できません。 NPR-14804：CQ-91499 のホットフィックス要求
* タッチ操作対応UIのインボックスと通知バッジのパフォーマンスが向上しました。 NPR-14145：CQ-101125 のホットフィックス
* ワークフローの開始中に、ワークフローのインボックスコンソールからペイロードをプレビューできません。 NPR-13226：CQ-100275 のホットフィックス
* SAML認証ハンドラーを使用して設定された「saml_request_path」 Cookieには、「?」が追加されたCookieセットが表示されます 文字. さらに、SAML応答がAEMにポストバックされると、AEM &#39;saml_request_path&#39; cookieは、既にエンコードされている文字のため無効な値を返します。 NPR-13517:GRANITE-11722およびGRANITE-14414用プロアクティブな修正プログラム

### ソリューションの統合{#solution-integration}

* AEM 6.2をSearch&amp;Promoteと統合した後、ユーザーがバナーを返す用語を検索すると、検索機能が応答しなくなります。 NPR-14549：CQ-109631 の CFP

### Dynamic Media {#dynamic-media}

* AEMアクティベーション中にレプリケーション中にアーカイブジョブとして記録された場合に作成および取り消されたAEM-Scene7スリングジョブが多数あります。 NPR-12835：CQ-86115 のホットフィックス

### セキュリティ {#security-5}

* WCMDebugフィルタの入力検証の問題を解決する要求です。 NPR-12444：CQ-94890 のホットフィックス要求
* 起動の作成ウィザードを使用中にXSSの動作を修正するためのプロアクティブなリクエスト。\
   NPR-13062：CQ-99577 のホットフィックス要求

#### Forms アドオンパッケージ {#forms-add-on-package-19}

`Adaptive Forms`

* アダプティブフォームを使用して繰り返し可能なパネルを作成する場合、パネルのタイトルを実行時に更新することはできません。 NPR-15325
* 保存または送信時にラジオボタンのデフォルト値が設定され、デフォルト値以外の値が選択された場合、その値は事前入力時に表示されません。 NPR-15304
* Google Chromeで、ドロップダウンリストの値を動的に埋め込んだり、選択した項目の値を送信したりするオプションイベントの使用に関して、誤った動作が表示されます。 NPR-15198
* アダプティブフォームを使用して繰り返し可能なパネルを作成する場合、パネルのタイトルを実行時に更新することはできません。 NPR-15181
* アダプティブフォームで編集モードを使用している場合、- 「コンポーネントのハンドラーが無効です」、&#39;guidelibが未定義です&#39;などのJavaScriptエラーが発生します。 NPR-15112
* 繰り返しパネル内の遅延読み込みフラグメントが期待どおりに機能しません。 NPR-13916、NPR-14785

`Correspondence Management`

* `'Repeat with condition'`式セットを持つCorrespondence Managementアセットが正しく表示されません。 NPR-14844
* Correspondence Managementアセット(レター、ドキュメントフラグメント、その他のタイプなど)を検索すると、ダウンロード用のキューアイコンがツールバーに表示されなくなります。 NPR-14745
* リストモジュールの作成時に、アセット固有のプロパティ（編集可能、必須など）の切り替えが動作しません。 NPR-14689
* データディクショナリを選択せずに条件式が作成された場合、モジュールビルダーユーティリティのデータ要素パネルは読み込みを続けます。 NPR-14688
* レターのプレビュー時に、タブスペースを使用してコンテンツを表形式で整列することはできません。 NPR-14481
* Correspondence Managementアセットをユーザーインターフェイスから一括で書き出す場合、AEM Formsサーバーは不要なログを生成します。 NPR-15226
* レターをプレビューすると、均等配置されたテキストは別のフォントで表示されます。 NPR-15468

`**Forms Portal**`

* Formsポータルで送信済みフォームの添付ファイルは、ポータルの送信から新しいドラフトが送信されると表示されません。 NPR-13515

`**Forms Manager**`

* *FormsandDocuments*&#x200B;ディレクトリ内で移動中、ユーザーがアセットをコピーしてから別のフォルダーに移動した場合、「貼り付け」ボタンは表示されません。 CQ-111327

#### Forms JEE インストーラー {#forms-jee-installer-19}

`Rights Management`

* ユーザーログイン関連の監査イベントに無効な時間が記録されます。 監査イベントの正しい時間は追跡できません。 NPR-13107
* Adobe AcrobatReaderとMicrosoft Officeは、拡張認証で保護されたドキュメントを開けません。 NPR-14482

`Process Management`

* HTML Workspaceで転送されたドラフトタスクが最初のユーザーに返されると、そのタスクは最初のユーザーのキューに表示されません。 NPR-15178

`Assembler Service`

* AEM Formsで、3つ以上の署名があるPDF/A-2bの検証に失敗した。 NPR-14101

`XTG`

* プリンターバイパストレイを使用してドキュメントを印刷する場合、`GeneratePrintedOutput`機能は右側のバイパストレイから用紙を取り込むことを許可しません。 NPR-14079

#### Forms - Designer {#forms-designer-2}

* 選択したフォームロケールをフランス語（カナダ）に設定してスペルチェックユーティリティを実行すると、FormsDesignerがクラッシュする。 NPR-13740
* ユーザーがフォームフィールドのイベントの計算またはイベントの検証を選択し、その言語をJavaScriptに変更して&#x200B;**[!UICONTROL スクリプトエディター]**&#x200B;ウィンドウに`this.`を入力すると、Formsデザイナーがクラッシュします。 NPR-12974

### CFP1に含まれる機能パック{#feature-packs-included-in-cfp-3}

`Mobile Forms` (追加Formsオンパッケージ):

* XDPファイルからアダプティブフォームを作成した場合、アクセシビリティ用のタブ順序は設定パターンに従いません。 NPR-12562

`Adaptive forms` (追加Formsオンパッケージ):

* アダプティブフォームのルールビルダーでは、ロールベースのアクセスは提供されません。 作成者が行った変更は追跡できません。 NPR-12840

`Core` (Forms JEE インストーラー):

* サーブレットフィルターとしてのコアクロス接触チャネルリソース共有(CORS)機能は、Jboss+では有効になっていません。 NPR-13050

## ソフトウェア配布によるCFPのダウンロード手順{#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>AEM Formsのお客様には、AEM Service Pack、Cumulative Service Pack、または機能パックをインストールした後に、AEM Formsアドオンパッケージをインストールすることが不可欠です。

CFPパッケージは、ソフトウェア配布から直接ダウンロードするか、次の手順を実行できます。

1. [ソフトウェア配布](https://experience.adobe.com/downloads)を開きます。 ソフトウェアディストリビューションにログインするには、Adobe ID が必要です。
1. ヘッダーメニューにある&#x200B;**[!UICONTROL Adobe Experience Manager]**&#x200B;をタップします。
1. パッケージ名をタップし、「**[!UICONTROL EULA条項に同意]**」を選択して、「**[!UICONTROL ダウンロード]**」をタップします。

## CFP {#installation-instructions-for-cfp}のインストール手順

このセクションでは、CFP をインストールするための要件と手順について説明します。

### インストールの前に  {#before-you-install}

>[!NOTE]
>
>アドビが提供するオプションの機能パックは、リリースのバージョンと累積修正パックに依存関係があります。機能パックがインストールされている場合は、[AEM サポートチーム](https://helpx.adobe.com/jp/marketing-cloud/contact-support.html)に連絡し、AEM 6.2 用のこの累積修正パックとの互換性を検証してください。

>[!NOTE]
>
>パッケージをインストールする前に、新しいインストールパッケージごとに検証を実行することをお勧めします。事前検証では、インストール前に検出されたエラーを分析し、報告し、エラー、オーバーレイ、権限を事前にユーザーに通知します。
>
>「検証」オプションのドキュメントは、[https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/package-manager.html#Package%20Validator)から入手できます。

* AEM 6.2 Service Pack 1はCFPの前提条件です。 インストール手順については、[AEM 6.2 サービスパック 1 リリースノート](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)を参照してください。

* 累積Fix Packのダウンロードは、AEMインスタンスから直接アクセスできる[ソフトウェア配布](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20)で入手できます。
* （RDBMKまたはMongoDB）を使用したクラスターデプロイメントの場合、CFPパッケージは、Package Managerを使用する任意の作成者インスタンスにインストールできます。

* 累積修正パックをインストールする前に、必ず AEM インスタンスのスナップショットを作成するか、バックアップを作成してください。
* CFP のアンインストールはサポートされていません。

### ソフトウェア配布によるCFPのインストール{#install-the-cfp-via-package-share}

既存のAEM 6.2 SP1インスタンスにCumulative Fix Packをインストールするには、次の手順を実行します。

1. [「ソフトウェアの配布」](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip)リンクをクリックして、パッケージをダウンロードします。

1. [Package Manager](http://localhost:4502/crx/packmgr/index.jsp)を開き、「**[!UICONTROL パッケージをアップロード]**」をクリックして、パッケージをアップロードします。

1. パッケージ名を選択し、「**[!UICONTROL インストール]**」をクリックします。

### 自動インストール {#automatic-installation}

CFP は、次の方法で実行中のインスタンスに自動インストールできます。

* サーバーの実行中に、パッケージを。./crx-quickstart/installに配置します。 パッケージは自動的にインストールされます。
* Package Manager](https://helpx.adobe.com/jp/experience-manager/6-2/sites/administering/using/package-manager.html)の[HTTP APIを使用します。`cmd=install&recursive=true`を使用していることを確認し、ネストされたパッケージをインストールします。

### インストールの検証 {#validate-installation}

1. 製品情報ページ(/system/console/ productinfo )の「Installed Products」に、更新されたバージョン文字列「Adobe Experience Manager、バージョン6.2.0.SP1-CFP20」が表示されるようになりました。
1. すべての OSGI バンドルは、OSGI コンソール（Web コンソールを使用：/system/console/bundles）で ACTIVE または FRAGMENT です。

>[!NOTE]
>
>パッケージが正常にインストールされると、「Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 installed successfully.」など、コンテンツパッケージが正常にインストールされたことを示す情報メッセージが表示されます。

>[!NOTE]
>
>AEM 6.2 SP1-CFP1以降、Jackrabbit FileVaultのログレベルは、ほとんどのメッセージでINFOからDEBUGに変更されました。 AEM 6.2 SP1-CFP1以上にインストールされたコンテンツパッケージのインストールログを取得するには、`org.apache.jackrabbit.vault.packaging.impl`のDEBUGログレベルを有効にします。

### AEM Forms のインストール {#install-forms}

>[!NOTE]
>
>AEM Forms を使用していない場合は、このセクションをスキップしてください。

#### AEM Forms アドオンのインストール  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**JEE上のAEM Formsのみ**)JEE上のAEM FormsにCFPをインストールする手順は、[AEM FormsJEE上のCFPのインストール](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee)で説明しています。

1. AEM 6.2 SP1 CFPパッケージがインストールされていることを確認します。
1. [AEM Formsリリース](aem-forms-releases.md)に記載されている、お使いのオペレーティングシステム用の対応するFormsアドオンパッケージをダウンロードしてください。
1. [AEM formsアドオンパッケージのインストール](https://helpx.adobe.com/jp/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html)の説明に従って、Formsアドオンパッケージをインストールします。

#### AEM Forms JEE バンドルパッケージのインストール {#install-aem-forms-jee-bundles-package}

AEM Forms JEE の修正は別のインストーラーを介して配布されます。JEE の AEM Forms に CFP をインストールする方法については、[AEM Forms JEE への CFP のインストール](install-cfp-aem-forms-jee.md)を参照してください。

#### Forms Designer インストーラー  {#designer-installer}

1. 更新プログラムをインストールするには、Designer6.2.0_&lt;Language>_Cumulative_QF.mspファイルを実行します。
1. ようこそ画面で「**次へ**」をクリックします。インストールが開始されます。
1. インストールが完了したら、「**完了**」をクリックします。

## DTM、Analytics、ターゲット、Search &amp; Promote接続用のユーザーが設定できるタイムアウトパラメーター{#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

AEMの累積Fix Pack 6.2 SP1-CFP7以降のリリースでは、次の詳細に従って、上記のすべての接続で接続のタイムアウト期間を設定できるようになりました。

| **接続** | **接続タイムアウト*** | **ソケットタイムアウト**** |
|---|---|---|
| DTM | 30000 ms | 30000 ms |
| 分析 | 30000 ms | 30000 ms |
| ターゲット | 60000 ms | 30000 ms |
| Search&amp;Promote | 30000 ms | 30000 ms |

* **接続タイムアウト*** — 接続が確立されるまでのタイムアウト（ミリ秒）。タイムアウト値が0の場合は、無限タイムアウトと解釈されます。
* **ソケットタイムアウト**** — データを待機する時間（ミリ秒）、または2つの連続するデータパケットの間に無操作状態が最大限に発生する時間（ミリ秒）。

>[!NOTE]
>
>AEMの累積Fix Pack 6.2 SP1-CFP6以降のリリースでは、Search &amp; Promote統合に使用されるOSGi設定はApache HTTP Components Proxy Configurationです。 Day Commons HTTP Client 3.1 のプロキシ設定は使用されなくなりました。

## タグ付けコンソール（クラシックUI）のレプリケーション状態を無効にする(NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

CFP3以降を使用している場合は、次の手順に従ってクラシックUIのタグ付けコンソールで複製ステータスを無効にします。

* *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;*&#x200B;を&#x200B;*/apps*&#x200B;にオーバーレイ

* 追加`replicationStateRequired`:行#416の後に「false」が追加されました。

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## 最新のJava 8 Update 131は例外(NPR-21355) {#latest-java-update-throws-an-exception-npr}をスロー

>[!NOTE]
>
>これらの設定は、ドキュメントセキュリティを使用するAEM Formsのお客様専用です。

NPR-21355はCFP12.1に含まれています。CFP12.1以降をインストールする場合は、次の手順を実行してJBossアプリケーションサーバー上でNPR-21355を設定します。 oracleWebLogicまたはIBM WebSphereアプリケーションサーバー上で実行しているAEM FormsサーバーにCFP12.1をインストールする場合は、次の追加設定は不要です。

1. 新しいmodule.xmlファイルをバックアップ、削除および作成します。 ファイルのデフォルトの場所は[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/です。

1. 新しく作成したmodule.xmlファイルを開いて編集します。 次のコードを ファイルに追加します。

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/にあるjsafeFIPS.jar、jsafeJCEFIPS.jar、certjFIPS.jarファイルのバックアップを作成し、前述のディレクトリからファイルを削除します。

   [Adobeサポート](https://helpx.adobe.com/marketing-cloud/contact-support.html)に問い合わせて、新しいJARファイルを取得します。 [Adobeサポート](https://helpx.adobe.com/marketing-cloud/contact-support.html)から取得したJARファイルを[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/に配置します。

1. （Windowsのみ）`[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat`または`domain.conf.bat`構成ファイルを変更します。

   * スタンドアロン設定のJBossサーバーの場合は、standalone.conf.batを開いて編集します。
   * クラスター設定のJBossサーバーの場合は、domain.conf.batを開いて編集します。

   最後追加に次の行があり、ファイルを保存します。

   &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;を設定します。

   &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;を設定します。

1. （LinuxベースのOSのみ）[AEM_Forms_Installation_directory]/jboss/standalone.confまたはdomain.confの構成ファイルを変更します。

   * スタンドアロン設定のJBossサーバーの場合は、standalone.confを開いて編集します。
   * クラスター設定のJBossサーバーの場合、domain.confを開いて編集します。

   最後追加に次の行があり、ファイルを保存します。

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## NPR-19778 に必要な設定 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778はCFP14の一部です。

共有キューの数は、デフォルトでは、ユーザーがタスクを要求したときに他のユーザーに対して更新されません。 このため、新しいプロパティを導入しました。 次の手順に従って、AEMインスタンスでこのプロパティを設定します。

1. 管理UI/サービス/Workspace/グローバル管理に移動します。
1. グローバル設定を書き出し
1. ダウンロードしたXMLファイルに`<client_tasksPollingInterval>10</client_tasksPollingInterval>`タグを追加します。ここでは、10が秒単位のサンプル値です。 適宜変更できます。
1.  ファイルを保存します。
1. 管理UI/サービス/Workspace/グローバル管理に戻ります。
1. 「グローバル設定を読み込み」セクションでxmlファイルを読み込みます。
1. これで、システムからログアウトして、再びログインできます。
1. ワークスペース内の他の開始が更新する共有キューユーザーの数です。
1. ポーリングをオフにするには、値を0に変更し、XMLファイルを再度読み込みます。

## UIの変更{#ui-changes}

* dcを持つ画像の画像カード上のタイトルの表示に関する動作の変更：titleプロパティが文字列[] ( multifield )に設定されました：UIのイメージカードには、最新の変更されたタイトルのみが表示されますが、すべてのタイトルはCRXに保存されます。 CQ-4217165 のホットフィックス

## 既知の問題 {#known-issues}

* AEM 6.2SP1-CFP19とAEM 6.2SP1-CFP20をCFP18からアップデートすると、/sites.html/contentではなく、Classic UIのようこそページにルートリダイレクトが変更されます。 スリングの修正が必要になる場合があります。/welcome.htmlから/index.htmlへのターゲットプロパティ（CRX Explorerを使用） この問題は、CFP 17以前のバージョンからのアップデートでは発生しません。

AEM 6.2 SP1-CFPxをインストールすると、次の一時的なエラーが発生する場合があります。 ただし、これらのエラーはAEMインスタンスに影響を与えず、CFPのインストール後に消えるので、これらのエラーの解決は必要ありません。

* AEM 6.2SP1-CFP20インスタンスをAEM 6.5にアップグレードすると、次のようなバニティURLが機能しない場合があります。

   * */projects.html*
   * */sites.html*

ただし、回避策として、アップグレード後にAEMインスタンスを再起動します。

* Webconsoleコンポーネントの詳細ページが開かれたときにHTTP 500内部サーバエラーが発生する。
* **コンポーネントインスタンス**&#x200B;および&#x200B;**サービスファクトリがNULL**&#x200B;を返しましたが、リポジトリの再起動が原因で発生しました：

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)]参照profileManagerのバインドに失敗したため、コンポーネントインスタンスを作成できません
   * org.apache.sling.commons.スケジューラーFrameworkEvent ERROR (org.osgi.framework.ServiceException:サービスファクトリがNULLを返しました。 (コンポーネント：com.day.cq.taging.impl.TagGarbageCollector (1687))

* MongoとDB2のCFPインストールでエラーが発生する：**org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry:例外：java.lang.NullPointerException**. このエラーは、CFP 8上でCFPをインストールした後は発生しません。
* (AdobeGraniteメンテナンススケジューラーの更新タスク)com.adobe.granite.maintenance.impl.TaskScheduler:WorkflowPurgeTaskという名前のWorkflowPurgeTaskという名前のメンテナンスタスクが見つかりませんでした(window granite:weekly)
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* スマートタグ機能パックを含むAEM 6.2 SP1にCFPxをインストールすると、以前に追加したスマートタグアセットのワークフロー手順がDAM Update Assetワークフローから削除されます。

AEM 6.2 SP1[の既知の問題のリスト(https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known既知の問題)を参照してください。]

## Uber Jar {#uber-jar}

6.2 SP1-CFP20用のUber Jarは、[AdobeパブリックMavenリポジトリ](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/)で入手できます。

Maven プロジェクトで Uber Jar を使用するには、プロジェクト POM に次の依存関係を追加します。

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## {#osgi-bundles-and-content-packages-included-5}に含まれるOSGIバンドルとコンテンツパッケージ

次のテキストドキュメントには、CFPに含まれるOSGIバンドルとコンテンツパッケージのリストが示されています。

* [AEM 6.2 SP1-CFP20に含まれるOSGiバンドルのリスト](assets/do-not-localize/updated.txt)
* [AEM 6.2SP1-CFP20に含まれるコンテンツパッケージのリスト](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 ホットフィックスページ](https://helpx.adobe.com/jp/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1リリースノート](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2 リリースノート](https://docs.adobe.com/docs/ja/aem/6-2/release-notes.html)
>* [AEM 製品ページ](http://www.adobe.com/jp/solutions/web-experience-management.html)
>* [AEM 6.2 ドキュメント](https://helpx.adobe.com/jp/support/experience-manager/6-2.html)
>* [](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) Subscribeto [Adobeの優先度製品の更新](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

