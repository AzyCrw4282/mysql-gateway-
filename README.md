This project allows interaction with the MySQL database over HTTP


## What is it?

To interact wit the `mysql` database it requires you to either access it via the 
work-bench or on the `cmd-line/terminal` through `mysql` cli. This for simple operation
is cumbersome and so this was born to solve that, e.g.

To `SELECT * from users`, you simply do
```
curl http://localhost:8080/getTable=users
```

## Intended Features

- get the table, 
- get a row by id, 
- get required coloumns
- update where field=<value>,
- delete where field=<value>,
- insert operation

-- For all above, be able to limit results

- get filtered values from multiple columns

-- For all above, perform aggregate function

- Perform operations on relational table 


## Usage | Instructions

First create a `.env` file and add your details. An example is shown below:
```.env
listenAddr=:8080
ost=localhost
user=postgres
password=
db=User1
port=58379
```

- get the table, 

To `SELECT * from users`, you simply do
```
curl http://localhost:8080/getTable=users
```
- get a row by id(PK), 

To `SELECT * from users WHERE x=$1`, you simply do
```
curl http://localhost:8080/getTable=users?WHERE x=$1
```

- get required coloumns

To `SELECT $0,$1,$2 from users`, you simply do
```
curl http://localhost:8080/getTable=users?SELECT= $0,$1,$2
```

----------------------------TBD, Once above are complete---------------------------

- update where field=<value>,
To `SELECT  from users`, you simply do
```
curl http://localhost:8080/getTable=users
```



- delete where field=<value>,

To `SELECT  from users`, you simply do
```
curl http://localhost:8080/getTable=users
```



- insert operation
To `SELECT  from users`, you simply do
```
curl http://localhost:8080/getTable=users
```



- get filtered values from multiple columns





- Perform operations on relational table 





#### Acknowledgements

This project was inspired by the works from user @just1689 and his project, `pg-gatway` where postgresql db can be interacted 
over HTTP using module such as `curl` .



#### Packages used