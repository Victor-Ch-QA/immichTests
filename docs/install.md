## Установка приложения immich

Windows 10/11, Docker Desktop for Windows (или WSL2)  
(Linux/MacOS опционально - некоторые команды отличаются)

Системные требования:  
ОЗУ: минимум 4ГБ  
Процессор: минимум 2 ядра  
ПЗУ: минимум 5ГБ

### Пример алгоритма установки / Команды
Запустить Windows PowerShell и выполнить клманды:  
New-Item -Path 'D:\immich' -ItemType Directory - создать папку на диске D  
cd D:\immich - перейти в созданный каталог  
wget -O docker-compose.yml https://github.com/immich-app/immich/releases/latest/download/docker-compose.yml - загрузить файл docker-compose.yml  
wget -O .env https://github.com/immich-app/immich/releases/latest/download/example.env - загрузить файл с примером настроек  
docker-compose pull - загрузить docker-образы  
docker-compose up -d - запустить контейнеры приложения

### Обновление сервера (по необходимости)
В  Windows PowerShell выполнить последовательно команды:  
cd D:\immich  
docker-compose pull  
docker-compose up -d

https://immich.app/docs/install/docker-compose


