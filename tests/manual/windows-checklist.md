# Windows integration checklist

1. GitHub Actions の Windows test build が成功したことを確認する。
2. 実行結果の Artifacts から markdown-studio-windows-（コミットSHA）をダウンロードして展開する。
3. markdown-sheet/src-tauri/target/release/markdown-sheet.exe を起動する。Windows の WebView2 Runtime が必要。
4. 同梱の front-matter.md を開く。status / owner / last_updated と open_issues の2項目が表示されること。
5. ライト・ダークの両テーマで見切れがないこと。
6. 本文の編集・表編集・保存・再読込で内容が保持されること。元のファイルのコピーで試す。
7. 長い本文でスクロール同期とプレビューからの編集位置がずれないこと。
8. ヘッダーなし、CRLF改行、入れ子、複数行の値、不正なYAMLでも内容が消失しないこと。
9. PDF / HTML / Word出力と書式付きコピーを試し、本文が欠けないこと。メタデータの出力有無も記録する。

記録する情報: Actions実行URL、コミットSHA、Windowsバージョン、各項目の合否、画面と再現手順。

自動ビルドの成功だけでは、この手動結合テストは完了していません。
このワークフローはインストーラーやGitHub Releaseを作成せず、確認用exeを14日間保存します。
