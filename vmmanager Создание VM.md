# Адрес панели  
https://lee15636.justinstalledpanel.com:1500/vmmgr  

# **Создание VM**  
Управление -> Виртуальные машины  

# Заполняем данные

**Наименование** - Наименование виртуальной машины. **ОБЯЗАТЕЛЬНОЕ ПОЛЕ. После создания изменить нельзя!!!**  


**Владелец** - Владелец виртуальной машины  

**Узел кластера** - Узел кластера, на котором будет создана виртуальная машина  

**Шаблон VM** - Шаблон виртуальной машины. В нем заданы основные ресурсы
Создано два шаблона  
Windows 10  
Ubuntu 18.04  

**Тип установки** - Тип начальной установки: из шаблона ОС или с ISO-диска  

**Шаблон ОС** - Шаблон операционной системы  

**Рецепт** - Выполнить указанный рецепт (скрипт) в вирутальной машине после установки ОС. 
Для разворачивания XFCE+FF+RDP создан рецепт **xfce**. **Данный рецепт применим только для Debian и Ubuntu!!!**

**Операционная система** - Произвольное наименование операционной системы, установленной на этой машине  

**Тип IP-адреса** - Публичный - с доступом из сети Internet, приватный - без, NAT - для использования с сетями NAT  

**IP-адрес** - Основной IP-адрес  

**Домен** - Доменное имя виртуальной машины. **ОБЯЗАТЕЛЬНОЕ ПОЛЕ**.  

**Размер основного диска** - Размер основного диска в мебибайтах. После создания изменить нельзя  

**Оперативная память** - Объем оперативной памяти в мебибайтах. При изменении необходим перезапуск виртуальной машины  

**Количество процессоров** - Количество виртуальных процессоров доступных виртуальной машине. При изменении необходим перезапуск виртуальной машины  

**Пароль** - Пароль суперпользователя, так же для доступа по VNC. Для доступа по VNC используются только первые 8 символов пароля  

**Подтверждение пароля** - При эмуляции процессора "по умолчанию" используется виртуальный процессор QEMU. При эмуляции в режиме 'host-model' используется описание процессора, определенное libvirt на основе процессора узла кластера. В режиме 'host-passthrough' в точности эмулируется процессор узла кластера. Настройка режима эмуляции может потребоваться для запуска ОС Windows 2016. Не изменяйте режим эмуляции без необходимости  

**Режим эмуляции процессора**  

**MAC-адрес**  

**Отключить антиспуфинг**  

**Установка времени**  

**Вес CPU**  

<span style="color:red">text in red</span>
