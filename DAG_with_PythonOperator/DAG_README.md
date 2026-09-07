# Submit a DAG

1. Open a terminal and run the command below to set the ```AIRFLOW_HOME```

```sh
export AIRFLOW_HOME=/home/project/airflow
echo $AIRFLOW_HOME
```

2. Run the command below to submit the DAG that was created in the previous exercise

```sh
 cp my_first_dag.py $AIRFLOW_HOME/dags
```

3. Verify that your DAG actually got submitted

4. Run the command below to list out all the existing DAGs

```sh
airflow dags list
```

5. Verify that ```my-first-python-etl-dag``` is a part of the output

```sh
airflow dags list|grep "my-first-python-etl-dag"
```

6. You should see your DAG name in the output.

7. Run the command below to list out all the tasks in ```my-first-python-etl-dag```

```sh
airflow tasks list my-first-python-etl-dag
```

8. You should see all the four tasks in the output

**Output**
```
check
extract
load
transform
```

9. You can run the task from the Web UI. You can check the logs of the tasks by clicking the individual task in the Graph view.