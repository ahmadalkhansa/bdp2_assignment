# bdp2_assignment

- create a repository structure
- create a Dockerfile in the docker directory and use it to install matplotlib in jupyter notebook minimal image
- after commiting dockerhub will build the docker file automatically
- run the built image in dockerhub using this command ```docker run -p 8888:8888 2281995/bdp2_assignment```
- use the data in 'https://raw.githubusercontent.com/pcm-dpc/COVID-19/master/dati-json/dpc-covid19-ita-andamento-nazionale.json' file to plot a graph, exploiting any information inside it.
- ```docker run -v /home/ubuntu/assignment/bdp2_assignment/work/:/home/jovyan/work -p 8888:8888 2281995/bdp2_assignment``` is used for mapping the repo directory "work" to the container directory "work"
- Next stop jupyter and portainer to form an application stack of both. It is built using Docker-compose.yml file. Install docker-compose ```sudo apt update && sudo apt install -y docker-compose```
- build the stack ```docker-compose up -d```.
- portainer is used to get the token for accessing jupyter-notebook container. In addition, X.509 certificate is generated using GEN_CERT=yes attribute in the jupyter environment. Therefore, jupyter is accessed through https instead of the usual http.
