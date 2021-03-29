# Docker 

**1.Use Docker to create network**

 `docker network create PythonMySQL`

**2.MySQL container**

`docker run -v "$(pwd)":/var/lib/mysql --name PythonMySQL -e MYSQL_ROOT_PASSWORD=****** --network PythonMySQL -d mysql:5.7`

**3.Jupyter container**

`docker run -d --name PythonSQL -p 8890:8888 --network PythonMySQL -v "$(pwd)":/home/jovyan/work jupyter/datascience-notebook start-notebook.sh --NotebookApp.token=''`