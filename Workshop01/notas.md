# Taller de Vagrant y Debian Bookworm

**Curso:** Administración de Sistemas Operativos  
**Estudiante:** Robert Quesada  
**Fecha:** [Fecha de entrega]

---

# Objetivo

Instalar y configurar un entorno virtual utilizando VirtualBox y Vagrant para aprovisionar una máquina virtual con GNU/Linux Debian Bookworm 64 Bits.

---

# Requisitos

- Sistema operativo Linux (Pop!_OS)
- Conexión a Internet
- Permisos de administrador (sudo)

---

# 1. Instalación de VirtualBox

## Verificar si VirtualBox está instalado

```bash
virtualbox --help
```

### Captura de pantalla

![Verificación de VirtualBox](images/virtualbox-check.png)

---

## Instalación de VirtualBox

Se descargó VirtualBox desde su sitio oficial y se instaló siguiendo las instrucciones correspondientes al sistema operativo.

### Captura de pantalla

![Instalación de VirtualBox](images/virtualbox-install.png)

---

# 2. Instalación de Vagrant

## Verificar si Vagrant está instalado

```bash
vagrant --version
```

### Captura de pantalla

![Versión de Vagrant](images/vagrant-version.png)

---

## Instalación de Vagrant

Se descargó el paquete oficial de Vagrant y se instaló utilizando el gestor de paquetes del sistema.

### Captura de pantalla

![Instalación de Vagrant](images/vagrant-install.png)

---

# 3. Creación del proyecto Vagrant

## Crear directorio de trabajo

```bash
mkdir taller-vagrant
cd taller-vagrant
```

### Captura de pantalla

![Directorio de trabajo](images/project-folder.png)

---

## Inicializar Vagrant

```bash
vagrant init debian/bookworm64
```

Este comando genera el archivo `Vagrantfile`.

### Captura de pantalla

![Vagrant Init](images/vagrant-init.png)

---

# 4. Aprovisionamiento de Debian Bookworm

## Levantar la máquina virtual

```bash
vagrant up
```

Vagrant descargará la imagen de Debian Bookworm 64 Bits y creará la máquina virtual automáticamente.

### Captura de pantalla

![Vagrant Up](images/vagrant-up.png)

---

## Verificar el estado de la máquina virtual

```bash
vagrant status
```

### Captura de pantalla

![Estado VM](images/vagrant-status.png)

---

# 5. Acceso a la máquina virtual

## Conectarse mediante SSH

```bash
vagrant ssh
```

### Captura de pantalla

![Vagrant SSH](images/vagrant-ssh.png)

---

# 6. Comandos Bash aprendidos durante el taller

## Mostrar directorio actual

```bash
pwd
```

Ejemplo:

```bash
vagrant@bookworm:~$ pwd
/home/vagrant
```

---

## Listar archivos

```bash
ls
```

```bash
ls -la
```

### Captura de pantalla

![Comando ls](images/bash-ls.png)

---

## Crear directorios

```bash
mkdir laboratorio
```

---

## Cambiar de directorio

```bash
cd laboratorio
```

---

## Crear archivos

```bash
touch archivo.txt
```

---

## Visualizar contenido

```bash
cat archivo.txt
```

---

## Editar archivos

```bash
nano archivo.txt
```

---

## Copiar archivos

```bash
cp archivo.txt respaldo.txt
```

---

## Mover o renombrar archivos

```bash
mv archivo.txt nuevo_nombre.txt
```

---

## Eliminar archivos

```bash
rm nuevo_nombre.txt
```

---

## Información del sistema

```bash
uname -a
```

---

## Usuario actual

```bash
whoami
```

---

# 7. Prueba del servidor web

Se creó una página HTML simple.

## Archivo index.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>Vagrant</title>
</head>
<body>
    <h1>Esta es una página sencilla servida con Vagrant</h1>
</body>
</html>
```

### Captura de pantalla

![Página web](images/web-page.png)

---

# 8. Apagar la máquina virtual

```bash
vagrant halt
```

### Captura de pantalla

![Vagrant Halt](images/vagrant-halt.png)

---

# 9. Eliminar la máquina virtual

```bash
vagrant destroy
```

### Captura de pantalla

![Vagrant Destroy](images/vagrant-destroy.png)

---

# Conclusiones

Durante el taller se aprendió a:

- Instalar VirtualBox.
- Instalar Vagrant.
- Aprovisionar una máquina virtual Debian Bookworm.
- Acceder a la máquina mediante SSH.
- Utilizar comandos básicos de Bash.
- Administrar el ciclo de vida de una máquina virtual con Vagrant.

---

# Referencias

- Documentación oficial de Vagrant.
- Documentación oficial de VirtualBox.
- Apuntes y práctica realizada durante el taller.