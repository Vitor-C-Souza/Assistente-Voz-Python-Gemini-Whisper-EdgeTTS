# 🎙️ Assistente de Voz Inteligente com Gemini & Whisper

Este projeto é um assistente virtual capaz de ouvir comandos de voz, processar a intenção usando Inteligência Artificial de última geração e responder com voz neural de alta fidelidade. Originalmente desenhado para automação de tarefas, como a limpeza de e-mails antigos do Hotmail/Outlook.

## 🚀 Funcionalidades

* **Captura de Áudio:** Interface via JavaScript para gravação direta no navegador (Google Colab).
* **Transcrição (STT):** Utiliza o **OpenAI Whisper** para transformar fala em texto com alta precisão.
* **Cérebro (LLM):** Processamento de linguagem natural via **Google Gemini 1.5/2.0 Flash**.
* **Voz Neural (TTS):** Respostas humanizadas utilizando a tecnologia **Microsoft Edge-TTS** (evitando bloqueios de API comuns no gTTS).
* **Automação:** Lógica integrada para gerenciamento de e-mails via protocolo IMAP.

## 🛠️ Tecnologias Utilizadas

| Camada | Tecnologia |
| --- | --- |
| **Linguagem** | Python 3.12+ |
| **Transcrição** | OpenAI Whisper (Local) |
| **IA Generativa** | Google Gemini SDK (`google-genai`) |
| **Síntese de Voz** | Microsoft Edge-TTS |
| **Interface** | Google Colab / IPython |

## 🔧 Como Configurar

### 1. Requisitos Próximos

* Uma chave de API do [Google AI Studio](https://aistudio.google.com/).
* Uma "Senha de Aplicativo" da Microsoft (se for usar a função de e-mail).

### 2. Instalação

No seu ambiente (Colab ou Local), instale as dependências:

```bash
pip install whisper google-genai edge-tts nest-asyncio

```

### 3. Configuração de Variáveis

Certifique-se de configurar suas chaves de acesso:

```python
os.environ["GEMINI_API_KEY"] = "sua_chave_aqui"

```

## 🧠 Evolução do Projeto (Destaque Técnico)

Durante o desenvolvimento, o projeto evoluiu para superar limitações comuns de infraestrutura:

1. **Migração de API:** Substituição da OpenAI pela Google Gemini para melhor aproveitamento de cotas gratuitas.
2. **Voz de Alta Qualidade:** Migração do `gTTS` (sujeito a Erro 429) para o `Edge-TTS` (qualidade neural superior e maior estabilidade).
3. **Tratamento de Dados:** Implementação de limpeza de Markdown via Regex para garantir uma fala natural e fluida.

## ✒️ Autor

* **Vítor Cavalcante Souza** - [Github](https://github.com/Vitor-C-Souza)
