# StoreSalesReport-Airflow


## Project workflow:

![workflow](https://github.com/SaiKumarOfficial/StoreSalesReport-Airflow/assets/95096218/57e4b02b-6f85-4d7a-b1bc-8ddbee687b20)

```bash
docker-compose -f .\docker-compose-LocalExecutor.yml up -d
```

Click on http://localhost:8080/

## Mysql connetion on Airflow

Set the Mysql connetion on Airflow by following steps

1. Open webapp and select Admin option
2. Click on Connections
3. Set configuration and save it.
4. Place the connection id at your tasks

After connetion, Click on Trigger DAG and it start running.

## To view the table 

Run the following command

```bash
docker exec -it <mysql-container-id> bash
```
```bash
mysql -u root -p
```
Next, Enter your mysql password

```bash
use mysql;
```
Check the clean_store_transactions table is present or not

```bash
show tables;
```
Finally, after successfully run all the tasks, check your specified email id.

You will get Location wise profit and Store wise profit to your email.


