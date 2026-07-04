# AGENTS.md

このファイルは`VSA-Mainapp-Release`リポジトリ固有の運用ルールです。

## 役割

- GitHub Releases配布導線とGitHub Pages公開文書の管理repoとして扱う。
- ソース実装repoではないため、アプリ本体コードやhook運用の正本は持たない。

## 変更対象

- `docs/`: 公開ドキュメント、利用ガイド、利用規約、プライバシーポリシー
- `assets/`: 公開用画像や配布導線で使う静的資産
- `README.md`: 配布導線の案内

## 非対象

- `VSA/`本体や`vsa-website/`本体の実装判断
- Git hook追加やローカル開発用script追加
- 共有orchestration資産の正本化

## 確認方法

- 参照リンク、文書導線、公開文面の整合を確認する。
- 必要なら`docs/`配下と`README.md`の相互参照だけを見直す。
- repo rootにhookは置かない。必要になった時だけ明示追加する。

## 関連skills

- worktree開始: `../.agents/skills/source-command-worktree-start/SKILL.md`
- レビュー: `../.agents/skills/source-command-review-governance/SKILL.md`
- コミット: `../.agents/skills/source-command-commit-governance/SKILL.md`
