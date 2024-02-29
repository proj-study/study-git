# 2. 中級・上級

※ CI等でコードのformatをチェックする際は、CodacyやSonarQube、Qodanaなどを使っても良い  

1. stashを使う
    - 応用: stashを使わず保存
      - diffから変更をpatchファイルに入れて一時的に保存する
      - applyでpatchファイルを適用する
2. revertで該当のPRの変更を取り消す
    - 特定のcommitを取り消す
    - 複数のcommitを取り消す
3. projectsでissueとPRの管理
    - labelなどのfieldを駆使してissueとPRを管理する
    - 作業状態(例: Idea, ToDo, WIP, Done)やiteration(例: 2024Feb01, 2024Feb02)やmilestone(例: alpha-1, v1.0.0)などを使う
    - viewごとにレイアウトをカスタマイズして、プロジェクトの進捗を可視化する
4. webhookを使って、Discordに通知を飛ばす
    - PRのopen, comment, mergeや特定ブランチのpush時に指定のDiscordチャンネルに通知を飛ばす
    - 応用: webhookの通知を適当なサーバーに一旦POSTして、そのサーバーで通知を管理する(その後カスタムしたメッセージをDiscordに飛ばす)
5. CI(github actions)の実践的利用
    - game-ciを使ってactivateから適切にUnityのWindowsビルドを行う(artifactを使ってビルド結果を保存する)
    - RPがopenした時に、コードのformatをチェックする
      - 応用: コードのformatを自動で修正する
    - PRがopenした時に、指定のユーザーを自動でreviewerに設定する
    - チェックボックスが複数あるPRテンプレートを作成し、チェックが全てついていない限りマージできないようにCIを作る(当然チェックの変更時などには自動でCIを動かしてチェックboxを確認する)
    - リリースの作成時に、自動でdeploy用のciを動かす(unityのwebGLビルドとかその辺りを適当に)
6. Git Hooksを利用した自動化
    - Pre-commit, pre-pushなど使ってみる
    - 独自のbashスクリプトを作ってみる
    - commit or push時に、コードのformatをチェックする
    - 応用: 作成したpre-commit, pre-pushでCIを動かす
7. READMEを書く
    - プロジェクトの概要
      - プロジェクトの目的、機能、使い方、利点、制限事項などを簡潔に説明する
    - 実行環境を書く
      - プロジェクトを実行するために必要なソフトウェアやハードウェアの環境を詳細に記述します。例えば、特定のOS、プログラミング言語のバージョン、必要なライブラリやツールなど
    - インストール方法と使用方法
      - プロジェクトをどのようにセットアップするか、必要な依存関係をどのようにインストールするかを説明する
    - バッチ
      - CIの状態を表示するバッチや、最新のリリースのバージョンを表示するバッチなど、プロジェクトの現在の状態を視覚的に示すバッチをREADMEに追加する
      - GitHub Actionsのステータス、リリースバージョン、ライセンス、テストカバレッジなど。
8. マルチリポジトリプロジェクトの管理
    - サブモジュールの利用する、リポジトリ間の依存関係の管理
