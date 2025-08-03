# Useful saltstack commands


#### Test minion from master 

$ salt 'minion_id' test.ping 

**Example:** salt 'server' test.ping


#### Copy files from minion to master

$ salt 'minion_id' cp.push /path/file_name [ File should exist in minion ]

**Example:** salt 'server' cp.push /etc/fstab