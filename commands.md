
# إنشاء pod
kubectl run my-nginx --image=nginx
kubectl run my-nginx --image=nginx123

# التحقق من حالة pod
kubectl describe pod my-nginx

# حذف pod
kubectl delete pod my-nginx

# إنشاء pod من YAML
kubectl apply -f pod.yaml
ReplicaSet

# إنشاء ReplicaSet من YAML
kubectl apply -f replicaset.yaml

# زيادة عدد replicas
kubectl scale replicaset nginx-replicaset --replicas=5

# تعديل ReplicaSet مباشرة
kubectl edit replicaset nginx-replicaset
Deployment

# إنشاء deployment
kubectl create deployment httpd-frontend --image=httpd:2.4-alpine --replicas=3

# تغيير صورة deployment
kubectl set image deployment/httpd-frontend httpd=nginx777

# التراجع عن deployment
kubectl rollout undo deployment/httpd-frontend

# الحصول على معلومات deployment
kubectl describe deployment <deployment-name>
Docker commands

# بناء image
docker build -t bushetaa66/taskk8s:latest .

# تسجيل الدخول إلى DockerHub
docker login

# رفع image
docker push bushetaa66/taskk8s:latest

# التحقق من جميع الموارد
kubectl get all

# التحقق من pods
kubectl get pods

# التحقق من deployments
kubectl get deployments

# وصف مورد محدد
kubectl describe pod <pod-name>
kubectl describe replicaset <replicaset-name>
kubectl describe deployment <deployment-name>