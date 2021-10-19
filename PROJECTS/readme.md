# Project use  

First you need to create your cutsoms secrets 


## MYSQL_SECRET

kubectl create secret generic mysql-wp \
--from-literal=rootpwd=Password \ --from-literal=database=wordpress \
--from-literal=user=dbuserwordpress \
--from-literal=userpwd=UserPassword \
 -o yaml  > mysqlsecret.yaml \



