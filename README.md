# How to create a RabbitMQ server with Azure Portal or Azure CLI

## 1. Create a RabbitMQ server with Azure Portal

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/50dbe78b-ed4c-4d4e-aefe-3552cecd4a50)

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/c9dcd06f-dcda-4bf5-9716-cb99fa602b00)

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/907810d0-c35b-4ab6-9dea-ec91b01d7b45)

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/dbef1c2e-c49b-47a8-be9b-d2c13c7bbaa1)

## 2. Create a RabbitMQ server with Azure CLI

We type this command to create a new RabbitMQ server in Azure

```
az vm create ^
--resource-group myRG ^
--name rabbitmq ^
--admin-username azureuser ^
--generate-ssh-keys ^
--image bitnami:rabbitmq:rabbitmq:latest ^
--plan-name rabbitmq ^
--plan-product rabbitmq ^
--plan-publisher bitnami ^
--public-ip-sku Standard ^
--location westeurope
```

We connect to the 


```
az account list --output table
```

```
az account set --subscription XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

```
az group list --output table
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

http://23.97.142.56:15672/

http://localhost:15672/

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/60db7d9a-e960-4d80-9987-9655e5adb47d)

![image](https://github.com/luiscoco/Azure_RabbitMQ_bitnami/assets/32194879/e2d80471-841b-4b89-80c5-57617d8a8306)

You can use the username:guest and password:guest
