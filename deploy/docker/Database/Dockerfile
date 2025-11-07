FROM mongo:3.4

# Copia los scripts/archivos de inicialización a la ruta que la imagen oficial
# de MongoDB ejecuta automáticamente al iniciar cuando la base está vacía.
# Esto evita sobrescribir el ENTRYPOINT/CMD y evita pasar opciones obsoletas
# como --smallfiles o --rest.
COPY drop/* /docker-entrypoint-initdb.d/

# No sobreescribimos el ENTRYPOINT ni el CMD de la imagen oficial.
