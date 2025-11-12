# Construir imagen
docker build --no-cache -t josegm13/dmc_proyecto_gestion_infra:latest 

# Listar la imagen construida
docker images | grep "dmc_proyecto_gestion_infra

# Ejecutar contenedor
docker run -d -p 8080:8080 josegm13/dmc_proyecto_gestion_infra

# Probar con curl
curl http://localhost:8080/hello

# Tagear la imagen
docker tag josegm13/dmc_proyecto_gestion_infra josegm13/dmc_proyecto_gestion_infra:1

# Logearse a DockerHub
docker login

# Subimos la imagen a DockerHub
docker push josegm13/dmc_proyecto_gestion_infra:1