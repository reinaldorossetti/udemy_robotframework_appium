# 📱 Manual Profissional de Instalação do Appium com Appium Doctor

Este guia irá ajudá-lo a instalar e configurar o Appium para automação de testes em dispositivos Android e iOS, garantindo que todas as dependências estejam corretamente ajustadas utilizando o **Appium Doctor**.

---

## 1️⃣ Verificando Node.js e npm

Abra o terminal e execute:
```bash
node -v
npm -v
```
Você deverá ver as versões instaladas de cada um.

---

## 2️⃣ Java Development Kit (JDK) ☕

Necessário para automação de testes Android.

- **Download:**  
  - [OpenJDK (Adoptium)](https://adoptium.net/)  
  - [Oracle JDK](https://www.oracle.com/java/technologies/downloads/)  
  - *JDK 8 ou superior; JDK 11 ou 17 são boas escolhas.*

### ⚙️ Configuração da variável de ambiente JAVA_HOME

#### 🪟 **Windows**
1. Pesquise por "variáveis de ambiente" e selecione "Editar as variáveis de ambiente do sistema".
2. Clique em "Variáveis de Ambiente…".
3. Em "Variáveis do sistema", clique em "Novo…".
   - Nome da variável: `JAVA_HOME`
   - Valor da variável: Caminho para o diretório de instalação do JDK  
     Exemplo: `C:\Program Files\Java\jdk-11.0.x`
4. Adicione `%JAVA_HOME%\bin` à variável `Path` do sistema.

#### 🍎 **macOS/Linux**
Adicione ao seu arquivo de perfil do shell:
```bash
export JAVA_HOME=/caminho/para/seu/jdk
export PATH=$JAVA_HOME/bin:$PATH
```
Recarregue o perfil:
```bash
source ~/.bash_profile
```

#### ✅ **Verificação**
```bash
java -version
javac -version
echo $JAVA_HOME # (macOS/Linux)
echo %JAVA_HOME% # (Windows)
```

---

## 3️⃣ Android SDK (para testes Android) 🤖

Necessário para interagir com dispositivos e emuladores Android.

- **Download:** [Android Studio](https://developer.android.com/studio)

### ⚙️ Instalação e configuração do SDK

1. Instale o Android Studio.
2. Abra o Android Studio e siga o assistente de configuração.
3. Pelo SDK Manager, certifique-se de instalar:
   - ✅ Android SDK Platform-Tools
   - ✅ Android SDK Build-Tools
   - ✅ Pelo menos uma versão da plataforma Android SDK

### 🌐 Configuração das variáveis de ambiente ANDROID_HOME e PATH

#### 🪟 **Windows**
- Crie uma variável de sistema `ANDROID_HOME`  
  Exemplo: `C:\Users\SeuUsuario\AppData\Local\Android\Sdk`
- Adicione ao `Path`:
  ```
  %ANDROID_HOME%\platform-tools
  %ANDROID_HOME%\tools
  %ANDROID_HOME%\tools\bin
  %ANDROID_HOME%\emulator
  ```

#### 🍎 **macOS/Linux**
Adicione ao seu arquivo de perfil do shell:
```bash
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/emulator
```

#### ✅ **Verificação**
```bash
adb version
echo $ANDROID_HOME # (macOS/Linux)
echo %ANDROID_HOME% # (Windows)
```

---

## 4️⃣ Configuração para iOS (apenas macOS) 🍎

Para automação de testes iOS, é necessário um Mac.

- **Xcode:** Instale pela Mac App Store
- **Xcode Command Line Tools:**
  ```bash
  xcode-select --install
  ```
- **Homebrew:** [Instale aqui](https://brew.sh/)
- **Dependências adicionais:**
  ```bash
  npm install -g ios-deploy
  brew install libimobiledevice ideviceinstaller
  brew install carthage
  brew install ios-webkit-debug-proxy
  ```
- **Aceitar licenças do Xcode:**
  ```bash
  sudo xcodebuild -license accept
  ```

---

## 5️⃣ Instalação do Appium Server 🚀

Com os pré-requisitos configurados, instale o Appium Server globalmente:
```bash
npm install -g appium
```
⏳ *Este comando pode levar alguns minutos.*

#### ✅ **Verificação**
```bash
appium -v
```

---

## 6️⃣ Appium Inspector (Opcional) 🔍

Para uma interface gráfica, baixe o [Appium Inspector](https://github.com/appium/appium-inspector/releases).

---

## 7️⃣ Instalação do Appium Doctor 🩺

O appium-doctor verifica se sua configuração está correta:
```bash
npm install -g appium-doctor
```
#### ✅ **Verificação**
```bash
appium-doctor --version
```

---

## 8️⃣ Verificando a Instalação com Appium Doctor 🔎

### 🌍 Verificação Geral
```bash
appium-doctor
```

### 🤖 Verificação Específica para Android
```bash
appium-doctor --android
```

### 🍎 Verificação Específica para iOS
```bash
appium-doctor --ios
```

### 📊 Interpretando a Saída

- ✅ **✓ (Verde):** Dependência configurada corretamente
- ❌ **✖ (Vermelho):** Problema encontrado
- ⚠️ **! (Amarelo):** Dependência opcional ausente

**Exemplo de saída:**
```
info AppiumDoctor ### Diagnostic starting ###
info AppiumDoctor ✔ The Node.js binary was found at: /usr/local/bin/node
info AppiumDoctor ✔ Node version is 18.16.0
...
info AppiumDoctor ✖ ANDROID_HOME is NOT set! [Fix Manual]
info AppiumDoctor ✖ JAVA_HOME is NOT set! [Fix Manual]
...
info AppiumDoctor ### Diagnostic completed, 2 fixes needed. ###
```
🔧 **Ação:** Configure as variáveis de ambiente conforme descrito acima.

---

## 9️⃣ Instalação de Drivers (Appium 2.x) 🔌

Com o Appium 2.x, os drivers são instalados separadamente.

- **Listar drivers disponíveis:**
  ```bash
  appium driver list
  ```
- **Instalar driver UiAutomator2 (Android):**
  ```bash
  appium driver install uiautomator2
  ```
- **Instalar driver XCUITest (iOS):**
  ```bash
  appium driver install xcuitest
  ```
- **Verificar drivers instalados:**
  ```bash
  appium driver list --installed
  ```

---

## 🔧 Solução de Problemas Comuns

- **🔐 Permissões:**  
  Em macOS/Linux, configure o npm para não exigir sudo.  
  Consulte: [Resolving EACCES permissions errors](https://docs.npmjs.com/resolving-eacces-permissions-errors)
- **🌐 Variáveis de Ambiente:**  
  Feche e reabra o terminal após definir variáveis.  
  No Windows, pode ser necessário reiniciar o sistema.
- **🔥 Firewall/Antivírus:**  
  Permita conexões do Node.js e Appium.
- **📋 Versões Incompatíveis:**  
  Verifique a documentação oficial para compatibilidades e mantenha os componentes atualizados.

---

## 🎯 Próximos Passos

Com tudo instalado e verificado pelo appium-doctor, você está pronto para:

1. **🚀 Iniciar o Servidor Appium**
   - **Windows:**
     ```bash
     appium -p 4723 -a 127.0.0.1 -pa wd/hub --allow-cors
     ```
   - **macOS:**
     ```bash
     appium -p 4723 -a 0.0.0.0 -pa wd/hub --allow-cors
     ```

2. **🔍 Usar o Appium Inspector**
   - Baixe e execute o Appium Inspector para inspecionar elementos da UI do seu aplicativo.

3. **📝 Escrever Scripts de Teste**
   - Utilize a linguagem de sua preferência para automação.

---

## 📚 Recursos Adicionais

- [Documentação Oficial do Appium](https://appium.io/docs/en/about-appium/intro/)
- [Comunidade Appium](https://discuss.appium.io/)
- [Issues no GitHub](https://github.com/appium/appium/issues)
- [Contribuindo para o Appium](https://github.com/appium/appium/blob/master/CONTRIBUTING.md)

---

## 🤝 Contribua com este Guia

Se você encontrou algum problema ou tem sugestões de melhorias:

1. 🍴 Faça um fork deste repositório
2. 🌟 Crie uma branch para sua feature
3. 📝 Commit suas mudanças
4. 🚀 Push para a branch
5. 🔄 Abra um Pull Request

⭐ Se este guia foi útil, deixe sua estrela! ⭐

---