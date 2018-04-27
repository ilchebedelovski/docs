<!-- TITLE: Helm -->
<!-- SUBTITLE: A quick summary of Helm -->

## Helm

`$ helm init`

List all installed charts
`$ helm list`
`$ helm list --all`

Delete chart
`$ helm delete`
Will remove whole chart with purge
`$ helm delete --purge psql-service`

For installing chart
`$ helm install ./crunchy-postgres -n psql-service --namespace services`

Upgrade chart
`$ helm upgrade crunchy-postgres  ./crunchy-postgres  --namespace crunchy-postgres `

Examines a chart for possible issues
`$ helm lint`
For debugging for possible errors in the release
`$ helm lint releasename`

This command shows the details of a named release
`$ helm get`
`$ helm get release`
Get details for release
`$ helm get manifest relase`

Rollback to previous version
`$ helm rollback happy-panda 1`

Will download the deis repo
`$ helm fetch deis/workflow`