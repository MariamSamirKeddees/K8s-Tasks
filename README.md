# K8s-Tasks - Task1
i created a kubectl secret using this command:
	kubectl create secret generic db-root-password --from-literal=MYSQL_ROOT_PASSWORD=[pass]
then i created a deployment yaml file to contain:
	service - deployment - mysql containers - PVC - env variable to store password secret
	
#############################################################################################

# K8s-Tasks - Task2
