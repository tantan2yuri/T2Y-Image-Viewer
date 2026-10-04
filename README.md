# T2Y Image Viewer

**T2Y Image Viewer (TIV)** is a Windows image viewer and tag management application.

It combines image browsing, embedded Prompt parsing, Danbooru tag inference, manual tag editing, and tag-based filtering.

## Features

- **Browsing:** folder tree, thumbnails, fullscreen viewing, recent folders, and favorites
- **Display controls:** fit to window/height/width, zoom, Crop Zoom, rotation, and flipping
- **Tag extraction:** embedded Prompt parsing and ONNX-based Danbooru inference
- **Tag management:** manual editing, image information reanalysis, and unnecessary tag cleanup
- **Filtering:** AND/OR conditions, excluded tags, priority tags, and a folder-specific tag pool
- **Saved filters:** named presets with editing, duplication, selection, and filtering
- **File operations:** multiple selection, copy/cut/paste, rename, and delete
- **External applications:** registered application shortcuts, Show in Explorer, and Windows Properties
- **Interface:** Japanese/English and Light/Dark modes
- **Utilities:** Performance Monitor and application/database reset

## Installation

1. Download the distribution ZIP and extract it to a writable folder.
2. Run **T2Y_Image_Viewer.exe**.
3. Select a folder in the Explorer pane or press Ctrl+O.

Keep the executable, `resources`, DLLs, and other included files together. The tag database and thumbnail cache are created when the application starts.

## Supported formats

- Images: PNG, JPG/JPEG, WebP, BMP, PSD
- Archives: ZIP, CBZ, 7Z, RAR, LZH, TAR, GZ, TGZ, BZ2

Archive extraction depends on the format, file condition, and available 7-Zip support. Editing, deleting, and collecting tags for images inside archives are restricted.

## Tag collection

Prompt-derived tags require Prompt information embedded in the image file. A Prompt displayed on a generation website is not necessarily included in the downloaded image.

Images without embedded Prompt information can use Danbooru inference or manual tag editing. Inference requires an available ONNX model and matching tag definitions. It estimates tags from image content and does not recover the original Prompt or guarantee accurate results.

Folder scans process images directly inside the selected folder; subfolders are not included.

## Common shortcuts

| Action | Shortcut |
|---|---|
| Open folder | Ctrl+O |
| Switch viewer/thumbnails | Space |
| Fit entire image | Ctrl+Shift+Q |
| Crop Zoom | Ctrl+Shift+Z |
| Image information | F3 |
| Tag filtering | F6 |
| Help | F1 |
| Operation Guide | Shift+F1 |

Press F4 for the complete shortcut list and current availability.

## Notes

- Display rotation, flipping, and zoom do not modify the original image file.
- Confirmed file deletion is permanent and does not use the Recycle Bin.
- Multiple selection does not restrict viewer browsing to selected images.
- LTA integration and the Edit menu's Select by Tags command are deferred for future consideration. Selection through saved tag filters is available.

## Release

**V1.0 — Initial Release**

Bug reports and suggestions are welcome. Please include reproduction steps, error messages, and your system environment when reporting an issue.

## Support development

https://ko-fi.com/tantan2yuri
-----------------------------------------------------------------------
# T2Y Image Viewer

**T2Y Image Viewer（TIV）** は、Windows向けの画像ビューワ・タグ管理アプリケーションです。

画像の閲覧、埋め込みPromptからのタグ取得、Danbooruタグ推定、手動タグ編集、条件によるフィルタリングをまとめて行えます。

## 主な機能

- **画像閲覧**：フォルダツリー、サムネイル、全画面表示、履歴、お気に入り
- **表示調整**：全体・高さ・幅に合わせる、ズーム、クロップズーム、回転・反転
- **タグ取得**：埋め込みPromptの解析、ONNXモデルによるDanbooru推定
- **タグ管理**：手動編集、画像情報の再解析、不要タグの整理
- **フィルタリング**：AND／OR、除外タグ、優先タグ、現在フォルダに含まれるタグの一覧
- **登録フィルター**：条件の保存・編集・複製、対象画像の選択・抽出
- **ファイル操作**：複数選択、コピー・切り取り・貼り付け、名前変更、削除
- **外部連携**：登録アプリで開く、エクスプローラで表示、Windows標準のプロパティ
- **表示設定**：日本語／英語、ライト／ダーク
- **補助機能**：パフォーマンスモニタ、設定・タグDBの初期化

## 導入方法

1. 配布ZIPをダウンロードして、書き込み可能なフォルダへ展開します。
2. **T2Y_Image_Viewer.exe** を起動します。
3. フォルダを選ぶか、Ctrl+Oで画像フォルダを開きます。

EXEだけを移動せず、`resources`、DLLなどの同梱ファイルを一緒に配置してください。タグDBとサムネイルキャッシュは起動時に作成されます。

## 対応形式

- 画像：PNG、JPG／JPEG、WebP、BMP、PSD
- 圧縮ファイル：ZIP、CBZ、7Z、RAR、LZH、TAR、GZ、TGZ、BZ2

圧縮ファイルの展開可否は、形式・ファイルの状態・7-Zipの対応範囲に依存します。圧縮内画像の編集・削除・タグ取得には制限があります。

## タグ取得について

Prompt由来タグの取得には、画像ファイルに埋め込まれたPrompt情報が必要です。生成サイトにPromptが表示されていても、ダウンロードした画像に保存されているとは限りません。

Prompt情報のない画像には、Danbooru推定または手動タグ編集を利用できます。推定には利用可能なONNXモデルと対応するタグ定義が必要です。画像からの推定結果は、元のPromptの復元や正確性を保証するものではありません。

フォルダのスキャンは、そのフォルダ直下の画像を対象とします。サブフォルダは含みません。

## 主なショートカット

| 操作 | キー |
|---|---|
| フォルダを開く | Ctrl+O |
| ビューワ／サムネイル切り替え | Space |
| 全体を表示 | Ctrl+Shift+Q |
| クロップズーム | Ctrl+Shift+Z |
| 画像情報 | F3 |
| タグフィルタリング | F6 |
| ヘルプ | F1 |
| 操作ガイド | Shift+F1 |

全ショートカットと利用可能な状態は、F4で確認できます。

## 注意事項

- 回転・反転・ズームは表示上の操作で、元画像を書き換えません。
- ファイル削除は確認後に完全削除します。ごみ箱には移動しません。
- 複数選択しても、ビューワの表示対象は選択画像だけには限定されません。
- LTA連携と編集メニューの「タグで選択」は、今後の検討項目です。登録フィルターからの選択は利用できます。

## リリース

**V1.0 — 初回リリース**

不具合報告には、再現手順、エラーメッセージ、利用環境を添えていただけると助かります。

## 開発応援

https://ko-fi.com/tantan2yuri
