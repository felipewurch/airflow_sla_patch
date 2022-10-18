# airflow_sla_patch
In Airflow’s context, SLA can be seen as “for how long your DAG can run before you need to do something about it”. You can set any datetime interval you want, and if the execution time of your DAG exceeds that, Airflow will automatically trigger a function defined by you. However, Airflow`s SLA has some issues:
- SLA only works for scheduled DAGs
- SLA for tasks is counter intuitive
