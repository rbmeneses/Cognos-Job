# ⚡ Cognos Job AI Pro

> **Seu Co-piloto de Carreira impulsionado por Inteligência Artificial.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.30%2B-red)](https://streamlit.io/)
[![Gemini AI](https://img.shields.io/badge/AI-Google%20Gemini-purple)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

O **Cognos Job AI Pro** é uma ferramenta open-source desenvolvida para democratizar o acesso a estratégias de recolocação profissional de alto nível. Utilizando o poder do **Google Gemini** e técnicas avançadas de Web Scraping, o sistema atua como um recrutador pessoal, analisando a compatibilidade do seu currículo com vagas reais e preparando você para entrevistas.

---

## 📸 Screenshots

| Busca Inteligente | Análise de Match |
|:---:|:---:|
| <img src="https://github.com/rbmeneses/Cognos-Job/blob/main/Screenshot_9.png" alt="Busca de Vagas" width="400"> | <img src="https://github.com/rbmeneses/Cognos-Job/blob/main/Screenshot_15.png" alt="Análise de Match" width="400"> |
| *Busca integrada com filtros reais* | *Análise detalhada de gaps e forças* |

| Preparação | Documentação |
|:---:|:---:|
| <img src="https://github.com/rbmeneses/Cognos-Job/blob/main/Screenshot_12.png" alt="Guia de Entrevista" width="400"> | <img src="https://github.com/rbmeneses/Cognos-Job/blob/main/Screenshot_14.png" alt="Feedback da IA" width="400"> |
| *Guia de entrevista personalizado* | *Currículo e Carta otimizados* |

---

## 🚀 Funcionalidades Principais

* **🔍 Busca de Vagas Integrada:** Utiliza a API do Google Custom Search para encontrar vagas em sites confiáveis (Gupy, LinkedIn, Glassdoor, Greenhouse, Lever), filtrando agregadores de spam.
* **🕸️ Web Scraping Resiliente:**
    * Extração inteligente de descrições de vagas, mesmo em sites dinâmicos (renderizados via JavaScript).
    * Limpeza automática de "ruídos" (banners de cookies, menus, rodapés).
    * Fallback automático para leitores de IA (Jina) caso o acesso direto seja bloqueado.
* **🧠 Análise de Match com IA:**
    * Compara seu currículo com a descrição da vaga.
    * Gera uma pontuação de compatibilidade (0-100%).
    * Identifica pontos fortes e gaps de competência.
* **📝 Gerador de Documentos:**
    * **Currículo Otimizado:** Reescreve seu perfil focando em palavras-chave para passar em sistemas ATS.
    * **Carta de Apresentação:** Cria cartas personalizadas conectando suas experiências aos requisitos da vaga.
    * Exportação para **DOCX** e **Markdown**.
* **🎤 Treinador de Entrevistas:** Gera um guia de preparação com perguntas técnicas e comportamentais específicas para a vaga selecionada, sugerindo respostas no modelo STAR.

---

## 🛠️ Tecnologias Utilizadas

* **Python 3.10+**
* **Streamlit:** Interface web interativa.
* **Google Gemini (via `google-generativeai`):** Cérebro da análise e geração de texto.
* **BeautifulSoup4 & Requests:** Raspagem de dados web.
* **Google Custom Search JSON API:** Motor de busca de vagas.
* **Python-Docx:** Geração de arquivos para download.

---

## ⚙️ Instalação e Configuração

### 1. Clone o repositório
```bash
git clone [https://github.com/SEU_USUARIO/cognos-job-ai.git](https://github.com/SEU_USUARIO/cognos-job-ai.git)
cd cognos-job-ai
2. Crie um ambiente virtual (Recomendado)
Bash

python -m venv venv
# No Windows:
venv\Scripts\activate
# No Linux/Mac:
source venv/bin/activate
3. Instale as dependências
Bash

pip install -r requirements.txt
(Certifique-se de que o arquivo requirements.txt contém: streamlit, google-generativeai, requests, beautifulsoup4, google-api-python-client, python-docx)

4. Obtenha as Chaves de API
Para o sistema funcionar, você precisará de 3 chaves gratuitas:

Gemini API Key: Obtenha no Google AI Studio.

Google Custom Search API Key: Obtenha no Google Cloud Console.

Search Engine ID (CX): Crie um motor de busca em Programmable Search Engine.

Dica: Ao configurar o motor de busca, ative a opção "Pesquisar em toda a web" ou adicione os sites específicos (Gupy, LinkedIn, etc.).

5. Execute a aplicação
Bash

streamlit run CognosJob.py
📖 Como Usar
Ao abrir a aplicação, vá até a Barra Lateral e insira suas chaves de API. Clique em "Salvar" (as chaves ficam salvas localmente em user_keys.json).

Cole o texto do seu Currículo atual no campo dedicado na barra lateral.

Na aba "Busca & Carga de Vagas", digite o cargo (ex: "Python Developer") e localização.

Clique em "Analisar ⚡" em uma das vagas encontradas.

Vá para a aba "Análise de Match" para ver suas chances.

Use a aba "Preparação da Candidatura" para gerar seu novo CV e treinar para a entrevista.

🛡️ Aviso Legal
Esta ferramenta foi criada para fins educacionais e de auxílio pessoal.

Dados: As chaves de API e o currículo são processados localmente ou enviados diretamente para a API do Google. Nenhum dado é salvo em servidores externos pelos desenvolvedores deste projeto.

Web Scraping: O uso de scrapers pode violar os termos de serviço de alguns sites. Use com responsabilidade e moderação.

🤝 Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir Issues ou enviar Pull Requests.

Faça um Fork do projeto

Crie sua Feature Branch (git checkout -b feature/MinhaFeature)

Commit suas mudanças (git commit -m 'Adicionando nova feature')

Push para a Branch (git push origin feature/MinhaFeature)

Abra um Pull Request

Criado por Ricardo B Meneses

📝 Mini-Tutorial: Como obter as Chaves de Acesso
Para usar o Cognos Job AI online, você precisa de 3 chaves gratuitas do Google. O processo leva cerca de 5 minutos.

1️⃣ Chave Gemini (IA) - A mais fácil
Acesse: Google AI Studio

Faça login com sua conta Google.

Clique em "Create API key" (Criar chave de API).

Copie o código gerado. Esta é sua Gemini API Key.

2️⃣ Motor de Busca Personalizado (CX ID)
Acesse: Programmable Search Engine

Em "Nome do motor de pesquisa", digite qualquer coisa (ex: "Vagas").

Importante: Em "O que pesquisar?", selecione "Pesquisar em toda a Web".

Clique em "Criar".

Na tela seguinte, copie o código que aparece em "ID do motor de pesquisa" (geralmente começa com números e letras como 012345...). Este é seu Google CX ID.

3️⃣ Chave da API de Busca (Google Custom Search Key)
Acesse o Google Cloud Console.

Crie um novo projeto (ou selecione um existente).

Na barra de busca no topo, digite "Custom Search API", clique nela e depois em "Ativar".

No menu lateral, vá em "Credenciais" -> "Criar Credenciais" -> "Chave de API".

Copie a chave gerada. Esta é sua Google API Key.

💡 Dica: O Google oferece uma cota gratuita generosa para testes pessoais (100 buscas/dia na API de Search e uso gratuito do Gemini Free).
