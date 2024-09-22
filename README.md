backup
=================

Setup backup setting

OS Platform
-----------------

### Debian

- bookworm
- bullseye

Role Variables
--------------

### [defaults/main.yml](defaults/main.yml)

設定方法の詳細については[defaults/main.yml](defaults/main.yml)のサンプルコードなどを参照してください。

#### `backup_base_dir`

バックアップ処理のベースディレクトリ

#### `backup_script_dir`

バックアップスクリプト格納用ディレクトリ

#### `backup_data_dir`

バックアップデータ格納用ディレクトリ

#### `backup_repo_dir`

バックアップデータの世代管理(リポジトリ)用ディレクトリ

#### `backup_repo_password_dir`

リポジトリのパスワード用ディレクトリ

#### `backup_restic_default_repo_type`

リポジトリ種別の初期値  
※設定値の値は「vars/main.yml」の「restic_allow_repo_types」変数を参照  
@see https://restic.readthedocs.io/en/stable/030_preparing_a_new_repo.html

#### `backup_restic_default_forget_keep_type`

スナップショットのクリーンアップ方法の初期値  
※設定値の値は「vars/main.yml」の「restic_allow_forget_keep_types」変数を参照  
@see https://restic.readthedocs.io/en/stable/060_forget.html#removing-snapshots-according-to-a-policy

#### `backup_restic_default_forget_keep_value`

スナップショットのクリーンアップ方法の値の初期値  
@see https://restic.readthedocs.io/en/stable/060_forget.html#removing-snapshots-according-to-a-policy

#### `backup_settings`

バックアップ設定

#### `backup_restic_init_common_options`

`restic init`実行時の共通オプション

#### `backup_restic_backup_common_options`

`restic backup`実行時の共通オプション

#### `backup_restic_forget_common_options`

`restic forget`実行時の共通オプション

#### `backup_data_dir_permission`

バックアップデータディレクトリのアクセス権

### [vars/main.yml](vars/main.yml)

設定値については[vars/main.yml](vars/main.yml)を参照してください。

#### `restic_allow_repo_types`

リポジトリ種別の選択肢

#### `restic_allow_forget_keep_types`

世代数の管理方法の選択肢

#### `backup_script_permission`

バックアップスクリプトのアクセス権

#### `backup_password_file_permission`

パスワードファイルのアクセス権

#### `backup_repo_dir_permission`

ローカルのリポジトリディレクトリのアクセス権

Example Playbook
--------------

```yaml
- hosts: servers
  roles:
    - role: backup
```

License
--------------

Apache License 2.0
