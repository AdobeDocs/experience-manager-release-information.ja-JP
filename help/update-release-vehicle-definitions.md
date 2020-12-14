---
title: リリース車両定義の更新
description: この記事では、完全リリース、機能パック、サービスパックを含む、様々なタイプの [!DNL Experience Manager] リリースについて説明します。
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 61%

---


# [!DNL Experience Manager] リリース車の定義を更新する  {#update-release-vehicle-definitions}

このドキュメントには、[!DNL Adobe]がお客様に提供するフルリリース、機能パック、サービスパックなど、様々なタイプの[!DNL Adobe Experience Manager]リリースの詳細が含まれています。

>[!NOTE]
>
>[!DNL Experience Manager]アップデートリリースのリリーススケジュールについては、[[!DNL Experience Manager] アップデートリリースロードマップ](update-releases-roadmap.md)を参照してください。

## 完全リリース {#full-release}

| アイテム | 説明 |
|-------|------|
| 定義 | <ul> <li> 予定されたリリース </li> <li> リリースノートで定義されている、特定のバージョンに対するアップグレードパスをサポート </li> </ul> |
| 命名 | <ul> <li> メジャーリリースのバージョン番号は、数式X+1.Y.Zに基づいて増加します。 </li> <li> マイナーリリースのバージョン番号は、X.Y+1.Z という式に基づいて大きくなります。 </li> </ul> ここで、Xはプライマリ・バージョン番号、Yはセカンダリ・バージョン番号、Zはパッチ番号を表します。 |
| 含まれるもの | <ul> <li> 新機能 </li> <li>  機能強化 </li> <li>  バグの修正 </li> </ul> |
| ドキュメント | <ul> <li> リリースノートはドキュメントポータルで入手できます。 </li> <li> 機能、機能強化およびバグの修正に関するドキュメントは、ドキュメントポータルで入手できます。 </li> </ul> |
| タイミング | 毎年 |
| 入手可能性とインストール | <ul> <li> スタンドアロンの製品インストーラーとして提供されます。 </li> <li>  ライセンスWebサイトとManaged Servicesから入手可能 </li> <li> ライセンスWebサイトでは、コンテンツリポジトリの移行が必要な場合があります </li> </ul> |
| テストのレベル | QA によって完全に検証済み |

## サービスパック  {#service-pack}

| Item | 説明 |
|-----|-----|
| 定義 | <ul> <li> 予定されたリリース </li> <li> 現在はロールバック不可 </li> </ul> |
| 命名 | <ul> <li> パッチのリリース番号は 1 桁の数字です。 </li> <li> インストール後、X.Y.Z.SPxの式に基づいて、インストール済みのリリース番号のパッチ桁を増やします。 </li> </ul> ここで、Xはプライマリ・バージョン番号、Yはセカンダリ・バージョン番号、Zはパッチ番号を表します。 x はサービスパック番号です。 |
| 含まれるもの | <ul> <li> 新機能</li> <li>  機能強化 </li> <li> バグの修正 </li> <li> Common Interest 機能パック（ある場合） </li> </ul> |
| ドキュメント | <ul> <li> リリースノートはドキュメントポータルで入手できます。 </li> <li> 機能、機能強化およびバグの修正に関するドキュメントは、ドキュメントポータルで入手できます。 </li> </ul> |
| タイミング | 毎四半期 |
| 入手可能性とインストール | <ul> <li> パッケージとして提供 </li> <li> ソフトウェア配布時に利用可能</li> <li>  既存機能のインストールが必要 </li> </ul> |
| テストのレベル | <ul> <li> すべての修正が QA 検証済み </li> <li>  自動実行を使用したパッケージ全体の健全性 </li> </ul> |

## 累積修正パック   {#cumulative-fix-pack-aem}

| 項目 | 説明 |
|-----|-----|
| 定義 | <ul> <li> 複数の修正を一度にリリースする提供モデル </li> <li> 個々のコンポーネントからなるコンテンツパッケージを含む集積コンテンツパッケージ </li> <li>  ホットフィックスのロールオーバーであり、機能強化は含まない  </li> </ul> |
| 命名 | X.Y.Z.CFPx <br> Xはプライマリバージョン番号、Yはセカンダリバージョン番号、Zはパッチ番号です。 x は累積サービスパック番号です。 |
| 含まれるもの | CFP は、指定された日付以降のすべてのコンポーネントの修正を含む、累積修正パックです。例えば、CFP3 を適用する場合、CFP3 = CFP1 + CFP2 です。 |
| ドキュメント | リリースノートはドキュメントポータルで入手できます。 |
| タイミング | 毎四半期 |
| 入手可能性とインストール | <ul> <li> パッケージとして提供 </li> <li>  ソフトウェア配布時に利用可能 </li> <li>  リリースされている最新のサービスパックに依存 </li> <li>  CFPは自己依存です。 ユーザーは依存関係の検索や解決を気にする必要はありません。CFP は、最新リリースのサービスパック上にインストールする必要があります。 </li> <li>  CFP は、単一パッケージとしてインストールでき、エクスペリエンスを向上させます。  </li> </ul> |
| テストのレベル | 統合レベルでの QA 検証済みおよび回帰テスト |

## オーバーレイ {#overlay}

| 項目 | 詳細 |
|-------|--------|
| 命名 | overlay-&lt;ticket ID> |
| 含まれるもの | JS ファイルまたは JSP ファイルのバグの修正 |
| ドキュメント | なし |
| タイミング | 必要に応じて |
| 入手可能性とインストール | <ul> <li> [!DNL Experience Manager]カスタマーケアからパッケージとして配信  </li> <li> サービスパックまたはフルリリースに必ずしも含まれていない </li> </ul> |
| テストのレベル | カスタマーケアによって検証済み |

## 機能パック  {#feature-pack}

| アイテム | 詳細 |
|--------|-----|
| 定義 | <ul> <li>機能パックはアドオン機能であり、サービスパックを通じて提供されます。[!DNL Experience Manager]バージョンが最後のService Packをリリースした場合、Adobeは将来、その機能パックを提供しなくなります。 </li> <li> FPには、製品の拡張が含まれており、以降の製品リリースに向けて予定されていますが、[!DNL Adobe's]製品管理の決定に基づいて早い段階で提供されています。</li> <li>  機能は常に次のメジャーリリースと統合され、お客様が必要とする[!DNL Experience Manager]バージョンに移植されます。 </li> <li>  Common Interest 機能パックと GA 機能パックは次のサービスパックに統合されます。  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 含まれるもの | <ul> <li> 新機能 </li> <li> 機能強化 </li> <li> バグの修正（製品の増分アップデート） </li> </ul> |
| ドキュメント | ドキュメントはadobe.comで入手できます。 |
| タイミング | 製品領域によって異なります。 |
| 入手可能性とインストール | <ul> <li>サービスパックを使用して配信 </li> <li> ソフトウェア配布時に利用可能。 お客様は、ソフトウェアの配布を通じて[!DNL Adobe's]利用条件に同意します。 </li> </ul> |
| テストのレベル | 一般提供の機能パックは QA 検証済み. |

* 1:OAKの修正は、個々のホットフィックスとしては提供されません。 しかし、以降の累積 Oak ホットフィックスに含まれます。必要に応じて、最新の COFP 上で診断ビルドを利用できます。前提条件は、最新の COFP を実行していることです。診断ビルドは、ホットフィックスと同じレベルの品質保証を提供するだけです。したがって、累積修正パック、サービスパックまたは製品リリースと同じレベルの品質保証を提供するものではありません。最終的な修正は、次のCFPで提供されます。