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
      - 作業状態(例: Idea, ToDo, WIP, Done)やiteration(例: 2024Feb01, 2024Feb02)やmilestone(例: alpha-1, v1.0.0)を使う
4. webhookを使って、Discordに通知を飛ばす
    - PRのopen, comment, mergeや特定ブランチのpush時に指定のDiscordチャンネルに通知を飛ばす
    - 応用: webhookの通知を適当なサーバーに一旦POSTして、そのサーバーで通知を管理する(その後カスタムしたメッセージをDiscordに飛ばす)
5. CI(github actions)の実践的利用
    - RPがopenした時に、コードのformatをチェックする
      - 応用: コードのformatを自動で修正する
    - チェックボックスが複数あるPRテンプレートを作成し、チェックが全てついていない限りマージできないようにCIを作る(当然チェックの変更時などには自動でCIを動かしてチェックboxを確認する)
    - リリースの作成時に、自動でdeploy用のciを動かす(unityのwebGLビルドとかその辺りを適当に)
6. Git Hooksを利用した自動化
    - Pre-commit, pre-pushなど使ってみる
    - 独自のbashスクリプトを作ってみる
    - commit or push時に、コードのformatをチェックする
    - 応用: 作成したpre-commit, pre-pushでCIを動かす


