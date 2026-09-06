# Apache_Airflow

# Apache Airflow provides some command line options

## 1. Apache Airflow CLI

1. Run the command below in the terminal to list all the existing DAGs.

```sh
airflow dags list
```

**Output**

```
dag_id                          | fileloc                       | owners  | is_paused
================================+===============================+=========+==========
conditional_dataset_and_time_ba | /home/airflow/.local/lib/pyth | airflow | True     
sed_timetable                   | on3.9/site-packages/airflow/e |         |          
                                | xample_dags/example_datasets. |         |          
                                | py                            |         |          
consume_1_and_2_with_dataset_ex | /home/airflow/.local/lib/pyth | airflow | True     
pressions                       | on3.9/site-packages/airflow/e |         |          
                                | xample_dags/example_datasets. |         |          
                                | py                            |         |          
```

2. Run the command below in the terminal to list all tasks in the DAG named ```example_bash_operator```

```sh
airflow tasks list example_bash_operator
```

**Output**

```
also_run_this
run_after_loop
run_this_last
runme_0
runme_1
runme_2
this_will_skip
```

## 2. Pause or Unpause a DAG

1. Run the command below in the terminal to unpause a DAG named tutorial

```sh
airflow dags unpause tutorial
```

**Output**

```
INFO - Filling up the DagBag from /home/project/airflow/dags
dag_id   | is_paused
=========+==========
tutorial | True     
```

2. Run the command to pause the DAG.

```sh
airflow dags pause tutorial
```

**Output**

```
INFO - Filling up the DagBag from /home/project/airflow/dags
dag_id   | is_paused
=========+==========
tutorial | False    
```