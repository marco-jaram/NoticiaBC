# Portal de noticias
### Requiere
- Docker, docker-compose
- Levantando servico docker con mysql:
  
```
  docker-compse up -d
```

### Obteneindo direccion ip de BD mySql

```
docker ps
```
Sustituir <CONTAINER ID> por el id de tu contenedor
```
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <CONTAIDER ID>
```
```
salida de ejemplo 172.18.0.2
```
- Con la direccion ip , el nombre y la clave podras conectarte a la BD desde cualquier gestor 
- Si usas Dbeaver
en connection properties habilita allowPublicKeyRetrieval poniendole true
```
allowPublicKeyRetrieval | true

```