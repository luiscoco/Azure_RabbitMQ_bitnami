# How to create a RabbitMQ server with Azure Portal or Azure CLI

## 1. Create a RabbitMQ server with Azure Portal

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/50dbe78b-ed4c-4d4e-aefe-3552cecd4a50)



## 2. Create a RabbitMQ server with Azure CLI

```
az vm create --resource-group myRG --name rabbitmq --admin-username azureuser --generate-ssh-keys --image bitnami:rabbitmq:rabbitmq:latest --plan-name rabbitmq --plan-product rabbitmq --plan-publisher bitnami --public-ip-sku Standard
```

```
az account set --subscription 99888cc6-c635-4ebd-b0ac-1be1dace0089
```

```
az vm open-port --port 5672 --name rabbitmqvm --resource-group myRG
```

```
az vm open-port --port 15672 --name rabbitmqvm --resource-group myRG --priority 1100
```

```
cat ./bitnami_credentials
```


http://172.160.241.201:15672/


http://localhost:15672/




