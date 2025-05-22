
# Kubernetes - Comandos Imperativos

## 🐳 Pods
```bash
kubectl run NOME_POD --image=IMAGEM [--restart=Never]
kubectl run nginx-pod --image=nginx --restart=Never
```

## 📦 Deployments
```bash
kubectl create deployment NOME_DEPLOY --image=IMAGEM
kubectl create deployment nginx-deploy --image=nginx
```

## 🔁 Atualizar imagem de um deployment
```bash
kubectl set image deployment/NOME_DEPLOY NOME_CONTAINER=IMAGEM:NOVA_TAG
kubectl set image deployment/nginx-deploy nginx=nginx:1.21
```

## 🌐 Services
```bash
kubectl expose pod NOME_POD --port=80 --target-port=80
kubectl expose deployment NOME_DEPLOY --type=ClusterIP|NodePort|LoadBalancer --port=PORTA
```

## 📁 Namespaces
```bash
kubectl create namespace NOME_NAMESPACE
```

## 📄 ConfigMap
```bash
kubectl create configmap NOME_CM --from-literal=chave=valor
kubectl create configmap NOME_CM --from-file=/caminho/do/arquivo
```

## 🔐 Secret
```bash
kubectl create secret generic NOME_SECRET --from-literal=chave=valor
kubectl create secret generic NOME_SECRET --from-file=/caminho/do/arquivo
```

## 💾 PersistentVolume (gerar YAML)
```bash
kubectl create pv NOME_PV --dry-run=client -o yaml > pv.yaml
```

## 📦 PersistentVolumeClaim
```bash
kubectl create pvc NOME_PVC --access-modes=ReadWriteOnce --resources=requests.storage=200Mi --dry-run=client -o yaml > pvc.yaml
```

## 🔧 Jobs
```bash
kubectl create job NOME_JOB --image=IMAGEM
```

## ⏰ CronJobs
```bash
kubectl create cronjob NOME_CJ --image=IMAGEM --schedule="*/5 * * * *"
```

## 🚫 Deletar objetos
```bash
kubectl delete pod NOME_POD
kubectl delete deployment NOME_DEPLOY
kubectl delete svc NOME_SERVICE
```

## 🧪 Gerar YAML com dry-run
```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml
```

## 📌 Dicas Extras

- Listar pods: `kubectl get pods`
- Ver detalhes de pod: `kubectl describe pod NOME_POD`
- Logs de um pod: `kubectl logs NOME_POD`
- Entrar no pod: `kubectl exec -it NOME_POD -- /bin/sh`
