# Minkoo
Minkoo is a community-first application where you can connect with others to make things happen! It is inspired by the tradition of the [minka](https://en.wikipedia.org/wiki/Minka), where people in a community get together to help each other out through voluntary, collective labor.

## Architecture overview
```mermaid
architecture-beta
  group minkoo[Minkoo]

  service user(internet)[User]

  group aws(cloud)[AWS] in minkoo
  group docker_2(cloud)[Docker container] in aws
  group docker_3(cloud)[Docker container] in aws
  service back(server)[NestJS Backend] in docker_2
  service db(database)[PostgreSQL DB] in docker_3

  group vercel(cloud)[Vercel] in minkoo
  service front(server)[Nuxt Frontend] in vercel

  front:L -- R:user
  back:L -- R:front
  db:L -- R:back
```

## Related repositories
- [digivoro/minkoo-front](https://github.com/digivoro/minkoo-front) - Nuxt frontend
- [digivoro/minkoo-back](https://github.com/digivoro/minkoo-back) - NestJS backend

## Local development
### Prerequisites
> [!IMPORTANT]  
> Work in progress

### Quick start
1. Clone repositories
2. Copy environment files
3. Start application
4. Visit http://localhost:3000 to see the application running

## Deployment
> [!IMPORTANT]  
> Work in progress

## Features
> [!IMPORTANT]  
> Work in progress

## Roadmap
- Markets and Listings to be added as features