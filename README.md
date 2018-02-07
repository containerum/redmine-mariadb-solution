# Redmine with MariaDB

Redmine is a flexible web application for project management. It includes Gantt charts, calendar, wiki, forums, role management, e-mail notifications, etc.

### How it works

The server with Redmine and MariaDB database is launched on containerum.com platform. Redmine provides a web UI for managing your projects.

### It consists of:

* Redmine
* MariaDB


To launch this solution on Containerum.com sign up with the service, download and use [Containerum CLI](https://github.com/containerum/chkit) `chkit`.

1. Run the Solution with `chkit solution`:
```
chkit solution run redmine-mariadb-solution -e VOLUME=storage
```
* VOLUME parameter should contain your Volume name on containerum.com platform (VOLUME=volumename)

2. Make sure that the Solution is running:
```
$ chkit get deploy

+------------------------+------+-------------+------+-------+-----+
|     NAME               | PODS | PODS ACTIVE | CPU  |  RAM  | AGE |
+------------------------+------+-------------+------+-------+-----+
| solution-mariadb-2fiiq |    1 |           1 | 500m | 512Mi | 5m  |
| solution-redmine-2fiiq |    1 |           1 | 500m | 512Mi | 5m  |
+------------------------+------+-------------+------+-------+-----+
```

3. Using `chkit get` get the address and the port to access the running Solution:
```
$ chkit get svc

+------------------------+---------------+----------+-------------------+----------------+-----+
|     NAME               |  CLUSTER-IP   | EXTERNAL |       HOST        |     PORTS      | AGE |
+------------------------+---------------+----------+-------------------+----------------+-----+
| solution-mariadb-2fiiq | 10.98.107.80  | false    |                -- | 3306/TCP       | 6m  |
| solution-redmine-2fiiq | 10.97.175.125 | true     | x3.containerum.io | 32643:3000/TCP | 6m  |
+------------------------+---------------+----------+-------------------+----------------+-----+
```
4. Go to `x3.containerum.io:32643`and create queues using UI.

![](/gif/redminepsqlsln.gif)
