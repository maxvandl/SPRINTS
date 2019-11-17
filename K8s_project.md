Требование к инфраструктуре K8s тестовый  
0. Операционная система RHEL.  
1. Колличество ВМ 7  шт.  
Master Node - 5 шт. (RAM - 4GB, HDD - 100 GB)  
Worker Node - 3 шт. (RAM - 64Gb, HDD - 400Gb)  


Краткая схема и описание архитектуры развертывания  
![Diagram](https://hsto.org/webt/qo/mi/un/qomiunfreqwd2oyor5h-hjrjzm8.png)
|Имена хостов   |	IP адрес|Описание |	Компоненты|
| ------------- |:---------:| :------:|:---------:|
|hb-master01 ~ 03| 	172.26.133.21 ~ 25| 	master nodes * 5| 	keepalived, nginx, etcd, kubelet, kube-apiserver, kube-scheduler, kube-proxy, kube-dashboard|
|N\A |	172.26.133.20 |	keepalived virtual IP |	N\A
hb-node01 ~ 03 |	172.26.133.26 ~ 28 	|Рабочие ноды * 3 	|kubelet, kube-proxy|



2. Необходимые инфраструктурные изменения
- DNS зона.
- Диапазон  адресов.
- AD авторизация.
- Внесение изменений в код приложений для работы с Service Discovery K8s.
- Переход стадии CD на использование Config server.
- Переход на использование репозитория Кубернетес.
- Создание служебного пользователя
  - для репозитория артефактов
  - для К8s
3. Выбор типа сети внутри K8s.
4. Выбор типа сетевого хранилища K8s. (VmFS, etc...)
5. Необходимо принять решение о внесении/ не внесении, саттелитных сервисов внутрь Кубера.
Примечание: Если внести их внутрь Кубера кратно возрастёт затрата на хранилище
6. Необходимо определить необходимое колличество Namespaces.

Примечание: Данные требования только для тестовой инсталяции, которая включает 19 контейнеров и необходимое для оценки колличество сред. Необходимо принять решение вносятся ли в K8s базы данных и стека ELK. Колличество артефактов описывается методом GFS. 
Для ELK Необходимо учесть текущие ошибки, как то грамотно рассчитать необходимый размер хранилища и политику ротации логов.
