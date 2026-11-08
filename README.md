# 🎟️ Ticket Sales API

API REST para venda de ingressos de eventos: parceiros cadastram eventos e lotes de ingressos, e clientes compram e cancelam compras.

> 🚧 **Em desenvolvimento.** As regras de negócio completas estão em [`requisitos.md`](requisitos.md).

## Stack
TypeScript · Node.js · Express 5 · MySQL (mysql2) · bcrypt

## O que já funciona
- `POST /partners`: cadastra usuário + parceiro, com senha criptografada (bcrypt)
- Modelagem do banco em [`db.sql`](db.sql): `users`, `partners`, `customers`, `events`

## Próximos passos
- Cadastro de clientes e eventos, login com JWT
- Compra de ingressos com controle de concorrência
- Testes automatizados, Docker e documentação Swagger

## Como rodar
```bash
cp .env.example .env   # configure o MySQL
mysql -u root -p < db.sql
npm install
npm run dev
```
Exemplos de requisição em [`api.http`](api.http).
