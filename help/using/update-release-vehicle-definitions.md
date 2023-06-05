---
title: アップデートリリースの提供に関する定義
description: この記事では、完全リリース、機能パック、サービスパックなど、 [!DNL Experience Manager]  の各種リリースについて詳しく説明します。
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: ce1026216ccb79a3c268b3f6b24698fa3a3388dc
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 73%

---

# [!DNL Experience Manager] アップデートリリースの提供に関する定義 {#update-release-vehicle-definitions}

このドキュメントでは、[!DNL Adobe] から提供される完全リリース、機能パック、サービスパックなど、[!DNL Adobe Experience Manager] の各種リリースについて詳しく説明します。

>[!NOTE]
>
>[!DNL Experience Manager] アップデートリリースのリリーススケジュールについては、[[!DNL Experience Manager]  アップデートリリースロードマップ](update-releases-roadmap.md)を参照してください。

## 完全リリース {#full-release}

| アイテム | 説明 |
|-------|------|
| 定義 | <ul> <li> 予定されたリリース </li> <li> リリースノートで定義されている、特定のバージョンに対するアップグレードパスをサポート </li> </ul> |
| 命名 | <ul> <li> メジャーリリースのバージョン番号は、X+1.Y.Z という式に基づいて大きくなります。 </li> <li> マイナーリリースのバージョン番号は、X.Y+1.Z という式に基づいて大きくなります。 </li> </ul> X はプライマリバージョン番号、Y はセカンダリバージョン番号、Z はパッチ番号です。 |
| 含まれるもの | <ul> <li> 新機能 </li> <li>  改善点 </li> <li>  バグの修正 </li> </ul> |
| ドキュメント | <ul> <li> リリースノートはドキュメントポータルで入手できます </li> <li> 機能、改善点およびバグ修正に関するドキュメントは、ドキュメントポータルで利用できます。 </li> </ul> |
| タイミング | 毎年 |
| 入手可能性とインストール | <ul> <li> スタンドアロンの製品インストーラーとして提供されます。 </li> <li>  および Managed Services Licensing Website から入手可能です。 </li> <li> ライセンス Web サイトでは、コンテンツリポジトリーの移行が必要な場合があります </li> </ul> |
| テストのレベル | QA によって完全に検証済み |

## サービスパック   {#service-pack}

| 項目 | 説明 |
|-----|-----|
| 定義 | <ul> <li> 予定されたリリース </li> <li> 現在、ロールバックできません </li> </ul> |
| 命名 | <ul> <li> パッチのリリース番号は 1 桁の数字です。 </li> <li> インストール後、X.Y.Z.SPx という式に基づいて、インストールされたリリース番号のパッチの数字が大きくなります。 </li> </ul> X はプライマリバージョン番号、Y はセカンダリバージョン番号、Z はパッチ番号です。x はサービスパック番号です。 |
| 含まれるもの | <ul> <li> 新機能</li> <li>  改善点 </li> <li> バグの修正 </li> <li> Common Interest 機能パック（存在する場合） </li> </ul> |
| ドキュメント | <ul> <li> リリースノートはドキュメントポータルで入手できます。 </li> <li> ドキュメントポータルの機能、改善点、バグ修正に関するドキュメント </li> </ul> |
| タイミング | 毎四半期 |
| 入手可能性とインストール | <ul> <li> パッケージとして提供 </li> <li> ソフトウェア配布時に利用可能</li> <li>  既存機能のインストールが必要 </li> </ul> |
| テストのレベル | <ul> <li> すべての修正 QA 検証済み </li> <li>  自動化実行によるパッケージの全体的な健全性 </li> </ul> |

## 累積修正パック      {#cumulative-fix-pack-aem}

| 項目 | 説明 |
|-----|-----|
| 定義 | <ul> <li> 修正をリリースする単一配信モデル </li> <li> 個々のコンポーネントのコンテンツパッケージを含む集約コンテンツパッケージ </li> <li>  CFP はホットフィックスのロールオーバーであり、改善は含まれていません。  </li> </ul> |
| 命名 | X.Y.Z.CFPx <br> X はプライマリバージョン番号、Y はセカンダリバージョン番号、Z はパッチ番号です。x は累積サービスパック番号です。 |
| 含まれるもの | CFP は、指定した日付までのすべてのコンポーネントの修正を含む累積修正パックです。 例えば、顧客が CFP3 を適用する場合、CFP3 = CFP1 + CFP2 になります。 |
| ドキュメント | リリースノートはドキュメントポータルで入手できます。 |
| タイミング | 毎四半期 |
| 入手可能性とインストール | <ul> <li> パッケージとして提供 </li> <li>  ソフトウェア配布時に利用可能 </li> <li>  リリースされている最新のサービスパックに依存 </li> <li>  CFP は自己依存型です。ユーザーは依存関係の検索や解決を気にする必要はありません。CFP は、最新リリースの Service Pack にインストールする必要があります。 </li> <li>  CFP は、単一のパッケージとしてインストールでき、顧客体験を向上させます。  </li> </ul> |
| テストのレベル | 統合レベルおよび回帰テストで QA 検証済み |

## オーバーレイ {#overlay}

| 項目 | 詳細 |
|-------|--------|
| 命名 | オーバーレイ-&lt;チケット ID> |
| 含まれるもの | JS ファイルまたは JSP ファイルのバグの修正 |
| ドキュメント | なし |
| タイミング | 必要に応じて |
| 入手可能性とインストール | <ul> <li> [!DNL Experience Manager] がパッケージとして提供  </li> <li> 必ずしもサービスパックや完全リリースに含める必要はありません </li> </ul> |
| テストのレベル | カスタマーケアによって検証済み |

## 機能パック {#feature-pack}

| アイテム | 詳細 |
|--------|-----|
| 定義 | <ul> <li>機能パックはアドオン機能であり、サービスパックを通じて提供されます。[!DNL Experience Manager] バージョンの最後のサービスパックがリリースされた場合、以後、アドビではそのバージョンの機能パックを提供しません。 </li> <li> 機能パックには、製品の機能強化が含まれます。以降の製品リリースで予定されているが、[!DNL Adobe's] の製品管理部門の決定に基づいて予定より早く提供されます。</li> <li>  機能は常に次のメジャーリリースに統合され、顧客が必要とする [!DNL Experience Manager] バージョンに移植されます。 </li> <li>  Common Interest 機能パックと GA 機能パックは次のサービスパックに統合されます。  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 含まれるもの | <ul> <li> 新機能 </li> <li> 改善点 </li> <li> バグの修正（製品の増分アップデート） </li> </ul> |
| ドキュメント | ドキュメントは adobe.com で入手できます。 |
| タイミング | 製品領域によって異なります。 |
| 入手可能性とインストール | <ul> <li>サービスパックを使用して配信  </li> <li> ソフトウェア配布時に利用可能。お客様は、ソフトウェアの配布を通じて [!DNL Adobe's] 利用条件に同意します。 </li> </ul> |
| テストのレベル | 一般提供の機能パックは QA 検証済み。 |

* 1：Oak の修正は、個別のホットフィックスとしては提供されません。ただし、後続の累積 Oak ホットフィックスに含まれます。 必要に応じて、最新の COFP の上にある診断ビルドを使用できます。 前提条件は、顧客が最新の COFP を実行していることです。 診断ビルドは、ホットフィックスと同じレベルの品質保証を提供します。 したがって、累積修正パック、サービスパック、または製品リリースほどの品質保証を提供するものではありません。最終的な修正は、次の CFP で提供されます。