Configurando Ambiente Virtual Python com .env

Este guia detalha como configurar um ambiente virtual Python, instalar bibliotecas e gerenciar variáveis de ambiente usando um arquivo .env, tudo via terminal.

Pré-requisitos
* Python 3.x instalado no seu sistema.
* Acesso ao terminal ou linha de comando.

Passo a Passo:
Siga estes passos no seu terminal:

1. Navegue para o Diretório do seu Projeto

Abra o terminal e vá para a pasta onde seu projeto Python está ou onde você deseja criá-lo.
```
git clone https://github.com/reinaldorossetti/udemy_robotframework_appium.git
cd ./udemy_robotframework_appium
```

2. Crie um Ambiente Virtual

Use o módulo venv (que vem com o Python) para criar um ambiente virtual. O nome comum para o diretório do ambiente virtual é .venv ou venv.
```
python -m venv .venv
```

Isso criará uma pasta chamada .venv dentro do seu diretório de projeto, contendo uma cópia mínima do Python e do pip.

3. Ative o Ambiente Virtual

Antes de instalar qualquer biblioteca, você precisa ativar o ambiente virtual. O comando varia ligeiramente dependendo do seu sistema operacional e shell.

Windows (Command Prompt):
```
   ./.venv/Scripts/activate.bat
```
Windows (PowerShell):
```
   ./.venv/Scripts/Activate.ps1
```
macOS/Linux:
```
   source ./.venv/Scripts/activate
```

Após a ativação, o nome do seu ambiente virtual (geralmente (.venv)) aparecerá no início da linha de comando, indicando que você está trabalhando dentro dele.

4. Instale as Bibliotecas Necessárias

Com o ambiente virtual ativado, use pip para instalar as bibliotecas que seu projeto precisa.

3. Install requirements in Venv
```
pip install -r requirements.txt
# caso não esteja instalado de forma alguma no .venv, segunda opção seria remover e instalar novamente.
./.venv/Scripts/python.exe -m pip install -r requirements.txt
```