---
title: AEM 6.2 累積修正パック
description: AEM 6.2 累積修正パックのリリースノートの詳細をご覧ください。
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '21082'
ht-degree: 72%

---

# AEM 6.2 累積修正パックのリリースノート{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived by way of UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## リリース情報 {#release-information}

| **製品** | Adobe Experience Manager |
|---|---|
| **バージョン** | 6.2 |
| **リリース** | 累積修正パック 6.2 SP1-CFP20 |
| **前提条件** | [AEM 6.2 サービスパック 1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **一般リリース** | 2019年6月6日（PT） |

### 累積修正パック     {#cumulative-fix-pack}

アドビは、複数の修正を一度にリリースする配信モデルを導入しました。アドビでは、個々の問題に対するホットフィックスをリリースする代わりに、毎月累積修正パック（CFP）をリリースしています（品質チェックに合格することを条件とします）。CFP は複数の修正を集約したコンテンツパッケージです。CFP には主にバグ修正が含まれていますが、機能パックも含まれる場合があります。CFP には、個別のホットフィックスリリースに比べて次の利点があります。

* 累積的な性質（例えば、ある CFP には以前の CFP で提供された修正が含まれています）
* 品質保証の向上
* インストールの単純化（最新のサービスパック以外の依存関係がない単一パッケージとして CFP をインストールします）。

CFP および他のタイプのリリースの詳細については、[メンテナンスリリースの提供](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)を参照してください。

## リリースについて {#about-the-release}

AEM 累積修正パック 6.2 SP1-CFP20 は、AEM 6.2 用の最後の累積修正パックで、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

>[!CAUTION]
>
>インストールされた機能パック間の互換性を検証せずに CFP を適用すると、システム障害またはカスタム設定の損失が発生する可能性があり、解決するためにバックアップからの復元が必要になる場合があります。

>[!NOTE]
>
>* AEM 累積修正パック 6.2 SP1-CFP10 には、新しい Sling `discovery- api` バンドル Johnzon 1.0.0 が含まれています。さらに、サービスユーザー sling-discovery には、CRX リポジトリーのノード */var/discovery* に対する読み取りおよび書き込み権限が追加されています。
>
>* Apache Commons のメールバンドル **org.apache.commons/commons-email/1.5** が追加され、**com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002** を置き換えます。
>
>* アドビでは、AEM インスタンス上のユーザーが多いお客様には、インストールフォルダーを通じて CFP をデプロイすることをお勧めします。
>

## 含まれる問題 {#issues-included}

このセクションでは、現在の CFP に含まれるすべての問題とホットフィックスについて説明します。

さらに、この CFP には、[以前の累積修正パック](#previous)で配信されたホットフィックスも含まれています。

### 統合 {#integration}

* 複数の Campaign ターゲティングのパーソナライゼーションの改善をバックポート。NPR-29163：CQ-4264126 のホットフィックス
* com.day.cq.personalization.impl.TeaserResourceEventHandler が無限ループに入り、パブリッシュインスタンスのノードをアップデートする原因になります。NPR-28561：CQ-4263096 のホットフィックス

### DAM - 一般 {#dam-general}

* 特定の Dam フォルダーの管理者以外のユーザーに対して、レプリケーションボタンを表示／非表示にできません。NPR-29026：CQ-4265361 のホットフィックス

### 脆弱性 {#vulnerability}

* CSRF 対策フレームワークがAEMの基盤フォームで機能しない。 NPR-28612：Granite-22231 のホットフィックス

### Forms {#forms}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package}

>[!NOTE]
>
>AEM Formsのお客様は、AEM サービスパック、累積修正パック、機能パックのいずれかをインストールした後で、AEM Forms アドオンパッケージをインストールする必要があります。

>[!NOTE]
>
>AEM Forms アドオンパッケージは、AEM サービスパックおよび累積修正パックとのフォーム機能の整合性を確保するために役立ちます。このため、何らかの AEM サービスパック、累積修正パックまたは機能パックをインストールした後で、AEM Forms アドオンパッケージをインストールすることが不可欠です。

#### アダプティブフォーム {#adaptive-forms}

* iOS 12.1 デバイス用の手書きメモコンポーネントの使い勝手の問題。NPR-29082：CQ-4261765 のホットフィックス

#### Forms - Document Security {#forms-document-security}

* PAdES（PDF Advanced Electronic Signatures）を使用して PDF のすべての署名を検証すると、InvalidOperationException がスローされます。NPR-27848：CQ-4244837 のホットフィックス

#### Forms - 通信 {#forms-correspondence}

* レターをPDFとしてプレビューする場合、プライマリページに配置されたテキストフィールドは、「データ」タブまたは指定されたデータリンケージに従って入力された値を受け入れません。 NPR-29239：CQ-4266856 のホットフィックス。

#### Forms - インタラクティブコミュニケーション {#forms-interactive-communication}

* アポストロフィを追加すると、レター内の事前入力されたフィールドは、通常のアルファベットではなく、ASCII 文字で表示されます。NPR-28863：CQ-4262900 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer}

* AEM Forms JEE インストーラーには、新しい修正はありません。

## 以前の累積修正パックに含まれていたホットフィックスと機能パック {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### 累積修正パック 19 {#cumulative-fix-pack-1}

AEM 累積修正パック 6.2 SP1-CFP19 は、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* MS® Translator API v3.0 の AEM 6.2 へのサポートを有効化しました。
* すべての SP、CFP、HF 用のパッケージが正常にインストールされた後、ログメッセージが追加されます。

### アセット {#assets}

* 権限の編集 ACL がない場合は、DAM フォルダーの名前を変更できません。 NPR-27555：CQ-104652 のホットフィックス
* 6.2.1 CFP 17 以降で、画像プリセットエディターツールが応答しない。 NPR-28147：CQ-4261041 のホットフィックス

### Sites {#sites}

* リンクチェッカーはジョブを完了せず、応答のないリンクで停止します。NPR-27373：CQ-4256030 のホットフィックス
* 追加のルートパスがセグメントのパスを壊すことが原因で、セグメントファイルが正しく読み込まれません。NPR-28014：CQ-4260332 のホットフィックス

### 統合 {#integration-1}

* ライブコピー継承のキャンセルが、対象コンテナで正しく機能しません。NPR-28129：CQ-4259813 のホットフィックス
* `cq:actions` が対象のコンポーネントに対して考慮されません。NPR-27616：CQ-4257497 のホットフィックス

* 継承を解除するためのアイコンの表示は一貫していません。 NPR-27671：CQ-4257779 のホットフィックス

### Felix {#felix}

* AEM 6.2 SP1 インスタンスに CFP 18 をインストールした後、Web コンソールコンポーネントの詳細が 500 で失敗します。NPR-28350：CQ-4261095 のホットフィックス

### 翻訳 {#translation}

* MS® Translator を API v3.0 にアップグレードした後、AEM 6.3 で MS® Translator サービスのサポートを有効化します。NPR-28123：CQ-4259096 のホットフィックス

### UI - 基盤 {#ui-foundation}

* OOTB Sites カレンダーに正しくない日付が表示されます。NPR-28392

### Granite {#granite}

* `sling:basename` を使用するリソースバンドルの辞書が無効になりません。NPR-27624

### 維持 {#sustenance}

* パッケージマネージャーのアクティビティログは、別のログファイルに抽出する必要があります。NPR-27323：Granite-14866 のホットフィックス
* インストールが完了したときに表示される error.log 内のフレーズ／単語／ログ行を標準化しました。NPR-27835
* Granite パッケージプラグインは、org.apache.sling.i18n の下位バージョンの依存関係を選択しています。 CQ-4263245 のホットフィックス
* 6.2SP1-CFP15 以降の最新の CFP をインストールすると、com.adobe.cq.com.adobe.cq.ui.commons バンドルが削除されます。CQ-4258808 のホットフィックス

### Forms {#forms-1}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-1}

#### アダプティブフォーム {#adaptive-forms-1}

* AEM Forms の XML インジェクションの脆弱性。NPR-27843：CQ-4257315 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-1}

* AEM Forms JEE インストーラーには、新しい修正はありません。

### 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included}

次のドキュメントには、CFP に含まれている OSGi バンドルとコンテンツパッケージの一覧が記載されています。

AEM 6.2 SP1-CFP19 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2 SP1-CFP19 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/cfp19_content_packages.txt)

### 累積修正パック 18 {#cumulative-fix-pack-2}

AEM 累積修正パック 6.2 SP1-CFP18 は、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* DAM CommandLineProcess で、長時間実行中のプロセスを停止するサポートを追加しました。
* ReplicationEventListener でのセッションリークを修正しました。
* コアページコンポーネントにリダイレクトのサポートを追加しました。

### アセット {#assets-1}

* 大量の取り込みが行われる間に `Camera RAW` プロセスが停止し、最終的にすべてのワークフロー処理がブロックされます。NPR-26990：NPR-23860 のホットフィックス
* このダウンロード機能では、匿名ユーザーがすべてのアセットをダウンロードできるアセットダウンロードサーブレットとしてAEM Assetsを使用します。 NPR-27054：CQ-4254732 のホットフィックス
* AEM のメールテンプレートの件名行に、特殊文字が壊れて表示されます。NPR-26470：CQ-4252368 のホットフィックス

### Sites {#sites-1}

* ConfigPostProcessor クラスの不正な動作により、親画像を中断すると、子ページから `cq:LiveRelationship` 混合タイプが削除されます。NPR-26745：CQ-4254163 のホットフィックス
* コアページコンポーネントにリダイレクトのサポートを追加しました。 NPR-26576：CQ-110529 のホットフィックス
* ContextHub を `jQuery` 3 に移行しました。NPR-26956：CQ-4255472 のホットフィックス
* アンカー入力フィールドは、ダイアログボックス上のブラウザーの表示セクションの外に、最大化されるまで表示されます。NPR-26852：CQ-4255019 のホットフィックス
* 不要なテキストを挿入してテキストをコピーペースト &lt;br> コンテンツフラグメントで定義します。 NPR-26660：CRTE-151 のホットフィックス
* クラシックサイト管理で、一部のページの右側のパネルにリストがレンダリングされない。 NPR-27247：CQ-4251621 のホットフィックス
* （クラシック UI）ページの移動／名前変更を試みると、「ページの移動中にエラーが発生しました」というエラーが発生します。NPR-27179：CQ-4235907 のホットフィックス

### 統合 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever が、使用可能なブランドを収集するために、ツリー全体を調べます。NPR-27060：CQ-4255790 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components}

* 基盤リストコンポーネントに関する検索機能の問題。NPR-26817：CQ-4250324 のホットフィックス

### Platform {#platform}

* 特殊文字 em dash により、パブリッシャーでキャッシュのフラッシュに関する問題が発生しています。 NPR-27199：CQ-4242790 のホットフィックス

### Granite {#granite-1}

* パッケージ検証ツールが、CFP/SP に含まれるパッケージを検証しません。NPR-26775：Granite-22825 のホットフィックス

### レプリケーション {#replication}

* ReplicationListener での JCR セッションリーク。NPR-27063：CQ-4232088 のホットフィックス

### Forms {#forms-2}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-2}

* AEM Forms アドオンパッケージには、新しい修正はありません。

### Forms JEE インストーラー {#forms-jee-installer-2}

* AEM Forms JEE インストーラーには、新しい修正はありません。

#### 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included-1}

AEM 6.2 SP1-CFP18 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### 累積修正パック 17 {#cumulative-fix-pack-3}

AEM 累積修正パック 6.2 SP1-CFP17 は、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* At-integration.js でサイト拡張なし URL のサポートを追加しました。
* S7 ポーリングインポーターを S7 クラウドサービス設定から削除しました。
* マルチテナント実装のフォルダー構造をサポートするように、オーディエンス表示を変更しました。
* jqueryui clientlib v1.12.1 に更新しました。

### アセット {#assets-2}

* アセット UI からワークフローを開始するには、ユーザーに書き込み／削除／変更権限が必要です。NPR-25688：CQ-4250140 のホットフィックス
* 「公開」ボタンと「非公開」ボタンは、「複製」権限を持たないユーザーでも表示されます。NPR-25094
* （ワークフロー）スマートタグアセットワークフローは、AEM プロキシ設定を通じて処理されません。NPR-25915：CQ-4248202 のホットフィックス
* S7 クラウドサービス設定から S7 ポーリングインポーターを削除しました。NPR-25239：CQ-95236 のホットフィックス

### Sites {#sites-2}

* エディター／ページ情報から開始したワークフローに、ペイロード内のコンテキストパスが含まれます。NPR-26389：CQ-76804 のホットフィックス
* （外部リンクチェッカー）無効な https リンクが有効なリンクとして表示されます。NPR-25541：CQ-4201333 のホットフィックス
* （クラシック UI）ライブコピーの下にスタンドアロンページを作成する場合、そのページはライブコピーとして作成されます。NPR-25610：CQ-4249801 のホットフィックス
* ページがアクティブ化されたときにデザインインポーターコンポーネントに関連付けられたリソースを公開する際の問題。NPR-25638：CQ-102532 のホットフィックス
* RTE リッチテキストエディターツールバーが選択リストをカバーしています。 NPR-25165：CQ-4248948 のホットフィックス
* ContextHub を jQuery 3 に移行しました。NPR-25059：Granite-19902 のホットフィックス
* ネストされた Parsys コンポーネントの場合、デザインを満たす最初の（ネストされたパスが最も少ない）部分が、複数の使用可能なコンポーネントから常に適用されます。詳しくは、[デザインパスの解決](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)を参照してください。NPR-25250：CQ-4246276 のホットフィックス

### 統合 {#integration-3}

* OOTB Target 統合を使用して、コンポーネントをターゲット設定すると、空のターゲットコンポーネントではなく、ページ全体がレンダリングされます。 NPR-25273：CQ-4248003 のホットフィックス
* ターゲティングモードで、継承を無効にしても、編集モードでターゲットコンポーネントの継承が有効であると示されます。NPR-25324：CQ-4248162 のホットフィックス
* ページでパーソナライゼーションが定義され、オーディエンスが解決されると、対応するエクスペリエンスが編集モードで表示されます。NPR-25731：CQ-4249465 のホットフィックス
* デフォルト以外のコンテキストパスで AEM を使用した場合に、誤ったティーザー URL が表示されます。NPR-25971：CQ-4250953 のホットフィックス
* オプトアウトを使用した場合の空白のレンダリング。NPR-25295：CQ-4246792 のホットフィックス
* オーサー環境から削除されたエクスペリエンスが、ページのアクティベーション時に公開済みサイトから削除されません。NPR-24869：CQ-4247832 のホットフィックス

### DAM - DM クライアント {#dam-dm-client}

* （Chrome、Firefox）VideoPlayer では、タッチ操作対応デバイスで行ったマウスクリックが無視されます。CQ-4247370 のホットフィックス

### Platform {#platform-1}

* パッケージの取得／解放時に最大再試行数を設定できるようにしました。NPR-25328：Granite-22376 のホットフィックス
* レプリケーションエラーが発生した場合のログが間違っています。NPR-25308：CQ-4249402 のホットフィックス
* Forms AEM 6.2 Forms CFP8 を CFP14 にインストールすると、Apache POI が失敗します。NPR-25053：Granite-21771 のホットフィックス

### Granite {#granite-2}

* OakConstraint0022 例外が発生し、ユーザー同期プロセスが失敗します。NPR-25729：Oak-7428 のホットフィックス

### Communities {#communities}

* cq-social-as-provider バンドルが Mongo ドライバー 3.x バージョンで開始されない。 NPR-26271：CQ-4252710 のホットフィックス

### UI - 基盤 {#ui-foundation-1}

* jqueryui clientlib v1.12.1 に更新しました。NPR-25090：Granite-21981、CQ-4248897 のホットフィックス

* （オムニサーチ）：Sites の「Title」プロパティが、クロスサイト（XSS）スクリプティングに対して脆弱です。NPR-24994：Granite-19933 のホットフィックス

### Forms {#forms-3}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-3}

#### アダプティブフォーム {#adaptive-forms-2}

* アダプティブフォームからデータを送信中に間違ったエンコーディングが発生する。 NPR-25539

#### Forms - 管理 {#forms-management}

* ページの公開時に関連のないフォームアセットがリファレンスとして報告されます。NPR-26167：CQ-4251004 のホットフィックス

### Forms - JEE インストーラー {#forms-jee-installer-3}

#### Document Security {#document-security}

* 変数はデータタイプ List として入力され、サブタイプは文字列ですが、「オブジェクトを強制できません」エラーが発生します。 NPR-26194：CQ-4252287 のホットフィックス
* 6.2-SP1-CFP15 のインストール後、透かしの設定にアクセスできません。NPR-26130：CQ-4250984 のホットフィックス

### 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included-2}

AEM 6.2 SP1-CFP17 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2 SP1-CFP17 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### 累積修正パック 16 {#cumulative-fix-pack-4}

AEM 累積修正パック 6.2 SP1-CFP16 は、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* Day CQ メールサービスに STARTTLS サポートを追加しました。
* プロファイルポップオーバーでの ContextHub アイコンの位置揃えを修正しました。
* ドロップダウンコンポーネントの表示／非表示機能を修正しました。
* 最新の Jackson バージョン 2.8.11 にアップグレード

### アセット {#assets-3}

* リスト表示からワークフローを開始できない。NPR-24393：CQ-4245788 のホットフィックス
* （Firefox／Chrome）アセット共有ページでアセットをダウンロードできない。NPR-24523：CQ-4224408 のホットフィックス
* AEM のビデオプレビューのデフォルト画質を向上。NPR-24148：CQ-4244310 のホットフィックス

### 統合 {#integration-4}

* コンポーネントがパブリッシュインスタンスをターゲットにすると、ターゲットに設定されたエクスペリエンスより前にデフォルトのエクスペリエンスがちらつきで表示されます。NPR-23992：CQ-4242038 のホットフィックス
* オーサー環境から削除されたエクスペリエンスが、ページのアクティベーション時に公開済みサイトから削除されません。NPR-24869：CQ-4247832 のホットフィックス

### Platform {#platform-2}

* clientlib から jQuery 1.12.4 にパッチを適用して、セキュリティ修正を含めます。NPR-24129：Granite-20058 のホットフィックス
* Day CQ メールサービスに STARTTLS サポートを追加しました。NPR-23941：CQ-4240397 のホットフィックス
* デフォルトの MERGE_PRESERVE aclHandling を削除。NPR-24593：Granite-21889 のホットフィックス
* リクエストに無効なクエリパラメーターが含まれている場合、LineChecker がリンクの外部化に失敗します。 NPR-24127：CQ-4241893 のホットフィックス

### MSM {#msm}

* クロスサイトスクリプティング攻撃（XSS）に対するプロアクティブなホットフィックス。 NPR-21893：CQ-4223385 のホットフィックス
* MSM LiveRelationship:BlueprintConfig がルートにある場合、有効な RolloutConfig は間違っています。 NPR-23999：CQ-4243000 のホットフィックス

### Sites {#sites-3}

* ライブコピー領域でエクスペリエンスを作成するには、継承を設定できるように、まず継承の機能を停止する必要があります。NPR-24995：CQ-4248209 のホットフィックス
* （タッチ UI）ページのロックまたはロック解除をおこなうと、上部のツールバーのいくつかのアイコンが非表示になります。NPR-23954：CQ-4243345 のホットフィックス
* ContextHub 内のフィールドの配置が正しくありません。NPR-23958
* ロックされたページに対するPublish アクションにより、オーサリングが中断される。 NPR-23970：CQ-4243203 のホットフィックス
* /Etc/reports/ の OOTB レポートが正常に機能せず、履歴データグラフが表示されません。NPR-20035：CQ-4220180 のホットフィックス
* プロジェクトで「ローンチをリクエスト」ワークフローを開始すると、ローンチの作成に失敗します。 NPR-24255：CQ-4245030 のホットフィックス
* CFP10 のインストール後にメールを送信する際に HTML タグと属性が無視される 。NPR-24287：CQ-4240028 のホットフィックス
* TagPicker：タグメタデータスキーマタグフィールドでのタグ提案は、タグ付け可能なノードをクエリするため、読み込みに時間がかかります。NPR-24347：CQ-4244291 のホットフィックス
* Salesforce 統合がプロキシ設定で失敗します。NPR-24418：CQ-4245300 のホットフィックス
* （WCM）リビジョンの作成中、PageManager が例外時にページをチェックインしたままにします。NPR-24565：CQ-4246203 のホットフィックス
* CFP14 を適用すると、「デバイスエミュレーター」ボタンが編集モードとプレビューモードで非表示になります。NPR-24566：CQ-4247060 のホットフィックス
* （クラシック UI）ダイアログボックスで作成すると、タグ全体が空として表示されます。 NPR-24688：CQ-4246407 のホットフィックス
* 1 回目でバージョンを作成できません。 NPR-24774：CQ-4232176 のホットフィックス
* /Etc/reports/ の OOTB レポートが正常に機能せず、履歴データグラフが表示されません。NPR-24138：CQ-4220180 のホットフィックス

### 脆弱性 {#vulnerability-1}

* Salesforce 統合が、サーバーサイドリクエストフォージェリ（SSRF）に対して脆弱です。NPR-24289：CQ-4245277 のホットフィックス
* ReportingServicesProxyServlet が、サーバーサイドリクエストフォージェリ（SSRF）に対して脆弱です。NPR-24657：CQ-4246880 のホットフィックス

### Granite {#granite-3}

* メタデータの読み取り操作を終了できません。NPR-24240：Granite-19866 のホットフィックス
* 脆弱性を修正するために、Jetty を 9.4.11.v20180605 に更新しました。NPR-25033：Granite-22120 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-1}

* ページの並べ替え中に PageComparator が ClassCastException をスローします。NPR-24123：CQ-4244048 のホットフィックス
* フォームドロップダウンコンポーネントの表示／非表示機能が期待どおりに機能しません。NPR-24562：CQ-4222853 のホットフィックス

### ユーザーインターフェイス {#user-interface}

* 管理者の検索機能のリクエストが多いため、CPU 使用率が高くなります。 NPR-23588：Granite-21286 のホットフィックス
* （クラシック UI）コンポーネントが、関連するフォームデータモデルサービスが空のフィールドに設定されている場合でも、デフォルト値を表示します。 NPR-21903：Granite-19744 のホットフィックス
* リクエストに FormData が存在しない場合に NPE をスローするマルチフィールド。 NPR-24513：Granite-21055 のホットフィックス

## Forms {#forms-4}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-4}

#### コア {#core}

* （OSGi）AEM Forms OSGi は、ジャクソンデータバインディングセキュリティ警告の影響を受けています。NPR-24274：CQ-4230245 のホットフィックス

#### Rights Management {#rights-management}

* AEM 6.2 SP1-CFP14 のインストール後に、Apache POI が失敗します。NPR-25054、NPR-25052：CQ-4245898、CQ-4244778 のホットフィックス

#### HTML5 のフォーム {#html-forms}

* HTML プレビューで、複数行のフィールドの事前入力でデータが入力されません。NPR-23357：CQ-4244212 のホットフィックス
* デフォルトのプレビューでレターをプレビューすると、「プレビュー」をクリックしたときにレイアウトフラグメントのマッピングが正しく表示されず、正しく表示されません。 NPR-22993：CQ-4237745 のホットフィックス
* テンプレートに社会保障番号パターンが適用された場合の、テキストフィールドの HTML プレビューに関する問題。NPR-23205

#### アダプティブフォーム {#adaptive-forms-3}

* AEM フォームを Parsys コンポーネントに追加中に、「Guidelib が定義されていません」というエラーが発生します。NPR-24269：CQ-4244546 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* シェルスクリプトファイルのウィンドウ行の終わりが、UNIX® で LCM が実行されない原因となります。NPR-22958

### 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included-3}

AEM 6.2 SP1-CFP16 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2 SP1-CFP16 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### 累積修正パック 15 {#cumulative-fix-pack-5}

AEM 累積修正パック 6.2 SP1-CFP15 は、[AEM 6.2 SP1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* 設計の一貫性を維持するために、基盤テーブルのセキュリティをプロアクティブに修正します。
* 値を文字列として保存するための typeHint のサポートを追加しました。
* Forms 事前入力サービスのセキュリティを強化しました。
* Reader 拡張機能の修正については、最新の adobe-reader-extensions-dsc.jar ファイルに更新してください。
* ブースト値の入力で `:invalid` 項目を考慮するように検証フックを調整しました。

### アセット {#assets-4}

* EmbedXMP data は、TIFFピラミッド生成プロセスでは常に「アクティブ」に設定されます。 NPR-22776：CQ-4234498 のホットフィックス
* 複数値フィールドに複数のデフォルト値を設定できません。NPR-22900：CQ-4239000 のホットフィックス
* （Dynamic Media）「動的レンディション」チェックボックスをオンにすると、ダウンロードした zip ファイルから 0 バイトのファイルを含む元のTIFF画像が生成されます。 NPR-22410：CQ-4198471 のホットフィックス
* （タッチ UI）列表示でのアセットのデフォルトアップロード場所。NPR-23475：CQ-4237057 のホットフィックス

### 統合 {#integration-5}

* ターゲットモードで、作成者がブループリントから継承されたコンポーネントを、継承をキャンセルせずに変更できます。NPR-22751：CQ-4237907 のホットフィックス
* パス変数が適切にエンコードされておらず、永続的でないクロスサイトスクリプティング（XSS）が発生します。 NPR-22851

### MSM {#msm-1}

* 複数のロールアウト設定を持つライブコピーのロールアウト中に、ResourceNameConflict がルートの下に発生した場合、すべてのブランチを含めずにロールアウトフローが終了します。NPR-22842：CQ-4236188 のホットフィックス

### Platform {#platform-3}

* 1 回のリクエストで、逆引きのアプリケーションに対してポーリング制限を実装しました。NPR-23351：Granite-21135 のホットフィックス****
* メッセージパターンの変更がカスタムロガーに反映されません。NPR-23486：CQ-4241974 のホットフィックス

### Sites {#sites-4}

* リッチテキストエディターのテキスト内に、スペースや他の特殊文字を含むドキュメントへのリンクを作成しても、機能しません。NPR-22289：CQ-4224321 のホットフィックス
* セグメントを大きな値（10000000000）で保存すると、ブーストが 0 に設定され、エラーメッセージが表示されます。 NPR-22524：CQ-4237006 のホットフィックス
* マルチフィールドコンポーネントの「項目を追加」をクリックできません。NPR-22552：CQ-4237404 のホットフィックス
* セグメントのタイトルが長い場合、水平スクロールバーは表示されません。 NPR-22615：CQ-4237001 のホットフィックス
* 空のオーディエンスを読み込むと、誤った JavaScript コードが生成されます。NPR-22974：CQ-4238734 のホットフィックス
* アクティベーションをスケジュール設定または非アクティブ化する場合、ワークフロータイトルは必須なので、カスタムワークフロータイトルはタイムラインで翻訳されません。NPR-23121：CQ-4237552 のホットフィックス
* Sites の Target セグメントに関する問題に対する修正のリクエスト。NPR-23128
* （Firefox）選択したペルソナのチェックボックスが正しくありません。 NPR-23345
* 異なるモードのラベルは、アイコンと共に表示されます。NPR-23275
* AEM 6.0 から AEM 6.2 にコンポーネントを移行する際の「無効な再帰セレクター値」エラー。NPR-23503：CQ-4241258 のホットフィックス

### Communities {#communities-1}

* グループへのメッセージ失敗により、Web およびメール通知がトリガーされません。NPR-23447：CQ-4242880 のホットフィックス

### 翻訳 {#translation-1}

* 翻訳設定で「翻訳しない」アセットが設定されている場合、アセット言語コピーが作成されます。 NPR-22540：CQ-4237962 のホットフィックス

### ユーザーインターフェイス {#user-interface-1}

* オムニサーチでハイフンを使用すると、サーバーエラーが返されます。NPR-22999：Granite-19674 のホットフィックス
* DatePicker が、非表示フィールドによって設定された外部タイプヒントの手動設定をサポートしていません。 タイプヒントを変更すると、変換エラーが発生します。NPR-23333：Granite-21194 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-2}

* セキュリティ向上のため、CAPTCHA コンポーネントは非推奨（廃止予定）になりました。 CAPTCHA コンポーネントを使用すると、6.2 SP2-CFP15 以降のリリースをインストールした後、「Captcha コンポーネントは非推奨なので使用しないでください」というメッセージが表示されます。 セキュリティ向上のために reCAPTCHA を含めることで AEM コンポーネントをカスタマイズできます。NPR-22151：CQ-4220052 のホットフィックス
* WCM 基盤コンポーネント「テーブル」が、保存されたクロスサイトスクリプティングに対して脆弱です。NPR-23206：CQ-4240760 のホットフィックス

### 脆弱性 {#vulnerability-2}

* 管理 UI のプロジェクトリンクのクロスサイトスクリプティング（XSS）。NPR-23272：CQ-4241795 のホットフィックス

## Forms {#forms-5}

### Forms アドオンパッケージ {#forms-add-on-package-5}

#### Correspondence Management {#correspondence-management}

* デフォルトのプレビューでレターをプレビューすると、「プレビュー」ボタンをクリックしてもレイアウトフラグメントのマッピングが表示されず、正しく表示されません。 NPR-23335：CQ-4237745 のホットフィックス
* XDP で定義されたバインディングに対応するレターのデータは、ダイレクトレター URL を使用して入力されません。 NPR-24145：CQ-4244290 のホットフィックス

#### モバイルフォーム  {#mobile-forms}

* （Correspondence Management）ターゲット XML でレターを読み込む際のデータのずれ。NPR-22993：CQ-4237663 のホットフィックス

#### Reader Extensions サービス {#reader-extensions-service}

* Reader Extension を Adobe PDF に適用できません。NPR-23067

#### Forms Manager {#forms-manager}

* サイトに埋め込まれたFormsは、サイトページを再公開する際に公開されません。 NPR-23014：CQ-4236566 のホットフィックス

#### 脆弱性 {#vulnerability-3}

* クロスサイトスクリプティングの事前ホットフィックス。 NPR-20624：CQ-4206055 のホットフィックス
* Forms Manager の「メモ」タブに表示される、ストアドクロスサイトスクリプティング（XSS）の脆弱性。 NPR-27157：CQ-4255556 のホットフィックス

#### Encryption サービス {#encryption-service}

* （OSGI） [JEE] 「署名プロセスの検証」を使用して検証する際に、添付ファイル付きのPDFのPDFステータスが正しくありません。 NPR-23269、NPR-23737

### Forms JEE インストーラー {#forms-jee-installer-5}

#### コア {#core-1}

* コア拡張の静的コード分析で報告された問題を修正する必要があります。NPR-13947

#### PDFG サービス {#pdfg-service}

* HTML から PDF への変換が機能しません。NPR-21545

### 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included-4}

次のドキュメントには、CFP に含まれている OSGi バンドルとコンテンツパッケージの一覧が記載されています。

AEM 6.2 SP1-CFP15 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2 SP1-CFP15 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### 累積修正パック 14 {#cumulative-fix-pack-6}

AEM 累積修正パック 6.2 SP1-CFP14 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* アセットのメタデータプロパティの編集性が向上しました。
* 既に期限切れの状態にあるアセットのパスワード有効期限通知ジョブを再設定しました。
* タッチ UI コンソールをカスタマイズして、より多くのロケールを拡張しました。
* 効率的な Livecopyindex 同期のために cq-msm-core をアップデートしました。
* 様々なロールアウトへのレプリケーション機能を合理化しました。

### アセット {#assets-5}

* 免責事項を含み、長いファイル名が付いたアセットをダウンロードできません。 NPR-22163：CQ-4235274 のホットフィックス
* 一重引用符文字が原因で、一括表示でのメタデータの更新ができず、クイックツールバーアクションを使用してアセットのプロパティを開くと UI が壊れます。 NPR-22317、NPR-22353：CQ-4236990、CQ-4236469 のホットフィックス
* アセットの有効期限通知ジョブで、有効期限切れのアセットが非アクティブ化されない。 NPR-22346：CQ-4237188 のホットフィックス
* Safari でアセットの Digital Rights Management を使用すると、アセットをダウンロードできません。NPR-22378：CQ-4236460 のホットフィックス
* 小さい画像の Web レンディションのピクセルサイズが正しくありません。NPR-22435：CQ-4236742 のホットフィックス

### Sites {#sites-5}

* （タッチ UI）移動されたタグが、ページのプロパティの古い場所と新しい場所に表示される。NPR-21921：CQ-4238598 のホットフィックス
* （タッチ UI）リッチテキストエディターが、&lt;a> タグから id 以外のすべての属性を削除する。NPR-22045：CQ-4234133 のホットフィックス
* Ctrl + V キーを押しながらリッチテキストエディターにコンテンツを直接貼り付けると、改行がスキップされる。NPR-22117：CUI-5881 のホットフィックス
* （タッチ UI）名前空間の下に 40 個を超えるタグを表示できない。 NPR-22290：CQ-99114 のホットフィックス
* RSS フィードの問題、ポート - 1 から AEM 6.2 NPR-22158：CQ-4233339 のホットフィックス
* （IE）リッチテキストフィールド内の任意の文字を初めてオーサリングする場合、文字の末尾に空白が追加される。 NPR-22443：CQ-4235343 のホットフィックス
* パッケージ名を一致させようとすると、Java™ Use オブジェクトは、パッケージ宣言の末尾の空白文字が原因で SightlyJavaCompilerService をフリーズします。 NPR-22557：Granite-20836 のホットフィックス
* タッチ UI コンソールで、タグ付けに使用する新しい言語が取得されません。NPR-22250：CQ-4239194 のホットフィックス

### Mobile On-Demand {#mobile-on-demand}

* （Digital Publishing Suite）公開日とカバー日の両方が、DPS にアップロードされる前にポートフォリオに対して必須のフィールドです。 NPR-22484

### Commerce {#commerce}

* Commerce Create Catalog ウィザードに複数のクロスサイトスクリプティング（XSS）の脆弱性があります。 NPR-22344：CQ-4237017 のホットフィックス

### MSM {#msm-2}

* LiveCopyIndex の同期により、長時間のインデックス更新中にスレッドが輻輳します。NPR-22214：CQ-90667 のホットフィックス
* `cq:cugEnabled` プロパティは、ライブコピー内の別のフィールドが編集された場合に無効になり、ページが保護されなくなります。NPR-22246：CQ-4236050 のホットフィックス
* ページのロールアウトアクションは、ページが中断されたときに子を更新できません。NPR-22483：CQ-4236956 のホットフィックス
* プライマリで移動された構造をロールアウトすると、問題が発生する `cq:moveTarget`. NPR-22373：CQ-4232536 のホットフィックス

### 統合 {#integration-6}

* オファーセレクターライブラリでオファーを並べ替えようとすると、異常な動作が発生します。NPR-22208：CQ-4235439 のホットフィックス
* 長時間実行されるクエリで TargetContentImpl を使用すると、AEM の速度が低下します。NPR-22361：CQ-4236907 のホットフィックス
* Target エンジン（mbox.js、at.js）では、マッピングされた URL を使用せず、特定のデプロイメントで失敗する可能性のあるコロンを含んだ URL を使用します。 NPR-22366：CQ-4237854 のホットフィックス
* ページのパーソナライゼーションには、ブランドノード上での投稿権限が必要です。NPR-22370：CQ-4236895 のホットフィックス

### 基盤 {#foundation}

* Apache Sling スクリプティング Sightly モデルは、プロバイダーバンドル **org.apache.sling.scripting.sightly.models.provider/1.0.18** を使用します。NPR-22614：Sling-5944、Sling-6866 のホットフィックス

### プロジェクト {#projects}

* ワークフロースターターは、String の TypeHint 値を受け入れることができません。 NPR-22436：CQ-4237855 のホットフィックス

### 翻訳 {#translation-2}

* プレビュー機能の問題を調査しました。NPR-22201：CQ-4223753 のホットフィックス

### ユーザーインターフェイス {#user-interface-2}

* （クラシック UI）コンポーネントが、関連するフォームデータモデルサービスが空のフィールドに設定されている場合でも、デフォルト値を表示します。 NPR-21903：Granite-19744 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-3}

* Adobe Campaign のインポーターページを指すライブコピーページを公開する際にエラーが発生します。NPR-22470：CQ-4237164 のホットフィックス
* エクスペリエンスフラグメントエディターを開くときに JavaScript エラーが発生します。NPR-22598：CQ-4238415 のホットフィックス

### ワークフロー {#workflow}

* Day CQ ワークフローメール通知サービスは、WorkflowCompleted 通知と WorkflowAborted 通知用に、Mongo ノードごとに 1 つのメールをトリガーします。NPR-22486：CQ-4238172 のホットフィックス

## Forms {#forms-6}

### Forms アドオンパッケージ {#forms-add-on-package-6}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

#### アダプティブフォーム {#adaptive-forms-4}

* IE11 とChromeをまたいだ、アダプティブフォームのドロップダウンプレースホルダー値の不整合。 NPR-22405：CQ-4227096 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-6}

#### LCM のインストール {#install-lcm}

* インストーラーと LCM で Jsafe Jars を Cryptoj 6.1.3.1 に更新しました。NPR-22744

### 含まれている機能パック {#feature-packs-included}

#### プロセス管理 {#process-management}

* （HTMLのWorkspace）ユーザーがタスクを要求すると、キューのカウントは、その特定のユーザーに対してのみ更新されます。 つまり、ページが更新されない限り有効です。 NPR-19778：CQ-4233665 のホットフィックス

### CFP14 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp}

AEM 6.2 SP1-CFP14 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2 SP1-CFP14 に含まれているコンテンツパッケージの一覧

[ファイルを取得](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM 累積修正パック 6.2 SP1-CFP13 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* AT.js をクライアントライブラリとして使用する際に、ターゲットコンポーネント設定内の静的パラメーターフィールド設定を有効にしました。
* ドロップダウンコンポーネントの表示／非表示機能を修正しました。
* ターゲット同期オーディエンスの使用に関する修正をおこないました。
* Correspondence Management の汎用性が向上し、特殊文字に対応します。

### アセット {#assets-6}

* バージョンの削除で、古いバージョンのアセットを削除できません。NPR-21682：CQ-4212996 のホットフィックス
* 並べ替え可能なフォルダーで、フォルダーの並べ替えが保持されません。NPR-21964：CQ-4231761 のホットフィックス

### Sites {#sites-6}

* （タッチ UI）（クラシック UI）HTL およびコアコンポーネントでの複数のクロスサイトスクリプティング（XSS）脆弱性。NPR-21532：CQ-4232305 および CQ-4232511 のホットフィックス
* 選択したテキストのコンテンツの作成／書式設定（新しいリストスタイルの割り当て／削除など）は、Internet Explorer 11 では正常に機能しません。NPR-21533：CQ-4230689 のホットフィックス
* （Safari）アセットファインダーパネルで一部のアセットが表示されません。 NPR-21981：CQ-4213720 のホットフィックス
* タイムワープで「RecursionTooDeepException」エラーが返され、ページが文字化けし、日付が変更されても新しいバージョンが作成されません。 NPR-21707：CQ-4199536 のホットフィックス
* エディターでページを読み込むと、WorkflowStatusprovider （pageinfo.json）が 3 回読み込まれ、AEM インスタンスのパフォーマンスが低下します。 NPR-21778：CQ-59232 のホットフィックス

### 統合 {#integration-7}

* オーサリングターゲットモードでのモバイルタイプとブラウザーのオーディエンスの作成が、AEM で動作しません。NPR-21676、NPR-21681：CQ-4232100 のホットフィックス
* ターゲットコンポーネントの更新中に待ち時間が長い場合、コンポーネントが完全に更新される前に別のオファーを追加できます。NPR-21744：CQ-4233158／CQ-4234293 のホットフィックス
* クラウド設定で AT.js をクライアントライブラリとしてテストすると、mbox 呼び出しでテスト静的パラメーターの値が表示されません。 NPR-21930：CQ-4234520 のホットフィックス

### Platform {#platform-4}

* ユーザーまたはグループの数が多い場合、ユーザー同期のパフォーマンスの問題。 NPR-20431：CQ-4223282 のホットフィックス
* ユーザーは、Sling 配布を使用してユーザー同期と同期できません。 NPR-21911：Granite-20404 のホットフィックス
* （Geometrixx ページの）検索抜粋で、停止ワードがハイライトされるのを防ぎます。NPR-21835：Granite-21067 のホットフィックス
メモ：この修正には、Oak CFP 1.4.20 以降が必要です。

### 翻訳 {#translation-3}

* 翻訳プロジェクトの作成中に、イニシエーターユーザー ID の jcr プロパティがありません。 NPR-21715：CQ-4230713 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-4}

* フォームドロップダウンコンポーネントの表示／非表示機能が期待どおりに機能しません。NPR-22164：CQ-4235288 のホットフィックス

## Forms {#forms-7}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-7}

#### アダプティブフォーム {#adaptive-forms-5}

* アダプティブフォームでの XML 外部実体攻撃（XXE）。NPR-21982：CQ-109878 のホットフィックス
* （iOS11）添付ファイルコンポーネントをクリックすると、添付ファイルがデバイスのファイルブラウザーではなくカメラを開きます。NPR-21926：CQ-4214348 のホットフィックス
* テーマ作成 UI にタイトルが見つからない場合、例外が発生し、ダイアログボックスのレンダリングに失敗します。CQ-4236143 のホットフィックス

#### Correspondence Management {#correspondence-management-1}

* 特殊文字を含む xml データのレンダリングの問題。NPR-21712：CQ-4229137 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-7}

#### Assembler サービス {#assembler-service}

* `6.2.0-ASM-1017-003` を使用して生成された PDF ファイルが破損しています。NPR-21427：CQ-4228046 のホットフィックス

#### PDFG サービス {#pdfg-service-1}

* PNG、JPEG、TIFF ファイルの予期しないページサイズ（PDF）が原因で OCR に失敗します。NPR-19489：CQ-4209079 のホットフィックス

## CFP13 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp-1}

AEM 6.2 SP1-CFP13 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2 SP1-CFP13 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM 累積修正パック 6.2 SP1-CFP12.1 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* 複数値フィールドのメタデータ処理を改善しました。
* 翻訳ワークフローでの複数文字（2 つ以上）の国コードをサポートします。
* 複数のネストされたコンポーネントを含むページのレンダリングを改善しました。
* AEM と Adobe Digital Publishing Suite の間でアセットの公開日の同期を改善しました。

### アセット {#assets-7}

* オムニサーチの文字が多すぎると、AEM サーバーがクラッシュする可能性があります。 NPR-21083：CQ-4223602 のホットフィックス
* メタデータスキーマの複数値フィールドの 2 番目のオプションで指定された値が、CRX-de で以前に指定した値に追加されません。 NPR-21220：CQ-4224526 のホットフィックス
* Safari でアセットの Digital Rights Management を使用すると、アセットをダウンロードできません。NPR-21387：CQ-4230287 のホットフィックス

### Sites {#sites-7}

* （DAM）（クラシック UI）AEM CQ オーサー／パブリッシュクイックスタートの一部の SWF ファイルに、複数のクロスサイトスクリプティング（XSS）脆弱性が存在します。NPR-21073、NPR-21074：NPR-20612 のホットフィックス
* 複数の言語で使用可能なタグがタグピッカーで翻訳されません。NPR-21221：CQ-78855 のホットフィックス
* 複数のネストされたコンポーネントを使用すると AEM 記事コンソールでの動作が遅くなるレンダリングの問題。NPR-21271：CQ-4224158 のホットフィックス

### 統合 {#integration-8}

* Target フレームワークを追加する場合、エディターの「モードを選択」リストでターゲティングモードを使用できません。 NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* （Digital Publishing Suite）AEM の Folio の公開日が、Folio Producer に表示される日付と一致しません。NPR-21145

### MSM {#msm-3}

* LC の最初のローカルページを削除した後、ライブコピーのリセットプロセスが停止します。 NPR-21276：CQ-4229743 のホットフィックス

### Platform {#platform-5}

* AEM 6.3 にアップグレード後、スクリプトとして実装されたタグを参照するカスタムタグライブラリが見つからない。NPR-20149:Granite-18433 のホットフィックス

### 翻訳 {#translation-4}

* 2 文字を超える lang_country コードがある場合、変換ワークフローが失敗します。NPR-21088：CQ-4197439 のホットフィックス
* 翻訳プロジェクトが完了するまで、翻訳プロジェクトにアセットページを再度送信しないでください。NPR-21219：CQ-4209908 のホットフィックス

### ユーザーインターフェイス {#user-interface-3}

* 選択コンポーネントは、フォームの送信中に target プロパティを削除しません。 NPR-21163：Granite-14125 のホットフィックス
* HTTP.encodePathOfURI 展開プラス記号「+」を二重エンコードします。 NPR-21417：Granite-16340 のホットフィックス

### 脆弱性 {#vulnerability-4}

* DAM メタデータエディターでのクロスサイトスクリプティング（XSS）。 NPR-21434：CQ-83472 のホットフィックス
* 複数のSWFファイルが、クロスサイトスクリプティング（XSS）に対して脆弱です。 NPR-20612：CQ-4213297 のホットフィックス

## Forms {#forms-8}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-8}

#### Correspondence Management {#correspondence-management-2}

* （IE11）完全な UI が読み込まれた後、右側が断続的に読み込まれている間に、HTML コンテンツの初期レンダリングが左側でのみ発生します。NPR-21554
* AEM 6.2 SP1-CFP9 をインストールすると、「レターのプレビュー」送信ボタンが無効になります。 NPR-21547
* アセットリンケージタイプを選択する際に、レターデータ連結を編集ウィザードでアセットセレクターウィンドウが開きません。 NPR-21164：CQ-4194567 のホットフィックス
* インラインまたは編集可能なテキストモジュールを編集するには、関連する編集アイコンをタップするか、レターのプレビューで関連するテキストモジュールをダブルクリックします。NPR-21402

#### アダプティブフォーム {#adaptive-forms-6}

* AEM Forms の送信ボタンコンポーネントには、type=&quot;submit&quot; ではなく type=&quot;button&quot; と表示されます。NPR-21007
* 繰り返し可能なパネルの新しいパネルを追加または削除しても、データが保持されます。NPR-21408

### Forms JEE インストーラー {#forms-jee-installer-8}

#### コア {#core-2}

* 最新の Java™ 8 Update 131 にアップグレードすると、「JsafeJCE プロバイダーが無効です。FIPS 140 に必要な自己整合性チェックに失敗しました」という例外がスローされる。 NPR-21355

**メモ：**&#x200B;この NPR には、さらに設定が必要です。[Java™ 8 の最新のアップデート](#latest-java-update-throws-an-exception-npr)を参照してください。

* Jsafe Jar は、コア、暗号化、署名、ドキュメントセキュリティの CryptoJ 6.1.3.1 に更新されました。 NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### LCM のインストール {#install-lcm-1}

* インストーラーと LCM で Jsafe の Jar を CryptoJ 6.1.3.1 にアップデートしました。NPR-21362

#### PDFG サービス {#pdfg-service-2}

* PDFG の Jsafe Jar を CryptoJ 6.1.3.1 にアップデートしました。NPR-21359

#### プロセス管理 {#process-management-1}

* （HTML ワークスペース）名前カテゴリーが切り捨てられて表示されないように列のサイズ変更を有効にしました。NPR-19770：CQ-4233668 のホットフィックス

#### Reader Extensions サービス {#reader-extensions-service-1}

* Jsafe Jar は、RE で CryptoJ 6.1.3.1 に更新されました。 NPR-21357

## CFP12.1 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp-2}

AEM 6.2 SP1-CFP12.1 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM 累積修正パック 6.2 SP1-CFP11 は、AEM 6.2 SP1 の一般リリース（GA）以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* 効率的な Livecopyindex 同期のために cq-msm-core をアップデートしました。
* コンテンツフラグメントの編集効率が向上しました。
* ACL 権限を検出するための検証オプションがパッケージマネージャーに用意されています。
* 顧客対応のメール ID を含むキャンペーン機能を導入しました。
* Dynamic Media ファイルのビデオエンコーディング機能を改善しました。
* Sightly コンポーネントとライブコピーの修正。

### アセット {#assets-8}

* 名前にスペースが含まれるファイルの Dynamic Media ビデオエンコーディングが失敗します。NPR-20818：CQ-102469 のホットフィックス
* AEM CQ オーサー／パブリッシュクイックスタートの一部の SWF ファイルに、複数のクロスサイトスクリプティング（XSS）脆弱性が存在します。NPR-21071、NPR-21072
* 免責事項を含み、長いファイル名が付いたアセットをダウンロードできません。 NPR-20255：CQ-4222139 のホットフィックス

### Sites {#sites-8}

* AEM と Campaign の統合：Adobe Campaign で特別なリンクが書き換えられ、顧客がメールで mailto: ハイパーリンクを送信できません。NPR-20787：CQ-4225760 のホットフィックス
* （タッチ UI）言語がフランス語に設定されている場合の、AEM のユーザビリティに関する問題とパフォーマンスの問題。NPR-20854：CQ-4227628 のホットフィックス
* RTE のリンクプラグインを使用してエンコードされたアセットファイルをリンクすると、空のリンクが返されます。 NPR-20626、NPR-21059：CQ-4223011 のホットフィックス
* コンテンツフラグメントのメタデータエディターを使用すると、コンテンツ作成者はコンテンツフラグメントに対する変更を保存できません。 NPR-20641：CQ-4224755 のホットフィックス
* ページプロパティのエイリアスは、「公開の要求／非公開の要求」に結び付きます。NPR-20731：CQ-4226227 のホットフィックス
* RTE 要素でのリンクのエンコードに関するテキストコンポーネントの問題。NPR-20755：CQ-4224321 のホットフィックス

### Platform {#platform-6}

* ResourceResolverImpl.map() が ResourceDecorator を呼び出しません。NPR-20788：Granite-19718 のホットフィックス
* `org.apache.sling.i18n.DefaultLocaleResolver` は、org.apache.sling.engine.SlingRequestProcessor を介してリクエストを処理できません。 NPR-20706：CQ-94880 のホットフィックス
* 特定のパッケージに対する ACL 許可／権限が変更されたかどうかを検出する検証オプションをパッケージマネージャーに追加するリクエスト。CQ-4229196 のホットフィックス

### ワークフロー {#workflow-1}

* AEM 実稼働サーバーのデプロイメントに関する安定性の問題。NPR-20979：Granite-19104 のホットフィックス

### プロジェクト {#projects-1}

* （タッチ UI）チームメンバーをプロジェクトに追加できません。NPR-20990：CQ-4205375 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-5}

* Sightly 画像コンポーネントの「リンク先」で.html 拡張子が欠落していることが原因で 403 エラーが発生する。 NPR-20823：CQ-4195909 のホットフィックス
* ライブコピーを使用する設計図サイトで、フォームコンポーネントを削除しようとすると、NullPointerException がスローされ、フォームコンポーネントを削除する代わりに追加し直します。NPR-20855：CQ-4204628 のホットフィックス
* LiveCopyIndex の同期により、長時間のインデックス更新中にスレッドが輻輳します。NPR-20634：CQ-90667 のホットフィックス

### セキュリティ {#security}

* XSS ライブラリのプロアクティブな更新。NPR-21174
* メール送信用の簡易 API を表示する Apache Commons Email 1.5 にアップグレードしました。 NPR-20509：Granite-18240 のホットフィックス
* XSS のバイパスの可能性を排除するために、Apache Sling XSS Protection API にセキュリティパッチを適用。NPR-21290：Granite-19924 のホットフィックス
* XSSAPI#getValidHref 関数の XSS バイパス。NPR-21174：Granite-19924 のホットフィックス

### モバイルアプリ {#mobile-apps}

* AEM の OOTB アセットに対する curl Head リクエストの問題を修正しました。NPR-20511：CQ-4221520 および CQ-103024 のホットフィックス

## Forms {#forms-9}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

AEM Forms の主なハイライトは次のとおりです。

* Workbench ユーザーの証明書認証を有効化。
* Correspondence Management、HTML5 フォーム、AEM Forms ワークスペースのユーザビリティを修正しました。

### Forms アドオンパッケージ {#forms-add-on-package-9}

#### HTML5 のフォーム {#html-forms-1}

* iOS 10 および 11 デバイスでの手書きメモコンポーネントの使い勝手の問題。NPR-21092

#### Correspondence Management {#correspondence-management-3}

* （通信 UI）ワンクリック後の「送信」ボタンの無効化 NPR-21078

### Forms JEE インストーラー {#forms-jee-installer-9}

#### Assembler サービス {#assembler-service-1}

* docConvertor が、エラー「The prefix &quot;stEvt&quot; for element でPDF/A を生成できない `stEvt:action` 縛られてはいません」 NPR-21032：CQ-4222540 のホットフィックス
* サービス OMPFSubmission/PDFA/PDFtoPDFA を呼び出し中に、`java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` という名前の例外が発生します。この例外により、短期間有効な署名検証プロセスがサーバーが再起動するまで完了しなくなります。 NPR-20792

#### Workbench {#workbench}

* Workbench ユーザーの証明書認証を有効化。NPR-17548：CQ-4214486 のホットフィックス

#### プロセス管理 {#process-management-2}

* モバイルフォームが dataref パラメーターでレンダリングされると、データ準備プロセスは複数回呼び出します。 NPR-19801：CQ-4230427：CQ-4230400 のホットフィックス

## CFP11 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp-3}

AEM 6.2 SP1-CFP11 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM 累積修正パック 6.2 SP1-CFP10 は、AEM 6.2 SP1 の一般リリース（GA）以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* テスト用にユーティリティ関数 onDialogLoaded を追加しました。
* ClientLibraryProxyServlet にフロントエンドユニットテストと設定を追加しました。
* 複数のイメージインプレイスエディターコンポーネントのパフォーマンスを修正しました。
* Apache Sling JCR ResourceBundleProvider の設定の更新。

### アセット {#assets-9}

* アセットの更新ワークフローが無効になっていると、アセットプレビューが機能しません。NPR-20543：CQ-4204986 のホットフィックス
* Granite：クラスプロパティに追加されたクラスのレンダリングの問題（cq-damadmin-admin-assets-upload）NPR-20514：CQ-4219238 のホットフィックス
* タイトルに特殊文字が含まれるサムネールアセットで、NPR-20347 の alt 属性の中に Java™ オブジェクトが表示される：CQ-4223620 のホットフィックス
* ライセンスの問題により、バージョン比較コードをアドビ独自のコードに置換。NPR-20273：CQ-4223758 のホットフィックス
* 複数のアルファレイヤーを持つ CMYK PSB ファイルをアップロードする際の処理の問題。NPR-20251：CQ-4220869 のホットフィックス
* org.apache.sling.i18n 2.5.6 でサーバーを再起動すると、国際化辞書が機能します。NPR-20525:Granite - 19490 のホットフィックス
* デフォルトのスレッドダンプコレクター設定（デフォルトのAEM起動）を使用した、スケジューラー期間に従って、スレッドダンプが生成されていない。 NPR-20288:GRANITE-19488/GRANITE-12741 CQ-90647 のホットフィックス。

### Sites {#sites-9}

* 保存した検索を開いた後に変更日フィルターを変更しても、結果には影響しません。 また、表示される結果は、変更日フィルターの以前に保存した値と同じです。 NPR-19739：CQ-4219425 のホットフィックス
* ネストされたコンポーネントを含むページの読み込みに失敗します。NPR-20312
* ワークフローパッケージの削除時に、削除の要求ワークフローがトリガーされます。NPR-20266：CQ-4221686 のホットフィックス
* （タッチ UI）OS クリップボードと内部 AEM クリップボードでコピー／ペーストをおこなう場合の問題。NPR-20228：CQ-4220383 のホットフィックス
* 複数のアセット（100 を超える）が読み込まれると、AEM インスタンスがリスト表示で遅くなります。NPR-20034：CQ-4222695 のホットフィックス
* （タッチ UI）クラシック UI コンソールを介してローンチを削除すると、すべてのページが編集できなくなります。 NPR-20520：CQ-4225074 のホットフィックス
* ターゲットドロップダウンは、ダイアログボックス内の複数の RTE コンポーネントでは機能しません。NPR-20345：CQ-4220981 のホットフィックス

### Platform {#platform-7}

* 匿名セッションを使用してアクセスした場合、ClientLibraryProxyServlet は、公開されたインスタンス上のクライアントライブラリへのリクエストをプロキシせず、HTTP 404 not found エラーをスローします。 NPR-20195：Granite-14409 のホットフィックス

### 統合 {#integration-10}

* ターゲットエンジンをAdobe Targetとして選択すると、コンポーネントが読み込まれなくなり、サーバーログにエラーがスローされる。 NPR-20058：CQ-88071、CQ-109698、CQ-4201600 のホットフィックス

### Commerce {#commerce-1}

* 同じページから製品を作成する際に、確認またはリダイレクトのポップアップメッセージが表示されません。 NPR-20257：CQ-4223414 のホットフィックス

### ユーザーインターフェイス {#user-interface-4}

* 日付選択が複数のフィールドに含まれるフィールドの場合、日付フィールドに保存された値は、コンポーネントの編集中に保持されません。NPR-20077：Granite-19147 のホットフィックス
* 連続したクエリがトリガーされて誤った結果が生じても、以前のクエリが中止されません。NPR-20397：Granite-19306 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-6}

* 複数画像インプレースエディターコンポーネントから画像を削除した後でも、ImageMap プロパティは引き続き存在します。 NPR-20142：CQ-4222982 のホットフィックス

## Forms {#forms-10}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-10}

#### アダプティブフォーム {#adaptive-forms-7}

* valueCommit スクリプトは、UI を通じて変更されたときに、DropDownList に対して 2 回実行されます。 NPR-19989：CQ-110212 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-10}

**プロセス管理**

* CFP パッケージに AEM Forms HTML Workspace バージョン 2.2.26 が含まれています。NPR-20099
* モバイルフォームがPDFとして表示するように設定されている場合、事前入力されたフォームは機能しません。 NPR-20566

**Rights Management**

* CAC/相互認証証明書選択ダイアログには、拡張キー使用法（EKU）を持つ証明書がクライアント認証またはスマート カード ログオンとして表示されます。 NPR-20708
* Forms JEE が PKCS#11 相互認証をサポート。NPR-15001

## CFP10 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp-4}

AEM CFP 6.2 SP1-CFP10 に含まれている OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/bundle-list-cfp10.txt)

AEM CFP 6.2 SP1-CFP10 に含まれているコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM 累積修正パック 6.2 SP1～CFP9 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* シークレット入力用に Analytics クラシック UI の設定を変更。
* Context hub の独立した永続性キャッシュの修正。
* アセットディメンションの正確な計算。
* Brand Portal にアセットを公開する際の AEM のパフォーマンスを最適化しました。
* キャンバスノードの `Resourcetype` 値を修正しました。
* ドキュメントフラグメントコンテンツで、大文字と小文字の区別と、特殊文字の検索を有効化しました。
* アダプティブフォームが強化され、Safari で添付ファイルとして PDF を添付できるようになりました。
このエクスペリエンスにより、新しいDynamic Media パブリッシュインフラストラクチャに接続する新しいDynamic Mediaが提供され、レプリケーションの速度と拡張性が向上します。

### アセット {#assets-10}

* AEM Assets は、InDesign アセットへの重複リンクを含むサブアセット参照を抽出できません。NPR-19006：CQ-4204186 のホットフィックス
* Commerce でコレクション内のアセットに対して並べ替えオプションが機能しません。NPR-19508：CQ-4213622 のホットフィックス
* 既存のアセットと同じ名前を持つアセットが同じ場所に移動された場合、アセットの `cq:lastReplicationAction` の値が入れ替わるので、誤ったメタデータが作成されます。NPR-19531
* すべてのアセットが正しく公開されているにもかかわらず、多数のアセットを公開すると、エラーメッセージが表示されます。NPR-19629：CQ-4219611 のホットフィックス
* 静的レンディションは固定サイズで表示され、実際のレンディションのサイズは反映されません。NPR-20004
* 4 つを超える複数のアセットが Brand Portal に公開されているとき、AEM インスタンスの動作が遅くなります。NPR-20009

### Sites {#sites-10}

* ユーザーが公開しようとすると、AEMに予期しない動作が表示される `/unpublish/create` 別のユーザーによってロックされているページのバージョン。 NPR-19249：CQ-4215298 および CQ-4203856 のホットフィックス
* ネストされたローンチを手動で昇格させると、子ページが削除されます。 NPR-19704
* ContextHub が初期化中にデフォルトの永続化レイヤーを上書きするときの永続化の問題。 NPR-19979：CQ-4218399 のホットフィックス
* コンテンツフラグメントは他のボタンと重なっています。NPR-19980：CQ-4221519 のホットフィックス
* SiteAdmin でエイリアスを使用して表示すると、サイトページが表示されない。 NPR-20053：CQ-4221478 のホットフィックス
* Adobe Campaign のインポーターページを指すライブコピーページを公開する際にエラーが発生します。NPR-20066：CQ-4220846 のホットフィックス

### Platform {#platform-8}

* Apache POI をバージョン 3.16 にアップグレードし、PPT スライドの背景画像をレンディションに含めるサポートを追加。NPR-18286
* 同じフォルダー内の複数のアセットをアップロードする際に、Internet Browser 11 および Edge でレンダリングの問題が発生します。NPR-20062

### 統合 {#integration-11}

* 匿名ユーザーでアクセスすると、カスタム at.js ファイルが公開されません。NPR-19542：CQ-4219592 のホットフィックス
* Analytics の既存の資格情報を WSSE 認証に移行。NPR-19962

### Brand Portal {#brand-portal}

* タグ管理/タグ付けコンソールからAEMからBrand Portalへのタグの公開を有効にする。 NPR-20271

## Forms {#forms-11}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-11}

#### Correspondence Management {#correspondence-management-4}

* ドキュメントフラグメントで、レターのプレビュー時に実際のテキストを検索する機能を有効化。NPR-19712

#### アダプティブフォーム {#adaptive-forms-8}

* アダプティブフォームが強化され、Safari で添付ファイルとして PDF を添付できるようになりました。既存のフォームでも同じ機能をサポートするには、添付ファイルウィジェットと「サポートされているファイルタイプ」の設定を変更して、.pdf ではなく application/pdf の値をアップデートします。 NPR-19623

#### Forms Manager {#forms-manager-1}

* アダプティブフォームのフィールドで validationState が定義されておらず、elementFocusChanged イベントが発生した場合は、エラーイベント（errorState）がAdobe Analytics サーバーに返されます。 NPR-19513

### Forms JEE インストーラー {#forms-jee-installer-11}

#### コア {#core-3}

* シャットダウン中は接続マネージャーを使用できません。 デプロイ解除されるオーサー EAR によって破損の問題が発生する前に、JBoss® は JDBC 依存関係を切り離します。NPR-19703

## 含まれている機能パック {#feature-packs-included-1}

* Dynamic Media でサムネールの補正と透明度を改善しました。NPR-15207

## CFP9 に含まれている OSGi バンドルおよびコンテンツパッケージ {#osgi-bundles-and-content-packages-included-in-cfp-5}

AEM 6.2SP1-CFP9 で更新されたコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

AEM 6.2SP1-CFP9 で更新された OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM 累積修正パック 6.2 SP1-CFP8 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* Adobe メールテンプレートサービスのカスタムユーザーテンプレートにタグを導入。
* デスクトップアプリケーションのタッチ UI ボタンの機能強化。
* 翻訳ページで複数のフォームを送信できないようにするには、クリックの送信ボタンを無効にしました。
* 1 つのダイアログに複数の RTE コンポーネントを設定しました。
* ライブコピーで ReferenceUpdates を強化しました。
* ドキュメントフラグメントコンテンツで、大文字と小文字を区別した検索機能が有効になりました。
* Linux® ライブラリの一覧を AEM Forms のインストールドキュメントに追加しました。

### アセット {#assets-11}

* Safari ブラウザーでスマートコレクションにオムニサーチフィルターを適用する場合の問題。 NPR-19511
* PDF アセットに複数のキーワードが関連付けられている場合、PDF キーワードメタデータが適切に抽出されず、誤って変更されます。この問題を解決するために、PDF アセットのサブジェクトフィールドメタデータプロパティを削除しました。ただし、メタデータスキーマを編集して、サブジェクトフィールドに複数値のテキストフィールドを追加することは可能です。NPR-19126
* ワークフロー通知サービスは、メール内のリンクをエンコードしないので、ユーザーがリンクをクリックした後に読み込むことができません。 NPR-19490：CQ-4218055 のホットフィックス
* Chromeを使用して、列表示でページ/アセットの完全なリストを読み込めない。 NPR-19458：CQ-4214248 のホットフィックス
* 「アクティベーションのリクエスト」ワークフローをアクティベートすると、誤った「オフタイム」アイコンがAEM インボックスに表示される。 NPR-19365：CQ-4216174
* リスト表示での並べ替えに関する問題。NPR-19217：CQ-95602
* アセットフォルダーの設定でタイトルまたはサムネール画像を変更すると、フォルダーの元のグループと権限が上書きされます。 NPR-19283：CQ-4216080 のホットフィックス
* `Windows 10` ワークステーションがタッチモードに自動的に切り替わり、一部のボタンが機能しなくなります。NPR-19183

### Sites {#sites-11}

* ダイアログボックスに複数の RTE コンポーネントがある場合の問題。 NPR-19311：NPR-19587
* Vanilla AEM 6.2 での自動バージョンパージは、VersionManagerImpl が初期化された後、1 回だけ機能します。 NPR-19315：CQ-4217175 のホットフィックス
* ワークフローインスタンスが「Salesforce.comの書き出し」ワークフローステップで停止する。 NPR-19222：CQ-4212976 のホットフィックス
* ライブコピーから作成された言語コピーページは編集できません。 NPR-18967
* 階層の変更に伴い、ReferencesUpdateAction は、ネストされたライブコピーへのリンクを更新できません。NPR-18715：CQ-4214105 のホットフィックス

### Platform {#platform-9}

* Adobeメールテンプレートサービスが、カスタムユーザーテンプレートにタグを追加する。 NPR-19190：CQ-4217113 のホットフィックス

### プロジェクト {#projects-2}

* プロジェクトエディターが、プロジェクトアセットフォルダーにアセットをコピー/貼り付けることができない。 NPR-19619
* 6.2 SP1-CFP1 をインストールした後、翻訳プロジェクトのプレビューを生成できない。NPR-16481：CQ-4204655

### 統合 {#integration-12}

* クラシック UI の Adobe Digital Publishing Solution で誤って設定されている記事のプロパティにアクセスします。NPR-19366
* AEM記事コンソールでの記事のサイズが最大になるため、サムネールのレンダリングが遅くなる。 NPR-19086：CQ-4217148
* ユーザーが複数の領域にアクセスできる場合、キャンペーンを介してオファーをパーソナライズするときの、自動フォールドの不正な動作。NPR-19290：CQ-4218029 のホットフィックス
* ターゲットモジュールを編集して複数回保存すると、ターゲティングモードでターゲティングダイアログボックスが表示されません。 NPR-19144：CQ-4216708 のホットフィックス

### ワークフロー {#workflow-2}

* インボックスクラシック UI のユーザー/グループで、インボックス内の通知をフィルタリングできない。 NPR-19122：CQ-4215374 のホットフィックス
* 画像マップは、HTL 画像コンポーネントで選択された座標を保持しません。 NPR-18911：CQ-4211584

## Forms {#forms-12}

* AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-12}

* コンテンツをMicrosoft®Word または web ブラウザーから Correspondence Manager テキストエディターにコピーすると、スタイルが失われます。 NPR-19530
* 改行のないコンテンツは折り返しできません。 NPR-19481
* ドキュメントフラグメントで、レターのプレビュー時に実際のテキストを検索する機能を有効化。NPR-17792：CQ-4214501 のホットフィックス

#### Correspondence Management {#correspondence-management-5}

>[!NOTE]
>
>テキストフラグメントの検索機能には、いくつかの制約があります。
>
>* ドキュメントフラグメントのコンテンツでは大文字と小文字が区別され、タイトルでは大文字と小文字が区別されません。
>* 検索された単語の一部が異なるスタイル設定になっている場合や、「、」または「」のような特殊文字が含まれている場合、検索結果はハイライト表示されません。
>* ドキュメントフラグメント内の動的コンテンツ（データディクショナリ要素の値や変数値など）に対しては、検索は機能しません。

#### Forms Manager {#forms-manager-2}

* AEM 6.2 で CFP6 を適用した後に、アダプティブフォームの XML スキーマプロパティを編集できません。CQ-4219684 のホットフィックス
* AEM Forms Manager コアバンドルのすべてのサービスが、サーバーの再起動時に開始されません。 CQ-4217014 のホットフィックス

### Forms JEE インストーラー {#forms-jee-installer-12}

#### LCM のインストール {#install-lcm-2}

* CFP6 をインストールすると、Microsoft® Windows の管理画面にバージョン番号 6.0 が表示されます。 CQ-4217573 のホットフィックス

## 含まれている機能パック {#feature-packs-included-2}

* デスクトップアプリケーションのタッチ UI ボタンの機能強化。NPR-18676

## CFP8 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp}

AEM 6.2 SP1-CFP8 で更新された OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/updated-bundles-list-cfp8.txt)

AEM 6.2SP1-CFP8 で更新されたコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM 累積修正パック 6.2 SP1-CFP7 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* dc: title プロパティが String （マルチフィールド）に設定された画像で、画像カードにタイトルを表示する際の動作を変更しました。
* Dynamic Media Cloud Service、タッチ UI およびセキュリティ UI インターフェイスのパフォーマンスの問題を修正しました。
* Apache Felix Http Bridge 3.0.8 の修正点
* オーサーとパブリッシュ環境間のバイナリレスレプリケーション（BLR）を解決しました。
* Target ライブラリファイル AT.JS のサポートは、Adobe Targetとのクライアントサイド統合のための実装ライブラリで、通常の web 実装とシングルページアプリケーションの両方に使用できるように設計されています。
* ユーザーが設定可能な接続タイムアウト時間を Analytics、DTM および Target に導入して、AEM のパフォーマンスを向上しました。

### アセット {#assets-12}

* Dynamic Media Cloud Services で設定された AEM 6.3 でビデオ取得をテストする際に、「開いているファイルが多すぎます」という例外が発生します。NPR-18734：CQ-4211407 のホットフィックス
* AEM インスタンスを再起動した後、ページ上のアセットのバニティ URL 設定が機能しません。NPR-18634：Granite-18085 のホットフィックス
* タッチ UI で、アセットを公開する権限を持たないユーザーに対して「公開」ボタンが表示されます。NPR-18620：CQ-4214042 のホットフィックス
* ライセンス契約が設定されると、アセットのダウンロードダイアログボックスに動的レンディションオプションが表示されなくなります。NPR-18607：CQ-4212342 のホットフィックス
* 名前にスペースが含まれるアセットのダイナミックレンディションをダウンロードできません。NPR-18571：CQ-4211738 のホットフィックス
* Creative Cloud でアセットフォルダーを共有する際に、複数のユーザーを保存できません。NPR-18489：CQ-103297 のホットフィックス
* dc: title と dc: description が、crx/de でマルチフィールド値に変更されません。NPR-18474：CQ-4209086 のホットフィックス
* アセットの移動操作がパフォーマンスの低下を引き起こします。NPR-18346
* デフォルトの「すべてを表示」オプションを設定して開いた場合、タイムラインに項目が表示されません。NPR-18302：CQ-4211957 のホットフィックス
* ASCII／UTF-8 エンコードされたテキストファイルが AEM Assets にアップロードされ、サムネールの生成に失敗すると、エラーが発生します。NPR-18006：CQ-4209345 の CFP
* Publishのアクションボタンは、ユーザーが複製アクセス権を持っていない場合でも表示されます。 NPR-17353：CQ-4209269 のホットフィックス
* min:gcc;obfuscate=true を使用して縮小が有効になっている場合、サイト管理とその他の管理は両方とも機能しません。 NPR-18593：CQ-4209220 のホットフィックス
* 毎回、画面が更新されるまでカスタムメニュー項目が表示されません。NPR-18500：CQ-4213581 のホットフィックス
* Moment.js を 2.10.6 にアップグレードしました。NPR-18596：Granite-11881 のホットフィックス
* DM マクロに権限を適用すると、管理者ユーザーの表示が壊れる。 NPR-18544：CQ-4211729 のホットフィックス
* アセットの「後で公開」で、不正な ArgumentException が発生します。CQ-4214532

### Sites {#sites-12}

* MongoDB を使用したアクティブ – アクティブのオーサークラスターで、コンテンツのオンタイムに設定された時間に達すると、両方のオーサーが同じコンテンツのレプリケーションをトリガーにしようとします。 NPR-18708：CQ-4210982 のホットフィックス
* Jcr: コンテンツノードのない参照を持つリソースを移動する場合の NPE。NPR-18664
* プレースホルダーが複数の Parsys コンポーネントを含んだページに表示されません。NPR-18645：CQ-110253 のホットフィックス
* AbstractCopyMoveCommand の並行性の問題。NPR-18591
* テキストを別の AEM インスタンスから Parsys コンポーネントにコピーする場合、Parsys が resourceType が設定されていない状態で作成されます。NPR-18511：CQ-4212306 のホットフィックス

### Platform {#platform-10}

* JCR インストーラーが、パッケージのインストール後にバンドルバージョンを更新しません。 NPR-18728：NPR-15135 のホットフィックス
* バイナリレスレプリケーション（BLR）は、作成と公開の環境を含むバイナリで失敗します。NPR-18704
* AEM環境での Apache Felix Http Bridge解決リクエスト。 NPR-18297
* 同じ構造を持つ複数のページが Sling コンテンツ配信と同時に複製される場合、レプリケーションは失敗します。NPR-18665：Granite-13712 のホットフィックス
* Sling 配布パッケージが構築されて、自動クリーニングされません。NPR-18601：Granite-16183 のホットフィックス

### 統合 {#integration-13}

* ライブラリフォルダーから公開されたオファーを表示すると NPE となります。NPR-18732：CQ-4214593 のホットフィックス
* アクティビティの開始／終了日が JCR で更新されず、ターゲットが特定の日付から「アクティブ／非アクティブの場合」に変更された場合にも更新されません。NPR-18612：CQ-104831 のホットフィックス
* AEM との Analytics 統合では、httpclient 接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。NPR-18497
* AEM との DTM 統合では、httpclient 接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。NPR-18495
* AEM との Target 統合で、httpclient 接続に対して接続タイムアウトやソケットタイムアウトが設定されていません。NPR-18494
* 追加のエクスペリエンスを追加した後、ターゲットアクティビティが無効化されます。NPR-18227：CQ-4201895 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-7}

* 画像マップは、HTL 画像コンポーネントで選択された座標を保持しません。 NPR-18530：CQ-4211584 のホットフィックス

### 翻訳 {#translation-5}

* 翻訳の検索結果に翻訳プロジェクト名が含まれません。NPR-18224：CQ-4210658 のホットフィックス

### Brand Portal {#brand-portal-1}

* タグ管理/タグ付けコンソールからAEMからBrand Portalへのタグの公開を有効にする。 CQ-4212165

## Forms {#forms-13}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-13}

#### Correspondence Management {#correspondence-management-6}

* フラグメントが保存されるまで、正しいデータが編集パネルに表示されません。NPR-19092
* ドキュメントフラグメントをレターに追加するのにかなり時間がかかります。NPR-18958
* データ xml ファイルに XML 宣言があり、POSTリクエストを通じてレターのレンディションが開始された場合、対応するレターがデータを表示できません。 NPR-18870
* CM アセットに実行されたアクションの監査ログが生成されません。NPR-16618

>[!NOTE]
>
>次の 2 つの問題の影響を受ける場合は、この CFP 追加オンパッケージをインストールしないでください。
>
>* Word/Web から CM テキストエディターにコピー&amp;ペーストすると、改行コンテンツが表示されます。 NPR-19530
>* 改行のないコンテンツを CM テキストエディターで折り返すことができない。 NPR-19449
>

#### アダプティブフォーム {#adaptive-forms-9}

* 繰り返し可能なパネルのパネルを追加すると、前のパネルのドロップダウンフィールドの値が削除されます。 NPR-18772
* 整数のみを受け入れるようにマークされたアダプティブフォームフィールドが、数値パッドからの特殊文字も受け入れます。NPR-18680
* ガイドルートパネルの initializer イベントでボタンタイトルを変更するスクリプトが機能しない。 NPR-18476
* ルールエディターで作成されたルールの右側のパネルにスクロールバーが表示されません。 NPR-18716

#### AEM Forms アプリケーション {#aem-forms-app}

* AEM Forms アプリがオフラインモードの場合、またはネットワークに接続されていない場合、Forms はアプリで正しくレンダリングされません。CQ-4218368

### Forms JEE インストーラー {#forms-jee-installer-13}

#### PDFG サービス {#pdfg-service-3}

* 指定されたブックマークレベルで PDF Generator が PDF ドキュメントを生成できません。CQ-4211102 のホットフィックス

## CFP7 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp-1}

AEM 6.2 SP1-CFP7 で更新された OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

AEM 6.2SP1-CFP7 で更新されたコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/cfp7_content_packages.txt)

AEM 累積修正パック 6.2 SP1-CFP6 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* タブレットのレイアウトモードでの非表示コンポーネントの効率的な管理。
* ハイブリッドデバイスでクイックアクションを導入しました。
* ライブコピーに関するコンポーネントレベルの同期の問題の解決。

### アセット {#assets-13}

* 必要な権限を持たないユーザーがアセットに対して操作を移動しようとすると、顧客がブロックされます。 NPR-18330：CQ-4212560 のホットフィックス
* 複数のスマートコンテンツサービスの設定を結合すると、ユーザビリティの問題が発生します。NPR-18273：CQ-4201557 のホットフィックス
* 約 1 回チェックアウトアクション/ワークフローをタイムラインコンソールから使用することはできません。 80 個のフラグメントがAssets フォルダーに追加されます。 NPR-18257：CQ-4211214 のホットフィックス。NPR-18251：CQ-4211216 のホットフィックス。
* メモリ不足でシステムがクラッシュし、アセットレポート中にページネーションが表示されません。NPR-17865：CQ-4209759 のホットフィックス
* 公開済みのビデオをエンコードされたビデオアセットで再生できません。NPR-17849：CQ-4210739 のホットフィックス
* PDFのサムネールは生成されません。 NPR-17831、NPR-17750：CQ-4210547 のホットフィックス
* Adobe CQ DAM Expiry Notification ジョブで、期限切れアセットが非アクティブ化されない。 NPR-17666：CQ-107766 のホットフィックス
* アセットに所有者が割り当てられていない場合、アセットの有効期限アクティビティは停止します。NPR-17665：CQ-4197946 のホットフィックス
* 150 を超える参照先を持つアセットフォルダーを移動すると、ヌルポインター例外が発生します。CQ-4200981

### Sites {#sites-13}

* Personalizationは、セグメント化ルールが IP 範囲に対して設定されている場合は、最初の IP に対してのみ機能します。 NPR-18121：CQ-83767 のホットフィックス
* historyShow プロパティが有効な場合、NumberFormatException が原因でログインに失敗します。 NPR-18073：CQ-101965 のホットフィックス
* マークされた削除済みページは、タッチ UI に表示されます。 NPR-18025：CQ-86694 のホットフィックス
* 多数（2000 以上）のオーディエンスを持つページをロードする場合のパフォーマンスの問題。NPR-17884：CQ-4209567 のホットフィックス
* ページ上の別の画像を削除した後は、画像を選択できません。 NPR-17711：CQ-4201323 のホットフィックス

### Platform {#platform-11}

* タッチ操作対応 UI のコントロールは、必要な権限を持つユーザーには表示されません。 NPR-17945：CQ-4211231 のホットフィックス
* タグピッカーフィールドに日本語タグがありません。NPR-17768：CQ-4210456 のホットフィックス
* FastQuerySize が有効な場合、getsize() クエリが誤った結果を返します。NPR-18018
* スタンバイインスタンスの Web コンソールにアクセスできません。 NPR-17861：Granite-14582 のホットフィックス

### Commerce {#commerce-2}

* クエリトラバーサルは、カタログのブループリントにセクションに対する条件が定義されていない場合に発生します。 NPR-18229：CQ-4211924 のホットフィックス

### Communities {#communities-2}

* PollingImporterImpl.によって AEM のシャットダウンが遅れます。NPR-18298：CQ-96133 のホットフィックス

### 統合 {#integrations}

* AEM Day HTTP Client 3.1 OSGI がダイジェスト認証を必要とするプロキシで設定されている場合に発生する可能性がある AEM Search コンポーネントエラーを解決。NPR 18128
* 継承を元に戻すためのチェックボックスがありません。 NPR-17753：CQ-4210139 のホットフィックスリクエスト
* 1 つのコンポーネントを複数のアクティビティでターゲティングする場合、優先順位を設定できません。NPR-18658：CQ-4210727 のホットフィックス
* /Etc/segmentation/group1 フォルダーの下に作成されたオーディエンスを選択するために /etc/segmentation フォルダーを参照できません。NPR-18522

### セキュリティ {#security-1}

* アセットの移動ウィザードは、ターゲットフォルダーに対する書き込み権限がない場合にハングします。NPR-18300
* Apache Sling API で org.apache.sling.servlets.post サーブレット（2.3.22）のアップグレードバージョンを使用して XSS の脆弱性を回避するリクエスト。 NPR-18963

### 翻訳 {#translation-6}

* 翻訳プロジェクトでは、プロジェクトが完了するまでアセットページを再度送信する必要はありません。 NPR-18249：CQ-4209908 のホットフィックス

### WCM - 基盤コンポーネント {#wcm-foundation-components-8}

* 編集可能テンプレートで WCM 基盤 Iparsys コンポーネントを使用できない。 NPR-18223：CQ-4210384 のホットフィックス
* 画像マップは、HTL 画像コンポーネントで選択された座標を保持しません。 NPR-18032：CQ-4211584 のホットフィックス
* HTL 画像コンポーネントがレンダリングされると、URL 内のファイル名が変更され、URL が破損します。 NPR-17908：CQ-4211587 のホットフィックス
* 変更を加えた後にページプロパティから終了できない。 NPR-17832：CQ-96110 のホットフィックス

## Forms {#forms-14}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、[AEM Forms リリース](aem-forms-releases.md)を参照してください。

### Forms アドオンパッケージ {#forms-add-on-package-14}

**Correspondence Management**

* レターのレンダリング中に、データディクショナリが繰り返し読み取られます。 NPR-18482：CQ-4210805 のホットフィックス
* com.adobe.livecycle.content クラスの JavaDocs を追加しました。NPR-18467
* レターの作成時に、レターの説明が保存されない。 NPR-18039
* テキストモジュールが保存され、テキストモジュールの式に開始または終了の式タグが含まれていない場合、エラーメッセージが表示されません。テキストモジュールがエラーメッセージを表示し、レターのレンダリングに失敗します。NPR-17798
* アドオンパッケージのインストール時にログに予期しないエラーが表示される。 NPR-18295

**Forms Manager**

* AEM Forms UI ですべてのアセットが古い順にリスト表示されます。ユーザーはアセットを新しい順に並べ替えることができません。NPR-18451

### Forms JEE インストーラー {#forms-jee-installer-14}

**Output サービス**

* AEM forms 6.2 の Output サービスのパフォーマンスの問題を改善しました。NPR-18033

**署名サービス**

* リモート ハードウェア セキュリティ モジュールでPDF ドキュメントに署名できません。 NPR-18017

## CFP6 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp-2}

AEM 6.2 SP1-CFP6 で更新された OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

AEM 6.2SP1-CFP6 で更新されたコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM 累積修正パック 6.2 SP1-CFP5 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* アセットの共有、移動、公開、ダウンロードに関する UI の問題をいくつか解決しました。
* 参照アセットを表示する際の移動ダイアログボックスの容量を増加しました。
* 非公開やバージョンのパージなど、WCM コンポーネントとワークフローに関するいくつかの問題を解決しました。
* ツールバーのアクションと Coral コンポーネントを表示する際のアクションバーの応答性を改善しました。

### アセット {#assets-14}

* Brand Portal への公開機能のパフォーマンスが向上しました。NPR-17189：CQ-4204150 のホットフィックス
* 「リンクを共有」オプションを使用してアセットを共有しても、フラットフォルダー構造を持つ zip ファイルがダウンロード用に作成されません。NPR-17513：CQ-4209381 のホットフィックス
* DAM でアセットを選択して「公開」をクリックしても、アセットの詳細ページに「Brand Portal に公開」オプションは表示されません。NPR-17351：CQ-94905 のホットフィックス
* DAM ワークフローステップでは、Session または ResourceResolver から取得したバイナリストリームを最終ブロックで閉じる必要があります。これにより、リソースリークの発生を確実に防止できます。NPR-17385：CQ-4209452 のホットフィックス
* DAM で Word ドキュメントをアップロードすると、ヌルポインター例外が発生し、ワークフローインスタンスが実行中の状態のままになります。NPR-17160：CQ-4207358 のホットフィックス
* 管理者以外のユーザーのメタデータエディターページで、期限切れのアセットに対して「共有」、「移動」、「公開」、「ダウンロード」ボタンが表示されます。NPR-16903：CQ-101440／CQ-104535 のホットフィックス
* 共有、移動、公開、コピーなどのアクションは、アセットコンソールの管理者ユーザーに対して表示されます。NPR-16902：CQ-4207111 のホットフィックス

### Sites {#sites-14}

* クラシック UI とタッチ UI のいずれかを使用してページを移動する場合、移動ダイアログに 150 を超える参照が表示されないので、ユーザーはこれらの参照を更新してページを再公開できません。この問題は、クラシック UI にプロパティ「maxRefNo」を導入し、サイト管理ノードで設定できるようにすることで修正されました。 `'/libs/wcm/core/content/siteadmin'`. このプロパティは、大量の移動操作が行われる前に表示される、参照の最大数（デフォルト値は 150）を指定します。ページに複数の参照がある場合、それらの参照は movePage ダイアログボックスには表示されません。この設定はノードに設定を適用することで、dam 管理とその他の管理にも機能します。 `'/libs/wcm/core/content/damadmin'` および `'/libs/wcm/core/content/miscadmin'` それぞれ。 NPR-17222：CQ-85878 のホットフィックス

* WCM コンポーネントを使用する場合、タッチ UI リッチテキストエディターで、スペースを含むハイパーリンクが削除されます。NPR-17698、NPR-17570：CQ-4206768 のホットフィックス
* ページのプロパティから非公開の要求ワークフローをトリガーすると、レプリケーション権限のないユーザーに対して JavaScript エラーが表示されます。NPR-17294：CQ-102064 のホットフィックス
* HTL 画像コンポーネントのレンダリングまたは書き出しをおこなうと、URL が数値に変更され、ファイル名が変更されるので、リンクが壊れます。NPR-17245：CQ-59616 のホットフィックス
* ネストされたローンチでローンチを削除すると、サブローンチが孤立します。NPR-17228：CQ-4202639 のホットフィックス
* Oak 1.4.13 が適用された AEM 6.2 でバージョンのパージを実行すると、ログに警告が繰り返し表示され続けます。NPR-17391：CQ-4206870 のホットフィックス
* ContextHub コンポーネント用の修正プログラムまたはアップグレードをインストールした後、コンテンツパッケージが /etc/segmentation/contexthub 内のすべてのセグメントを上書きするので、すべてのカスタム ContextHub セグメントが失われます。NPR-17250：CQ-79958 のホットフィックス
* ワークフローユーザーとしてネストされたグループを含むワークフローを実行する場合、WorkflowStatusProvider（pageinfo.json）によってワークフローインスタンスがロックアップされます。NPR-17555：CQ-4202056 のホットフィックス
* WCM ページエディターコンポーネントを使用する場合、オーサーインスタンスのタッチ UI 編集モードでは、ページの最後に膨大な空き領域が存在します。NPR-17510：CQ-4205441 のホットフィックス
* HTL 画像コンポーネントのレンダリングまたは書き出しをおこなうと、URL が数値に変更され、リンクが壊れます。NPR-17245：CQ-59616 のホットフィックス

### UI {#ui}

* アセットを選択して開発ツールをクリックした場合、遅い接続ではツールバーのアクションがアクションバーに表示されない場合があり、ページを再読み込みする必要があります。NPR-17568：CQ-108365 のホットフィックス
* アクションバーが更新され、coral-actionbar-container のかわりに coral-actionbar-primary と coral-actionbar-secondary の 2 つのコンテナが使用される必要があります。NPR-17591：Granite-15225 のホットフィックス

### Mobile-on-demand {#mobile-on-demand-2}

* AEM Mobile アプリケーションに対する「読み取り専用」権限を持つユーザーが、AEM Mobile Content Management ページからコンテンツをプレビューできません。 NPR-17390：CQ-4209690 のホットフィックス

### セキュリティ {#security-2}

* HTMLRendererServlet によって生成された出力の XSS 脆弱性。NPR-17136
* AEM Web Syndication フィードページで AEM バージョンの公開を防ぐリクエスト。NPR-16219

### Forms {#forms-15}

#### Forms アドオンパッケージ {#forms-add-on-package-15}

AEM Forms の修正は、このリリースで提供されるアドオンパッケージおよびその他のパッチインストーラーを通じて提供されます。詳しくは、AEM Forms リリースを参照してください。

**アダプティブフォーム**

* 添付ファイル付きのアダプティブフォームの場合、フォームが 2 回送信されると、afSubmissionInfo タグの重複エントリが送信済み XML に作成されます。 NPR-17364
* Google Chrome ブラウザーを使用中に、フォームから添付ファイルを削除した後に、同じ添付ファイルを再度添付しようとすると、エラーが発生します。NPR-17297
* ネストされた繰り返し可能な遅延読み込みパネルが XSD ベースまたは No-Form-model ベースのアダプティブフォームにある場合、フォームに入力された値はレコードのドキュメント（DOR）に保持されません。NPR-17176
* ルールエディターのエラーログに表示されるエラーを、JavaScript コードの try/catch ブロックの catch ブロックに追加する必要があります。NPR-16757
* フォーム内の添付ファイルをクリックすると、ブラウザーコンソールエラーがスローされ、添付ファイルプレビューが表示されません。NPR-17174

**Correspondence Management**

* 通信を作成の UI 機能は、UI にインラインテキストまたは空白行が追加された場合に壊れます。NPR-17748
* レターを編集用に開くと、ブラウザーが点滅します。NPR-17576
* 計算済みデータ辞書要素にリモート関数を追加する際に、関数の数がリモート関数を示すタブの長さより長い場合、タブにスクロールバーが表示されません。NPR-17359
* 読み込み用の API メソッド `com.adobe.icc.services.api.LetterInstanceService` が機能しません。NPR-17922、NPR-16008
* レターの編集中、テキストモジュールに追加された変数がデータ連結パネルに表示されません。NPR-17940
* HTMLの送信アクションでPOST方式を使用している場合は、Correspondence Management UI が起動しません。 NPR-17595

**Forms Manager**

* アダプティブフォームが AB テスト用に設定されている場合、「AB Testingを開始」をクリックしてもテストは開始されず、ブラウザーコンソールエラーがスローされる。 NPR-17838

**Forms サービス**

* OSGi Forms の静的コード分析で報告された問題を修正する必要があります。NPR-13951

#### Forms JEE インストーラー {#forms-jee-installer-15}

**Output サービス**

* AEM Forms 6.2 Output サービスを使用して特定のフォームをデータ XML と結合する場合、時間が 20 倍かかります。 現在は、Windows および Linux® 環境で修正されています。 NPR-17501

**LCM のインストール**

* AEM Forms 6.2 GM のビルドをインストールし、AEM 6.2 CFP を適用した後、LiveCycle Configuration Manager を実行すると、不要なセミコロンが「バージョン情報」に表示され、パッチのインストール日が更新されません。NPR-14322

**プロセス管理**

* TaskContext 変数が AEM Forms プロセスに入力されます。CQ-4211857

#### AEM Forms JEE バンドルパッケージ {#aem-forms-jee-bundles-package}

* JEE 管理 UI コンソールと OSGi コンソールのどちらを使用している場合でも、Forms ユーザーの機能は同じである必要があります。 NPR-17670

### CFP5 に含まれる機能パック {#feature-packs-included-in-cfp}

**Forms JEE パッケージ**

プロセス管理 - HTML ワークスペース

* ワークスペース手順を割り当てる際、添付ファイルまたはメモが複数ある場合に、「ワークスペースの添付ファイル」タブに添付ファイルまたはメモのカウンターが表示される必要があります。NPR-17771
* AEM JEE Forms で Office 365 のメール機能をサポートするリクエスト。NPR-13866

**Forms アドオンパッケージ**

Correspondence Management

* レターのプレビュー中にテキストエディターでフラグメントを編集する場合は、フラグメントで使用されるインライン条件ではなく、処理済みのテキストが編集用に表示されるはずです。 NPR-15748、NPR-17504

### CFP5 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp-3}

AEM 6.2 SP1 と CFP5 の間で更新された OSGi バンドルの一覧

[ファイルを入手](assets/do-not-localize/cfp5_osgi_bundles.txt)

AEM6.2 SP1 と CFP5 の間で更新されたコンテンツパッケージの一覧

[ファイルを入手](assets/do-not-localize/content-package-cfp5.txt)

AEM 累積修正パック 6.2 SP1-CFP4 は、AEM 6.2 SP1 の一般リリース以降にリリースされた主なお客様向け修正を含む重要なアップデートです。

この累積修正パックの主要点は次のとおりです。

* Camera Raw ファイルレンディションのアセット、タイムライン表示、画像の向きに関する修正をおこないました。
* 改善点

   * サイトでの WCM 起動
   * プロジェクトワークフロー
   * ContextHub コンポーネント

* Campaign、Mobile On-Demand、翻訳に関する修正
* アダプティブフォームのルールエディターでの操作性の向上
* フォームの Correspondence Management 用のインライン条件エディターの強化
* JEE 上の AEM Forms のプロセス管理と出力サービスに関する修正
* Forms Designer スクリプトエディター関連の修正

### Platform {#platform-12}

* への列の追加またはカスタマイズ **Assets オムニサーチ** オーバーレイによる結果 `/apps` は機能しません。 NPR-16737：CQ-4206785 のホットフィックス
* AEM 6.1 SP2 から AEM 6.2 SP1 へのインプレースアップグレード後、**診断ツール**&#x200B;ページが機能しなくなります。NPR-17121：CQ-4196786 のホットフィックス
* HTL：フォーラムを選択し、トピックと投稿を作成する際に、`Sightly SightlyCompiledScript` によって、`RequestDispatcherOption` に誤った `addSelectors` プロパティが追加されます。NPR-17008：Granite-16384 のホットフィックス

* `ReportImporter` で使用される `ManagedPollConfigs` に `CRON expressions` のサポートを追加しました。NPR-16608：CQ-4206066 のホットフィックス要求

* LDAP ユーザーのアバター画像をアップロードできません。NPR-16561：Granite-17013 のホットフィックス
* User Management 画面に表示される結果の数は、カード表示とリスト表示で異なります。 NPR-16241：Granite-16914 のホットフィックス
* Google Chrome ブラウザーでフルスクリーンモードで表示中に、ワークフロー通知の遅延読み込みが失敗します。NPR-17013：CQ-4207567 のホットフィックス

### アセット {#assets-15}

* 定義された方向を持つ画像を読み込む際に、画像の方向が正しく適用されません。NPR-16750：CQ-4204356 のホットフィックス
* 初期設定で「すべてを表示」が設定されている場合でも、アセットタイムライン表示にアセットが表示されません。NPR-16957：CQ-98780 のホットフィックス
* アセットにレンディションとして追加された `Camera RAW` ファイル（ARW、CR2、NEF、DNG、EPS など）を選択または削除できません。このようなファイルは、ユーザーがクリックすると自動的にダウンロードされます。 NPR-16949：CQ-4206846 のホットフィックス
* Assets UI の別のPDFー内でPDFを作成しても、作成したPDFは DAM UI に表示されません。 ただし、これらのPDFはCRX リポジトリには表示されます。 NPR-16833：CQ-4206501 のホットフィックス
* タッチ UI を使用して、アセットをそれ自体の直接の子ノードとしてアップロードすると、問題が発生します。アセットが以前に選択したアセットの直接の子としてアップロードされます。NPR-16534：CQ-4204287 のホットフィックス
* DAM UI で、アセットにコメントし、コメント内のユーザーにタグを付けても、メール通知が生成されません。NPR-16589：CQ-102318 のホットフィックス

### プロジェクト {#projects-3}

ワークフローがパージされると、プロジェクト ワークフローコンソールのページに NullPointerException が表示される。 NPR-17017：CQ-4194269 のホットフィックス

### Sites {#sites-15}

* `ContextHub` 内のファイルがオーサーインスタンス上で最小化されません。NPR-17022：CQ-79456 のホットフィックス
* WCM-Launch ローンチのプロモーションでは、ページの大きなツリーで構成されるローンチのプロモーションに時間がかかります。 NPR-16480：CQ-82731 のホットフィックス
* `ClientContext` セグメント条件レンダラーは、未完了または未完了のルールを使用してセグメント（またはオーディエンス）が作成された場合にクラッシュします。NPR-16759：CQ-4205104 のホットフィックス
* WCM ローンチでは、タッチ UI のページプロパティ内からアクションを開始した場合に、ローンチに関連付けられたページを非公開にすることはできません。 NPR-16560：CQ-4204681 のホットフィックス
* リンクリライターは、コロン「:」が JCR 名前空間を定義していると仮定し、コロンを含む href 値を誤って書き換えます。NPR-16753：CQ-4203762 のホットフィックス
* WCM-Design Importer で、テストインポーターページを開き、zip ファイルをアップロードしようとすると、それが以前にアップロードされて削除されている場合に問題が発生します。 NPR-16486：CQ-90962 のホットフィックス
* への移動 **[!UICONTROL グローバルナビゲーション]** firefox またはGoogle Chromeのブラウザーを使用したパネルで、異なるユーザーエクスペリエンスが得られます。 Firefox ブラウザーには、 **[!UICONTROL ツール]** メニュー。 Google Chrome ブラウザーには、次の項目が表示されます **[!UICONTROL ナビゲーション]** メニュー。 NPR-16770：CQ-4200456 のホットフィックス

### Campaign {#campaign}

* AEM キャンペーンテンプレートをテストし、「追加データ」を含めるようにシードアドレスを変更する際に、タッチ UI Context Hub でAdobe Campaign ドロップダウンが表示されなくなります。 NPR-16771：CQ-105748 のホットフィックス

### Mobile on-demand {#mobile-on-demand-3}

* AEM オーサーからのパブリケーションにプリフライトを実行すると、5 秒以上かかるプリフライトアクションにより、AEMM - AEM PECS 統合 Splunk ダッシュボードで異常なスパイクが発生し、多数のステータスリクエストが発生します。 NPR-16908：CQ-4207055 のホットフィックス
* AEM-6.2-SP1-CFP1-1.0 アップデートのインストール後、AEM Mobile の設定管理が失敗します。NPR-16909：CQ-4204892 のホットフィックス

### 翻訳 {#translation-7}

* 6.2 SP1 - CFP1 のインストール後、翻訳ジョブのプレビューが動作しません。NPR-16481：CQ-4204655 のホットフィックス
* 翻訳を使用して作成された言語コピーは、ローカルの国のライブコピーではなく、ルートプライマリを指します。NPR-17257：CQ-4208287 のホットフィックス

### セキュリティ {#security-3}

* ファイルのバイナリを AEM にアップロードする際に MIME タイプ検出が実行されません。NPR-16617
* LDAP ユーザーのアバター画像のアップロードに関する問題。NPR-16561

### Forms {#forms-16}

#### Forms アドオンパッケージ {#forms-add-on-package-16}

**アダプティブフォーム**

* アダプティブ Forms エディターで、head.jsp の Target Setting コメントを新しい Context Hub ステートメントに置き換える必要があります。 NPR-17173
* アダプティブ Formsのルールエディターで、 **[!UICONTROL 項目を選択]** イベントを「null」として表示します。 NPR-17139
* 送信されたフォームは、順方向矢印（>）を使用して前方に移動することで、再送信されます。 NPR-17080
* AJAXを介してアダプティブフォームを送信する際に、エラーが発生した場合、「error」コールバック関数は呼び出されません。 NPR-17034
* 実行時にルールエディターで「**[!UICONTROL フォームを保存]**」ボタンをクリックしてもフォームが保存されません。NPR-16905
* 静止テキストは、アダプティブフォームではタブ順序から除外する必要があります。NPR-16749
* 十進数フィールドの計算値が正しく表示されません。NPR-16596
* ヘルプコンテンツを表示するアイコンは、アダプティブフォームのタブ順序に含める必要があります。NPR-16484
* タイプの正規表現のサポート `dataRef=C:/Users/`が含まれる **[!UICONTROL デフォルトの事前入力サービス設定]**. このタイプは、アダプティブFormsのデータの事前入力用です。 NPR-16425

* ネストされた遅延読み込みシナリオがある場合、すべてのパネルで検証が正しくトリガーされません。NPR-15821

**Correspondence Management**

* レターに空白のテキストモジュール（テキストのないモジュール）が含まれる場合、レターのレンダリングが失敗します。NPR-17054
* 改行とタブスペースは、テキストエディターにペーストした後で、コンテンツから削除されます。NPR-17039
* テキストモジュールが多数のレターで参照されている場合、テキストモジュールの参照の表示に時間がかかります。NPR-17035
* ドキュメントフラグメントの参照の編集、保存、削除、設定に時間がかかります。NPR-17033
* 均等揃えされたテキストは、レターをプレビューする際に、異なるフォントでレンダリングされます。NPR-16976
* 検索されたテキストに複数の語句が含まれる場合、検索機能が正しく動作しません。NPR-16920
* ブラウザーにテキストエディターツールバーが断続的に表示されます。NPR-16919
* 構文 **[!UICONTROL フォームを保存]** ルールエディターからは機能しません。 NPR-16905
* Internet Explorer を使用してデータ辞書に基づいてテキストモジュールを作成する際、フォント ドロップダウンでフォントファミリーが設定されない。 NPR-16944
* テキストフラグメントを作成すると、レターのプレビュー時にレターのフォントが変更されます。NPR-16830
* ドキュメントフラグメントの先頭または式の間にタブスペースがあるレターは、レンダリングまたはプレビューできません。NPR-16769

**モバイルフォーム**

* モバイルフォームプレビューでは重なり合うコンテンツが表示されるが、フォームは PDF レンダリングに対して正しく表示されます。NPR-17105

**Forms ポータル**

* 送信されたフォームの「**[!UICONTROL ダウンロード]**」リンクをクリックすると、PDF フォームではなく HTML ページが開きます。NPR-17082

* `Upload Comments` 送信済みインスタンスの場合、ファイル添付は UI に表示されませんが、CRX リポジトリに格納された XML には存在します。 NPR-17075

**Reader Extensions サービス**

* 特定のファイルは、AEM Forms OSGi のインストールで Reader 拡張されていません。NPR-16625

#### Forms JEE インストーラー {#forms-jee-installer-16}

**コア**

* アップグレードプロセス中に、Configuration Manager がタイムアウトで失敗します。 NPR-16774（[コンポーネントレベルでの操作のタイムアウトの設定](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)を参照）。

**プロセス管理 - HTML ワークスペース**

* 「開始タスク」からのスタートポイントは、スタートポイントの送信時に送信されたデータで始まりません。NPR-16917
* HTML ワークスペース内でフォームの「**[!UICONTROL 戻る]**」ボタンをクリックすると、フォームが閉じられずにグループキューに戻ります。
NPR-16352

**プロセス管理**

* 以前のタスクの表示名をプロセスインスタンス内の次のタスクのいずれかに設定できるようにします。NPR-15382

**Output サービス**

* Output サービスは、に「ミリ秒」フィールドを追加するように変更されたPDFを処理できません `date-time format` メタデータ。 NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer のスクリプトエディターでは、フォームのプロパティのデフォルト値が `Calculate Event` および `Validate Event` に適用されません。NPR-15921

### CFP4 に含まれる機能パック {#feature-packs-included-in-cfp-1}

**Forms アドオンパッケージ**

* Correspondence Management 用のインライン条件エディターの機能強化。NPR-10981

### CFP4 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp-4}

AEM 6.2 SP1 と CFP4 の間で更新された OSGi バンドルのリスト

CFP3 の主なハイライト：

* ダイジェスト認証を使用したプロキシを使用した、クラシック UI および AEM 検索コンポーネントの検索機能を効率化しました。
* アセットのアップロードとアセットメタデータの表示の問題を修正しました。
* タイトルに特殊文字が含まれる場合の、フォルダーの作成時やページの移動時の問題を修正しました。
* タッチ UI でのターゲティング同期オーディエンスの使用、キャンペーンの公開および目標指標の選択に関する修正
* 翻訳ジョブの同期の問題を解決しました。
* Forms 事前入力サービスのセキュリティを強化しました。
* Forms ポータルのドラフトと送信コンポーネント、および Barcoded Forms サービスの改善
* ファイル添付ウィジェットまたは遅延読み込みフラグメントを含むアダプティブフォームの使い勝手を向上しました。
* 検索機能の強化、削除されたアセットのログ、データ辞書の読み込みなど、Correspondence Management での操作性が向上しました。

### Platform {#platform-13}

* **ModelAdapterFactory** の競合状態。2 つのスレッドが同じフィールドを挿入しようとすると、モデルが構築できない可能性があります。NPR-16443：SLING-6584 のホットフィックス
* の下にオーバーレイされたファイル（JSP またはJavaScript ファイル）間の競合を検出するための、パッケージマネージャーの「検証」オプション `/apps` の下のホットフィックスに含まれるもの `/libs`. その後、影響を受けるオーバーレイのベースを変更して、の下にあるファイルからの変更を含めることができます `/libs`. NPR-16216：CQ-81729 のホットフィックス
* パブリッシャーの起動後、error.log へのロギングが数秒後に停止し、再度実行するためにクリアする必要がある場合があります。ログフレームワークを更新し、Sling ログを提供するリクエスト。NPR-15913：Granite-15452 のホットフィックス
* HTL JavaScript Use API 実装の失敗を回避するために JavaScript &quot; `use"` API を更新するリクエスト。NPR-16461：SLING-6780 のホットフィックス

### Sites {#sites-16}

* AEM 6.0 から AEM 6.2 にアップグレードした後、多数のクエリが原因でタグを検索する際に、クラシック UI のパフォーマンスが遅くなります。この問題を解決するには、次の手順に従います [タグ付けコンソール（クラシック UI）のレプリケーション状態を無効にする](#disable-replication-status-in-tagging-console-classic-ui-npr) フォローできます。 NPR-15842：CQ-4201748 のホットフィックス。

* タッチ UI でページを作成する際、「名前」フィールドの入力チェックで、特殊文字「アポストロフィ」がチェックされません（クラシック UI と同じ）。 したがって、ページを移動できません。NPR-16404：CQ-4205321 のホットフィックス。
* リッチテキストエディターで 2 つの行に異なるスタイルを適用して結合すると、2 つ目の行に適用されたスタイルが削除されます。NPR-16389：CQ-4203835 のホットフィックス。
* タッチ UI サイト画面で、サブページのないページ内にページを貼り付けようとすると、「貼り付け」ボタンが使用できないので、機能しません。 NPR-15894：CQ-4201696 のホットフィックス。
* コンテンツファインダーパネルの「ページ」タブをスクロールすると、クラシック UI ではページのセットが無限に表示されるのに対して、タッチ UI では繰り返さないページのセットが制限されて表示されます。 NPR-16271：CQ-4202371 のホットフィックス
* ライブコピーのページプロパティをタッチ UI で開き、変更せずに「保存」をクリックすると、「ライブコピー」タブが書き出され、LiveSync Config ノードが作成されます。NPR-16327：CQ-108562 のホットフィックス
* フォーム制約は `ConstraintMessage` プロパティを読み取りできません。NPR-16388：CQ-101330 のホットフィックス
* `wcm/foundation/components/parsys` コンポーネントは 「**[!UICONTROL コンポーネントをここにドラッグ]**」プレースホルダーを表示しません。NPR:16748：CQ-4205187 のホットフィックス

### アセット {#assets-16}

* 6.2 SP1 または Hotfix 12430 のインストール後に、pdf ラスタライザーが動作を停止し、メモリ不足の問題が発生します。NPR-15991
* 文字列プロパティ `documentNumber` のメタデータが日付として表示されるが、数値である必要があります。NPR-16134：Granite-16916 のホットフィックス
* タイムラインイベントのバルーンのテキストが切り捨てられます。NPR-16226：CQ-85226 のホットフィックス
* タイトルに特殊文字が含まれるコンテンツ階層にフォルダーを作成すると、これらの文字のエンコードされたバージョンが表示されます。 NPR-15935：CQ-4202987 のホットフィックス
* 「作成」ボタンの使用時に表示される動作に一貫性がないので、ユーザーがアセットのアップロード中にアセットをアップロードしたり、フォルダーを作成したりできません。 NPR-16410：CQ-4204793 のホットフィックス
* AEM オーサリングの記事表示から共有 HTML リソースをアップロード中に予期しないエラーが発生します。NPR-16133：AEMM-4155970 のホットフィックス

### 統合 {#integration-14}

* ダイジェスト認証でプロキシ認証を有効にすると、AEM検索コンポーネントが ConcurrentModificationException をスローする。 NPR-15309：CQ-4199191 のホットフィックス
* AEMで「Target A/B テスト」アクティビティを作成する場合、オーディエンスは Target に同期されず、「オーディエンスがありません」と表示されます。 NPR-16229：CQ-4204210 のホットフィックス
* SP1+NPR-11577 v1.2 をインストールした後、Touch UI でターゲティングをおこなっているときに、目標指標に「Analytics 指標を使用」を選択した場合、指標のドロップダウンリストが読み込まれません。NPR-16129：CQ-4204316 のホットフィックス
* ターゲティングを使用する場合、キャンペーンを公開しても、ブランドとメイン部分を含むツリー全体が自動的には公開されません。 NPR-15855：CQ-94630 のホットフィックス

### 翻訳 {#translation-8}

* Sync Translation Job が自動的にトリガーされ、AEMのポーリングが、翻訳プロジェクトをポーリングせずに実行されるようになりました。 NPR-15163：CQ-90856 のホットフィックス

### Forms {#forms-17}

#### Forms アドオンパッケージ {#forms-add-on-package-17}

**アダプティブフォーム**

* アダプティブフォームを添付ファイルと共に保存する際に、添付ファイルのフルパスがに追加されます `fileAttachment` 添付ファイル名ではなく、生成された XML のタグ。 NPR-16529
* XDP ベースのアダプティブフォームでは、事前入力 XML に `afData/afBoundData` ラッパーがなくても、送信済み XML に `afData/afBoundData` ラッパーが存在します。NPR-16118

* 数値フィールドの指数表記：アダプティブフォームを使用する際に、合計 10 文字を超える小数の数値を入力すると、送信された XML でその数値が指数表記に変わります。NPR-16106
* 添付ファイルコンポーネントと遅延読み込みフラグメントの両方を含むフォームの場合、送信されたデータ xml には添付ファイルコンポーネントの情報が含まれません。NPR-16022
* 遅延読み込みが有効な繰り返し可能パネルで、繰り返し可能な親要素がない場合、パネルの 2 番目のインスタンス内の繰り返し可能な子要素は繰り返しに失敗します。NPR-15944
* フォームエディターでフラグメント内にフラグメントを保存しようとすると、フラグメントモデルルートに子フラグメントの値が入力されません。 NPR-15943
* 項目が 1 つだけのチェックボックスを作成し、項目のタイトルを非表示にしたままチェックボックスのタイトルを表示しようとすると、項目のテキストが空の場合、辞書の作成アクションは `ArrayIndexOutOfBoundException` をスローします。辞書が作成されず、画面にエラー応答が生成されません。NPR-15816
* 添付ファイルウィジェットを含むアダプティブフォームの場合、添付ファイルをプレビューした後、フォームの一部が無効になります。
NPR：16611

* 複数の添付ファイルを許可する添付ファイルウィジェットの場合、以前の添付ファイルが既にあるウィジェットに添付ファイルを含んだ新しいフォームインスタンスを送信すると、エラーコードが表示されます。 このエラーは、実際のコンテンツではなく、追加された添付ファイルを開いたときに発生します。 NPR-16258
* `file://`、`http://`、`ftp://` などのプロトコルを使用して、フォームの事前入力サービスを不正アクセスから保護します。参照： [Configuration Manager を使用した事前入力サービスの設定](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15414

* 検証ステップでアダプティブフォームをHTMLではなくPDF形式でレンダリングし、すべての添付ファイルをPDFに追加して、印刷でフォーム全体が表示されるようにすることをリクエストします。 NPR-9011

**Correspondence Management**

* プレビューまたは編集モードでレター内のテキストフラグメントを操作する際に、テキストがリストに変換されると、レター機能全体が機能しなくなります。 そして、JavaScript エラーが生成されます。 NPR-16460
* XSD ファイルを読み込んで Correspondence Management ノードにデータディクショナリを作成すると、XSD がアップロードされルートノードが選択されるたびにブラウザーが応答しなくなり、失敗します。 この問題はブラウザーに依存せず、サーバーログには表示されません。NPR-16452
* Internet Explorer ブラウザーを使用してレターをプレビューし、コンテンツのフォントサイズを編集しようとすると、フォントサイズドロップダウンで 8 ～ 72 の間の重複の値が表示されます。NPR-16387
* フローティングフィールドが XDP フラグメントからの入力フィールドとして表示される場合、Internet Explorer ブラウザーの使用中にレタープレビューでフィールドが展開されません。 NPR-16367
* プレビューから直接レターを送信しようとすると、レター名のポップアップが非表示になっているので、正しく表示されません。NPR-16353
* レターの編集中に追加された行スペースは、プレビューーウィンドウに反映されません。テキストフラグメント内のリストの場合、PDF 出力で正しい間隔が表示されません。NPR-16267
* Internet Explorer ブラウザーを使用してテキストドキュメントフラグメントで作業しているとき、カーソルがテキストインデントを許可しないので、テキストにインデントを設定しようとすると失敗します。 NPR-16128
* 既存のテキストドキュメントフラグメントに対してデータ要素を追加または変更すると、時間がかかり、ユーザーに通知されない場合があります。 NPR-16102
* スクロール可能なコンテンツを含むレターを Internet Explorer ブラウザーでプレビューしているときに、ブラウザーのスクロールバーがレターのスクロールバーと重なります。 そのため、右側のフラグメントではコンテンツ全体を表示できません。NPR-16068
* Google Chromeのブラウザーを使用してテキストドキュメントフラグメントを作成または編集する際に、色選択ドロップダウンが自動的にポップアップ表示され、削除できません。 ユーザーがフラグメントを編集するには、データ入力のタイプとしてリストを選択する必要があります。 NPR-16067
* `Letterinstance` API の使用中にメソッド `import com.adobe.icc.services.api.LetterInstanceService` が機能しません。NPR-16008
* Asset Composer 設定で日付の表示形式を `locale=en_US; dateFormat=MMM dd,yyyy;` に変更すると、期待どおりに動作せず、日付の形式が無効な文字として表示されます。NPR-16007
* 再オーサリング中のレター内のデータリンケージのタイプは、以前と異なる方法で設定された場合でも、「ユーザー」と表示されます。 NPR-16619

**Forms ポータル**

* ドラフトコンポーネントと送信コンポーネントのアップグレードシナリオが、データベースサンプルの実装では動作しません。NPR：16752

**Barcoded Forms サービス（BCF）**

* Barcoded Digital サービス（BCF）の静的コード分析は、問題を報告します。NPR-13855

#### Forms JEE インストーラー {#forms-jee-installer-17}

**プロセス管理 - HTML ワークスペース**

* 「file://」、「http://」、「ftp://」などのプロトコルを通じた不正アクセスからフォーム事前入力サービスを保護します。 詳しくは、を参照してください [Configuration Manager を使用した事前入力サービスの設定](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15434

**ユーザー管理**

* SAML ログイン画面に、AEM 6.2 サーバー上の不適切なバージョン（6.1.0）が表示されます。NPR-13825
* AEM Forms がシングルサインオン（Kerberos）認証を設定している場合、ログイン試行中にユーザー認証に失敗すると、エラーコード「404」が返されます。ページを更新した後でのみ、ユーザーはログインサイトにリダイレクトされます。NPR-15015

#### Forms Designer {#forms-designer-1}

* 辞書のスペルチェックでフォームロケールをフランス語（カナダ）に変更しても、AEM Forms Designer では機能しません。
NPR-15896

### CFP3 に含まれる機能パック {#feature-packs-included-in-cfp-2}

**Forms アドオンパッケージ**

* Correspondence Management でアセットを削除すると、警告メッセージが error.log ファイルに記録されます。 NPR-13225
* Correspondence Management でレターをプレビューしているときに、レターのタイトルやラベルのみを検索するのではなく、テキストフラグメントコンテンツ内のテキストを検索できるように、検索機能を強化しました。 NPR-16103

### CFP3 に含まれている OSGi バンドル {#osgi-bundles-included-in-cfp-5}

AEM 6.2 SP1 と CFP3 の間で更新された OSGi バンドルのリスト

[ファイルを入手](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt).
累積修正パック 2 の主なハイライトは次のとおりです。

* Sling フレームワークおよび操作を含む、AEM プラットフォームの安定性の修正とパフォーマンスの向上
* アセット管理を改善し、アセットのアクセス、移動、検索、アップロードおよび公開に関するいくつかの修正をおこないました。
* コンテンツフラグメント、アンカープラグイン、スライドショー、ContextHub コンポーネントの修正により、サイトのオーサリングと管理を改善しました。
* テキストエディター、オムニサーチ、バリアント作成プロセスなど、タッチ UI に関するいくつかの修正をおこないました。
* 翻訳ワークフローを改善しました。Azure ポータル用の新しい変換 API を使用するために Microsoft® コネクタを強化しました。
* プロジェクトとキャンペーンの修正点
* アダプティブフォーム、Correspondence Management、フォームポータルの機能を修正し、オーサリングと管理を強化しました。
* Forms の JEE コア、XTG、および HTML Workspace コンポーネントを修正しました。

### Platform {#platform-14}

* Sling フレームワークを直接参照するページが編集された場合に `SlingPostProcessor` がトリガーされます。NPR-15754：CQ-104153 のホットフィックス

* のタグの値 `tagBasePath` ページコンポーネントに移動している間、クラシック UI ダイアログボックスでプロパティが取得されない。 NPR-15543：CQ-4199950 のホットフィックス

* Sling 処理の実行中に、「chunk_n_n-1」 という名前があると、`SlingFileUpload handler.getLastChunk` は空のチャンクで永久ループに巻き込まれます。NPR-15455：SLING-5701 のホットフィックス

* インターフェイスが別のインターフェイスを拡張する場合、スーパーインターフェイス上のインジェクト可能なメソッドは正しく挿入されません。NPR-15202：SLING-5710 のホットフィックス。
* `com.adobe.granite.infocollector.impl.FilesTraversal` 関数呼び出しの使用時に、潜在的なヌルポインター例外を防ぐことができません。NPR-15169：CQ-4197640 のホットフィックス
* 一部の二次ノードではワークフローの状態が一貫しておらず、そのノードの監視イベントをディスパッチ中にエラーが表示されます。NPR-15701：Granite-13786 のホットフィックス
* ユーザーが CRXDE でノードを選択します（例： `/content/dam/`）に設定します。 次に、「アクセス制御」タブをクリックし、アクセス制御リストが存在することを確認します。 これで、一部の要素をドラッグ&amp;ドロップすると、選択した要素ではなく、要素が移動します。 NPR-15696：Granite-16300 のホットフィックス
* 別のユーザーとして実行する際に、ドロップダウンリストからユーザーを選択すると、ユーザー全体がポップアップ表示されなくなります。NPR-15774：CQ-4201738／Granite-11895 のホットフィックス
* オムニサーチでは、自動入力された提案を含むタグでの検索は機能しません。NPR-15088：GRANITE-14426 のホットフィックス。
メモ：この修正には Oak CFP 1.4.11 以降が必要です。

### Mobile AEM Author {#mobile-aem-author}

* ハイブリッドアプリケーションで AEM Mobile と ContentSync パッケージを使用する場合、AEM は、アプリケーションが要求したものの代わりに、最も古いパッケージを使用して、アプリケーションが作成したフェッチ要求（タイムスタンプ付き）に応答します。NPR-15749：CQ-104153 のホットフィックス

### Sites {#sites-17}

* WCM コアのワークフローインボックスの変更ステータスは、ユーザーがワークフローをアクティブ化した後にページを変更しても変更されません。 NPR-15684：CQ-4196974 のホットフィックス
* タッチ UI 用リッチテキストエディターのアンカープラグインで、アンカーアイコンをクリックして名前を追加すると、準拠していないHTML5 が生成される。 アンカー要素の HTML5 タグに、「name」属性の代わりに「id」属性を追加する必要があります。NPR-15650：CQ-89782 のホットフィックス
* 多数のフィールドを含むメタデータスキーマを作成してコンテンツフラグメントメタデータに適用すると、コンテンツフラグメントメタデータ画面にスクロールバーが作成されず、フィールドを編集できません。 NPR-15478：CQ-4202622 のホットフィックス
* `TagInput` フィールドコンポーネントの編集時に、以前に設定した値がダイアログボックスのフィールドに表示されません。NPR-15464：CQ-4200360 のホットフィックス

* コンテンツフラグメントエディター UI でコンテンツフラグメントのバリエーションが作成される場合、サイドパネルにスクロールバーが表示されず、すべてのバリエーションが移動されません。 NPR-15445：CQ-4199444 のホットフィックス
* ユーザーを直接グループから削除すると、継承されたグループに追加されます。NPR-15400：CQ-98758 のホットフィックス
* WCM オーサリング：タッチ UI オーサーは、名前にコンマが含まれるページを編集できません。NPR-15396：CQ-4199723 のホットフィックス
* オーサリングにタッチ UI を使用している場合、関数 `Granite.author.editableHelper.doSelectParent` が引数を誤った順序で渡すと、JavaScript エラーが発生します。NPR-15349：CQ-4198594 のホットフィックス
* ContextHub セグメントが、オプトアウト Cookie が存在する場合でもエクスペリエンスを表示します。NPR-15293：CQ-4198024 のホットフィックス
* クラシック UI のスライドショーコンポーネントでは、スライドを作成したり、画像をドラッグ＆ドロップしてスライドを作成できません。NPR-15281：CQ-4194164 のホットフィックス
* ユーザーには、権限に関係なく、サイト管理コンソールに「ページを作成」、「サイトを作成」、「ライブコピーを作成」、「起動を作成」、「カタログを作成」の各メニュー項目など、「作成」オプションが表示されます。NPR-15278：CQ-94436 のホットフィックス
* AEM 6.2 サービスパック 1 のインストール後、「サブページを含める」スライダーがページ起動時に機能しなくなります。NPR-15230：CQ-4198449 のホットフィックス
* バージョンのパージを拡張して、ブロック内のバージョンを取得して処理し、指定されたパスを XPath クエリに使用できるようにリクエストします。NPR-15186：CQ-109205 のホットフィックス
* Sites コンポーネントのページプロパティの「サムネール」タブに「消去」ボタンがありません。 NPR-15143：CQ-4196997 のホットフィックス
* ライブコピーを使用するサイトの場合、サイトAdmin Consoleの列ウィンドウで「ライブコピー」チェックボックスをオンにしても、ライブコピーのステータスが正しく表示されず、HTMLのマークアップのみが表示されます。 NPR-15108：CQ-97086 のホットフィックス
* コンテンツフラグメントを編集する際に、ユーザーが投稿の応答を取得する前に「完了」（「√」）をクリックして編集をクリックすると、編集したコンテンツが正しく保存されません。NPR-15014：CQ-4194095 のホットフィックス
* タイムワープモード中に編集ページを閉じ、サイト管理から再度開こうとすると、ステータスでエラーが発生します `500`. NPR-14965：CQ-109647 のホットフィックス：
* Digital Asset Manager (DAM) UI で、「ユーザーピッカー」の「認証可能な項目を検索」を使用すると、「メモリ不足」の例外が発生します。NPR:15307：CQ-98542 のホットフィックス

### アセット {#assets-17}

* オムニサーチでアセットを検索した後、アセットを選択し、をクリックしてプロパティを編集しようとする **プロパティを表示**&#x200B;を選択し、続いて **保存** ボタンをクリックすると、空白のページにユーザーがリダイレクトされる。 NPR-15900：CQ-4202372 のホットフィックス
* アセットユーザーインターフェイスがイベントに応答しません。アセットを選択して「公開」または「レンディション」をクリックしても、アクティビティが発生しません。NPR-15828：CQ-4202247 のホットフィックス
* カード表示からアセットを公開しても、公開済みの状態を反映するようにカードが更新されません。 代わりに、ページが更新されます。 NPR-15826：CQ-102732 のホットフィックス
* アセットのホットフィックスを含む累積的なホットフィックス。NPR-15225
* アセットフォルダーの名前にアンパサンド（「&amp;」）文字が含まれている場合、そのアセットに移動するときにフォルダー名が正しく表示されません。 NPR-15775：CQ-4201735 のホットフィックス
* アセットファイルの名前にアンパサンド（&amp;）文字を使用すると、そのプロパティにアクセスする際に問題が発生します。NPR-15770：CQ-4201737 のホットフィックス
* Assets内を移動し、「列表示」表示モードを使用する際に、アセットを選択してクリックした後にページを更新すると、更新されたコンテンツではなくアセットの詳細が表示されます。 NPR-15768：CQ-4201727 のホットフィックス
* PDS 取り込みでは、PDF サービス用のライブラリのヒープにより、CPU 使用率が 100% 増加します。NPR-15606：Granite-12929 のホットフィックス
* Firefox ブラウザを使用して「マイリンク共有」 UI にアクセスしても、共有項目やユーザーが表示されず、画面が使用できません。 NPR-15539：CQ-4200992 のホットフィックス
* Digital Asset Manager の使用時に、ページが一連の画像に関連付けられている場合、画像を新しいフォルダーに移動するとページの関連付けが壊れます。 そのため、関連するページに画像の一部が欠落します。 NPR-15538：CQ-111479 のホットフィックス
* Dam Viewer コンポーネントで、「nosamplecontent」実行モードを使用すると、ダイナミックメディアでエラーが発生します。NPR-15449：CQ-4195425 のホットフィックス
* ビデオプロファイルの作成時に、高品質と中品質の両方のビデオエンコーディングプリセットが選択されている場合、行われた変更が保存されません。NPR-15447：CQ-4195482 のホットフィックス
* サーバーエラーの応答が原因で Brand Portal へのアセットのアップロードに失敗した場合でも、Brand Portal UI のステータスが「公開済み」に更新され、失敗したファイルを追跡しにくくなります。NPR-15442：CQ-4197968 のホットフィックス
* アセットフォルダーを Brand Portal に公開する際に、公開に 1 時間以上かかる場合、一部のファイルが公開できないことがあります。NPR-15441：CQ-4199493 のホットフィックス
* 列表示でアセットファインダーコンソールを使用する場合、フォルダーを作成しようとすると、再試行で成功しますが、失敗します。 NPR-15370：CQ-4199448 のホットフィックス
* DAM UI で選択されたアセットまたはフォルダーの名前にコンマがある場合、「参照」タブは使用できず、「複数の選択で参照のリストは使用できません」というメッセージが表示されます。 NPR-15362：CQ-4199721 のホットフィックス
* Brand Portal にフォルダーを公開しても、フォルダーの下のアセットが正常に公開されても、フォルダーの公開状態は変更されません。NPR-15292：CQ-4197667 のホットフィックス
* タッチ UI でアセットコンソールに移動する際に、特定のアセットをアクティブ化する際に表示される例外が発生します。NPR-15217：CQ-108779 のホットフィックス
* プロキシサーバー経由の接続時の YouTube へのビデオ公開。NPR-15109：CQ-110332 のホットフィックス
* ドットまたはピリオド（.）を含む名前のアセットを使用する
data-sly-resource は同じアセットに解決されず、出力パスはドットで終了します。NPR-15069：CQ-4195914 のホットフィックス
* AEM 6.2 をサービスパック 1 にアップグレードした後、アセットを Scene7 に同期できません。公開済みアセットの場合でも、`dam:Scene7FileStatus` プロパティが `UploadFailed` ステータスを表示します。NPR-15269：CQ-4197708 のホットフィックス

### ユーザーインターフェイス {#user-interface-5}

* 対象： **[!UICONTROL タッチ UI]**&#x200B;を選択すると、Internet Chrome ブラウザーバージョン 56.0.2924.87 を使用している間、type=&#39;datetime&#39;となった日付フィールドに保存された日付が表示されます。NPR-15383:GRANITE-16481 のホットフィックス
* **[!UICONTROL タッチ UI]** では、リッチテキストエディターは、HTML テーブルのレンダリング中にスレッドとキャプション要素を HTML テーブルから削除します。NPR-15267：CRTE-41 のホットフィックス
* `FileUpload Validator` は、autostart が true の場合や、`uploadFile()` が手動で呼び出される場合を処理できず、このような場合には無効な検証レポートが生成されます。NPR-15295：Granite-13499 のホットフィックス

* オムニサーチでは、を使用しているお客様を許可していません。 `/apps` に場所設定がリストされていることを前提としているので、列データソースを追加する場合 */libs/granite/omnisearch/content/metadata/*. NPR-13188：Granite-16479 のホットフィックス
* **[!UICONTROL タッチ UI]** を使用する場合、製品のバリアントは、製品と同じレベルで作成されません。バリアント作成プロセスの状態がユーザーに通知されません。NPR-15345：CQ-4198948 のホットフィックス

**Scene7**

* Scene7 ワークフローを実行すると、開いているファイルが閉じません。 共有プール設定を使用して 1 つの HttpClient インスタンスを維持再利用できるようにAEM-S7 サービスを改善するリクエスト。 NPR-15357：CQ-109958 のホットフィックス

### 翻訳 {#translation-9}

* 翻訳プロジェクトの使用時に、言語コピーを英語のプライマリから更新すると、11 個の異なるローンチがすべて同じ名前とソースルートで生成されます。ただし、ページ名が設定されたパターンに従っている場合は、それぞれのローンチルートが若干異なります。NPR-15605：CQ-4200699 のホットフィックス
* 言語ルートの名前にハイフンやダッシュが含まれている場合、ページの翻訳プロジェクトは作成されません。NPR-15171：CQ-96286 のホットフィックス
* Microsoft® が Azure ポータルで利用できる Microsoft® Translator API を使用できるように Microsoft® コネクタを更新するようにリクエストします。NPR-15320：CQ-101010 のホットフィックス

### プロジェクト {#projects-4}

* 20 個を超える非アクティブなプロジェクトがリポジトリーに存在しているにもかかわらず、プロジェクト画面に表示されるのは 20 個の非アクティブなプロジェクトのみです。NPR-15656：CQ-4200903 のホットフィックス

### Campaign {#campaign-1}

* キャンペーンの使用中 – ターゲティングと `MAC` - Test および Target 統合コンポーネントで、アクティビティの非公開によってプライマリUI のアクティビティステータスが更新されない。 NPR-15401：CQ-4199839 のホットフィックス
* AEM Commerce で製品を移動する際、製品の移動ウィザードでは、製品名、タイトル、参照先ページ、作成者、作成日に対する事前入力済みの値が見つかりません。NPR-15228：CQ-98617 のホットフィックス

### セキュリティ {#security-4}

* フォームに GET メソッドで CSRF トークンパラメーターを追加しました。NPR-15229

### Forms {#forms-18}

#### Forms アドオンパッケージ {#forms-add-on-package-18}

`**Adaptive Forms**`

* アダプティブフォームに入力 XML を事前に埋め込むと、デフォルト値が XML 内の空の値によって上書きされます。NPR-15721
* この `afData/afBoundData` 事前入力 XML にはがありませんが、送信された XML にはラッパーが存在します。 `afData/afBoundData` xml スキーマベースのアダプティブフォームのラッパー。 NPR-15541

* アコーディオンバーのタイトルは、「a」タグではなく、HTML の「h2」見出しで編集可能にする必要があります。NPR-15475
* フォームパネルのアコーディオンレイアウトは、スクリーンリーダーユーザーはアクセスできません。ユーザーは、JAWS や NVDA などのスクリーンリーダーソフトウェアを使用して、キーボードだけでアコーディオンタブに移動することはできません。NPR-15474

`**Correspondence Management**`

* ドキュメントフラグメントの参照の保存、削除、設定にかなりの時間がかかります。NPR-15939
* CCR UI で、複数のヘッダーの区切りを含むテキストの「アセットを管理」でタブの整列を設定しました。NPR-15818
* Google Chrome のタブで作成された整列コンテンツが含まれていても、テキストモジュールのサムネールに整列コンテンツが表示されません。NPR-15819

`**Forms Portal**`

* 事前入力サービスは、XDP Formsでは機能しません。 NPR-15466
* アダプティブフォームのドラフトとデータベースへの送信を保存する場合、何らかの理由（非アクティブ状態が長時間続いた後など）でデータベース接続が失敗すると、アダプティブフォームの状態が破損します。 NPR-15297

#### Forms JEE インストーラー {#forms-jee-installer-18}

`**Core**`

* 最新バージョンの Java™ 1.8.0_121-b13 にアップグレードした後は、管理者ユーザーインターフェイスは AEM Forms でアクセスできません。NPR-15330

`**XTG**`

* Output サービスを使用して特定のフォームを dataxml と結合する際の応答時間は、ES4 SP1 サーバーの所要時間と比較して 20 倍です。 NPR-15283

#### AEM Forms アプリケーション {#aem-forms-app-1}

* 未保存のタスクを回復する場合は、未保存のタスクの回復時に表示されるメッセージを明確にして、ユーザーエラーを減らす必要があります。NPR-15377
* AEM Forms アプリケーションが、カスタムテンプレートから作成されたフォームをレンダリングしません。NPR-15892
* ユーザーがAEM Forms アプリケーションにログインできません。 NPR-15891

AEM 6.2 SP2-CFP1 の主なハイライトは次のとおりです。

* サイトのレプリケーション機能を合理化： 

* ロールアウト、ライブコピー、書き込み障害の問題の修正

* タッチ UI の応答性が向上：

* アセットの検索
* サイズベースの並べ替え

* スマートコレクションのタグ管理を強化
* フォルダーに対する CRUD 操作中のアクセス制御を強化

### Platform {#previous}

* レプリケーションエージェントの起動中に `ReplicationQueue#forceRetry` API 呼び出しを削除するリクエスト。このような呼び出しは、特に多数のレプリケーションエージェントを持つ場合に、インスタンスの速度を大幅に低下させます。NPR-14032：Granite-13095 のホットフィックス
* `DurboImportConfigurationProviderService` OSGi 設定に対して、値の配列を格納できるフィールドをサポートするリクエスト。NPR-14570：CQ-108684 のホットフィックス
* AEM 6.2 への移行後にページで Sightly コンポーネントを使用すると、ページのプロパティダイアログボックスが機能しなくなります。NPR-14328：CQ-108355 のホットフィックス
* 以前にスケジュールされたジョブのスケジュールを解除しても、*/var/eventing/scheduled-jobs* の下の対応するノードは削除されません。NPR-14253：SLING-5666 のホットフィックス
* 管理者が削除されたユーザーとして動作しようとすると、ユーザーインターフェイスが更新できません。NPR-14247：CQ-107446 のホットフィックス
* Sightly コンポーネントで XSS 保護チェックが原因で、誤ったエンコーディングが発生する。 NPR-14004：CQ-93821 のホットフィックス
* 複数の問題を解決するために、Jackrabbit ファイルコンテナを 3.1.30 にアップグレードするようにリクエストします。 NPR-13454
* Sling 配布が配布パッケージをオーサー環境からパブリッシュ環境に同期すると、キャッシュエラーが発生します。 NPR-13034：Granite-13970 のホットフィックス

### Sites {#sites-18}

* VersionManagerImpl で、バージョン履歴から正しくないバージョンが削除される問題。NPR-14372
* WCM Sightly 基盤 Parsys コンポーネントが、コンポーネント宣言タグ名（`cq:htmlTag / cq:tagName`）を無視します。NPR-14225
* タッチ UI で JavaScript を通じて挿入されたコンポーネントを Sightly Parsys を使用してレンダリングする場合、ページが更新された後、カスタムデコレーションが無視されます。NPR-14122
* リンクなどのリッチテキストフィールドが複数作成される場合、タッチ UI ダイアログボックスで Target ドロップダウンリストが機能しない。 NPR-13911
* ダイアログボックス（タッチ UI）で複数のリッチテキストエディター（RTE）プロパティを使用してテキストフィールドを編集する場合、フォーカスがランダムに特定の RTE プロパティに移動します。NPR-13703
* デフォルトの標準ビデオコンポーネントは、ビデオのサムネールをレンダリングしません。 NPR-14976
* 情報は、テンプレートエディターの「ライブ使用状況」タブでゆっくりと読み込まれます。 NPR-14880：CQ-83417 のホットフィックス
* AEM 6.2 インスタンスに Hotfix-10936 をインストールすると、Iparsys コンポーネントが無効になります。 NPR-14330：CQ-106982 のホットフィックス
* AEM 6.1 SP1 への移行後、複数のロールアウトコンポーネントの問題とライブコピーの問題が発生します。NPR-15256
* ページロールアウトアクションは、複数のロールアウト設定でも、最初のレベルを超える子を作成できません。NPR-15055
* エディターからページプロパティダイアログボックスを送信すると、「ライブコピー」タブにある変更されていないデータが書き換えられます。 NPR-14693
* エディターからページプロパティダイアログボックスが送信されると、MSM Post プロセッサーは、リクエストの `msm:writeLiveCopyConfig` パラメーター。 NPR-14434
* ロールアウトコンポーネント、ライブコピー、および MSM のその他の側面に関する複数の問題。NPR-12235

### アセット {#assets-18}

* 解凍ワークフローで、画像ファイル名に特殊文字が含まれる画像を処理できない。 NPR-15227：CQ-103887 のホットフィックス
* 「条件を指定して繰り返し」式を持つアセットが正しく表示されません。`*CDN3835RLCEN*` レターテンプレートをプレビューすると、本文のターゲット領域にあるアセットが表示されません。複数の添付ファイルを許可する添付ファイルウィジェットの場合、以前の添付ファイルが既にあるウィジェットに添付ファイルを含んだ新しいフォームインスタンスを送信すると、エラーコードが表示されます。 NPR-14844

* スマートコレクションの作成時に、スマートコレクションを保存する際にスタイルタグが保持されません。NPR-15081：CQ-4195494 のホットフィックス
* 複数のユーザーが同時に検索している場合、タッチ UI でのアセット検索クエリの実行に時間がかかる。 NPR-15019：CQ-4195405 のホットフィックス
* タイプ `Long[]` のプロパティに対して抽出されたメタデータは、元のアセットを別の場所に再アップロードすると、タイプ `String[]` に変換されます。NPR-15016：CQ-4195005 のホットフィックス

* ユーザーが保存済みの検索やスマートコレクションを削除できない。 NPR-14924：CQ-108494 のホットフィックス
* 基になるメタデータスキーマのドロップダウンフィールドで TypeHint のブール値を使用して、アセットのメタデータを一括（追加モード）で編集するとエラーが発生します。NPR-14529：CQ-106876 のホットフィックス
* レプリケーション権限を持つユーザーは、アセットフォルダーを削除できるようになりました。 NPR-14321：CQ-88271 のホットフィックス
* チャネルエディターでビデオのビデオプロファイルを編集しようとすると、デザインダイアログボックスが開かず、エラーログで null ポインター例外が発生します。 NPR-14144：CQ-81101 のホットフィックス
* アセットのプロパティページに表示される、システム生成の「作成済み」タイムスタンププロパティが正しくありません。 NPR-13992：CQ-95029 のホットフィックス
* AEM Assets で、「読み取り」アクセスを持たないユーザーの重複アセットの検出を有効にするリクエスト。NPR-13851：CQ-102281 のホットフィックス
* ユーザーがプロパティページからアセットのメタデータを一括で編集できない。 NPR-13721：CQ-100703 のホットフィックス
* 重複アセットがアップロードされたときに、クラシック UI に正しくないエラーメッセージが表示されます。エラーメッセージに、アップロードが失敗した理由が示されません。NPR-13691：CQ-99272 のホットフィックス
* フォルダーに多数のアセットが含まれる場合、AEM Assets はリスト表示で一度に 50 個を超えるアセットをサイズ別に並べ替えできません。CQ-100588
* アセット/フォルダー URI が長すぎる場合、複数のアセットを選択すると、「応答コード - 414 （リクエスト URI が長すぎます）」というエラーが発生します。 NPR-13516：CQ-76076 のホットフィックス
* `Configure Columns` ダイアログボックスですべての選択肢を選択すると、アセットレポートページが応答しなくなります。NPR-13187：CQ-95589 のホットフィックス
* Safari および Internet Explorer のタグピッカーの予期しない動作。 NPR-13134
* アセット管理者の検索パネルで保存済みの検索を編集すると、保存済みの検索をネストされたスマート選択として保存できるので、環境の安定性に問題が生じます。NPR-13119：CQ-99460 のホットフィックス
* ファイル（またはフォルダー）を移動してから名前を変更した後、`cq:name` メタデータには新しいファイル名（フォルダー名）が反映されません。NPR-13036：CQ-99141 のホットフィックス
* 特殊文字を含む名前のアセットは、メールで共有されるダウンロードリンクからダウンロードできません。NPR-12872：CQ-95795 のホットフィックス
* アセットが多数ある場合に生成される標準のアセットレポートでは、検索がインデックスにヒットせず、CPU 使用率のスパイクが発生する大量のトラバーサルが発生します。 NPR-12811：CQ-84409 のホットフィックス
* 異なるネットワークから AMS AEM Assets オーサーインスタンスにアクセスする場合、フォルダーに対する削除権限がないとチャンクのアップロードを使用してアセットをアップロードできません。 NPR-12768：CQ-82715 のホットフィックス
* アセット検索レールを使用したタグベースのアセット検索では、先読み入力機能では、自体がルートパスに制限されず、すべての名前空間のタグが表示されます。NPR-12666
* StaticRenditions コンポーネントはヌルポインター例外を発生させます。NPR-12665
* バッジ通知 UI で、「入力をスキャンできません」というランタイム例外が発生し、ページが区切られる原因となるので、MissingMetadataNotificationJob を無効にするリクエスト。NPR-12500：CQ-93573 のホットフィックス
* タグフィールドの「編集を無効にする」オプションが、タッチ UI のアセットプロパティページで機能しません。NPR-12429：CQ-88835 のホットフィックス
* Companion App SMB 実装の AEM Assets 6.2 で API を修正しました。NPR-11099
* 以降 `Jquery` 更新すると、ユーザーはアセットコレクションを選択できず、コンテンツフラグメントのコンテンツを関連付けパネルで選択を確定できません。 NPR-14847：CQ-4194209 のバックポート
* クライアントサイドで無限の並べ替えを呼び出した場合でも、UI に現在表示されている記事／バナー／コレクションのみが並べ替えられます。NPR-14493：CQ-109926 のホットフィックス
* AEM mobile-on-demand サービス用のオムニサーチ機能の実装リクエスト。記事、コレクション、バナーのキーワード検索では一致は返されません。NPR-14093：CQ-101394 のホットフィックス
* ダイアログボックスで Coral-select コンポーネント（*granite/ui/components/coral/foundation/form/select*）を使用する際、選択された値に単一の項目が含まれていると、Internet Explorer（IE11 または Edge ブラウザー）で値の初期化が正しく機能しません。NPR-13395：CQ-101013 のホットフィックス

### プロジェクト {#projects-5}

* 翻訳方法を「人間」として、翻訳プロバイダーを「なし」として作成した翻訳プロジェクトを書き出す場合、GUID マッピングファイルがないので、translation_export_summary.xml ファイルが生成されません。 NPR-13137：CQ-91976 のホットフィックス
* AEM プロジェクトでは、due-date プロパティが設定されたプロジェクトを作成すると、サーバーとクライアントのタイムゾーンの違いによって、日付変換で時間が正しく設定されません。NPR-13003：CQ-98288 のホットフィックス
* 翻訳プロジェクトが更新されたときに、「サイトで表示」オプションが翻訳ジョブに含まれていません。NPR-12966：CQ-93740 のホットフィックス
* 書き出したサイトページ用に翻訳プロジェクトを作成すると、プレビューでは正しくレンダリングされません。NPR-12964：CQ-84627 のホットフィックス

### ワークフロー {#workflow-3}

* ワークフローコンソールの「アーカイブ」タブのペイロードリンクをクリックすると、応答コード「404」でエラーが返されます。 NPR-14993：CQ-4194977 のホットフィックス
* AEM のデフォルトのワークフローを使用する場合、CQ メーラーは、1 人のメンバーのメールアドレスがないグループにメール通知を送信できません。NPR-14804：CQ-91499 のホットフィックス要求
* タッチ UI のインボックスと通知バッジのパフォーマンス向上。NPR-14145：CQ-101125 のホットフィックス
* ユーザーがワークフローを開始する際、ワークフローインボックスコンソールからペイロードをプレビューできません。 NPR-13226：CQ-100275 のホットフィックス
* SAML 認証ハンドラーを使用して設定された「saml_request_path」 Cookie は、cookie セットにが追加で表示されます `?` 文字。 さらに、SAML 応答が AEM にポストバックされると、AEM「saml_request_path」クッキーは、既にエンコードされている文字のため無効な値を返します。NPR-13517：Granite-11722 と Granite-14414 のホットフィックス

### Dynamic Media {#dynamic-media}

* レプリケーション中に AEM アクティベーションがアーカイブジョブとして記録された際に作成および取り消された多数の `AEM-Scene7` Sling ジョブ。NPR-12835：CQ-86115 のホットフィックス

### セキュリティ {#security-5}

* WCMDebug フィルターの入力検証の問題を解決するリクエスト。NPR-12444：CQ-94890 のホットフィックス要求
* ローンチを作成ウィザードの使用中に XSS の動作を修正するプロアクティブなリクエスト。
NPR-13062：CQ-99577 のホットフィックス要求

#### Forms アドオンパッケージ {#forms-add-on-package-19}

`Adaptive Forms`

* アダプティブフォームを使用して繰り返し可能なパネルを作成する場合、パネルのタイトルを実行時に更新できません。NPR-15325
* 保存または送信時にラジオボタンのデフォルト値を設定して別の値を選択した場合、選択した値は事前入力に表示されません。 NPR-15304
* Google Chromeで、ドロップダウンリストに動的に値を入力し、選択した項目の値を送信するためのオプションイベントを使用すると、誤った動作が表示されます。 NPR-15198
* アダプティブフォームを使用して繰り返し可能なパネルを作成する場合、パネルのタイトルを実行時に更新できません。NPR-15181
* アダプティブフォームに対して編集モードを使用すると、「コンポーネントのハンドラーが無効です」や「guidelib が定義されていません」などのJavaScript エラーが発生します。 NPR-15112
* 繰り返しパネル内の遅延読み込みフラグメントが期待どおりに機能しません。NPR-13916、NPR-14785

`Correspondence Management`

* `'Repeat with condition'` 式セットを持つ Correspondence Management アセットが正しく表示されません。NPR-14844
* Correspondence Management アセット（レター、ドキュメントフラグメント、その他のタイプなど）を検索すると、ダウンロード用のキューアイコンがツールバーに表示されなくなります。NPR-14745
* リストモジュールの作成時に、アセット固有のプロパティ（編集可能、必須など）の切り替えが動作しません。NPR-14689
* 式ビルダーユーティリティのデータ要素パネルは、データディクショナリを選択せずに条件モジュールが作成された場合、読み込みを続けます。 NPR-14688
* レターのプレビュー時に、タブスペースを使用してコンテンツを表形式で整列することはできません。NPR-14481
* Correspondence Management アセットをユーザーインターフェイスから一括で書き出すと、AEM Forms サーバーは不要なログを生成します。NPR-15226
* レターをプレビューすると、均等配置されたテキストが別のフォントで表示されます。NPR-15468

`**Forms Portal**`

* フォームポータルで送信済みフォームの添付ファイルが、ポータルの送信から新しいドラフトが送信されると表示されません。NPR-13515

`**Forms Manager**`

* でナビゲーションを行う際 *フォームとドキュメント* ユーザーがアセットをコピーしてから別のフォルダーに移動すると、ディレクトリの「貼り付け」ボタンは表示されません。 CQ-111327

#### Forms JEE インストーラー {#forms-jee-installer-19}

`Rights Management`

* ユーザーログイン関連の監査イベントに無効な時間が記録されます。監査イベントの正しい時間は追跡できません。 NPR-13107
* Adobe Acrobat Reader と Microsoft® Office で、拡張認証で保護されたドキュメントを開けません。NPR-14482

`Process Management`

* HTMLWorkspaceで転送されたドラフトタスクが初期ユーザーに戻されても、タスクは初期ユーザーのキューに表示されません。 NPR-15178

`Assembler Service`

* AEM Forms で、3 つ以上の署名がある PDF/A-2b の検証に失敗します。NPR-14101

`XTG`

* プリンターバイパストレイを使用してドキュメントを印刷する場合、`GeneratePrintedOutput` 機能は右側のバイパストレイから用紙を取り込むことを許可しません。NPR-14079

#### Forms Designer {#forms-designer-2}

* 選択したフォームロケールをフランス語（カナダ）としてスペルチェックユーティリティを実行すると、Forms Designerがクラッシュする。 NPR-13740
* ユーザーがフォームフィールドのイベントの計算またはイベントの検証を選択し、言語を JavaScript に変更して&#x200B;**[!UICONTROL スクリプトエディター]**&#x200B;ウィンドウに `this.` を入力すると、Forms Designer がクラッシュします。NPR-12974

### CFP1 に含まれる機能パック {#feature-packs-included-in-cfp-3}

`Mobile Forms`（Forms アドオンパッケージ）：

* アダプティブフォームを XDP ファイルから作成する場合、アクセシビリティのタブは設定されたパターンに従いません。 NPR-12562

`Adaptive forms`（Forms アドオンパッケージ）：

* アダプティブフォームのルールビルダーでは、ロールベースのアクセスは提供されません。作成者がおこなった変更が追跡できません。NPR-12840

`Core` (Forms JEE インストーラー):

* サーブレットフィルターとしての CoreCross オリジンリソース共有（CORS）機能が JBoss®+ で有効になっていません。NPR-13050

## ソフトウェア配布による CFP のダウンロード手順 {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>AEM Formsをご利用のお客様は、AEM サービスパック、累積サービスパック、機能パックのいずれかをインストールした後で、AEM forms アドオンパッケージをインストールする必要があります。

CFP パッケージについては、ソフトウェア配布から直接ダウンロードするか、次の手順を実行します。

1. [ソフトウェア配布](https://experience.adobe.com/jp/downloads)を開きます。ソフトウェア配布にログインするには、Adobe ID が必要です。
1. ヘッダーメニューで「**[!UICONTROL Adobe Experience Manager]**」をタップします。
1. パッケージ名をタップし、「**[!UICONTROL EULA 条項に同意]**」を選択して、「**[!UICONTROL ダウンロード]**」をタップします。

## CFP のインストール手順 {#installation-instructions-for-cfp}

このセクションでは、CFP をインストールするための要件と手順について説明します。

### インストールの前に   {#before-you-install}

>[!NOTE]
>
>アドビが提供するオプションの機能パックは、リリースのバージョンと累積修正パックに依存関係があります。機能パックがインストールされている場合は、[AEM サポートチーム](https://experienceleague.adobe.com/ja?support-solution=General#support)に連絡し、AEM 6.2 用の累積修正パックとの互換性を確認してください。

>[!NOTE]
>
>パッケージをインストールする前に、新しいインストールパッケージごとに検証を実行することをお勧めします。事前検証は、インストール前に見つかったエラーを分析および報告し、そのようなエラー、オーバーレイ、権限を事前に警告します。
>

* AEM 6.2 サービスパック 1 が CFP の前提条件です。インストール手順について詳しくは、[AEM 6.2 サービスパック 1](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) のリリースノートを参照してください。

* 累積修正パックは AEM インスタンスから直接アクセスできる[ソフトウェア配布](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html)からダウンロードできます。
* （RDBMK または MongoDB）を使用したクラスターデプロイメントの場合、CFP パッケージは、パッケージマネージャーを使用する任意のオーサーインスタンスにインストールできます。

* 累積修正パックをインストールする前に、必ずAEM インスタンスのスナップショットを作成するか、バックアップを作成してください。
* CFP のアンインストールはサポートされていません。

### ソフトウェア配布を使用した CFP のインストール {#install-the-cfp-via-package-share}

既存の AEM 6.2 SP1 インスタンスに累積修正パックをインストールするには、次の手順を実行します。

1. パッケージをダウンロードするには、「[ソフトウェア配布](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip)」をクリックします。

1. [パッケージマネージャー](http://localhost:4502/crx/packmgr/index.jsp)を開き「**[!UICONTROL パッケージをアップロード]**」をクリックしてパッケージをアップロードします。

1. パッケージ名を選択して、「**[!UICONTROL インストール]**」をクリックします。

### 自動インストール {#automatic-installation}

CFP は、次の方法で実行中のインスタンスに自動インストールできます。

* サーバーの実行中に ../crx-quickstart/install にパッケージを配置します。パッケージは自動的にインストールされます。
* [パッケージマネージャーから HTTP API](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) を使用します。`cmd=install&recursive=true` を使用して、ネストされたパッケージをインストールします。

### インストールの検証 {#validate-installation}

1. 製品情報ページ（/system/console/productinfo）の「インストールされた製品」に更新バージョンの文字列「Adobe Experience Manager、バージョン 6.2.0.SP1-CFP20」が表示されています。
1. すべての OSGi バンドルが、OSGi コンソールでアクティブまたはフラグメントです（web コンソールを使用：/system/console/bundles）。

>[!NOTE]
>
>パッケージが正常にインストールされると、コンテンツパッケージが正常にインストールされたことを示す情報メッセージ、例えば「Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 installed successfully.」が表示されます。

>[!NOTE]
>
>AEM 6.2 SP1-CFP1 以降、Jackrabbit FileVault のログレベルは、ほとんどのメッセージで INFO から DEBUG に変更されました。AEM 6.2 SP1-CFP1 以降にインストールされたコンテンツパッケージのインストールログを取得するには、`org.apache.jackrabbit.vault.packaging.impl` の DEBUG ログレベルを有効にします。

### AEM Forms のインストール {#install-forms}

>[!NOTE]
>
>AEM Forms を使用していない場合は、この節をスキップしてください。

#### AEM Forms アドオンのインストール  {#install-aem-forms-add-on}

>[!NOTE]
>
>（**JEE 上の AEM Forms のみ**）JEE 上の AEM Forms に CFP をインストールする手順は、[AEM Forms JEE 上の CFP のインストール](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee)で説明しています。

1. AEM 6.2 SP1 CFP パッケージがインストールされていることを確認してください。
1. [AEM Forms リリース](aem-forms-releases.md)のリストから、使用しているオペレーティングシステムに対応する Forms アドオンパッケージをダウンロードします。
1. [AEM Forms アドオンパッケージのインストール](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)の記載どおりに Forms アドオンパッケージをインストールします。

#### AEM Forms JEE バンドルパッケージのインストール {#install-aem-forms-jee-bundles-package}

AEM Forms JEE の修正は、別個のインストーラーで提供されます。AEM Forms on JEE への CFP のインストールについては、[AEM Forms JEE への CFP のインストール](install-cfp-aem-forms-jee.md)を参照してください。

#### Forms Designer インストーラー  {#designer-installer}

1. アップデートをインストールするには、Designer6.2.0_&lt;言語>_Cumulative_QF.msp ファイルを実行します。
1. ようこそ画面で「**更新**」をクリックします。インストールが開始されます。
1. インストールが完了したら、「**終了**」をクリックします。

## DTM、分析、Target 接続のユーザーが設定できるタイムアウトパラメーター {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

AEM 累積修正パック 6.2 SP1-CFP7 以降のリリースでは、次の詳細に従って、上記のすべての接続で接続のタイムアウト期間を設定できるようになりました。

| **接続** | **接続タイムアウト&#42;** | **ソケットタイムアウト&#42;&#42;** |
|---|---|---|
| DTM | 30,000 ミリ秒 | 30,000 ミリ秒 |
| Analytics | 30,000 ミリ秒 | 30,000 ミリ秒 |
| ターゲット | 60000 ミリ秒 | 30,000 ミリ秒 |

* **接続タイムアウト&#42;** - 接続が確立されるまでのタイムアウト（ミリ秒）。0 のタイムアウト値は、無限タイムアウトと解釈されます。
* **ソケットタイムアウト&#42;&#42;** - タイムアウトするまでデータを待機する時間（ミリ秒）、または 2 つの連続したデータパケット間の無操作状態の最長時間。

## タグ付けコンソール（クラシック UI）のレプリケーション状態を無効にする（NPR-15842）  {#disable-replication-status-in-tagging-console-classic-ui-npr}

CFP 3 以降を使用している場合は、次の手順に従ってクラシック UI のタグ付けコンソールで複製ステータスを無効にします。

* オーバーレイ *「/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js」* 。対象： *`/apps`*

* `replicationStateRequired` の追加：行 #416 の後に「false」を追加しました。

```js
415 baseParams: {
416 count: "false",
417 "replicationStateRequired": "false"
418 },
```

## 最新の Java™ 8 アップデート 131 による例外のスロー（NPR-21355） {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>これらの設定は、Document Security を使用するAEM Formsのお客様に固有です。

NPR-21355 は CFP12.1 に含まれています。CFP12.1 以降をインストールする場合は、以下の手順を実行して、JBoss® アプリケーションサーバーに NPR-21355 を設定します。 Oracle WebLogic または IBM® WebSpehere アプリケーションサーバーで実行されている AEM Forms Server に CFP12.1 をインストールする場合、追加の設定は必要ありません。

1. module.xml ファイルをバックアップ、削除、作成します。 ファイルのデフォルトの場所は [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ です。

1. 新しく作成した module.xml ファイルを開いて編集します。次のコードをファイルに追加しました。

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

1. のバックアップを作成 `jsafeFIPS.jar`, `jsafeJCEFIPS.jar`、および `certjFIPS.jar` のファイル [AEM_Forms_Installation_directory]`/jboss/modules/system/layers/base/com/adobe/livecycle/main/` 前述のディレクトリからファイルを削除します。

[アドビサポート](https://experienceleague.adobe.com/ja?support-solution=General#support)に問い合わせて、新しい JAR ファイルを取得してください。[Adobe サポート](https://experienceleague.adobe.com/ja?support-solution=General#support)から取得した JAR ファイルを [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ に配置します。

1. （Windows のみ）構成ファイル `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` または `domain.conf.bat` を変更します。

* スタンドアロン設定の JBoss® サーバーの場合は、standalone.conf.bat を開いて編集します。
* クラスター設定の JBoss® サーバーの場合は、domain.conf.bat を開いて編集します。

  末尾に次の行を追加し、ファイルを保存します。

  `JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true` の設定

  `JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE` の設定

1. （Linux ベースの OS のみ）[AEM_Forms_Installation_directory]/jboss/standalone.conf または domain.conf の構成ファイルを変更します。

* スタンドアロン設定の JBoss® サーバーの場合は、standalone.conf を開いて編集します。
* クラスター設定の JBoss® サーバーの場合は、domain.conf を開いて編集します。

  末尾に次の行を追加し、ファイルを保存します。

  `JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"`

  `JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"`

## NPR-19778 に必要な設定 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 は CFP14 の一部です。

ユーザーがタスクを要求しても、共有キューのカウントが他のユーザーに対して更新されない。 そのため、Adobeは新しいプロパティを導入しました。 次の手順に従って、AEM インスタンスでこのプロパティを設定します。

1. 管理 UI／サービス／ワークスペース／グローバル管理に移動します。
1. グローバル設定を書き出します。
1. ダウンロードした XML ファイルで、タグを追加します `<client_tasksPollingInterval>10</client_tasksPollingInterval>`. 10 は秒単位の例の値です。 適宜変更できます。 
1.  ファイルを保存します。
1. 管理 UI／サービス／ワークスペース／グローバル管理に戻ります。
1. グローバル設定を読み込みセクションで xml ファイルを読み込みます。
1. これで、システムからログアウトして、再びログインできるようになりました。
1. ワークスペース内の他の開始が更新する共有キューユーザーの数です。
1. ポーリングをオフにするには、値を 0 に変更し、XML ファイルを再度読み込みます。

## UI の変更 {#ui-changes}

* `dc:title` プロパティが文字列 []（マルチフィールド）に設定された画像で、画像カードにタイトルを表示する際の動作の変更：UI の画像カードには、最新の変更されたタイトルのみが表示されますが、すべてのタイトルは CRX に保存されます。CQ-4217165 のホットフィックス

## 既知の問題 {#known-issues}

* AEM 6.2SP1-CFP19 と AEM 6.2SP1-CFP20 を CFP18 からアップデートすると、ルートリダイレクトが /sites.html/content ではなく、クラシック UI のようこそページに変更されます。Sling で /welcome.html から /index.html へのターゲットプロパティの修正が必要になる場合があります（CRX Explorer を使用）。この問題は、CFP 17 以前のバージョンからのアップデートでは発生しません。

AEM 6.2 SP1-CFPx をインストールすると、次の一時的なエラーが発生することがあります-。しかしこれらのエラーは、AEM インスタンスに影響を与えず CFP がインストールされると発生しなくなるので、解決は必要ありません。

* AEM 6.2SP1-CFP20 インスタンスを AEM 6.5 にアップグレードすると、次のようなバニティ URL が機能しない場合があります。

* */projects.html*
* */sites.html*

ただし、回避策は、アップグレード後に AEM インスタンスを再起動することです。

* Web コンソールのコンポーネントの詳細ページが開かれると、HTTP 500 内部サーバーエラーが受信されます。
* エラー（例：） **コンポーネントインスタンスを作成** および **サービスファクトリが null を返しました** リポジトリの再起動によって発生します。

* com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
* org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null.（コンポーネント：com.day.cq.taging.impl.TagGarbageCollector (1687)）

* Mongo と DB2® の CFP インストールでエラー **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException** が観察されています。このエラーは、CFP 8 で CFP をインストールした後は発生しません。
* （Adobe Granite メインテナンススケジューラーアップデートタスク）com.adobe.granite.maintenance.impl.TaskScheduler: No maintenance task found with name WorkflowPurgeTask for window `granite:weekly`
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
* スマートタグ機能パックを含むAEM 6.2 SP1 に CFPx をインストールすると、以前にスマートタグAssetsに追加したワークフローステップが DAM アセットの更新ワークフローから削除されます。

## Uber Jar {#uber-jar}

6.2 SP1-CFP20 の Uber Jar は、Adobeの Public Maven リポジトリーで入手できます。

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

## 含まれている OSGi バンドルとコンテンツパッケージ {#osgi-bundles-and-content-packages-included-5}

次のドキュメントには、CFP に含まれている OSGi バンドルとコンテンツパッケージの一覧が記載されています。

* [AEM 6.2 SP1-CFP20 に含まれている OSGi バンドルの一覧](assets/do-not-localize/updated.txt)
* [AEM 6.2 SP1-CFP20 に含まれているコンテンツパッケージの一覧](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 ホットフィックスページ](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [AEM 6.2 SP1 リリースノート](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [AEM 6.2 リリースノート](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [AEM 製品ページ](https://business.adobe.com/jp/products/experience-manager/adobe-experience-manager.html)
>* [AEM 6.2 ドキュメント](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Adobe の優先製品アップデート](https://experienceleague.adobe.com/ja/docs/release-notes/experience-cloud/current)
