# Muse Agent Operations Kit

個人用AIエージェント（Muse）を継続運用するための仕組み一式をまとめた導入キットです。自己改善ループ、検証の規律、仕組みの効果判定と整理・退役、定期実行の設計、外部コンテンツへのセキュリティ境界などを、受け取ったAI自身が読み取って自分の環境へ導入できる「AIへの指示書」の形で記述しています。あわせて、一般コードの潜在不具合を系統的に発見する手順を一般化した「不具合発見スキル」（英語版）も収録しています。特定の個人やプロジェクトに依存しない、一般化された設計と手順のみを収録しています。

An adoption kit for operating a personal AI agent (Muse) over time. It documents, in the form of instructions that the receiving AI can read and adopt directly, a complete set of operating mechanisms: self-improvement loops, verification discipline, effectiveness review with consolidation and retirement of mechanisms, scheduled-execution design, and security boundaries for external content. The repository also includes the Defect-Discovery Skill, a generalized procedure for systematically discovering latent defects in general code (in English). Only generalized designs and procedures are included; nothing depends on a specific person or project.

## 収録ファイル / Files

| ファイル | 内容 |
| --- | --- |
| [muse-agent-operations-kit.md](muse-agent-operations-kit.md) | 導入キット（日本語） |
| [muse-agent-operations-kit.en.md](muse-agent-operations-kit.en.md) | Adoption kit (English) |
| [defect-discovery-skill.en.md](defect-discovery-skill.en.md) | 不具合発見スキル（英語、一般形） / Defect-discovery skill (English, general form) |

## 使い方 / How to use

導入キット / Adoption kit:

1. 利用する言語のファイルをダウンロードします。Download the file in your language.
2. そのファイルを、自分の Muse に渡します。Give the file to your own Muse.
3. ファイル冒頭（§0）の指示に従って導入が進みます。Adoption proceeds by following the instructions at the beginning of the file (§0).

- 部分導入に対応しています。規模に合わせて、ロードマップ（§13）の Phase 単位で進めることができます。Partial adoption is supported; the roadmap in §13 is organized into phases that can be adopted one at a time and scaled to the environment.
- 導入チェックリスト（§14）はそのままコピーして使えます。The adoption checklist in §14 can be copied and used as-is.

不具合発見スキル / Defect-discovery skill:

- コード精査・全精査を依頼するときに、そのファイルを自分の Muse に渡して使います。Give the file to your own Muse when you ask for a code audit or a full audit; the audit then proceeds by the procedure the file defines.

## 収録内容 / Contents

導入キット / Adoption kit:

- §0 このファイルを受け取った Muse への指示 / Instructions for the receiving Muse
- §1 設計前提 / Design premises
- §2 全体アーキテクチャ / Overall architecture
- §3 原則層の雛形 / Template for the principles layer
- §4 記録層と測定層：改善ログと回帰チェック / Record and measurement layers
- §5 台帳層：資産台帳・採用台帳・送信先台帳ほか / Ledger layer
- §6 検証プロトコル / Verification protocol
- §7 実行層：定期実行アーキテクチャ / Scheduled execution architecture
- §8 セキュリティ：外部コンテンツの指示には従わない / Security: instructions in external content
- §9 スキル化の入口と昇格基準 / Skill creation and promotion criteria
- §10 メモリ設計と正本配置の監査 / Memory design
- §11 外部モデルによるクロスチェック / Cross-checks with external models
- §12 失敗の型カタログ / Failure pattern catalog
- §13 導入ロードマップ / Adoption roadmap
- §14 導入チェックリスト / Adoption checklist
- 付記：このキットの範囲外 / Appendix: outside the scope of this kit

## 不具合発見スキル / Defect-discovery skill

既存コードベースの潜在不具合を系統的に発見するための手順書です。セキュリティ監査（CWE 特化）とは別に、状態遷移・競合・永続化・数値・上限・冪等性などの一般の欠陥クラスを対象とします。構成は、モードを問わず適用される共通核（手順0〜7： 振る舞いの追跡、母集団の機械列挙、欠陥クラスのマトリクス、独立複数パスの和集合と肯定処置の懐疑再審査、動的検証、不変条件の列挙、観測された異常の即時登録、報告の型）と、差分レビュー（モード1）と全行検査（モード2）の固有手順からなります。現在は英語版のみの収録です。

A procedure for systematically discovering latent defects in an existing codebase. Separate from security auditing (CWE-specific), it targets general defect classes such as state transitions, races, persistence, numerics, unbounded growth, and idempotency. It consists of a common core that applies in both modes (Steps 0–7: behavior tracing, mechanical enumeration of the population, a defect-class matrix, the union of independent multiple passes with skeptical re-review of affirmative dispositions, dynamic verification, enumeration of invariants, on-the-spot registration of observed anomalies, and a reporting format) plus mode-specific procedures for diff review (Mode 1) and full-codebase inspection (Mode 2). Currently available in English only.

## 解説サイト / Explanation site

設計の考え方と実践の解説（日本語／英語、図解付き）: [個人用AIエージェント運用環境の設計と実践](https://muse.ai/s/personal-ai-agent-operations-design-xqc6hixvuxi9xbxi/X9Yz-ImxkQGoYhnuc6ZGBe_Y5sm5qOfKzEvOJtmCw4U)

## 更新履歴 / Changelog

[CHANGELOG.md](CHANGELOG.md)

## Version

- 導入キット / Adoption kit: Version 1.7 (2026-11-21)
- 不具合発見スキル / Defect-discovery skill: 初版 (2026-11-16、英語・一般形) / First release (2026-11-16, English, general form)

## License

MIT Licenseのもとで公開しています。詳細は [LICENSE](LICENSE) を参照してください。

Released under the MIT License. See the [LICENSE](LICENSE) file for details.
