# DenTag

Android向けのMP3・FLACタグ編集アプリの配布用リポジトリです。

最新バージョン：**v1.1.0 UI更新版**

- [UI更新版APKをダウンロード](https://github.com/denngaku-chan/DenTag-Release/raw/refs/heads/main/releases/v1.1.0-ui/DenTag-v1.1.0-ui.apk)
- [UI更新版の公開用ソース](https://github.com/denngaku-chan/DenTag-Release/raw/refs/heads/main/releases/v1.1.0-ui/DenTag-v1.1.0-ui-source-public.zip)
- [変更点・検証結果](releases/v1.1.0-ui/release-notes.md)
- [公開済みRelease一覧](https://github.com/denngaku-chan/DenTag-Release/releases)

曲名・アーティスト・アルバム名・トラック番号・発売年・ジャンルとジャケット画像を編集できます。保存時は「元の曲に上書き」と「編集したコピーを保存」を選べます。Android 8.0以上に対応しています。既存版と同じ署名のため、上書きインストールできます。

## UI更新

「まずは曲を選んでください」のカードをタップして曲を選べます。選択後もカードから曲を変更できます。MP3Gain画面下部の操作を整理し、「設定を使って戻る」を画面下に固定しました。

## MP3Gain

MP3本体の音量を再エンコードせずに変更します。ReplayGain非対応プレーヤーでも反映されます。89 dBを標準とする自動調整、約1.5 dB刻みの手動調整、クリッピング警告、永続Undoを備えています。MP3Gain画面で設定し、編集画面の「保存する」で反映します。今回は1曲ごとの処理に対応します。FLACでは使用できません。

## 音量補正（ReplayGain）

ReplayGainも独立した機能として残しています。曲ごとの音量補正タグを編集できます。マイナスで小さく、プラスで大きく、0で補正なし、空欄・解除で曲単位の音量補正タグを削除します。「-1 dB」「+1 dB」ボタンでも調整できます。

ReplayGainの編集だけでは音声データを変更しません。対応プレーヤーでReplayGainを有効にし、曲単位（トラック）を選んでください。

公開用ソースには署名鍵を含めていません。処理系の232ケースを検証済みです。Android実機での画面操作・解析・SAF保存は未確認です。
