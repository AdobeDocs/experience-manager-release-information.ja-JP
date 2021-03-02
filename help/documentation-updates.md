---
title: '[!DNL Experience Manager] 最近のドキュメントの更新'
description: ' [!DNL Experience Manager] ドキュメントの新機能、更新、変更点'
contentOwner: trushton
translation-type: tm+mt
source-git-commit: aafdb3e36e9f856de37d5462af923aad32a73f6d
workflow-type: tm+mt
source-wordcount: '3220'
ht-degree: 18%

---


# [!DNL Experience Manager] ドキュメント：最近のドキュメントの更新  {#aem-documentation-recent-documentation-updates}

このページでは、新年の開始以降の[!DNL Adobe Experience Manager]に関する重要なドキュメントの変更と更新をリストしています。

[以前のドキュメントのアップデート](previous-documentation-updates.md)もご覧になれます。

## [!DNL Adobe Experience Manager] as a [!DNL Cloud Service] {#aem-as-a-cloud-service}

>[!NOTE]
>
>Cloud ServiceとしてのAEMは毎月リリースされます。
>
>個々のリリース（現在および以前のバージョン）に関するドキュメントについては、[リリースノート](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html)を参照してください。

| 日付 | トピック | 変更内容 |
| --- | --- | --- |
| 2020年12月2日 | バッチセットプリセット | Dynamic Media のバッチセットプリセットを使用して画像セットとスピンセットの作成を自動化する方法を説明します。詳しくは、[バッチセットプリセット](https://experienceleague.corp.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/batch-set-presets-dm.html#dynamicmedia)を参照してください。 |
| 2020年12月2日 | Dynamic Media でのアクセシビリティ | Dynamic MediaとDynamic Mediaのビューアは、オーサリングユーザーインターフェイス全体で、キーボード制御とJAWSやNVDAスクリーンリーダーなどの支援テクノロジーをサポートしています。 [Dynamic Mediaのアクセシビリティ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/accessibility-dm.html#dynamicmedia)を参照してください。 |
| 2020年10月29日 | コアコンポーネント | コアコンポーネントリリース2.12.0では、新しいPOSTフォームハンドラーが導入されました。コンテキストに応じた設定を使用して、カスタムCSS、JavaScript、メタデータタグを含める機能。と&#x200B;**DataLayerBuilderユーティリティ**&#x200B;を追加し、カスタムコンポーネントでのデータレイヤー統合をシンプルにします。 このリリースは、GitHubで入手可能な[オーサリングドキュメント](https://docs.adobe.com/content/help/ja-JP/experience-manager-core-components/using/introduction.html)、[開発者の詳細およびプロジェクトのダウンロードと共に利用できます。](https://github.com/adobe/aem-core-wcm-components) |
| 2020年9月24日 | 新しいDynamic Media設定の後のインボックス通知 | 新しいDynamic Media構成がセットアップを終了すると、[!DNL Experience Manager]インボックス内にステータス通知が届きます。 この通知は、設定が成功したかどうかを通知します。 設定が失敗した場合は、エラーコードが通知に表示されます。 Adobeケアに問い合わせる際は、このエラーコードを使用します。<br>「新しいDynamic Media設定の [トラブルシューティング」を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#troubleshoot-dm-config) |
| 2020年9月24日 | Dynamic Media設定内でのパスワードのリセット | 最初の一時パスワードと、その後のパスワードのリセットを、Dynamic Mediaクラシックを経由するのではなく、Dynamic Media内で許可します。 「[s](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services)での新しいDynamic Media構成の作成、手順6と7、[Dynamic Mediaへのパスワードの変更」も参照してください。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#change-dm-password) [!DNL Cloud Service] |
| 2020年9月24日 | Dynamic Media での選択的公開の操作 | [!DNL Experience Manager]またはDynamic Mediaとの間で、Dynamic Mediaインスタンス全体のすべてのフォルダにグローバルな設定を持つDynamic Mediaの設定に頼る代わりに、パブリケーションの管理またはクイックパブリッシュを使用して、アセットの発行または非公開を選択できます。<br>詳しくは、[Dynamic Media での選択的公開の操作](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/selective-publishing.html)を参照してください。 |
| 2020年9月11日 | 単一ページアプリケーション | 単一ページアプリケーション（SPA）エディター JavaScript SDK が[オープンソース](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/reference-materials.html)になりました。 |
| 2020年8月27日 | Dynamic MediaでのCDNの無効化 | 現在は、Dynamic Mediaからリクエストを送信し、CDNキャッシュの有効期限を数分で設定できます。 この機能は、アセットを更新し、その変更をWebサイトで直ちに有効にする場合に便利です。<br>詳しくは、Dynamic Media経由でのCDNキャッシュの [無効化を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/invalidate-cdn-cache-dynamic-media.html) |
| 2020年8月11日 | ページ公開のオン/オフ時間 | [オン/オフ時間](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html#basic)を使用してページを公開する場合、ページプロパティの「基本」タブを参照してください。[自動レプリケーションを事前に構成できるようになりました。](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/replication.html?lang=en#on-and-off-times-trigger-configuration) |
| 2020年7月23日 | コアコンポーネント | コアコンポーネントリリース2.11.0は、AMPのサポートを導入し、GitHubで利用可能な[オーサリングドキュメント](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)および[開発者の詳細とプロジェクトのダウンロードと共に利用できるようになりました。](https://github.com/adobe/aem-core-wcm-components) |
| 2020年7月16日 | スリングチートシート | [Sling cheat sheet](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/sling-cheatsheet.html)は、[HTL.](https://docs.adobe.com/content/help/ja-JP/experience-manager-htl/using/overview.html)を参照するように更新されました。 |
| 2020年6月24日 | コンテンツフラグメント | [モデルが標準になったので、ドキュメントが更新されました。](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) |
| 2020年6月19日 | [!DNL Adobe Experience Manager] | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |
| 2020年6月19日 | コアコンポーネント | コアコンポーネントリリース2.10.0ではPDFビューアコンポーネントが導入され、GitHubで入手可能な[オーサリングドキュメント](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)および[開発者の詳細とプロジェクトのダウンロードと共に利用できるようになりました。](https://github.com/adobe/aem-core-wcm-components) |
| 2020年6月4日 | Brand Portalで[!DNL Experience Manager Assets]を[!DNL Cloud Service]として設定 | Adobe I/Oは、新しいブランディング、ユーザーインターフェイス、ワークフローを使用してAdobeDeveloper Consoleにアップグレードされました。  ドキュメントは、最新AdobeのDeveloper Consoleワークフローに基づいて更新され、[Brand Portalで [!DNL Experience Manager Assets] as a [!DNL Cloud Service] configure](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)されます。 |
| 2020年6月1日 | リッチテキストエディター（RTE） | [!DNL Experience Manager]に[!DNL Cloud Service]として&lt;RTE)用の次の記事を<br>- [RTEを設定](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html)<br>- [各プラグインを設定](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)&lt;a8/- [アクセシブルなページを作成するにはRTEを設定10/><br>- [RTEを使用したコンテンツの作成](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/rich-text-editor.html)<br>](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/rte-accessible-content.html) |
| 2020年5月29日 | コアコンポーネント | コアコンポーネントリリース2.9.0では、Adobeクライアントデータレイヤーと新しいプログレスバーコンポーネントの統合が導入され、オーサリングドキュメント、開発者の詳細、プロジェクトのダウンロードと共にGitHubで利用できるようになりました。 |
| 2020年5月20日 | アクセシビリティとWCAG 2.1ガイドライン | WCAG 2.1ガイドライン<br>- [[!DNL Experience Manager] as a [!DNL Cloud Service] およびWebアクセシビリティガイドライン](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [WCAG 2.1](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [アクセシブルコンテンツの作成(WCAG 2.1 Conformance8 a8)に関する更新/>](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |
| 2020年5月4日 | Dynamic Mediaでサポートされていない画像形式 | Dynamic Mediaでサポートされていないラスターイメージファイル形式のサブタイプに関する情報です。<br>詳しくは、Dynamic Mediaで [サポートされていないラスターイメージ形式を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/administer/assets-formats.html#unsupported-image-formats-dynamic-media) |
| 2020年4月20日 | コンテンツフラグメント |  [!DNL Experience Manager] アセットHTTP API](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/admin/assets-api-content-fragments.html)の[コンテンツフラグメントのサポート、[コンテンツフラグメント](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-customizing.html)のカスタマイズと拡張、[レンダリング用コンポーネントの設定に関する情報です。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-configuring-components-rendering.html) |
| 2020年4月9日 | Brand Portalで[!DNL Experience Manager Assets]を[!DNL Cloud Service]として設定 | Brand Portalは、[!DNL Experience Manager Assets]を[!DNL Cloud Service]としてサポートするようになりました。 Adobe I/O<br>- [ブランドポータルで[!DNL Experience Manager Assets]を[!DNL Cloud Service]として](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)持つBrand Portalテナントを<br>- 構成 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] - [ブランドポータルにアセットを公開](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020年4月9日 | Adobeアセットリンクv2.0のリリース | Adobeアセットリンク2.0は、複数の[!DNL Experience Manager]環境の操作をサポートし、[!DNL Cloud Service]として[!DNL Experience Manager]をサポートします。 [!DNL Experience Manager] は、AALを使用してアセットをフォルダにアップロードする場合、マーケターのニーズに合わせて、アセット処理ワークフローの自動実行を設定します。<br> 「 [Adobeアセットリンク」を参照してください。](https://helpx.adobe.com/jp/enterprise/using/adobe-asset-link.html) |
| 2020年3月24日 | Dynamic Media Cloud Service の設定 | Dynamic MediaCloud Service <br>**一部の発行**&#x200B;を設定すると、新しいオプションが使用できます。このオプションを選択すると、セキュリティで保護されたプレビューのみを目的としてアセットが自動公開され、公開ドメインでの配信のためにDMS7に公開せずに[!DNL Experience Manager]に明示的に公開できます。<br>「Dynamic MediaCloud Serviceの [設定」を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services) |
| 2020年3月2日 | Dynamic Media — スマートクロップ | Dynamic Mediaコンポーネントのスマート切り抜きで作業する場合に、新しいオプションが使用できます。<br>**縦横比の一致を有効にする** — 元の画像の縦横比に最も適したスマート切り抜きレンディションをDynamic Mediaに選択させます。<br>スマート切り抜き [を使用する場合を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/adding-dynamic-media-assets-to-pages.html#when-working-with-smart-crop) |
| 2020年2月25日 | ロールに基づく権限 | Cloud Manager には、適切な権限を持つ事前設定済みの役割が用意されています。各ロールには、特定の権限、事前設定済みのタスクまたは権限が関連付けられています。[「役割に基づく権限」](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/onboarding/what-is-required/role-based-permissions.translate.html) ページには、使用可能な関数とその関数を実行できる役割が表示されます。 |
| 2020年2月16日 | クラウド内の Dispatcher | [ディスパッチャーとCDN](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/dispatcher/overview.html#dispatcher-cdn)と[明示的なディスパッチャーキャッシュの無効化](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/dispatcher/overview.html#explicit-invalidation)のセクションが更新され、使用可能なオプションとその動作方法が明確になりました。 |

## [!DNL Experience Manager] 6.5  {#aem-65}

| 日付 | トピック | 変更内容 |
| --- | --- | --- |
| 2020年11月25日 | Dynamic Media でのアクセシビリティ | Dynamic MediaとDynamic Mediaのビューアは、オーサリングユーザーインターフェイス全体で、キーボード制御とJAWSやNVDAスクリーンリーダーなどの支援テクノロジーをサポートしています。 [Dynamic Mediaのアクセシビリティ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/accessibility-dm.html#dynamic)を参照してください。 |
| 2020年11月26日 | [!DNL Experience Manager] 6.5 Service Pack 7 | [[!DNL Experience Manager] 6.5 Service Pack 7](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html#service-pack) がリリースされました。 |
| 2020年9月3日 | Dynamic MediaでのCDNの無効化 | 現在は、Dynamic Mediaからリクエストを送信し、CDNキャッシュの有効期限を数分で設定できます。 この機能は、アセットを更新し、その変更をWebサイトで直ちに有効にする場合に便利です。<br>詳しくは、Dynamic Media経由でのCDNキャッシュの [無効化を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/invalidate-cdn-cache-dynamic-media.html) |
| 2020年9月3日 | Dynamic Media での選択的公開の操作 | [!DNL Experience Manager]または&#x200B;**パブリケーションの管理**&#x200B;または&#x200B;**クイックパブリッシュ**&#x200B;を使用して、Dynamic Mediaインスタンス全体にグローバルな設定を持つ&#x200B;**Dynamic Mediaの設定**&#x200B;だけに依存する代わりに、フォルダーレベルでアセットを公開または非公開にできます。<br>詳しくは、[Dynamic Media での選択的公開の操作](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/selective-publishing.html)を参照してください。 |
| 2020年9月3日 | [!DNL Experience Manager] 6.5 Service Pack 6 | [[!DNL Experience Manager] 6.5 Service Pack 6](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html) が利用可能です。 |
| 2020年7月29日 | マルチサイトマネージャー | [新しい同期アクションの作成](https://docs.adobe.com/content/help/en/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)および[新しいロールアウト設定の作成の手順が更新されました。](https://docs.adobe.com/content/help/en/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration) |
| 2020年7月16日 | スリングチートシート | [Sling cheat sheet](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/sling-cheatsheet.html)は、[HTL.](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html)を参照するように更新されました。 |
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |
| 2020年6月4日 | [!DNL Experience Manager Assets]をBrand Portalに構成 | Adobe I/Oは、新しいブランディング、ユーザーインターフェイス、ワークフローを使用してAdobeDeveloper Consoleにアップグレードされました。 ドキュメントは最新AdobeのDeveloper Consoleワークフローに基づいて更新され、[!DNL Experience Manager Assets]をBrand Portalで設定<br>- [ [!DNL Experience Manager Assets] をBrand Portalで設定](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html)<br>- [既存の設定をAdobe開発者コンソールにアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| 2020年6月4日 | [!DNL Experience Manager] 6.5 Service Pack 5 | [[!DNL Experience Manager] 6.5 Service Pack 5](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html) が利用可能です。 |
| 2020年5月25日 | アクセシビリティとWCAG 2.1.ガイドライン | WCAG 2.1ガイドライン：<br>- [Adobe Experience Manager(a2/)およびウェブアクセシビリティガイドライン](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [WCAG 2.1](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [アクセシブルコンテンツの作成(WCAG)に関する更新2.1準拠](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) [!DNL Cloud Service]  |
| 2020年4月13日 | アセットのバージョン管理 |  [!DNL Experience Manager]内のアセットの作成、プレビュー、および[バージョンへの復帰方法に関するコンテンツとビデオを更新しました。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/managing/managing-assets-touch-ui.html#asset-versioning) |
| 2020年4月13日 | アセット処理 | アセットの処理にワークフローを使用する方法について、新しい概要を追加しました。 また、新しいトピックでは、[自動トリガーワークフローでアセットを処理する方法を説明します。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/using/assets-workflow.html) |
| 2020年3月30日 | Dynamic Media — スマートイメージング | Smart Imagingヘルプ・トピック全体が更新され、追加されたSmart Imagingの最適化を表す画像アセットの例を含む新しい情報が追加されました。<br>詳しくは、 [スマートイメージングを参照してください。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/imaging-faq.html) |
| 2020年3月5日 | [!DNL Experience Manager] 6.5 Service Pack 4 | [[!DNL Experience Manager] 6.5 Service Pack 4](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/release-notes/sp-release-notes.html) が利用可能です。 |
| 2020年3月4日 | Dynamic Media - Scene7 モードの設定 | 新しい「すべてのコンテンツを同期」オプションが、ツール/Cloud ServicesにあるDynamic Mediaの設定ページで利用できるようになりました。<br>「Dynamic Media設定の [作成」を参照してください。](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/config-dms7.html#configuring-dynamic-media-cloud-services) |

## [!DNL Experience Manager] 6.4  {#aem-64}

| 日付 | トピック | 変更内容 |
| --- | --- | --- |
| 2020年11月26日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 3 | [[!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 3](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/cfp-release-notes.html) が利用できます。 |
| 2020年9月3日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 2 | [[!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/cfp-release-notes.html) が利用可能です。 |
| 2020年7月29日 | [マルチサイトマネージャー] | [新しい同期アクションの作成](https://docs.adobe.com/content/help/en/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)および[新しいロールアウト設定の作成の手順が更新されました。](https://docs.adobe.com/content/help/en/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration) |
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |
| 2020年6月4日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 1 | [[!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 1](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/cfp-release-notes.html) が利用可能です。 |
| 2020年4月13日 | アセット処理 | アセットの処理にワークフローを使用する方法について、新しい概要を追加しました。 また、新しいトピックでは、[自動トリガーワークフローでアセットを処理する方法を説明します。](https://docs.adobe.com/content/help/en/experience-manager-64/assets/using/assets-workflow.html) |
| 2020年3月30日 | Dynamic Media — スマートイメージング | Smart Imagingヘルプ・トピック全体が更新され、追加されたSmart Imagingの最適化を表す画像アセットの例を含む新しい情報が追加されました。<br>詳しくは、 [スマートイメージングを参照してください。](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/imaging-faq.html) |
| 2020年3月5日 | [!DNL Experience Manager] 6.4 Service Pack 8 | [[!DNL Experience Manager] 6.4 Service Pack 8](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) が利用可能です。 |

## [!DNL Experience Manager] 6.3  {#aem-2}

| 日付 | トピック | 変更内容 |
| --- | --- | --- |
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |
| 2020年3月30日 | Dynamic Media — スマートイメージング | スマートイメージングのヘルプトピック全体が新しい情報で更新されました。<br>詳しくは、 [スマートイメージングを参照してください。](https://helpx.adobe.com/experience-manager/6-3/assets/using/imaging-faq.html) |
| 2020年3月5日 | [!DNL Experience Manager] 6.3.3.8 |  6.3 の[累積修正パック 6.3.3.8](https://helpx.adobe.com/experience-manager/release-notes--aem-6-3-cumulative-fix-pack.html)[!DNL Experience Manager] が入手可能になりました。 |

## [!DNL Experience Manager] 6.2  {#aem-62}

| 日付 | トピック | 変更内容 |
|---|---|---|
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |

## [!DNL Experience Manager] 6.1  {#aem-61}

| 日付 | トピック | 変更内容 |
|---|---|---|
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |

## [!DNL Experience Manager] デスクトップアプリケーション {#aem-desktop-app}

| 日付 | トピック | 変更内容 |
|---|---|---|
| 2020年8月27日 | [!DNL Experience Manager] デスクトップアプリ2.0.3.2<br>デスクトッ [!DNL Experience Manager] プアプリは、 [!DNL Experience Manager] 6.5、 [!DNL Cloud Service]6.4および [!DNL Experience Manager]  [!DNL Experience Manager]  [!DNL Experience Manager] 6.3（互換性パッケージ付き）の形式でサポートします。 | [!DNL Experience Manager] デスクトップアプリ2.0.3.2は、クリエイティブ、マーケターおよび基幹業務ユーザーが使用できる状態で公開され [!DNL Experience Manager Assets]ます。<br>リリー [スノートを参照してください。](https://docs.adobe.com/content/help/en/experience-manager-desktop-app/using/release-notes.html) |

## [!DNL Experience Manager Assets Brand Portal] {#aem-assets-brand-portal}

| 日付 | トピック | 変更内容 |
| --- | --- | --- |
| 2020年10月27日 | [!DNL Experience Manager Assets] Brand Portalからアセットをダウンロード | このドキュメントでは、シンプルで迅速なダウンロードを実現するための、<br>- [強化されたダウンロードエクスペリエンス](https://docs.adobe.com/content/help/ja/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)に関する主要な更新を扱っています。 追加のダウンロード設定を管理者が指定すれば、ユーザーや企業のニーズに合ったエクスペリエンスを提供できます。<br> — 任意のページから、「ファイル」、「 [コレクション](https://docs.adobe.com/content/help/ja/experience-manager-brand-portal/using/share/brand-portal-share-collection.html)」、「共有リンク」への1クリックナビゲーションが可能になりました。<br> — ユーザーは、特定のレンディションスノーを [選択してダウンロードでき](https://docs.adobe.com/content/help/ja/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets-from-asset-details-page) ます。アセットの詳細ページのレンディションパネルで新しいレンディションダウンロードオプションが使用可能です。<br> — ゲストユーザーセッションのタイムアウトを15分に設定すると、すべての同時ユーザーに対して快適なエクスペリエンスを提供できます。 |
| 2020年10月27日 | [!DNL Experience Manager Assets] Brand Portal 2020.10.0リリース | Brand Portal 2020.10.0では、アセットのダウンロードのワークフローの強化、レンディションの除外、レンディションパネルからの直接ダウンロード、特定のユーザーグループのアクセス権とダウンロード権限の設定、すべてのBrand Portalページからのファイル、コレクション、共有リンクへの簡単なナビゲーションが含まれます。<br>- Brand Portal [の新機能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>-  [Brand Portal 2020.10.0リリースノート](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020年9月3日 | [!DNL Experience Manager Assets] Brand Portalからアセットをダウンロード | Brand Portal管理者は、ダウンロード設定を設定でき、Brand Portalからアセットをダウンロードする際のユーザー操作をシンプルにできます。<br>このドキュメントでは、<br>- Brand Portal [ -](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)<br> Download assets from Brand Portal [ - ](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/accelerated-download.html)<br>Guide(ブランドポータルからアセットをダウンロードして迅速にダウンロード [ — 画像プリセットを適用)を以下の主要な更新について説明しています。](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/admin-tools/brand-portal-image-presets.html) |
| 2020年8月12日 | [!DNL Experience Manager Assets] Brand Portal 6.4.7リリース | Brand Portal 6.4.7には、Brand PortalユーザーのアセットのダウンロードとPDF表示を強化する新機能が導入されています。<br>- Brand Portal [の新機能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>-  [Brand Portal 6.4.7リリースノート](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020年6月19日 | Adobe Experience Manager | Adobeでは、コード、ドキュメント、経験を通して、公平な用語を使用することを目指しています。<br>このため、このドキュメントセットに対して一連の更新を行っており、今後も引き続き行う予定です。 |
| 2020年6月4日 | [!DNL Experience Manager Assets] Brand Portal 6.4.6.2リリース | Brand Portal 6.4.6.2では、最新AdobeのDeveloper Consoleワークフローに基づいてドキュメントが更新され、[!DNL Experience Manager Assets]がBrand Portalに設定されます。 このリリースには、アセットソーシング機能の修正も含まれています。<br>詳細は、次の記事を参照してください。<br> — ブランドポータルを使用した構成ブ [ [!DNL Experience Manager Assets] ランド6.4.6.2ノート](https://docs.adobe.com/content/help/ja-JP/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br> — ブランドポータルの新しいブランドの注 [意 — ブランドポータルの新しい新しいブランドの注釈 — ブランドの概要 — ブランドの](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/introduction/brand-portal-release-notes.html)<br> [](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/introduction/whats-new.html)<br> [](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/introduction/brand-portal-faqs.html)<br> [](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/asset-sourcing-in-brand-portal/brand-portal-asset-sourcing.html)<br> [概要](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/introduction/brand-portal.html) |
| 2020年4月9日 | Brand Portalで[!DNL Experience Manager Assets]を[!DNL Cloud Service]として設定 | Brand Portalは、[!DNL Experience Manager Assets]を[!DNL Cloud Service]としてサポートするようになりました。 Adobe I/O上で[!DNL Experience Manager Assets]を[!DNL Cloud Service]として持つBrand Portalテナントをとして設定できます。<br>- [ [!DNL Assets] as a [!DNL Cloud Service] ブランドポータルで](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)<br>- [アセットをブランドポータルに発行](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020年3月6日 | [!DNL Assets] （オンプレミスおよびマネージドサービス）をBrand Portalに設定 | 異なるExperience Managerバージョン用に、Adobe I/O](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)上のBrand PortalでExperience Managerアセットを[設定する方法に関するドキュメントが導入されました。<br>詳細は、<br>**AEM 6.5**<br>-ConfigureWith Portal [ [!DNL Assets] -ConfigureUpgrade ConfigurationAdobe](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br> [](https://docs.adobe.com/content/help/en/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65)<br>****<br> [ [!DNL Assets] ](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br> [](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64)<br>****<br> [ [!DNL Assets] ](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html)<br> [I/OA_OA_OA_O_O_O_O_O_O_O_O_O_O_OブランドAdobebrand Portal — レガシー構成からAdobe I/Oへのアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| 2020年2月27日 | [!DNL Assets] Brand Portal 6.4.6リリース | Brand Portal 6.4.6では、[!DNL Assets]とBrand Portalの認証チャネルがAdobe I/Oに変更されます。Adobe I/Oを使用したBrand Portalの設定は、[!DNL Experience Manager Assets] 6.3以降でサポートされます。<br>- Brand Portal [の新機能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>- [ Brand Portalリリースノート](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
