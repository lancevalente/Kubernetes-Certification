# 🛠️ Comandos Helm para Kubernetes

## 📦 Instalação de Chart

```bash
helm install <nome-release> <repositório/chart> --namespace <namespace>
```

**Exemplo:**

```bash
helm install my-nginx bitnami/nginx --namespace web
```

---

## 🔍 Verificar Releases Instaladas

```bash
helm list --all-namespaces
```

---

## 📁 Adicionar Repositório Helm

```bash
helm repo add <nome-repo> <url-repo>
```

**Exemplo:**

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
```

---

## 🔄 Atualizar Repositórios

```bash
helm repo update
```

---

## 📈 Atualizar um Release

```bash
helm upgrade <nome-release> <repositório/chart> --namespace <namespace>
```

---

## 🔄 Rollback de um Release

```bash
helm rollback <nome-release> <número-da-versão>
```

---

## 🧪 Instalar em modo Dry-Run

```bash
helm install <nome-release> <repositório/chart> --dry-run --debug
```

---

## 📤 Desinstalar um Release

```bash
helm uninstall <nome-release> --namespace <namespace>
```

---

## ⚙️ Verificar Valores de um Chart

```bash
helm show values <repositório/chart>
```

---

## 📄 Usar valores personalizados

```bash
helm install <nome-release> <repositório/chart> -f valores.yaml --namespace <namespace>
```

---

## 🛑 Exemplo de `valores.yaml`

```yaml
replicaCount: 2
service:
  type: LoadBalancer
  port: 80
```

---

## 📚 Ver Documentação do Helm

```bash
helm help
helm install --help
```

---

## 🗃️ Ver Detalhes de um Release

```bash
helm get all <nome-release>
```
