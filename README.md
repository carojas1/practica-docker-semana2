# Informe de Práctica: Servidor Web con Docker

### 1. Título
Despliegue y personalización de servidores web Nginx mediante contenedores Docker.

### 2. Tiempo de duración
45 minutos.

### 3. Fundamentos:
Como estudiante de desarrollo, entiendo que Docker es una herramienta que nos facilita la vida al empaquetar aplicaciones en contenedores. A diferencia de las máquinas virtuales que cargan todo un sistema operativo y consumen mucha RAM, los contenedores comparten el núcleo del sistema anfitrión, lo que los hace súper rápidos y ligeros.

En esta práctica usamos **Nginx**, que es un servidor web muy potente. La ventaja de usar Docker es que podemos levantar varios servidores al mismo tiempo en la misma máquina sin que se peleen, simplemente mapeando diferentes puertos como el 8089 y el 8090.

### 4. Conocimientos previos.
Para esta práctica, necesité tener claros estos temas:
* Comandos básicos de la terminal de Linux (`echo`, `ls`, `cp`).
* Conceptos de redes y cómo funcionan los puertos.
* Manejo de repositorios en GitHub.

### 5. Objetivos a alcanzar
* Levantar contenedores con Nginx de forma independiente.
* Usar el comando `docker cp` para mover archivos de mi PC al contenedor.
* Personalizar el contenido de cada servidor web.

### 6. Equipo necesario:
* Computadora con Windows.
* Cuenta en GitHub.
* Entorno de laboratorio Killercoda.
* Navegador Chrome.

### 7. Material de apoyo.
* Guía de la asignatura de Tendencias Actuales.
* Documentación oficial de Docker.
* Tutoriales de Markdown.

### 8. Procedimiento

**Paso 1: Creación de los contenedores.** Empecé levantando los servidores con la imagen oficial de Nginx. El del instituto lo puse en el puerto 8089 y mi perfil personal en el 8090.

*(Aquí pon la foto donde se ve que escribiste el comando: `docker run -d --name nginx1...`)*
![Comando de creación](AQUÍ_PEGA_TU_FOTO_DE_LA_TERMINAL_1)

**Paso 2: Creación de los archivos HTML.**
Usé el comando `echo` para crear los archivos `index.html` con la información del IST y mis datos personales.

*(Aquí pon la foto donde se ve que escribiste el comando: `echo "<h1>IST..." > index1.html`)*
![Comando echo](AQUÍ_PEGA_TU_FOTO_DE_LA_TERMINAL_2)

**Paso 3: Transferencia con Docker CP.**
Finalmente, moví los archivos de la terminal hacia adentro de cada contenedor para que se actualice la página.

*(Aquí pon la foto donde se ve que escribiste el comando: `docker cp index1.html nginx1...`)*
![Comando docker cp](AQUÍ_PEGA_TU_FOTO_DE_LA_TERMINAL_3)

### 9. Resultados esperados:
Se logró que cada puerto muestre una página personalizada. Aquí las capturas del funcionamiento:

**Servidor 1: Información Institucional (Puerto 8089)**
![Resultado 8089](image_0e6edf.png)

**Servidor 2: Información Estudiante (Puerto 8090)**
![Resultado 8090](image_0e6ea8.png)

### 10. Bibliografía
* Turnbull, J. (2017). *The Docker Book: Containerization is the new virtualization*. Lulu.com.
* Hamilton, J. (2007). *On designing and deploying internet-scale services*. USENIX Association.
