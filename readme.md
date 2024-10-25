Instructions ( docker required ).  From the repo root:

#### Step 1

```
// run grafana and mysql
docker compose up
```

#### Step 2
Log into grafana and create another Org named `2`.

#### Step 3
```
docker stop grafana
```

#### Step 4
Now remove the comments from `./provisioning/dashboards` and `./provisioning/datasoources` to provision Org 2

#### Step 5
```
docker start grafana
```

#### Step 6
Log into grafana and see both Orgs.  Each org has the same dashboards.

#### Step 7
Copy the cluster.json file from `./providers/dashboards/1` to `./providers/dashboards/2`

#### Step 8
Check the `dashboard_versions` table in mysql.
```
localhost:3306
database=grafana
user=grafana
password=password
```



