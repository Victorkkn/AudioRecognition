# AudioRecognition

# 🏦 Sistema QuantumFinance - Atendimento por Voz

**MBA FIAP - Workshop Audição Cognitiva**  

---

## 📋 Sobre o Projeto

Sistema completo de atendimento bancário automatizado que utiliza:
- **TTS (Text-to-Speech)**: Síntese de voz em português
- **STT (Speech-to-Text)**: Reconhecimento de comandos por voz
- **Loop interativo**: Menu com 4 opções funcionais
- **Tratamento de erros**: Mensagens específicas para falhas

---

## ⚡ Instalação Rápida

### Pré-requisitos
- **Python 3.10** (IMPORTANTE: Não use Python 3.13!)
- **Windows 10/11** com microfone
- **Conexão com internet** (para Google Speech API)

### Passo 1: Instalar Python 3.10
```
Download: https://www.python.org/downloads/release/python-31011/
Baixar: "Windows installer (64-bit)"
Durante instalação: ✅ Marcar "Add Python to PATH"
```

### Passo 2: Instalar Dependências

```bash
# Tente instalar tudo de uma vez:
py -3.10 -m pip install pyttsx3 SpeechRecognition PyAudio

# Se der erro, instale uma por vez:
py -3.10 -m pip install pyttsx3
py -3.10 -m pip install SpeechRecognition  
py -3.10 -m pip install PyAudio

# Se PyAudio falhar, tente:
py -3.10 -m pip install pipwin
py -3.10 -m pipwin install pyaudio
```

### Passo 3: Navegar até a Pasta
```bash
cd "~\projeto_quantumfinance"
```

### Passo 4: Executar o Sistema
```bash
py -3.10 sistema_quantum_completo.py
```

### 🔍 Verificar Instalação
```bash
# Testar se Python 3.10 está instalado:
py -3.10 --version
# Deve mostrar: Python 3.10.11

# Testar se as bibliotecas estão instaladas:
py -3.10 -c "import pyttsx3; print('pyttsx3 OK')"
py -3.10 -c "import speech_recognition; print('SpeechRecognition OK')"
py -3.10 -c "import pyaudio; print('PyAudio OK')"
```

---

## 🎯 Como Usar

### Menu Inicial
Ao executar, escolha:
- **1** → Iniciar atendimento por voz
- **2** → Criar todos os áudios MP3
- **3** → Sair

### Modo Atendimento por Voz

O sistema apresentará 4 opções:

| Opção | Função | Palavras-chave aceitas |
|-------|--------|------------------------|
| **1** | Consultar Saldo | "saldo", "consultar", "conta", "um" |
| **2** | Compra Internacional | "compra", "internacional", "dólar", "dois" |
| **3** | Falar com Atendente | "atendente", "ajuda", "falar", "três" |
| **4** | Sair | "sair", "tchau", "encerrar", "quatro" |

### Exemplo de Interação

```
[SISTEMA]: Bem-vindo ao QuantumFinance! Sou seu assistente virtual.
[SISTEMA]: Por favor, escolha uma opção...
[OUVINDO]: (você fala) "quero consultar meu saldo"
[SISTEMA]: Você escolheu: Consultar saldo da conta.
[SISTEMA]: Seu saldo atual é de 5000.00 reais.
```

---

## 📂 Estrutura do Projeto

```
projeto_quantumfinance/
│
├── sistema_quantum_completo.py    # Código principal do sistema
├── DESCRICAO_SOLUCAO.txt         # Descrição técnica da solução
├── README.md                      # Este arquivo
│
└── audio/                         # Pasta com áudios gerados
    ├── 01_boas_vindas.mp3        # Mensagem de boas-vindas
    ├── 02_menu_opcoes.mp3        # Menu com as 4 opções
    ├── 03_confirma_saldo.mp3     # Confirmação opção 1
    ├── 04_saldo.mp3              # Valor do saldo
    ├── 05_confirma_compra.mp3    # Confirmação opção 2
    ├── 06_resultado_compra.mp3   # Resultado da simulação
    ├── 07_confirma_atendente.mp3 # Confirmação opção 3
    ├── 08_transferindo.mp3       # Transferindo para atendente
    ├── 09_atendente_ocupado.mp3  # Atendente não disponível
    ├── 10_confirma_sair.mp3      # Confirmação opção 4
    ├── 11_despedida.mp3          # Mensagem de despedida
    └── 12_opcao_invalida.mp3     # Erro - opção não identificada
```

---

## ✅ Requisitos Atendidos (10/10 pontos)

| Requisito | Pontos | Implementação |
|-----------|--------|---------------|
| **Gerar frases TTS** | 2.0 | ✅ 12 frases diferentes com identificação da empresa |
| **Armazenar em arquivos** | 2.0 | ✅ 12 arquivos MP3 salvos na pasta audio/ |
| **Capturar áudio STT** | 2.0 | ✅ Microfone captura e processa comandos |
| **Reconhecer palavras** | 2.0 | ✅ Identifica palavras-chave, não apenas números |
| **Opção não identificada** | 1.0 | ✅ Mensagem de erro e repetição do menu |
| **Encerrar com "Sair"** | 1.0 | ✅ Loop encerra corretamente |
| **TOTAL** | **10.0** | ✅ **100% Completo** |

---

## 🎥 Roteiro para Gravação do Vídeo

### 1. Walk-through do Código (30s)
- Mostrar imports e classe principal
- Destacar métodos `falar()` e `ouvir_comando()`
- Mostrar dicionário de palavras-chave

### 2. Execução com Identificação Positiva (30s)
- Executar o sistema
- Falar: "consultar saldo"
- Sistema deve confirmar e mostrar saldo

### 3. Execução sem Identificação (30s)
- Falar algo aleatório: "banana" ou "teste"
- Sistema deve dar erro e repetir menu

### 4. Saída do Loop (30s)
- Falar: "quero sair"
- Sistema deve confirmar e encerrar

---

## 🔧 Solução de Problemas

### Erro: "Python não reconhecido"
```bash
# Use py ao invés de python
py -3.10 sistema_quantum_completo.py
```

### Erro: "Módulo não encontrado"
```bash
# Reinstale as dependências
py -3.10 -m pip install --upgrade pip
py -3.10 -m pip install pyttsx3 SpeechRecognition PyAudio

# Se falhar, instale uma por vez:
py -3.10 -m pip install pyttsx3
py -3.10 -m pip install SpeechRecognition
py -3.10 -m pip install PyAudio
```

### Erro: "Microfone não detectado"
```bash
# Opção 1: Reinstalar PyAudio
py -3.10 -m pip uninstall pyaudio
py -3.10 -m pip install pyaudio

# Opção 2: Usar pipwin
py -3.10 -m pip install pipwin
py -3.10 -m pipwin install pyaudio

# Opção 3: Continue em modo manual (digite ao invés de falar)
```

### Erro: "Não consegui entender o áudio"
- Fale mais próximo do microfone
- Reduza ruído de fundo
- Fale palavras-chave claramente: "saldo", "compra", "atendente", "sair"
- Tente falar mais devagar

### Sistema sempre usa modo manual
- Normal se PyAudio não estiver instalado
- Digite as palavras-chave pelo teclado
- Funciona exatamente igual ao modo voz

---

## 👥 Informações do Projeto

**Disciplina**: Workshop Audição Cognitiva  
**Instituição**: FIAP - MBA em Inteligência Artificial  
**Professor**: Alexandre Gastaldi Fernandes  
**Ano**: 2024  

**Tecnologias**:
- Python 3.10.11
- pyttsx3 2.99
- SpeechRecognition 3.14.3
- PyAudio 0.2.14

---

## 📝 Entregáveis

1. ✅ **Código Python**: `sistema_quantum_completo.py`
2. ✅ **Descrição da Solução**: `DESCRICAO_SOLUCAO.txt`
3. ✅ **Documentação**: `README.md`
4. ⏳ **Vídeo Demonstrativo**: A ser gravado

---

**Última atualização**: Dezembro 2024  
**Status**: ✅ Pronto para entrega****
