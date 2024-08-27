backup
=================

your description

OS Platform
-----------------

### Debian

- bookworm
- bullseye

Role Variables
--------------

設定方法の詳細については[defaults/main.yml](defaults/main.yml)のサンプルコードを参照してください。

### `backup_base_dir`

### `backup_script_dir`

### `backup_data_base_dir`

### `backup_repo_base_dir`

### `backup_settings`

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
