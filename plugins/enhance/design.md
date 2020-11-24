# design

## service account

create a service account, clusterrole and clusterrole binding to allow
the service account to list and read namespaces to fetch labels associated with the service account 

the labels should be key/value pairs

in the example below, the `owner` label has value `mark'

```
k get ns cromark -o json | jq .metadata.labels
{
  "owner": "mark"
}
```

Note, the labels may or may not exist. In future , we will create a gatekeeper policy to ensure the namespace has the required labels to be enforced on admission control