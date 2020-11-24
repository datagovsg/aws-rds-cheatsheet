# RDS cheatsheet

Referenced from : [https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.MaxConnections](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Limits.html#RDS_Limits.MaxConnections)

## Maximum Concurrent Connections

### Aurora

| Instance       | Max Connections |
| -------------- | --------------- |
| db.t2.small    | 45              |
| db.t2.medium   | 90              |
| db.t3.small    | 45              |
| db.t3.medium   | 90              |
| db.r3.large    | 1000            |
| db.r3.xlarge   | 2000            |
| db.r3.2xlarge  | 3000            |
| db.r3.4xlarge  | 4000            |
| db.r3.8xlarge  | 5000            |
| db.r4.large    | 1000            |
| db.r4.xlarge   | 2000            |
| db.r4.2xlarge  | 3000            |
| db.r4.4xlarge  | 4000            |
| db.r4.8xlarge  | 5000            |
| db.r4.16xlarge | 6000            |


### MariaDB and MySQL

RDS MariaDB and MySQL max connections are constrained by the formula:

`Instance Memory / 12582880`

| Instance       | vCPUs | Memory (GB) | Max Connections |
| -------------- | ----- | ----------- | --------------- |
| db.t2.micro    | 1     | 1           | 85              |
| db.t2.small    | 1     | 2           | 171             |
| db.t2.medium   | 2     | 4           | 341             |
| db.t2.large    | 2     | 8           | 683             |
| db.t2.xlarge   | 4     | 16          | 1365            |
| db.t2.2xlarge  | 8     | 32          | 2731            |
| db.t3.micro    | 2     | 1           | 85              |
| db.t3.small    | 2     | 2           | 171             |
| db.t3.medium   | 2     | 4           | 341             |
| db.t3.large    | 2     | 8           | 683             |
| db.t3.xlarge   | 4     | 16          | 1365            |
| db.t3.2xlarge  | 8     | 32          | 2731            |
| db.r4.large    | 2     | 15.25       | 1301            |
| db.r4.xlarge   | 4     | 30.5        | 2603            |
| db.r4.2xlarge  | 8     | 61          | 5205            |
| db.r4.4xlarge  | 16    | 122         | 10411           |
| db.r4.8xlarge  | 32    | 244         | 20821           |
| db.r4.16xlarge | 64    | 488         | 41643           |


### PostgreSQL

RDS PostgreSQL max connections are constrained by the formula:

`LEAST({DBInstanceClassMemory/9531392}, 5000)`

| Instance       | vCPUs | Memory (GB) | Max Connections |
| -------------- | ----- | ----------- | --------------- |
| db.t2.micro    | 1     | 1           | 112             |
| db.t2.small    | 1     | 2           | 225             |
| db.t2.medium   | 2     | 4           | 450             |
| db.t2.large    | 2     | 8           | 901             |
| db.t2.xlarge   | 4     | 16          | 1802            |
| db.t2.2xlarge  | 8     | 32          | 3604            |
| db.t3.micro    | 2     | 1           | 112             |
| db.t3.small    | 2     | 2           | 225             |
| db.t3.medium   | 2     | 4           | 450             |
| db.t3.large    | 2     | 8           | 901             |
| db.t3.xlarge   | 4     | 16          | 1802            |
| db.t3.2xlarge  | 8     | 32          | 3604            |
| db.r4.large    | 2     | 15.25       | 1717            |
| db.r4.xlarge   | 4     | 30.5        | 3435            |
| db.r4.2xlarge  | 8     | 61          | 5000            |
| db.r4.4xlarge  | 16    | 122         | 5000            |
| db.r4.8xlarge  | 32    | 244         | 5000            |
| db.r4.16xlarge | 64    | 488         | 5000            |
