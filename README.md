# Laboratorio Ansible con Docker

## Objetivo de la práctica

Crear un laboratorio con dos servidores Ubuntu 24.04 en contenedores Docker y automatizar tareas básicas en ambos con Ansible: mostrar información del host y del sistema operativo, crear directorios y archivos, usar loops y aplicar condicionales.

## Comandos para iniciar los contenedores

```bash
docker compose up -d
docker ps
```

Instalar Python en cada contenedor:

```bash
docker exec server1 bash -c "apt update && apt install -y python3"
docker exec server2 bash -c "apt update && apt install -y python3"
```

Comprobar la conexión:

```bash
ansible docker -i inventory.ini -m ping
```

## Comando para ejecutar el playbook

```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Captura de la ejecución exitosa
<img width="1915" height="1093" alt="image" src="https://github.com/user-attachments/assets/3f76065a-4b75-4c61-b183-edd88bdad448" />
