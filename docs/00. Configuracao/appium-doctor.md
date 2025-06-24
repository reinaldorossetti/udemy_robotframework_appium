📱 Manual de Instalação do Appium com Appium Doctor
Bash
Copy
node -v
npm -v


Você deverá ver as versões instaladas de cada um.

☕ 2.2. Java Development Kit (JDK)

Necessário para automação de testes Android.

📥 Download: Oracle JDK ou OpenJDK (JDK 8 ou superior; JDK 11 ou 17 são boas escolhas).
OpenJDK (Adoptium): https://adoptium.net/
Oracle JDK: https://www.oracle.com/java/technologies/downloads/

⚙️ Configuração da variável de ambiente JAVA_HOME:
🪟 Windows:

Pesquise por "variáveis de ambiente" e selecione "Editar as variáveis de ambiente do sistema".

Clique em "Variáveis de Ambiente…".

Em "Variáveis do sistema", clique em "Novo…".
Nome da variável: JAVA_HOME
Valor da variável: Caminho para o diretório de instalação do JDK

Exemplo: C:\Program Files\Java\jdk-11.0.x

Adicione %JAVA_HOME%\bin à variável Path do sistema.
🍎 macOS/Linux:

Adicione as seguintes linhas ao seu arquivo de perfil do shell:

Bash
Copy
export JAVA_HOME=/caminho/para/seu/jdk
export PATH=$JAVA_HOME/bin:$PATH


Recarregue o perfil: source ~/.bash_profile

✅ Verificação: Abra um novo terminal e execute:
Bash
Copy
java -version
javac -version
echo $JAVA_HOME # (macOS/Linux)
echo %JAVA_HOME% # (Windows)

🤖 2.3. Android SDK (para testes Android)

Necessário para interagir com dispositivos e emuladores Android.

📥 Download do Android Studio: https://developer.android.com/studio
⚙️ Instalação do SDK:
📦 Instale o Android Studio
🚀 Abra o Android Studio e siga o assistente de configuração
🔧 Pelo SDK Manager, certifique-se de ter:
 - ✅ Android SDK Platform-Tools

 - ✅ Android SDK Build-Tools

 - ✅ Pelo menos uma versão da plataforma Android SDK

🌐 Configuração das variáveis de ambiente ANDROID_HOME e PATH:
🪟 Windows:

Crie uma variável de sistema ANDROID_HOME:

Exemplo: C:\Users\SeuUsuario\AppData\Local\Android\Sdk

Adicione ao Path:
%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\tools
%ANDROID_HOME%\tools\bin
%ANDROID_HOME%\emulator

🍎 macOS/Linux:
Bash
Copy
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/emulator

✅ Verificação:
Bash
Copy
adb version
echo $ANDROID_HOME # (macOS/Linux)
echo %ANDROID_HOME% # (Windows)

🍎 2.4. Configuração para iOS (apenas macOS)

Para automação de testes iOS, você precisará de um macOS.

📱 Xcode: Instale a versão mais recente pela Mac App Store
🛠️ Xcode Command Line Tools:
Bash
Copy
  xcode-select --install

🍺 Homebrew: Instale de https://brew.sh/
📦 Dependências adicionais:
Bash
Copy
  npm install -g ios-deploy
  brew install libimobiledevice ideviceinstaller
  brew install carthage
  brew install ios-webkit-debug-proxy

📜 Aceitar licenças do Xcode:
Bash
Copy
  sudo xcodebuild -license accept

🚀 3. Instalação do Appium Server

Com os pré-requisitos configurados, instale o Appium Server globalmente:

Bash
Copy
npm install -g appium


⏰ Nota: Este comando pode levar alguns minutos para ser concluído.

✅ Verificação:
Bash
Copy
  appium -v

🔍 Appium Inspector (Opcional)

Para uma interface gráfica, baixe o Appium Inspector:

📥 Appium Inspector Releases
🩺 4. Instalação do Appium Doctor

O appium-doctor é uma ferramenta para verificar sua configuração do Appium:

Bash
Copy
npm install -g appium-doctor


✅ Verificação:
Bash
Copy
  appium-doctor --version

🔎 5. Verificando a Instalação com Appium Doctor
🌍 5.1. Verificação Geral
Bash
Copy
appium-doctor

🤖 5.2. Verificação Específica para Android
Bash
Copy
appium-doctor --android

🍎 5.3. Verificação Específica para iOS
Bash
Copy
appium-doctor --ios

📊 5.4. Interpretando a Saída

O appium-doctor exibirá uma lista de verificações:

✅ ✓ (Check verde): Dependência configurada corretamente
❌ ✖ (X vermelho): Problema encontrado
⚠️ ! (Aviso amarelo): Dependência opcional ausente
📝 Exemplo de saída:

info AppiumDoctor ### Diagnostic starting ###

info AppiumDoctor ✔ The Node.js binary was found at: /usr/local/bin/node

info AppiumDoctor ✔ Node version is 18.16.0

…

info AppiumDoctor ✖ ANDROID_HOME is NOT set! [Fix Manual]

info AppiumDoctor ✖ JAVA_HOME is NOT set! [Fix Manual]

…

info AppiumDoctor ### Diagnostic completed, 2 fixes needed. ###

🔧 Ação: Configure as variáveis de ambiente conforme descrito na seção de pré-requisitos.

🔌 6. Instalação de Drivers (Appium 2.x)

Com o Appium 2.x, os drivers não vêm instalados por padrão:

📋 Listar drivers disponíveis:
Bash
Copy
  appium driver list

📱 Instalar driver UiAutomator2 (Android):
Bash
Copy
  appium driver install uiautomator2

🍎 Instalar driver XCUITest (iOS):
Bash
Copy
  appium driver install xcuitest

✅ Verificar drivers instalados:
Bash
Copy
  appium driver list --installed

🛠️ 7. Solução de Problemas Comuns
🔐 Permissões
Em macOS/Linux, configure o npm para não exigir sudo
Consulte: Resolving EACCES permissions errors
🌐 Variáveis de Ambiente
Importante: Feche e reabra o terminal após definir variáveis
No Windows, pode ser necessário reiniciar o sistema
🔥 Firewall/Antivírus
Permita conexões do Node.js e Appium
Adicione exceções se necessário
📋 Versões Incompatíveis
Verifique a documentação oficial para compatibilidades
Mantenha versões atualizadas dos componentes
🎯 8. Próximos Passos

Com tudo instalado e verificado pelo appium-doctor, você está pronto para:

1. 🚀 Iniciar o Servidor Appium
Bash
Copy
appium


2. 🔍 Usar o Appium Inspector
Baixe e execute o Appium Inspector
Inspecione elementos da UI do seu aplicativo
3. 📝 Escrever Scripts de Teste

Linguagens suportadas:

📚 Recursos Adicionais
📖 Documentação Oficial do Appium
💬 Comunidade Appium
🐛 Issues no GitHub
🤝 Contribuindo

Se você encontrou algum problema ou tem sugestões de melhorias:

🍴 Fork este repositório
🌟 Crie uma branch para sua feature
📝 Commit suas mudanças

🚀 Push para a branch

🔄 Abra um Pull Request

⭐ Se este guia foi útil, dê uma estrela! ⭐