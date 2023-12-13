#### Helpful Linux Commands for Daily Use

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

###### Trigger Kubernetes Job from CronJob
```
kubectl create job --from=cronjob/<cronjob-name> <job-name-to-be-created> -n <namespace-name>
```
