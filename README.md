# redmine-mysql-solution

## About
![](images/redmine-mysql.png)

This solution consists two tools: [Redmine](http://www.redmine.org) and [MySQL](https://www.mysql.com).

[Redmine](http://www.redmine.org) is a flexible project management web application written using Ruby on Rails framework.

[MySQL](https://www.mysql.com) is an open-source relational database management system.


**Here we run this solution in one command with [Containerum](https://containerum.com).**

We use [this Redmine image](https://hub.docker.com/_/redmine/) and this [MySQL image](https://hub.docker.com/_/mysql/) from DockerHub.

## How to deploy on Containerum

**1.** Sign Up at [containerum.com](https://containerum.com)

**2.** Install CLI Containerum `chkit` following [instruction](https://containerum.com/documentation/Installing-Containerum-CLI-from-binaries).

**3.** Open Terminal and run `chkit login`

```
$ chkit login
Enter your email: test@gmail.com
Password:
********
Chosen namespace: mynamespace
Successful login
Token changed to:  QA0u64rOkTtCxxxxxxxxxxliUAnBnPlCbGQfpCQpzqM=
```
**4.** Use command `run solution`
