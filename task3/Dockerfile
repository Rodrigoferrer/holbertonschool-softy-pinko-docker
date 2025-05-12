# Usa la última imagen oficial de Ubuntu
FROM ubuntu:latest

# Actualiza y mejora el sistema
RUN apt-get update && apt-get upgrade -y

# Instala Python 3 y pip3
RUN apt-get install -y python3 python3-pip

# Elimina el error EXTERNALLY-MANAGED al instalar paquetes
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Instala Flask usando pip3
RUN pip3 install flask

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo api.py al contenedor
COPY ./api.py /app/api.py

# Expone el puerto 5252 para acceder al servidor Flask
EXPOSE 5252

# Ejecuta el servidor Flask
CMD ["python3", "api.py"]

