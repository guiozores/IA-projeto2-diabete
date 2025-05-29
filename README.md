# 🩺 Projeto de Machine Learning - Predição de Diabetes

Este projeto implementa uma esteira completa de aprendizado de máquina para predição de diabetes usando o dataset Pima Indians Diabetes do UCI Machine Learning Repository.

## 📋 Requisitos do Sistema

- Python 3.8 ou superior
- Git (opcional, para clonar o repositório)
- Jupyter Notebook ou VS Code com extensão Python

## 🚀 Instalação e Configuração

### 📥 1. Obtendo o Projeto

#### Opção A: Download direto

- Baixe os arquivos do projeto diretamente
- Extraia em uma pasta de sua escolha

#### Opção B: Clone via Git (se disponível)

```bash
git clone <url-do-repositorio>
cd diabetes-simples
```

### 🔧 2. Configuração do Ambiente Virtual

O uso de ambiente virtual é **altamente recomendado** para evitar conflitos entre dependências.

#### 🐧 Linux

```bash
# Navegue até a pasta do projeto
cd diabetes-simples

# Crie o ambiente virtual
python3 -m venv .venv

# Ative o ambiente virtual
source .venv/bin/activate

# Atualize o pip
pip install --upgrade pip

# Instale as dependências
pip install -r requirements.txt
```

#### 🪟 Windows

**PowerShell:**

```powershell
# Navegue até a pasta do projeto
cd diabetes-simples

# Crie o ambiente virtual
python -m venv .venv

# Ative o ambiente virtual
.\.venv\Scripts\Activate.ps1

# Atualize o pip
python -m pip install --upgrade pip

# Instale as dependências
pip install -r requirements.txt
```

**Command Prompt (CMD):**

```cmd
# Navegue até a pasta do projeto
cd diabetes-simples

# Crie o ambiente virtual
python -m venv .venv

# Ative o ambiente virtual
.\.venv\Scripts\activate.bat

# Atualize o pip
python -m pip install --upgrade pip

# Instale as dependências
pip install -r requirements.txt
```

#### 🍎 macOS

```bash
# Navegue até a pasta do projeto
cd diabetes-simples

# Crie o ambiente virtual
python3 -m venv .venv

# Ative o ambiente virtual
source .venv/bin/activate

# Atualize o pip
pip install --upgrade pip

# Instale as dependências
pip install -r requirements.txt
```

### 📦 3. Dependências Instaladas

O arquivo `requirements.txt` inclui:

- **pandas** (≥2.2.0) - Manipulação de dados
- **numpy** (≥2.2.0) - Computação numérica
- **matplotlib** (≥3.10.0) - Visualizações básicas
- **seaborn** (≥0.13.0) - Visualizações estatísticas
- **scikit-learn** (≥1.6.0) - Machine Learning
- **joblib** (≥1.5.0) - Serialização de modelos

## 🎯 Executando o Projeto

### 📓 Opção 1: Jupyter Notebook

```bash
# Com o ambiente virtual ativado, inicie o Jupyter
jupyter notebook

# Ou use o JupyterLab (interface mais moderna)
jupyter lab
```

1. Abra o arquivo `Projeto_ML_Diabetes_Simples.ipynb`
2. Execute as células sequencialmente (Shift + Enter)

### 💻 Opção 2: VS Code

1. Abra o VS Code na pasta do projeto:

   ```bash
   code .
   ```

2. Instale a extensão Python do VS Code (se não tiver)

3. Abra o arquivo `Projeto_ML_Diabetes_Simples.ipynb`

4. Selecione o interpretador Python do ambiente virtual:

   - Pressione `Ctrl/Cmd + Shift + P`
   - Digite "Python: Select Interpreter"
   - Escolha o Python da pasta `.venv`

5. Execute as células clicando no botão "Run" ou usando `Shift + Enter`

## 🔍 Estrutura do Projeto

```
diabetes-simples/
├── 📓 Projeto_ML_Diabetes_Simples.ipynb  # Notebook principal
├── 📓 explicacao_IQR.ipynb               # Notebook explicativo (IQR)
├── 📋 requirements.txt                   # Dependências Python
├── 📖 README.md                          # Este arquivo
└── 🗂️ .venv/                            # Ambiente virtual (criado após setup)
```

## 📊 O que o Projeto Faz

### 🎯 Objetivo

Predizer se uma pessoa tem diabetes baseado em características médicas como:

- Número de gestações
- Concentração de glicose
- Pressão arterial
- Espessura da pele
- Nível de insulina
- Índice de massa corporal (BMI)
- Função de hereditariedade do diabetes
- Idade

### 🔄 Metodologia (9 Etapas)

1. **📥 Dataset UCI/Kaggle**: Pima Indians Diabetes Dataset
2. **📊 Estatísticas Descritivas**: Análise exploratória dos dados
3. **🔄 Transformação em Colunas**: Balanceamento de classes
4. **🧹 Transformação em Linhas**: Remoção de valores inconsistentes
5. **📂 Divisão em 3 Conjuntos**: Treino (60%), Validação (20%), Teste (20%)
6. **🤖 Treinamento**: Modelo Random Forest
7. **📈 Avaliação**: Matriz de confusão e métricas
8. **🔮 Predição**: Exemplo prático com novo paciente
9. **📝 Documentação**: Comentários educacionais detalhados

## 🎓 Resultados Esperados

- **Acurácia**: ~85%
- **Modelo**: Random Forest com 100 árvores
- **Saída**: Arquivo `modelo_diabetes_simples.pkl` (modelo treinado)
- **Visualizações**: Gráficos de distribuição e matriz de confusão

## 🛠️ Resolução de Problemas

### ❌ Erro: "Module not found"

```bash
# Certifique-se de que o ambiente virtual está ativado
# Linux/macOS:
source .venv/bin/activate

# Windows PowerShell:
.\.venv\Scripts\Activate.ps1

# Windows CMD:
.\.venv\Scripts\activate.bat

# Reinstale as dependências
pip install -r requirements.txt
```

### ❌ Erro: "Python not found"

- Certifique-se de que o Python está instalado
- No Windows, adicione Python ao PATH durante a instalação
- Use `python3` em vez de `python` no Linux/macOS

### ❌ Jupyter não abre

```bash
# Instale o Jupyter explicitamente
pip install jupyter

# Ou use o notebook do VS Code
```

### ❌ Gráficos não aparecem

```bash
# Instale matplotlib com backend apropriado
pip install matplotlib --upgrade

# No Jupyter, use:
%matplotlib inline
```

## 🔄 Desativando o Ambiente Virtual

Quando terminar de usar o projeto:

```bash
# Em qualquer sistema operacional
deactivate
```

## 📞 Suporte

Se encontrar problemas:

1. **Verifique a versão do Python**: `python --version` ou `python3 --version`
2. **Confirme que o ambiente virtual está ativo**: deve aparecer `(.venv)` no terminal
3. **Reinstale as dependências**: `pip install -r requirements.txt --force-reinstall`
4. **Verifique se todas as bibliotecas foram instaladas**: `pip list`

## 📄 Licença

Este projeto é para fins educacionais e de aprendizado em Machine Learning.

---

**🎯 Objetivo Educacional**: Este projeto demonstra uma implementação completa de Machine Learning, desde a análise exploratória até a predição final, seguindo as melhores práticas da área.
