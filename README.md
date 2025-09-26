# K8s-Tasks - Task1
i created a kubectl secret using this command:
	kubectl create secret generic db-root-password --from-literal=MYSQL_ROOT_PASSWORD=[pass]
then i created a deployment yaml file to contain:
	service - deployment - mysql containers - PVC - env variable to store password secret
	
#########################################################

# K8s-Tasks - Task2
i created a private key to use in crt generating
then created the crt 
the crt got copied and pasted in the crt.yaml file, within the spec's request
applied the file
CSR approved
signed certificate is retrieved
RBAC created through applying role.yaml 
role binding is done in the same method
user's access validation --result is refused
new user added to kubectl 
user's context added
switched to the new user successfully 
user's access is now valid

#########################################################

# K8s-Tasks - Task3
i created the calculator using nodejs 
dockerized it and pushed it to docker hub
created k8s deployment using the docker image i pushed previously with its service and ingress
used nginx as ingress controller using following command:
-- kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.11.2/deploy/static/provider/cloud/deploy.yaml --

as i'm working on minikube i should create minikube tunnel everytime to make it accessible from browser, so when you clone the work do the following steps:
	- minikube tunnel in seperate terminal 
	- in your primary terminal use this command:
		kubectl get svc -n ingress-nginx 
	- to get the external ip you should put in the ingress yaml file as the host, then apply the file
	- go to browser and browse this: http://the-host-provided-in-ingress.yaml.nip.io 
