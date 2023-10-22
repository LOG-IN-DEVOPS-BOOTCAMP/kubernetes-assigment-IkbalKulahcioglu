# kubernetes-assigment-IkbalKulahcioglu
kubernetes-assigment-IkbalKulahcioglu created by GitHub Classroom


Node.js uygulamasını oluşturduktan sonra terminal üzerinden terminal üzerinden Dockerfile oluşturdum.

•	controlplane $ vi Dockerfile

Komutunu terminale girdim ardından Dockerfile içeriğini oluşturdum.

 

Docker image oluşturmak için aşağıdaki komutu kullandım

•	controlplane $ docker build -t web-app:v1         

Daha sonrasında deployment ve services dosyalarını oluşturdum.

Oluşturduğum bu yaml dosyalarını kullanarak Kubernetes’e kaydettim. Bunun için aşağıdaki komutu kullandım.

•	controlplane $ kubectl apply -f web-app-v1-deployment.yaml
•	deployment.apps/web-app-v1 created
•	controlplane $ kubectl apply -f web-app-v1-service.yaml
•	service/web-app-v1-service created

Aynı adımları ikinci ortamı oluşturmak içinde uyguladım.
Aşağıdaki komutlarla uygulamalara eriştim.

•	controlplane $ kubectl get svc web-app-v1-service
•	NAME                 TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE
•	web-app-v1-service   ClusterIP   10.101.113.171   <none>        80/TCP    5m9s
•	controlplane $ kubectl get svc web-app-v2-service
•	NAME                 TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)   AGE
•	web-app-v2-service   ClusterIP   10.103.151.21   <none>        80/TCP    32s


![image](https://github.com/LOG-IN-DEVOPS-BOOTCAMP/kubernetes-assigment-IkbalKulahcioglu/assets/65568713/8dbe444d-a2b1-4b13-a170-80b966a61d49)
