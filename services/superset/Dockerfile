FROM apache/superset
# Switching to root to install the required packages
USER root

COPY Cisco_Umbrella_Root_CA.cer ./
RUN pip install sqlalchemy-trino || \
    pip install --cert Cisco_Umbrella_Root_CA.cer  --trusted-host pypi.org sqlalchemy-trino 
# Switching back to using the `superset` user
USER superset

## ToDo: La mejor practica es hacer estos proceso al lanzar el conenedor utilizando "enviroment variables". Esto es 
#       solo una prueba de concepto
RUN superset fab create-admin \
               --username admin \
               --firstname Superset \
               --lastname Admin \
               --email admin@superset.com \
               --password admin && \
    superset db upgrade && \
    superset init

