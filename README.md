#### Helpful Commands for Daily Use

###### Disk usage
```
df -h
```

###### Find Size of a Dir and its content
```
du -hs /path/to/dir
```

###### Find Size of a Dir individual folders and sort by size
```
du -h | sort -h
```

###### use SUDO without password prompt for current user
```
sudo visudo
```

In the bottom of the file, add the following line:
```
$USER ALL=(ALL) NOPASSWD: ALL
```

###### Check port usage
```
sudo lsof -i :8000
```

###### Trigger Kubernetes Job from CronJob
```
kubectl create job --from=cronjob/<cronjob-name> <job-name-to-be-created> -n <namespace-name>
```

###### Find the current connection slot usage and limits in PostgreSQL
```
   select max_conn, used, res_for_super,((max_conn - res_for_super)-used) as res_for_normal
   from
   (select count(*) used from pg_stat_activity) t1,
   (select setting::int res_for_super from pg_settings
   where name='superuser_reserved_connections') t2,
   (select setting::int max_conn from pg_settings where name='max_connections') t3
```

###### Enable COPY PASTE between HOST machine and Virtualbox machine
https://codetryout.com/vbox-guest-additions-ubuntu-22/

###### Kdenlive Noise Suppressor Plugin for Ubundu
https://kentwest.neocities.org/westk/librnnoise

###### Export all env vars from `.env` before running a script
```
export $(cat .env | xargs) && python main.py
```
