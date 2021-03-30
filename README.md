# datalake4os
Development architecture to test data lake concepts in the context of the generation and publication of statistical and geographic data.

## Vision
![img](./img/datalake4os.jpg)

## How to run 
```bash
docker-compose up -d
```
After a short wait, a jupyter notebook can be accesed in any web browser at
http://[docker-ip]:8888
If you ar running docker localy then it should be 
http://localhost:8888
And the password is 'password'
Open the notebook in the directory 'scripts', follow the instructions and play arround with the examples.

You can also acces to web interfaces for
- Minio at port :9000 . User minio password minio123
- Trino at port :8080 . Just write aniting and it will let you pass 

*to stop*
```bash
docker-compose down
```

**Note:** If you are runnig it on windows and you receive an error /bin/bash not found on hive-metastore. You have to modify line endings to linux style on the files of services\hive\bin

## Inspired
This work is inspired by the repository: https://github.com/zhenik-poc/big-data-stack-practice