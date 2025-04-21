# Terraform-AKS
A simple AKS using Terraform

#### Comandos terraform
```bash
terraform init
terraform plan -out plan.out 
terraform apply "plan.out"
```

## Configuración de AKS 

### Suscription ID
- Encontrar suscripcion
```bash
az account show --query id --output tsv
```
- Seleccionarla
```bash
az account set --subscription "<subscription-name-or-id>"
```
### Credenciales para kubectl
```bash
az aks get-credentials --resource-group rg-aks-demo --name aks-demo
```
### Ver contexto
```bash
kubectl config current-context
```

### Destruir recursos con Terraform
```bash
terraform destroy
```

### Eliminar el contexto local
```bash
kubectl config delete-context <context-name>
```
