# 🐧 Trabajo Práctico Final – Administración de Sistemas Linux
## Grupo:
♦️ Alumno A: Andrea Lima

♦️ Alumno B: Federico Rodriguez

♦️ Alumno C: Cecilia Woitasen

## 🎯 Objetivo del Proyecto
El objetivo general de este trabajo práctico fue aplicar conocimientos clave de administración de sistemas Linux en un entorno virtualizado, colaborando como equipo a través de Git y desplegando servicios reales usando contenedores con Docker y Docker Compose.

## ⚙️ Tecnologías Utilizadas
### 🪟 En Windows
Vagrant + VirtualBox: Para la gestión automatizada de máquinas virtuales sobre arquitectura x86.

Ubuntu 22.04 (Jammy Jellyfish): Distribución utilizada como base del sistema operativo en la VM.

### 🍎 En Mac con chip M1
Vagrant + QEMU: Para la gestión de máquinas virtuales compatibles con arquitectura ARM.

CentOS 7: Distribución base del sistema operativo utilizada en la VM.

### ♣️ Git & GitHub: Control de versiones y trabajo colaborativo.

### 🐳 Docker & Docker Compose: Despliegue de servicios en contenedores.

### 🖥️ Neofetch: Visualización del sistema operativo.

### 🧰 Herramientas Linux: Bash, fdisk, mkfs, mount, etc.

## 📂 Estructura del Proyecto

```
practica-linux-lima-rodriguez-woitasen/
├── archivos/
│   └── verificacion_archivos.txt
├── contenedores/
│   ├── docker-compose.yml
│   ├── capturas/
│   └── verificacion_contenedores.txt
├── discos/
│   └── verificacion_discos.txt
├── permisos/
│   ├── usuarios_Chechu.txt
│   └── verificacion_permisos.txt
├── informacion/
│   └── system_info.txt
└── README.md
```

# 🛠️ Configuración del Entorno
## 📋 Requisitos Previos
### 🪟 En Windows:
◽️ Vagrant

◽️ VirtualBox (como proveedor de virtualización)

◽️ Git y Github

◽️ Docker y Docker Compose (se instalan dentro de la VM)

### 🍎 En Mac:
🔸 Vagrant

🔸 QEMU (como proveedor de virtualización compatible con arquitectura ARM)

🔸 Git y Github

🔸 Docker y Docker Compose (se instalan dentro de la VM)

# 👣 Pasos:

🔺 Clonar el repositorio en la VM.

🔺 Ejecutar vagrant up para levantar la máquina virtual.

🔺 Acceder con vagrant ssh.

# 🔍 Ejercicios Realizados
### 1. Neofetch
Cada alumno ejecutó neofetch y guardó la salida en informacion/system_info.txt.

### 2. Permisos y Usuarios
Se crearon usuarios locales y un grupo colaborativo.

Se configuraron permisos sobre directorios personales y compartidos.

Verificaciones en verificacion_permisos.txt.

### 3. Discos
Se agregó un disco adicional con Vagrant.

Se particionó, formateó y montó en /mnt/almacenamiento_*.

Se agregó entrada en /etc/fstab.

### 4. Archivos y Directorios
Estructuras creadas en los discos montados.

Operaciones básicas con archivos (cp, mv, rm, touch).

Registro en verificacion_archivos.txt.

### 5. Contenedores con Docker
Instalación de Docker y Docker Compose.

Creación del archivo docker-compose.yml.

Despliegue del contenedor Pi-hole.

# 🐛 Desafíos Encontrados
## Conectividad
Problemas con el acceso a la interfaz web del contenedor Pi-hole desde la VM para Mac M1. Se exploraron múltiples soluciones relacionadas con puertos, redes y configuraciones internas del contenedor.

## Configuración del Vagrantfile
Modificar el Vagrantfile para reenviar puertos causó conflictos en Mac M1 con QEMU. Se optó por mantener la configuración más estable posible sin afectar el arranque.

## SSH colgado y VM que no levantaba
A veces, la VM no permitía conectarse por vagrant ssh tras cambios en red o puertos. La solución fue reconstruir desde cero con vagrant destroy y revisar cuidadosamente los cambios.

# 📌 Conclusión
Este trabajo nos permitió afianzar conceptos clave de administración de sistemas Linux en un entorno colaborativo real. Desde la virtualización y el control de versiones hasta la contenedorización de servicios, cada etapa presentó desafíos que pudimos resolver en equipo.
Los mayores conflictos, se generaron dentro del Sistema Operativo de MacOS, por problemas de compatibilidades entre MacOS, CentOS, Docker, y demás tecnologías.
