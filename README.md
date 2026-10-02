# docker-mini-apps

Trois petites applications, chacune avec un `Dockerfile` en une seule étape et un `Dockerfile.multi` allégé.

- `spring` : Spring Boot 4.1.1, Java 21, port 8080
- `next-app` : Next.js 16.3.8, port 3000
- `node-app` : Node 24 et Express, port 3000

## Construire

```bash
docker build -t spring-mini:simple ./spring
docker build -f Dockerfile.multi -t spring-mini:multi ./spring

docker build -t next-mini:simple ./next-app
docker build -f Dockerfile.multi -t next-mini:multi ./next-app

docker build -t node-mini:simple ./node-app
docker build -f Dockerfile.multi -t node-mini:multi ./node-app
```

## Lancer

```bash
docker run --rm -p 8081:8080 spring-mini:simple
docker run --rm -p 8082:8080 spring-mini:multi
docker run --rm -p 3011:3000 next-mini:simple
docker run --rm -p 3012:3000 next-mini:multi
docker run --rm -p 3013:3000 node-mini:simple
docker run --rm -p 3014:3000 node-mini:multi
```

Spring répond `hello from spring` sur `/`. Next répond sur `/` et `/api/hello`. Node répond `hello from node` sur `/`.
