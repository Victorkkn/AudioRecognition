# Sistema QuantumFinance - Atendimento por Voz

**MBA FIAP - Workshop Audio Recognition**  

---

## Sobre o Projeto

Sistema completo de atendimento bancário automatizado que utiliza:
- **TTS (Text-to-Speech)**: Síntese de voz em português
- **STT (Speech-to-Text)**: Reconhecimento de comandos por voz
- **Loop interativo**: Menu com 4 opções funcionais
- **Tratamento de erros**: Mensagens específicas para falhas

---

## Instalação Rápida

### Pré-requisitos
- **Python 3.10** (IMPORTANTE: Não use Python 3.13!)
- **Windows 10/11** com microfone
- **Conexão com internet** (para Google Speech API)

### Passo 1: Instalar Python 3.10
```
Download: https://www.python.org/downloads/release/python-31011/
Baixar: "Windows installer (64-bit)"
Durante instalação: Marcar "Add Python to PATH"
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

### Verificar Instalação
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

## Como Usar

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

## Estrutura do Projeto

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
