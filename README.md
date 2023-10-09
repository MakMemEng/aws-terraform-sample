### EC2+SSH -> ECS Exec, SSM, ECS on Fargate

-   踏み台管理コスト削減

-   Local Stack
    -   SSH/RDP 接続は IPv6 での利用可能
    -   ターミナルソフトで IPV6 グローバル接続
    -   EC2 Instance Connect Endpoint 経由で IPv4 ローカル接続
    -   EC2 からインターネット接続は一部可能
    -   接続先が IPv6 に対応している場合に限定
    -   SystemsManager 通信は対策が必要
    -   IPV6 グローバル接続状態では利用出来なかった
    -   ECS タスクは IPv4 を使用してターゲットグループ登録する挙動が発生している模様
-   IPv4 -> IPv6
-   CloudFormation
    既存リソースを CloudFormation Stack に import
