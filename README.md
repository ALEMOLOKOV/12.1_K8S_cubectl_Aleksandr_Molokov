# 12.1_K8S_cubectl_Aleksandr_Molokov

Для выполнения задания использую ВМ в YandexCloud, пробую также установить на нее kubectl 

![ВМ](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/3f75b527-0c2e-4dc0-8a1c-c42f1e7a4330)

### Задание 1. Установка MicroK8S

1. Установить MicroK8S на локальную машину или на удалённую виртуальную машину.
2. Установить dashboard.
3. Сгенерировать сертификат для подключения к внешнему ip-адресу.

## Ответ

1. Установить MicroK8S на локальную машину или на удалённую виртуальную машину.

![1 1 mikrok8s install version and nodes](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/f1313d40-52fb-460c-b9e9-d201a7012a61)

2. Установить dashboard.
Установка dashbord с помощью команды microk8s enable dashboard

![enable dashboard](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/c61ff911-898d-4b6a-88b5-b9c780fde5d0)

![1 1 mikrok8s status](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/e318aa51-cc85-45b3-b339-5852fc797b8f)

3. Сгенерировать сертификат для подключения к внешнему ip-адресу.

Исправление файла /var/snap/microk8s/current/certs/csr.conf.template
![добавление IP](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/ca7c803a-7383-4a3f-9ab7-76e3311bc89c)

Обновление сертификата sudo microk8s refresh-certs --cert front-proxy-client.crt

![обновление сертификата](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/f4d34753-e9ca-485f-b9b9-7001a41ce526)

------

### Задание 2. Установка и настройка локального kubectl
1. Установить на локальную машину kubectl.



![2  kubectl install](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/af07da54-e83f-4c75-84b1-107fedb6a1ad)

2. Настроить локально подключение к кластеру.
Команда kubectl get nodes
![kubectlget nodes](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/a9048e28-c703-49ca-a601-831fedceed8c)

3. Подключиться к дашборду с помощью port-forward.

![port-forward](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/d095aff2-2172-4b10-9a8b-384941d2a359)

![kubectl-portforward](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/dadfc713-fe3a-4f2e-ac70-5b6dbd6b5a8f)





