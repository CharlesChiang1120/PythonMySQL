# PythonMySQL

**1.Use Docker to create network**
\- [x] Command : `docker network create PythonMySQL`

**2.MySQL container**
\- [x] Command : `docker run -v "$(pwd)":/var/lib/mysql --name PythonMySQL -e MYSQL_ROOT_PASSWORD=****** --network PythonMySQL -d mysql:5.7`

**3.Jupyter container**
\- [x] Command : `docker run -d --name PythonSQL -p 9000:8888 -v "$(pwd)":/home/jovyan/work jupyter/pyspark-notebook start-notebook.sh --NotebookApp.token=''`