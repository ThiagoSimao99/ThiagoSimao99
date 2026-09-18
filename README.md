# Olá, eu sou o Thiago Vitor Simão 👋

**Desenvolvedor Full-Stack** (Python · Django · React) e **Analytics Engineer em formação** (SQL · dbt · Airflow).
Brasília, DF 🇧🇷

Hoje sou estagiário de **desenvolvimento de sistemas no Ministério da Defesa**. Antes, fui estagiário de **Dados e Governança na Secretaria de Educação do DF** (Out/2025 – Set/2026), onde trabalhei num Data Warehouse que atende **400 mil alunos**. Em paralelo, desenvolvo aplicações web para clientes reais — **quatro sites meus estão no ar e em uso agora**.

Formo em **Análise e Desenvolvimento de Sistemas (UDF) em dezembro de 2026** e busco oportunidade como **Desenvolvedor Júnior** ou na área de **Dados**.

### 🌐 Portfólio completo: **[thiagosimao99.github.io](https://thiagosimao99.github.io/)**

---

## 🏛️ Onde eu estou hoje — Ministério da Defesa

Estagiário de desenvolvimento de sistemas (desde Set/2026): desenvolvimento e manutenção de sistemas em **PHP**, análise de documentação de negócio e requisitos, e testes de software.

## 🏢 O que eu fiz na SEEDF (Out/2025 – Set/2026)

Trabalhei na camada de governança e transformação de um Data Warehouse público:

- **Cataloguei 1.200+ tabelas** no OpenMetadata, organizando a descoberta e a qualidade dos dados
- **Escrevi 68+ documentações técnicas** para **35 projetos dbt**, mapeando a lineage completa — do banco de origem até o dashboard
- **Desenvolvi 10 consultas SQL analíticas** sobre o DW, validadas e adotadas para extração de indicadores educacionais
- **Construí modelos de staging e marts em dbt** a partir dessas consultas, com **mart em produção no esquema prata** alimentando painéis no Metabase
- **Montei dashboards no Metabase** para 20+ domínios (censo, matrículas, RH, programas sociais, transporte escolar)
- **Atuei em chamados de correção do i-Educar** (sistema de gestão escolar da rede), investigando e corrigindo inconsistências de histórico escolar direto no banco PostgreSQL de produção

`PostgreSQL` `SQL Analítico` `dbt` `Apache Airflow` `Metabase` `OpenMetadata` `DBeaver` `Git`

---

## 🚀 Projetos em produção

Sites que desenvolvi para clientes reais e que estão no ar hoje:

### 🥩 [Carboneiro Defumado](https://carboneiro.com.br)
Açougue artesanal em Brasília. Cardápio interativo com catálogo por categoria e pedido direto no WhatsApp via deep-link por produto.
**React 19 · Vite · React Router · Docker · Nginx** — deploy containerizado em VPS

### 🥊 [Maradok Academia](https://moradokmuaythai.com.br)
Academia de Muay Thai com duas unidades. Captação de leads por WhatsApp, galeria e integração com Google Maps.
**React 19 · Vite · Docker · Nginx · GitHub Actions** — *deploy automático:* o merge do PR na `main` dispara build e sobe o container na VPS por SSH

### 🛋️ [Brito Móveis](https://britomoveisnovoseusados.com)
Loja de móveis novos e usados. Catálogo com busca e filtro por categoria e preço, portal de avaliação de móvel usado e formulário de encomenda. A cliente gerencia o catálogo por um painel administrativo, sem depender de mim para publicar produto.
**React 19 · Tailwind v4 · PocketBase · Docker · Nginx · GitHub Actions · Certbot**

### 🏗️ [BM Construtora](https://bmconstrutora.site)
Construtora de Brasília com obras comerciais, industriais e residenciais. Portfólio com filtro por categoria e lightbox navegável por teclado, orçamento direto no WhatsApp. A cada PR o CI roda lint, build e **testa rotas, cache e headers contra um Nginx real**; a **acessibilidade (WCAG) e a performance foram medidas no build de produção** — contraste conferido pixel a pixel sobre as fotos, WebP, code splitting por rota e fontes auto-hospedadas.
**React 19 · Vite 8 · CSS puro · Docker · Nginx · GitHub Actions · Certbot**

### 🔧 A infraestrutura por trás dos quatro

Os quatro rodam na **mesma VPS Linux**, atrás de **um único proxy reverso Nginx** que termina TLS para os quatro domínios com Let's Encrypt e roteia cada requisição para o container certo.

No Brito o roteamento é **por caminho**: `/api/` e `/_/` vão para o PocketBase e `/` para o build do React — tudo no mesmo domínio, sem CORS. O **banco não expõe porta pública**: só é alcançável pela rede interna do Docker, através do proxy. Os containers têm **healthcheck, limite de memória e CPU, e rotação de logs**.

---

## 🛠️ Projetos em finalização

### 🏛️ SimãoDatta — Site institucional full-stack
Sistema para uma empresa de TI do setor público com 39 anos de atuação. O conteúdo do site (serviços, produtos, clientes, parceiros e notícias) vive no banco e é editado pelo Django Admin, **sem precisar de redeploy** — e o front tem fallback estático se a API cair.

- **Back:** Django 6 · DRF · PostgreSQL · Gunicorn · uv · settings separados por ambiente
- **Front:** React 19 · Tailwind CSS v4 · Framer Motion · React Hook Form
- **Qualidade:** Pytest · Ruff · CI a cada push · Docker (dev e prod) · workflow de deploy
- **Segurança:** honeypot anti-spam e rate limit de 5 envios/hora por IP no formulário

### 💎 Luxe Perfumes — E-commerce full-stack
Loja completa de perfumes importados, do carrinho ao rastreio do pedido.

- **Back:** Django 6 · DRF · JWT (SimpleJWT) · Google OAuth · MySQL
- **Integrações:** MercadoPago (Pix, cartão, boleto) · Melhor Envio (frete) · ViaCEP
- **Front:** React 19 · Vite · Axios · Swiper · React Router v7
- **Funcionalidades:** carrinho, checkout, rastreio por CPF, painel administrativo

---

## 🌱 Também em desenvolvimento

**Melhor Amigo** — clínica veterinária e pet shop · *React 19 · Vite · React Router v7*

**Portal Luís Carlos Alcoforado** — portfólio digital de um jurista, escritor e poeta: trajetória, artigos, livros e poesias · *React 19 · Vite*

> 🔒 **Sobre os repositórios estarem privados:** esses são projetos contratados por clientes reais, então o código não é meu para publicar. Posso apresentar arquitetura, decisões técnicas e demonstração ao vivo em qualquer conversa — é só chamar.

---

## 💻 Stack

**Back-end** · Python · Django · Django REST Framework · Gunicorn · APIs REST · JWT

**Front-end** · JavaScript · React 19 · Vite · Tailwind CSS v4 · Framer Motion · HTML5 · CSS3

**Dados** · SQL · PostgreSQL · MySQL · dbt · Apache Airflow · Metabase · OpenMetadata · Modelagem Relacional

**DevOps** · Docker · Nginx · GitHub Actions · Linux · Git · VPS

**Qualidade** · Pytest · Ruff · ESLint · uv

---

## 🎓 Formação e certificações

**Análise e Desenvolvimento de Sistemas** — UDF Centro Universitário · conclusão em Dez/2026
**Técnico em TI** — CEMIC · concluído em 2022

Python Essentials 1 (Cisco) · Introdução ao Git e GitHub (FGV Online) · GitHub Actions CI/CD (Udemy) · DevOps: Terraform, Kubernetes, Ansible, AWS e Azure (Udemy) · Python do Zero ao Avançado (Udemy) · Crie Agentes de IA: do Zero ao Deploy (Udemy) · Google AI Essentials (Google/Coursera)

**Idiomas:** Português (nativo) · Inglês (avançado) · Espanhol (básico)

---

## 📫 Contato

[![Portfólio](https://img.shields.io/badge/Portf%C3%B3lio-38BDF8?style=for-the-badge&logo=googlechrome&logoColor=white)](https://thiagosimao99.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thiagosimao-dev)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tvsimao2005@gmail.com)

📍 Brasília, DF · Aberto a vagas remotas, híbridas e presenciais

---

<details>
<summary><b>🇺🇸 In English</b></summary>

<br>

I'm a **Full-Stack Developer** (Python · Django · React) and **Analytics Engineer in training** (SQL · dbt · Airflow), based in Brasília, Brazil.

I currently work as a **Software Development intern at Brazil's Ministry of Defense** (PHP, requirements analysis, testing). Before that I was a **Data Governance intern at the Federal District Department of Education** (Oct 2025 – Sep 2026), on a Data Warehouse serving **400,000 students** — where I cataloged 1,200+ tables in OpenMetadata, wrote 68+ technical docs across 35 dbt projects, built staging and mart models feeding the analytics layer, and fixed student-record inconsistencies directly in the production PostgreSQL database.

Alongside that, I build web applications for real clients. **Four are live in production today**: [carboneiro.com.br](https://carboneiro.com.br), [moradokmuaythai.com.br](https://moradokmuaythai.com.br), [britomoveisnovoseusados.com](https://britomoveisnovoseusados.com) and [bmconstrutora.site](https://bmconstrutora.site) — all running on a single Linux VPS behind one Nginx reverse proxy terminating TLS for the four domains, with CI/CD via GitHub Actions.

I graduate in **Systems Analysis & Development (Dec 2026)** and I'm open to **junior developer** and **data engineering** roles.

Client repositories are private, but I'm happy to walk through architecture and decisions, or give a live demo.

</details>
