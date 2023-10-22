# kubernetes-assigment-IkbalKulahcioglu
kubernetes-assigment-IkbalKulahcioglu created by GitHub Classroom


Node.js uygulamasını oluşturduktan sonra terminal üzerinden terminal üzerinden Dockerfile oluşturdum.

•	controlplane $ vi Dockerfile

Komutunu terminale girdim ardından Dockerfile içeriğini oluşturdum.

 <img width="306" alt="image" src="https://github.com/LOG-IN-DEVOPS-BOOTCAMP/kubernetes-assigment-IkbalKulahcioglu/assets/65568713/6f113b0e-4b74-419f-8b8e-9b6c4fd78ed1">


Docker image oluşturmak için aşağıdaki komutu kullandım

	docker build -t web-app:v1         

Daha sonrasında deployment ve services dosyalarını oluşturdum.

Oluşturduğum bu yaml dosyalarını kullanarak Kubernetes’e kaydettim. Bunun için aşağıdaki komutu kullandım.

	kubectl apply -f web-app-v1-deployment.yaml
 
	kubectl apply -f web-app-v1-service.yaml

Aynı adımları ikinci ortamı oluşturmak içinde uyguladım.
Aşağıdaki komutlarla uygulamalara eriştim.

     kubectl get svc web-app-v1-service
 NAME                 TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE\

 web-app-v1-service   ClusterIP   10.101.113.171   <none>        80/TCP    5m9s
 
    kubectl get svc web-app-v2-service
  
NAME                 TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)   AGE

web-app-v2-service   ClusterIP   10.103.151.21   <none>        80/TCP    32s


