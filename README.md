# ead_java_alura_jsf

compilação de todas partes dos cursos de jsf da alura + docker

<!--
## Setup com Podman

- Inicie o Podman

```sh
podman machine init
podman machine start
```

> Caso precise mexer nos containers, pare eles com `podman-compose down --remove-orphan` e, após modificações, inicie novamente com `podman-compose up --build`

- Inicie o ambiente

```sh
podman-compose up
```

- A cada modificação, compile novamente

```sh
podman-compose exec compiler mvn clean package
```

- Acesse a partir de `http://localhost:8080/login.xhtml`
-->


## Setup com Docker

> Caso precise mexer nos containers, pare eles com `docker-compose down --remove-orphan` e, após modificações, inicie novamente com `docker-compose up --build`

- Inicie o ambiente

```sh
docker-compose up
```

- A cada modificação, compile novamente e move para a pasta correta

```sh
docker-compose exec compiler mvn clean package
docker-compose exec compiler mv target/livraria.war tomcat/webapps/livraria.war
```

- Acesse a partir de `http://localhost:8080/livraria/login.xhtml`
