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

Я Правильно понимаю, что все сертификаты и ключи которые нужны для подключения находятся в директории
![image](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/a378008b-f170-4a09-970b-571c60695cdc)

 Их можно испольховать для написания config файла для kubectl?

------

### Задание 2. Установка и настройка локального kubectl
1. Установить на локальную машину kubectl.

Устанавливаю на туже ВМ

![2  kubectl install](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/af07da54-e83f-4c75-84b1-107fedb6a1ad)

2. Настроить локально подключение к кластеру.

Понятно что нужно написать config файл, но не понимаю где брать ключи для подключения к серверу и пользователю.
Config файл без ключей и сертификатов

![config](https://github.com/ALEMOLOKOV/12.1_K8S_cubectl_Aleksandr_Molokov/assets/109212419/bcfb821c-10fc-4a16-9683-b301f7550927)

3. Подключиться к дашборду с помощью port-forward.


