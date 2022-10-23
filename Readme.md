[OCI] Oracle Functionsから Base Databaseのバックアップを取得
https://blogs.oracle.com/developers/oracle-functions-connecting-to-an-atp-database-with-a-wallet-stored-as-secrets

事前準備
    Functions 実行環境の整備（Cloud Shellでも可）

Functionの作成・動作確認

    アプリケーションの作成
        fn create app backupap

    ファンクションの作成/テストディレクトリの削除
        fn init --runtime java sampletimestamp
        cd sampletimestamp
        rm -r src/test/
        fn config function backupap sampletimestamp DATABASE_ID ocid1.database.oc1.XXXX

    ファンクションの作成

        pom.xmlファイル

        func.yamlファイル

        HelloFunction.javaファイル の編集（本ファイルに置き換え）


    ファンクションのデプロイと呼び出し
        fn deploy --app sampletimestamp
        fn invoke backupap sampletimestamp

