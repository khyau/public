# Generate TPC-DS data
https://github.com/gregrahn/tpcds-kit

```
cd ~/tpcds-kits/tools
./dsdgen -scale 1000 -f -dir /mnt/efs/fs1/1tb -parallel 2 -child 1&
./dsdgen -scale 1000 -f -dir /mnt/efs/fs1/1tb -parallel 2 -child 2&
```

# Install MySQL client
```
wget https://dev.mysql.com/get/mysql80-community-release-el7-3.noarch.rpm
sudo yum install ./mysql80-community-release-el7-3.noarch.rpm
sudo yum install mysql-community-client
```

# Create tables
```
cd ~/tpcds-kits/tools
mysql -h m\xxxxx.us-east-1.rds.amazonaws.com -u admin -p -D tpcds < tpcds.sql
```

# Load data
https://gist.github.com/corvuslee/dda9bae48ebfd19ff1c88900ffc0cc96

# Database metrics

