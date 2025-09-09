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
