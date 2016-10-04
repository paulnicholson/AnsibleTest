# AnsibleTest
Expected:
```
$ ansible-playbook test_playbook.yml                                                                                                                                                    2.0.0-p0
...
TASK [test : debug] ************************************************************
ok: [localhost] => { "name": "test1" }

TASK [test : include debug] ****************************************************
ok: [localhost] => { "name": "test1" }

TASK [test : debug] ************************************************************
ok: [localhost] => { "name": "test2" }

TASK [test : include debug] ****************************************************
ok: [localhost] => { "name": "test2" }
...
```

Actual:
```
$ ansible-playbook test_playbook.yml                                                                                                                                                    2.0.0-p0
...
TASK [test : debug] ************************************************************
ok: [localhost] => { "name": "test1" }

TASK [test : include debug] ****************************************************
ok: [localhost] => { "name": "test2" }

TASK [test : debug] ************************************************************
ok: [localhost] => { "name": "test2" }

TASK [test : include debug] ****************************************************
ok: [localhost] => { "name": "test2" }
...
```
