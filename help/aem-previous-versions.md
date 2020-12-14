---
title: AEM、CQ、およびCRXの古いバージョン
description: Adobe Experience Manager、CQ および CRX の以前のバージョンのドキュメントパッケージです。
translation-type: tm+mt
source-git-commit: 47b391ed659264b611f08d2fa9e45a923be5c445
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 24%

---


# [!DNL Adobe Experience Manager]、CQ、およびCRXの古いバージョン{#older-versions-aem-cq-crx}

## [!DNL Experience Manager]ドキュメント{#older-version-aem-documentation}の古いバージョン

このページに記載されている[!DNL Experience Manager]、CQ、およびCRXのバージョンは提供終了で、Adobeが正式に販売することはなくなりました。 これらの以前のバージョンについては、公式ドキュメントの最終バージョンがセルフヘルプ用に利用できます。最新バージョン（現在は[[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)）にアップグレードすることをお勧めします。

>[!NOTE]
>
>[!DNL Experience Manager]バージョンがコアサポートの終わりに達するかを知るには、[製品とテクニカルサポートの期間](https://helpx.adobe.com/jp/support/programs/eol-matrix.html)を参照し、`AEM`を検索してください。

### インストールの前に {#before-installation}

パッケージをダウンロードする前に、誰がコンテンツを使用するかを決めます。この決定により、デプロイ方法が決まります。

* 開発者は、クイックリファレンス用にローカルにインストールできます。
* 組織の幅広いドキュメントニーズに対応するには、内部でアクセス可能な、実稼動以外の AEM オーサーインスタンスにパッケージをデプロイすることをお勧めします。

>[!NOTE]
>
>[!DNL Experience Manager]作成者のこのコンテンツにアクセスするには、ユーザーは[!DNL Experience Manager]インスタンスにログインする必要があります。 このコンテンツは、デフォルトでは、AEM パブリッシュではアクセスできません（/libs 以下にあるので）。

## ソフトウェア配布場所{#software-distribution-locations}

有効なAdobe IDが必要です。

* Adobe IDがいない場合は、www.adobe.comで作成できます。
Adobe IDの作成や管理に関して支援が必要な場合は、[このガイド](https://helpx.adobe.com/manage-account.html)を参照してください。

| [!DNL Experience Manager] バージョン | ソフトウェア配布リンク |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.1 | [ソフトウェア配布からAEM-DOCS-6.1をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-1.zip) |
| [!DNL Experience Manager] 6.0 | [ソフトウェア配布からAEM-DOCS-6.0をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [ソフトウェア配布からAEM-DOCS-5.6.1をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5.6 | [ソフトウェア配布からAEM-DOCS-5.6をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [ソフトウェア配布からCQ-DOCS-5.5をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [ソフトウェア配布からCQ-DOCS-5.4をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [ソフトウェア配布からCQ-DOCS-5.3をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [ソフトウェア配布からCRX-DOCS-2.3をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [ソフトウェア配布からCRX-DOCS-2.2をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [ソフトウェア配布からCRX-DOCS-2.1をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [ソフトウェア配布からCRX-DOCS-2.0をダウンロード](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## ドキュメントパッケージのインストール方法 {#how-to-install-documentation-package}

レガシードキュメントパッケージをインストールするには、ローカルドライブまたはネットワークドライブに[!DNL Experience Manager]がインストールされ、実行されている必要があります。

### ドキュメントパッケージ{#download-documentation-package}をダウンロードします

1. 上の表から、ダウンロードする[!DNL Experience Manager]ドキュメントバージョンのリンクを選択してください。 （例：AEM 5.6.1）。

1. Adobe IDを使用してログインします。 ID をお持ちでない場合は、作成します。

1. 「**[!UICONTROL ダウンロード]**」ボタンを選択します。

1. 以下のような画面が表示されます。

![ソフトウェア配布の例](assets/screen_shot_2020-07-10at161922.jpg)

### パッケージをローカルインスタンス{#install-package-local-instance}にインストールします

1. [!DNL Experience Manager]ユーザーインターフェイスを開きます。 Webブラウザーで、次のように入力します。`http://localhost:4502/`. 管理者としてログインします。

1. **[!UICONTROL ツール]**／**[!UICONTROL デプロイメント]**／**[!UICONTROL パッケージ]**&#x200B;を選択します。

1. Package Manager UIから、「**[!UICONTROL パッケージをアップロード]**」を選択します。

1. AEM 5.6.1 パッケージ（aem-docs-5-6-1.zip）をダウンロードした場所を参照します。

1. パッケージを選択して、「**[!UICONTROL OK]**」をクリックします。

1. パッケージがアップロードされたら、インストールする必要があります。

1. Package Manager UIで、パッケージを探し、「**[!UICONTROL インストール]**」を選択します。

1. 確認ダイアログで、「**[!UICONTROL Install]**」を再度選択します。 注意：インストールには数分かかります。

1. Webブラウザーで、ドキュメントページを起動します。 AEM 5.6.1の例では、URLは次のようになります。http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html

## [!DNL Experience Manager]コミュニティ{#get-help-from-aem-community}からヘルプを入手

Experience Managerの使用に関するご質問は、[フォーラム [!DNL Experience Manager] ](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)で、経験豊富なコミュニティの専門家に&lt;a0/>お問い合わせください。
