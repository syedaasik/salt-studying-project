# Useful saltstack commands

### Ping
---
#### Test minion from master 

``` $ salt 'minion_id' test.ping ```

**Example:** salt 'server' test.ping

---

### Copy
---
#### Copy files from minion to master

``` $ salt 'minion_id' cp.push /path/file_name ``` [ File should exist in minion ]

**Example:** salt 'server' cp.push /etc/fstab

#### Copy directory from minion to master

``` $ salt 'minion_id' cp.push_dir /path/file_name ``` [ Folder should exist in minion ]

**Example:** salt 'server' cp.push_dir /tmp/test_folder

**Note:** File and folder pushed from minion to master will be stored in 
( /var/cache/salt/master/minions/minion_id/files/ )

---