<div align="center">

# ⚡ Afilimax

### Infraestrutura de Inteligência e Automação para Afiliados

<p align="center">
  <b>Recomendações inteligentes, curadoria de ofertas e automação em escala para impulsionar suas vendas como afiliado.</b>
</p>

[![Website](https://img.shields.io/badge/Website-afilimax.net-8A2BE2?style=for-the-badge&logo=google-chrome&logoColor=white)](https://afilimax.net)
[![Ecosystem](https://img.shields.io/badge/Open%20Source-Ecossistema%20Modular-blue?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Afilimax)
[![Node.js](https://img.shields.io/badge/Node.js-%3E%3D18.0.0-green?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/Libraries%20License-MIT-yellow?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

</div>

## 🎯 Sobre a Afilimax

A **Afilimax** é uma plataforma concebida para transformar a rotina de quem trabalha com marketing de afiliados no Brasil. Nossa missão é conectar afiliados às melhores oportunidades de mercado, entregando recomendações em tempo real de produtos de alta conversão, variações de preços, detecção de promoções relâmpago e links monetizados prontos para distribuição nos seus canais (WhatsApp, Telegram, redes sociais e sites).

Enquanto a **Plataforma Afilimax** (aplicação web, inteligência de recomendação, painel de controle e integrações avançadas) opera como um serviço de **código fechado (SaaS)** em [afilimax.net](https://afilimax.net), acreditamos firmemente no compartilhamento de conhecimento e na força da comunidade desenvolvedora.

Por essa razão, **toda a infraestrutura de integração, extração de dados e provedores de afiliados foi disponibilizada como código aberto (Open Source)** sob a licença MIT.

---

## 🏛️ Arquitetura do Projeto

```
                              ┌──────────────────────────────────┐
                              │       Afilimax Platform          │
                              │    (SaaS / Código Fechado)       │
                              │    Dashboard • IA • Analytics    │
                              │       https://afilimax.net       │
                              └─────────────────┬────────────────┘
                                                │
                                       consome e estende
                                                │
                 ┌──────────────────────────────┴──────────────────────────────┐
                 │                                                             │
                 ▼                                                             ▼
┌─────────────────────────────────┐                           ┌─────────────────────────────────┐
│        Afilimax CLI 💻          │                           │      @afilimax/core 📐          │
│   Terminal & Automações Dev     │                           │   Tipagens, Enums & Contratos   │
│   npm i -g @afilimax/cli        │                           │      npm i @afilimax/core       │
└────────────────┬────────────────┘                           └────────────────┬────────────────┘
                 │                                                             │
                 └──────────────────────────────┬──────────────────────────────┘
                                                │
                 ┌──────────────────────────────┴──────────────────────────────┐
                 │                                                             │
                 ▼                                                             ▼
┌─────────────────────────────────┐                           ┌─────────────────────────────────┐
│       Scrapers Resilientes 🕷️    │                           │    Provedores de Afiliados 🔗    │
│  • amazon-scraper               │                           │  • amazon-browser-provider      │
│  • mercado-livre-scraper        │                           │  • mercado-livre-provider       │
│  • aliexpress-scraper           │                           │  • aliexpress-provider          │
│                                 │                           │  • shopee-provider              │
│                                 │                           │  • magazine-luiza-provider      │
└─────────────────────────────────┘                           └─────────────────────────────────┘
```

---

## 🌐 Plataforma Afilimax (Proprietária)

A plataforma oficial opera em nuvem e oferece aos criadores e afiliados uma suíte de alta produtividade:

- 📊 **Radar de Ofertas**: Monitoramento contínuo de oscilações de preço e descontos reais nos principais marketplaces do Brasil.
- 🤖 **Curadoria & Recomendações**: Algoritmos de recomendação baseados no nicho, sazonalidade e interesse da sua audiência.
- ⚡ **Geração e Encurtamento de Links**: Conversão instantânea de links com tags personalizadas e sub-IDs para rastreamento de métricas.
- 📲 **Automação de Canais**: Disparo automático de promoções com textos persuasivos e imagens geradas dinamicamente para Telegram e WhatsApp.

> Acesse e conheça: **[afilimax.net](https://afilimax.net)**

---

## 🔓 Ecossistema Open Source

Todas as bibliotecas modulares que compõem o alicerce técnico da Afilimax são públicas, mantidas no GitHub e publicadas no registro oficial do NPM:

### 📐 Núcleo e Tipagens
| Pacote | NPM | Descrição |
| :--- | :--- | :--- |
| **[`@afilimax/core`](https://github.com/Afilimax/core)** | [![npm](https://img.shields.io/npm/v/@afilimax/core?color=blue)](https://www.npmjs.com/package/@afilimax/core) | Interfaces, contratos e tipagens TypeScript unificadas para produtos, scrapers e provedores de afiliação. |

### 💻 Ferramenta de Linha de Comando (CLI)
| Pacote | NPM | Descrição |
| :--- | :--- | :--- |
| **[`@afilimax/cli`](https://github.com/Afilimax/afilimax-cli)** | [![npm](https://img.shields.io/npm/v/@afilimax/cli?color=blue)](https://www.npmjs.com/package/@afilimax/cli) | CLI completa para geração rápida de links de afiliados, scraping de produtos e busca interativa com paginação direto no terminal. |

### 🕷️ Scrapers de Produtos
Scrapers focados no mercado brasileiro, preparados para contornar proteções anti-bot e extrair metadados ricos (preços, descontos, avaliações, frete grátis e fotos):

| Pacote | NPM | Marketplace | Estratégia |
| :--- | :--- | :--- | :--- |
| **[`@afilimax/amazon-scraper`](https://github.com/Afilimax/amazon-scraper)** | [![npm](https://img.shields.io/npm/v/@afilimax/amazon-scraper?color=blue)](https://www.npmjs.com/package/@afilimax/amazon-scraper) | Amazon Brasil | Extração rápida via seletores e evasão de CAPTCHAs |
| **[`@afilimax/mercado-livre-scraper`](https://github.com/Afilimax/mercado-livre-scraper)** | [![npm](https://img.shields.io/npm/v/@afilimax/mercado-livre-scraper?color=blue)](https://www.npmjs.com/package/@afilimax/mercado-livre-scraper) | Mercado Livre | Schema.org JSON-LD estruturado + Puppeteer Stealth (Headless) |
| **[`@afilimax/aliexpress-scraper`](https://github.com/Afilimax/aliexpress-scraper)** | [![npm](https://img.shields.io/npm/v/@afilimax/aliexpress-scraper?color=blue)](https://www.npmjs.com/package/@afilimax/aliexpress-scraper) | AliExpress Brasil | Cliente HTTP acelerado (`impit`) com fallback para Puppeteer |

### 🔗 Provedores de Afiliação
Módulos dedicados à conversão de URLs em links monetizados com as tags de parceiro:

| Pacote | NPM | Plataforma Suportada | Método |
| :--- | :--- | :--- | :--- |
| **[`@afilimax/amazon-browser-provider`](https://github.com/Afilimax/amazon-browser-provider)** | [![npm](https://img.shields.io/npm/v/@afilimax/amazon-browser-provider?color=blue)](https://www.npmjs.com/package/@afilimax/amazon-browser-provider) | Amazon Associados | Navegador automatizado / cookies de sessão |
| **[`@afilimax/mercado-livre-provider`](https://github.com/Afilimax/mercado-livre-provider)** | [![npm](https://img.shields.io/npm/v/@afilimax/mercado-livre-provider?color=blue)](https://www.npmjs.com/package/@afilimax/mercado-livre-provider) | Mercado Livre Afiliados | API oficial de links com sessão ativa |
| **[`@afilimax/aliexpress-provider`](https://github.com/Afilimax/aliexpress-provider)** | [![npm](https://img.shields.io/npm/v/@afilimax/aliexpress-provider?color=blue)](https://www.npmjs.com/package/@afilimax/aliexpress-provider) | AliExpress Open Platform | API oficial REST (App Key / Secret) |
| **[`@afilimax/shopee-provider`](https://github.com/Afilimax/shopee-provider)** | [![npm](https://img.shields.io/npm/v/@afilimax/shopee-provider?color=blue)](https://www.npmjs.com/package/@afilimax/shopee-provider) | Shopee Afiliados | GraphQL / API oficial de parceiros com HMAC |
| **[`@afilimax/magazine-luiza-provider`](https://github.com/Afilimax/magazine-luiza-provider)** | [![npm](https://img.shields.io/npm/v/@afilimax/magazine-luiza-provider?color=blue)](https://www.npmjs.com/package/@afilimax/magazine-luiza-provider) | Parceiro Magalu | Automação e cookies de autenticação |

### 📝 Parsers & Utilitários
| Pacote | NPM | Descrição |
| :--- | :--- | :--- |
| **[`@afilimax/message-text-parser`](https://github.com/Afilimax/message-text-parser)** | [![npm](https://img.shields.io/npm/v/@afilimax/message-text-parser?color=blue)](https://www.npmjs.com/package/@afilimax/message-text-parser) | Extrator de links, preços, cupons e descrições a partir de mensagens de canais de ofertas do Telegram. |

---

## 🚀 Começando com as Ferramentas Abertas

### 1. Utilizando a CLI

A maneira mais rápida de interagir com o ecossistema no dia a dia:

```bash
# Instalação global
npm install -g @afilimax/cli

# Geração automática de link de afiliado
afilimax create "https://www.amazon.com.br/dp/B09B8VGCR8"

# Scraping de produto com extração de metadados completos
afilimax scrape product "https://www.mercadolivre.com.br/p/MLB22649400"

# Pesquisa interativa com navegação e geração de link no terminal
afilimax scrape search amazon "echo dot"
```

### 2. Integrando um Scraper no seu Código

```typescript
import { MercadoLivreScraper } from "@afilimax/mercado-livre-scraper"

const scraper = new MercadoLivreScraper({ headless: true })

// Pesquisar produtos
const produtos = await scraper.searchProducts({
    query: "notebook gamer",
    limit: 10
})

console.log(produtos)

await scraper.close()
```

---

## 💡 Filosofia

> *"Acreditamos que ferramentas sólidas de integração e raspagem de dados devem ser bens públicos e acessíveis. Assim, criadores e desenvolvedores podem focar em inovação e conteúdo, enquanto nossa plataforma comercial provê a inteligência de negócios e a escala."*

- **Open Core**: Camada de rede, integração com lojas e scrapers são abertos e mantidos transparentemente.
- **Resiliência em Produção**: Todas as bibliotecas são testadas contra as mudanças constantes dos marketplaces brasileiros.
- **Foco no Mercado Brasileiro**: Suporte nativo ao Real (BRL), impostos locais, modelos de frete (Full, Prime) e parcelamento sem juros.

---

## 🤝 Como Contribuir

Contribuições são muito bem-vindas em qualquer um dos nossos repositórios públicos:

1. Faça um Fork do repositório correspondente.
2. Crie uma branch para sua funcionalidade ou correção (`git checkout -b feature/nova-funcionalidade`).
3. Commit suas alterações seguindo o padrão de commits convencionais (`git commit -m 'feat: adiciona suporte a novos seletores'`).
4. Envie para o GitHub (`git push origin feature/nova-funcionalidade`).
5. Abra um **Pull Request**.

---

## 📬 Contato & Suporte

- **Website Oficial**: [https://afilimax.net](https://afilimax.net)
- **Organização GitHub**: [https://github.com/Afilimax](https://github.com/Afilimax)
- **Reportar Problemas**: Abra uma issue no repositório correspondente da biblioteca.

---

<div align="center">
  <sub>Criado e mantido com dedicação por <b>Marcuth</b> e contribuidores da comunidade.</sub>
</div>
