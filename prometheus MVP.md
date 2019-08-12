

План реализации MVP мониторинга  
1. Выбираем провайдера где будем разворачивать VM для мониторинга  
2. Устанавливаем на выбор OS ( Ubuntu LTS/CENTOS 7)  
3. Устанавливаем Docker  
4. Устанавливаем контейнеры для работы с Prometheus  
https://github.com/stefanprodan/dockprom.git  
5. Пп. 1-4 выполняем с помощью terrafform файла  
6. Данные для prometheus берем из Consul  
7. Если объект мониторинга сервер на него надо установить NodeExporter  
https://github.com/prometheus/node_exporter  


![Diagram](https://github.com/maxvandl/SPRINTS/blob/master/Untitled%20Diagram.png)

