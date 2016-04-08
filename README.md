ANSIBLE-ROLE-CakePHPCS
=========

cakephp-codesnifferをインストールするロール  
ansible実行ユーザーのglobal領域にインストールする

Requirements
------------

php5.3以上  
composerが実行できること  
composerでphpcsが入っていること

Example
----------------

## ansible.cfg

```
[defaults]
roles_path = ./roles
```

## requirements.yml

requirements.ymlをロールとして欲しいplaybook配下で実行する

 ```
   - src: https://github.com/kkkw/ansible-role-phpcs
     scm: git
     version: master
     name: phpcs
   - src: https://github.com/kkkw/ansible-role-cakephpcs
     scm: git
     version: master
     name: cakephpcs
 ```
 ## インストールコマンド
  
 ```shell
$ ansible-galaxy install -r requirements.yml 
 ```
 