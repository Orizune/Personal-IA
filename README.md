# Personal-IA — Open WebUI + 9Router

Ambiente de IA pessoal com interface web, gateway unificado de modelos e recursos como pesquisa web, visão via Gemini, e túnel Cloudflare.

## O que funciona

- ✅ **Open WebUI** – interface de chat com suporte a RAG, pesquisa web, code interpreter e ferramentas.
- ✅ **9Router** – gateway que unifica provedores (DeepSeek, Gemini, OpenRouter, Groq, etc.) em uma única API compatível com OpenAI.
- ✅ **Pesquisa web** – integrada com Brave Search (free tier) e/ou SearXNG (local ou público).
- ✅ **Visão** – imagens e documentos processados via Gemini (free tier) através do 9Router.
- ✅ **Túnel Cloudflare** – exposição pública temporária (opcional, para testes).
- ✅ **Portabilidade** – todo o sistema configurado via Docker Compose com bind mounts; basta copiar a pasta e rodar `docker compose up -d`.

## Exemplo
  <img width="1600" height="855" alt="exemplo de uso 1" src="https://github.com/user-attachments/assets/4c3c5e64-b8f8-4c7e-a896-82c4cf1ea6a0" />
  <img width="1600" height="806" alt="2" src="https://github.com/user-attachments/assets/eff3da5c-5997-4fc2-936f-afb24b8bca60" />
  <img width="1600" height="854" alt="3" src="https://github.com/user-attachments/assets/e3085a36-61d5-437a-ac88-7744b9d215fd" />
  <img width="1600" height="847" alt="4" src="https://github.com/user-attachments/assets/0f4e46e1-00a7-417a-b720-278cccbb7eb9" />
  <img width="1600" height="847" alt="5" src="https://github.com/user-attachments/assets/97fc6902-63c7-407b-9540-153e97a6a80e" />
  <img width="1600" height="849" alt="6" src="https://github.com/user-attachments/assets/ca335ebc-83e0-4c85-9141-72f88a9b17e7" />
  <img width="1600" height="850" alt="7" src="https://github.com/user-attachments/assets/40e04fc7-f686-4afa-9003-ae7dde64b84a" />




## Stack

| Serviço | Tecnologia | Porta |
|---------|------------|-------|
| Interface | Open WebUI | 3000 |
| Gateway | 9Router | 20128 |
| Busca (opcional) | SearXNG | 8888 |
| Túnel | Cloudflare Tunnel | (dinâmico) |

## Pré‑requisitos

- Docker e Docker Compose (instalados)
- Git (para clonar)
- Chaves de API (criar contas nos serviços abaixo)

## Chaves necessárias (gratuitas / free tier)

- [DeepSeek API](https://platform.deepseek.com/) – paga, barata, para raciocínio.
- [Google Gemini](https://makersuite.google.com/app/apikey) – gratuita, para visão.
- [Brave Search](https://brave.com/search/api/) – gratuita, para pesquisa web.
- (opcional) Chaves para OpenRouter, Groq, etc., se desejar mais modelos.

## Instalação

```bash
git clone https://github.com/seu-usuario/Personal-IA.git
cd Personal-IA
cp .env.example .env   # preencha com suas chaves
docker compose up -d
