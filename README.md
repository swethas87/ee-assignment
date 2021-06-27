# ee-assignment
#Configure helloworld using python and loadbalance using minikube

I have used python to create the helloworld application (app.py)
configured docker file for the same- and was exposing using the port 3000. 


eval $(minikube docker-env)   #to enforce docker daemon
docker build -t helloworld_1:0.1 .


minikube tunnel

kubectl create deployment hello-world-dep --image=helloworld_1:0.1
deployment.apps/hello-world-dep created

niksa@DESKTOP-0VEF8N2 MINGW64 ~/OneDrive/Desktop/DevOps Projects/ee-assignment
$ kubectl expose deployment hello-world-dep --type=LoadBalancer --port=3000
service/hello-world-dep exposed


I have provided screeshots for the rest of the output. 

i tried to push the image to my dockerhub , but the container in the pod was crashing.
when i run the container using the docker- i get the output, but in the pod its crashing. 
