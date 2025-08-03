![saltstack](images/saltstack.png)

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

### Get
---
#### Get file from master to minion

``` $ salt 'server' cp.get_file salt://sample_file /tmp/sample_file ``` [ File should exist in salt roots]

**Example:** salt 'server' cp.get_file salt://test_file /tmp/test_file

#### Get directory from master to minion

``` $ salt 'server' cp.get_dir salt://sample_folder /tmp/sample_folder ``` [ File should exist in salt roots]

**Example:** salt 'server' cp.get_dir salt://test_folder /tmp/test_folder

---

### CMD 
---
#### Run any linux command on minion

``` $ salt 'minion_id' cmd.run 'command' ``` [ Run any linux command ]

**Example:** salt 'server' cmd.run uptime


