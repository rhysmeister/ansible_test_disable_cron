# Exampe Output

Why doesn't diff show all values?

```
WARNING  Driver docker does not provide a schema.
INFO     default scenario test matrix: dependency, cleanup, destroy
INFO     Performing prerun with role_name_check=0...
WARNING  Multiple versions of 'ansible.netcommon' were found installed, only the first one will be used, 1.4.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'ansible.posix' were found installed, only the first one will be used, 1.5.4 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.docker' were found installed, only the first one will be used, 3.11.0 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.general' were found installed, only the first one will be used, 6.6.0 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.library_inventory_filtering_v1' were found installed, only the first one will be used, 1.0.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.mongodb' were found installed, only the first one will be used, 1.7.5 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'google.cloud' were found installed, only the first one will be used, 1.0.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
INFO     Running default > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Running default > destroy
INFO     Sanity checks: 'docker'

PLAY [Destroy] *****************************************************************

TASK [Set async_dir for HOME env] **********************************************
ok: [localhost]

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=ubuntu)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: [localhost]: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=ubuntu)

TASK [Delete docker networks(s)] ***********************************************
skipping: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=3    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
➜  cron git:(master) ✗ molecule converge
WARNING  Driver docker does not provide a schema.
INFO     default scenario test matrix: dependency, create, prepare, converge
INFO     Performing prerun with role_name_check=0...
WARNING  Multiple versions of 'ansible.netcommon' were found installed, only the first one will be used, 1.4.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'ansible.posix' were found installed, only the first one will be used, 1.5.4 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.docker' were found installed, only the first one will be used, 3.11.0 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.general' were found installed, only the first one will be used, 6.6.0 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.library_inventory_filtering_v1' were found installed, only the first one will be used, 1.0.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'community.mongodb' were found installed, only the first one will be used, 1.7.5 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
WARNING  Multiple versions of 'google.cloud' were found installed, only the first one will be used, 1.0.1 (/Users/rhyscampbell/.ansible/collections/ansible_collections).
INFO     Running default > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Running default > create
INFO     Sanity checks: 'docker'

PLAY [Create] ******************************************************************

TASK [Set async_dir for HOME env] **********************************************
ok: [localhost]

TASK [Log into a Docker registry] **********************************************
skipping: [localhost] => (item=None)
skipping: [localhost]

TASK [Check presence of custom Dockerfiles] ************************************
ok: [localhost] => (item={'image': 'ubuntu:latest', 'name': 'ubuntu'})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'image': 'ubuntu:latest', 'name': 'ubuntu'})

TASK [Synchronization the context] *********************************************
changed: [localhost] => (item={'image': 'ubuntu:latest', 'name': 'ubuntu'})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/Users/rhyscampbell/.cache/molecule/cron/default/Dockerfile_ubuntu_latest', 'src': '/Users/rhyscampbell/.ansible/tmp/ansible-tmp-1730908778.8291268-55165-17401984486253/.source', 'md5sum': '4b5371d46746a8dc9fc3cc8bb66381ad', 'checksum': 'c75aaabd95b5bd8d709c54e533f97bb910802695', 'changed': True, 'uid': 501, 'gid': 20, 'owner': 'rhyscampbell', 'group': 'staff', 'mode': '0600', 'state': 'file', 'size': 1042, 'invocation': {'module_args': {'src': '/Users/rhyscampbell/.ansible/tmp/ansible-tmp-1730908778.8291268-55165-17401984486253/.source', 'dest': '/Users/rhyscampbell/.cache/molecule/cron/default/Dockerfile_ubuntu_latest', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': 'c75aaabd95b5bd8d709c54e533f97bb910802695', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'image': 'ubuntu:latest', 'name': 'ubuntu'}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
ok: [localhost] => (item=molecule_local/ubuntu:latest)

TASK [Create docker network(s)] ************************************************
skipping: [localhost]

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'image': 'ubuntu:latest', 'name': 'ubuntu'})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=ubuntu)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: [localhost]: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'failed': 0, 'started': 1, 'finished': 0, 'ansible_job_id': 'j920637864503.55287', 'results_file': '/Users/rhyscampbell/.ansible_async/j920637864503.55287', 'changed': True, 'item': {'image': 'ubuntu:latest', 'name': 'ubuntu'}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=9    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Running default > prepare

PLAY [Prepare] *****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [ubuntu]

TASK [Update repositories cache] ***********************************************
changed: [ubuntu]

TASK [Install requirements] ****************************************************
changed: [ubuntu]

PLAY RECAP *********************************************************************
ubuntu                     : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Running default > converge

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [ubuntu]

TASK [cron : Install a test cron job] ******************************************
changed: [ubuntu]

TASK [cron : What's in root's cron file?] **************************************
ok: [ubuntu]

TASK [cron : Disable the cron job] *********************************************
changed: [ubuntu]

TASK [cron : What's in root's cron file?] **************************************
ok: [ubuntu]

TASK [cron : Re-enable the cron job] *******************************************
changed: [ubuntu]

TASK [cron : What's in root's cron file?] **************************************
ok: [ubuntu]

TASK [cron : Use check mode to see if the job is disabled] *********************
changed: [ubuntu]

TASK [cron : View what's returned] *********************************************
ok: [ubuntu] => {
    "mycron": {
        "changed": true,
        "envs": [],
        "failed": false,
        "jobs": [
            "Test Job Name"
        ]
    }
}

TASK [cron : Fail the playbook but ignore] *************************************
fatal: [ubuntu]: FAILED! => {
    "assertion": "mycron.changed is false",
    "changed": false,
    "evaluated_to": false,
    "msg": "cron job is not disabled"
}
...ignoring

TASK [cron : Disable the cron job for real] ************************************
changed: [ubuntu]

TASK [cron : View what's returned] *********************************************
ok: [ubuntu] => {
    "mycron": {
        "changed": true,
        "envs": [],
        "failed": false,
        "jobs": [
            "Test Job Name"
        ]
    }
}

TASK [cron : Use check mode to see if the job is disabled] *********************
ok: [ubuntu]

TASK [cron : View what's returned] *********************************************
ok: [ubuntu] => {
    "mycron": {
        "changed": false,
        "envs": [],
        "failed": false,
        "jobs": [
            "Test Job Name"
        ]
    }
}

TASK [cron : Use check mode to see if the job is enabled] **********************
ok: [ubuntu]

TASK [cron : View what's returned] *********************************************
ok: [ubuntu] => {
    "mycron": {
        "changed": false,
        "envs": [],
        "failed": false,
        "jobs": [
            "Test Job Name"
        ]
    }
}

TASK [cron : Is my job disabled?] **********************************************
ok: [ubuntu] => {
    "changed": false,
    "msg": "cron job is disabled"
}

TASK [cron : What's in root's cron file?] **************************************
ok: [ubuntu]

PLAY RECAP *********************************************************************
ubuntu                     : ok=18   changed=5    unreachable=0    failed=0    skipped=0    rescued=0    ignored=1
```