# AGENTS.md

このファイルは`VSA-Mainapp-Release`リポジトリ固有の運用ルールです。

## 役割

- GitHub Releases配布導線とGitHub Pages公開文書の管理repoとして扱う。
- ソース実装repoではないため、アプリ本体コードやhook運用の正本は持たない。

## 変更対象

- `docs/`: 公開ドキュメント、利用ガイド、利用規約、プライバシーポリシー
- `assets/`: 公開用画像や配布導線で使う静的資産
- `README.md`: 配布導線の案内

## スクリーンショットPNGの生成元

- `assets/screenshots`配下のPNGは、`VSA/VSA-MainApp`で`bun run update:screenshots`を実行して再生成する（このrepo内で直接編集・撮影しない）。
- 詳細は`VSA/docs/runbooks/docs-screenshots.md`を正本とする。

## 非対象

- `VSA/`本体や`vsa-website/`本体の実装判断
- Git hook追加やローカル開発用script追加
- 共有orchestration資産の正本化

## 確認方法

- 参照リンク、文書導線、公開文面の整合を確認する。
- 必要なら`docs/`配下と`README.md`の相互参照だけを見直す。
- repo rootにhookは置かない。必要になった時だけ明示追加する。
- `assets/screenshots/`のPNG更新は、`VSA/VSA-MainApp`で`bun run update:screenshots`を実行してから差分を取り込む。
- commitする場合は公開releaseページ側の表示ユーザー名を分けるため、必ずrepo-localの `fefaether <fefaether@users.noreply.github.com>` 名義で実行する。
- commit前に `git config --local user.name` と `git config --local user.email` を確認し、`JUNSEI <junsei2005@outlook.jp>` またはglobal設定しか見えない場合は停止する。
- push前に `git log --format="%an <%ae> / %cn <%ce>" --all` で `JUNSEI` と `junsei2005@outlook.jp` が履歴に残っていないことを確認する。

## 関連skills

- 公開docs同期: `../VSA/.agents/skills/source-command-release-docs-sync/SKILL.md`
- worktree開始: `../.agents/skills/source-command-worktree-start/SKILL.md`
- レビュー: `../.agents/skills/source-command-review-governance/SKILL.md`
- コミット: `../.agents/skills/source-command-commit-governance/SKILL.md`
