# test senarios

## chaos

```
k run crash --namespace default --image=alpine --command -- sh  -c "while :; do cat /zz;  sleep 900 ; done"
```

```
k create job failed --image=alpine -- cat /zz
```