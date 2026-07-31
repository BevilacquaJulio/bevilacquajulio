<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./header-light.svg">
  <img src="./header-dark.svg" width="100%" alt="Julio Cesar — Desenvolvedor Full Stack" />
</picture>

<div align="center">

[![Portfólio](https://img.shields.io/badge/Portf%C3%B3lio-bevilabs.com.br-38BDF8?style=for-the-badge&logo=googlechrome&logoColor=white)](https://bevilabs.com.br)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julio-bevi)
[![E-mail](https://img.shields.io/badge/E--mail-juliobevi1@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:juliobevi1@gmail.com)

</div>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./sobre-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./sobre-light.svg">
  <img src="./sobre-dark.svg" width="100%" alt="Sobre mim" />
</picture>

---

## Arquitetura padrão

Não escrevo sistemas soltos. Os projetos abaixo compartilham **a mesma arquitetura, o mesmo
pipeline de deploy e as mesmas convenções** — o que torna cada novo sistema previsível de
construir e barato de manter.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./arquitetura-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./arquitetura-light.svg">
  <img src="./arquitetura-dark.svg" width="100%" alt="Arquitetura padrão: React/Vite → Traefik → NestJS → Prisma → MySQL" />
</picture>

```text
Controller  →  Service  →  Repository  →  Prisma  →  MySQL
   HTTP        regra de     acesso a      query      dados
   + Zod       negócio       dados       tipada
```

Cada camada tem uma responsabilidade única. O `Controller` valida com **Zod** e não conhece o
banco; o `Repository` conhece o banco e não conhece HTTP. Isso mantém a regra de negócio testável
sem subir infraestrutura.

---

## Stack

<table>
<tr><th align="left">Camada</th><th align="left">Tecnologias</th></tr>

<tr><td><b>Backend</b></td><td>
<img src="https://img.shields.io/badge/NestJS_11-E0234E?style=flat-square&logo=nestjs&logoColor=white">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white">
<img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white">
<img src="https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black">
<img src="https://img.shields.io/badge/Pino-687634?style=flat-square&logo=pino&logoColor=white">
<img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white">
</td></tr>

<tr><td><b>Frontend</b></td><td>
<img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black">
<img src="https://img.shields.io/badge/Vite_6-646CFF?style=flat-square&logo=vite&logoColor=white">
<img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white">
<img src="https://img.shields.io/badge/React_Hook_Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white">
<img src="https://img.shields.io/badge/React_Router-CA4245?style=flat-square&logo=reactrouter&logoColor=white">
<img src="https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white">
<img src="https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white">
</td></tr>

<tr><td><b>Dados</b></td><td>
<img src="https://img.shields.io/badge/Prisma_7-2D3748?style=flat-square&logo=prisma&logoColor=white">
<img src="https://img.shields.io/badge/MySQL_8.4-4479A1?style=flat-square&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white">
</td></tr>

<tr><td><b>Infra &amp; Deploy</b></td><td>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
<img src="https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white">
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white">
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
<img src="https://img.shields.io/badge/Hostinger_VPS-673DE6?style=flat-square&logo=hostinger&logoColor=white">
</td></tr>

<tr><td><b>Qualidade</b></td><td>
<img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white">
<img src="https://img.shields.io/badge/Testing_Library-E33332?style=flat-square&logo=testinglibrary&logoColor=white">
<img src="https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white">
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
</td></tr>

</table>

---

## Projetos em destaque

<table>
<tr>

<td width="50%" valign="top">

### 🏭 [Atlas Stock](https://github.com/BevilacquaJulio/atlas_stock)

ERP para empresas de **blindagem automotiva**. Centraliza compras, estoque,
projetos por veículo, consumo de materiais e movimentações financeiras.

Autenticação com *access* + *refresh token*, controle de acesso por função,
exclusão lógica e checklist de status por projeto.

`NestJS 11` `React 19` `Prisma 7` `Tailwind 4` `Docker`

</td>
<td width="50%" valign="top">

### 📋 [Change Tracker](https://github.com/BevilacquaJulio/change_tracker)

Rastreamento de **itens de mudança** em projetos web — bugs, melhorias e
implementações — com evidências visuais, auditoria e colaboração multiprojeto.

**Reescrito de FastAPI + vanilla para NestJS + React** mantendo banco, regras
de negócio e interface idênticos. Zero regressão visual.

`NestJS 11` `React 19` `Prisma 7` `Vitest` `Docker`

</td>
</tr>
<tr>

<td width="50%" valign="top">

### 🌐 [Bevilabs Portfólio](https://github.com/BevilacquaJulio/bevilabs_portfolio)

Portfólio construído como **sistema real de ponta a ponta**, não como página
estática: API própria, banco e painel de administração.

Em produção sob **Traefik**, com API e frontend em containers separados
compartilhando instância MySQL.

`NestJS 11` `React 18` `Prisma 7` `Traefik` `Nginx`

</td>
<td width="50%" valign="top">

### 💰 [Financeiro](https://github.com/BevilacquaJulio/financeiro)

Controle financeiro pessoal com categorização de lançamentos, relatórios e
fechamento por período.

API e SPA em containers independentes atrás do Traefik, usando o MySQL
compartilhado da infraestrutura.

`NestJS 11` `React 18` `Prisma 7` `Docker` `Traefik`

</td>
</tr>
</table>

<div align="center">

[![Controle de Pedidos](https://img.shields.io/badge/+_Controle_de_Pedidos-NestJS_·_React-1F2937?style=flat-square&logo=github&logoColor=white)](https://github.com/BevilacquaJulio/controle_pagamento)
[![Motor Racing](https://img.shields.io/badge/+_Motor_Racing-React_·_Canvas_scrubbing-1F2937?style=flat-square&logo=github&logoColor=white)](https://github.com/BevilacquaJulio/Formula1)

</div>

---

## De onde eu venho

Comecei em **Python/FastAPI** e **PHP**, com frontends em HTML/CSS/JS puro. Ao longo de 2026
migrei essa base para **NestJS + React/Vite + Prisma**, um sistema por vez, com um requisito
inegociável: *nenhuma mudança de comportamento visível para o usuário*.

Em vários casos o CSS original foi movido intacto e a marcação reproduzida classe por classe —
migrar stack sem quebrar a experiência de quem usa é uma restrição bem mais dura do que
reescrever do zero, e foi ela que definiu a arquitetura que uso hoje.

---

## Estatísticas

<div align="center">

<img src="./github-metrics.svg" width="100%" alt="Métricas do GitHub" />

</div>

---

<div align="center">

### Vamos conversar

[![Portfólio](https://img.shields.io/badge/bevilabs.com.br-38BDF8?style=for-the-badge&logo=googlechrome&logoColor=white)](https://bevilabs.com.br)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julio-bevi)
[![E-mail](https://img.shields.io/badge/juliobevi1@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:juliobevi1@gmail.com)

</div>
