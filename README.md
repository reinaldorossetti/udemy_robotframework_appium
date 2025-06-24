# udemy_robotframework_appium 🚀🤖

## 1. Pré-requisitos 🛠️
Antes de começar, certifique-se de ter os seguintes itens instalados e configurados em seu sistema:

- **Python 3.11.9**: O Robot Framework e a AppiumLibrary requerem Python.  
  * Verifique a instalação: `python --version` ou `python3 --version`  
  * [⬇️ Download Python Windows](https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe)  
  * [⬇️ Pagina com Todas as Plataformas](https://www.python.org/downloads/release/python-3119/)

> 💡 *O Python 3.11 é até 60% mais rápido que o 3.10. Veja [Faster CPython](https://devblogs.microsoft.com/python/python-311-faster-cpython/) para detalhes.*

- **Java Development Kit (JDK)**: Necessário para o Appium e ferramentas Android.  
  * Verifique a instalação: `java -version`  
  * [⬇️ Download JDK](https://www.oracle.com/java/technologies/downloads/)

- **Android Studio** (para Android): Inclui o Android SDK, ferramentas de linha de comando e emuladores.  
  * Configure as variáveis de ambiente `ANDROID_HOME` e adicione os diretórios `platform-tools` e `tools` ao seu `PATH`.  
  * [⬇️ Download Android Studio](https://developer.android.com/studio)
  * [⬇️ Download Android Studio 2025.1.1.13](https://redirector.gvt1.com/edgedl/android/studio/install/2025.1.1.13/android-studio-2025.1.1.13-windows.exe)

- **Xcode** (para iOS, macOS apenas): Necessário para desenvolver e testar aplicações iOS, inclui simuladores.  
  * Instale as ferramentas de linha de comando: `xcode-select --install`

- **Node.js 20.18.2 e npm (ou yarn)**: Necessário para instalar e rodar o Appium Server.  
  * Verifique a instalação: `node --version` e `npm --version`  
  * [⬇️ Download Node.js](https://nodejs.org/en/blog/release/v20.18.2)

- **Appium Inspector**  
  * [⬇️ Appium Inspector](https://github.com/appium/appium-inspector/releases/tag/v2025.3.1)

- **Git**  
  * [⬇️ Download Git](https://git-scm.com/downloads)

- **VS-CODE**  
  * [⬇️ Download Vs-Code](https://code.visualstudio.com/download)

Appium 2 - HOW TO
```bash
npm install -g appium 
appium driver install uiautomator2
appium driver update uiautomator2
appium -p 4723 -a 127.0.0.1 -pa wd/hub --allow-cors
```

Em caso de dar erro com certificado
```bash
npm config set strict-ssl false
```

- **VS Code**  
  * [🐍 Plugin do Python para VS Code](https://marketplace.visualstudio.com/items?itemName=ms-python.python)  
  * [🤖 Plugin Robot Library para VS Code](https://marketplace.visualstudio.com/items?itemName=robocorp.robotframework-lsp)

---



## Compatibility Matrix 📊

| Appium Python Client | Selenium binding | Python version |
|---------------------|------------------|---------------|
| `5.1.1`+            | <5.0.0           | 3.9+          |
| `4.5.0` - `5.1.0`   | 4.26.0 - 4.31.0  | 3.9+          |
| `4.3.0` -  `4.4.0`  | 4.26.0 - 4.31.0  | 3.8+          |
| `3.0.0` - `4.2.1`   | 4.12.0 - 4.25.0  | 3.8+          |
| `2.10.0` - `2.11.1` | 4.1.0 - 4.11.2   | 3.7+          |
| `2.2.0` - `2.9.0`   | 4.1.0 - 4.9.0    | 3.7+          |
| `2.0.0` - `2.1.4`   | 4.0.0            | 3.7+          |
| `1.0.0` - `1.3.0`   | 3.x              | 3.7+          |
| `0.52` and below    | 3.x              | 2.7, 3.4-3.7  |

> ⚠️ O Appium Python Client depende do [Selenium Python binding](https://pypi.org/project/selenium/), portanto, atualizações no Selenium podem afetar o funcionamento do Appium Client.

---

## Instalação dos Pacotes 📦

Veja mais em:  
https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/

**Versão do Robot Framework adotado no curso (Atual no momento do curso):**  
Robot Framework 7.3.1  
```bash
pip install robotframework==7.3.1
```
**Robot Appium Library**  
```bash
pip install robotframework-appiumlibrary==2.1.0
pip install Appium-Python-Client<4.0.0
```

---

## Download do APK do nosso primeiro exemplo 📱

[⬇️ ApiDemos-debug.apk](https://github.com/serhatbolsu/robotframework-appium-sample/blob/master/demoapp/ApiDemos-debug.apk)

---

## Documentação das Libraries 📚

- **Robot Framework:**  
  [User Guide](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html)  
  [GitHub](https://github.com/robotframework/robotframework)

- **Robot Appium:**  
  [AppiumLibrary Docs](https://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html)  
  [GitHub](https://github.com/serhatbolsu/robotframework-appiumlibrary)

- **Appium Client:**  
  [PyPI](https://pypi.org/project/Appium-Python-Client/)  
  [GitHub](https://github.com/appium/python-client)

- **Appium:**  
  [Quickstart Install](https://appium.io/docs/en/2.2/quickstart/install/)  
  [UIAutomator2 Driver](https://appium.io/docs/en/2.2/quickstart/uiauto2-driver/)
  [Appium Architecture](https://www.lambdatest.com/blog/appium-architecture/)

- **Boas Práticas:**
  [Style Guide](https://docs.robotframework.org/docs/style_guide)
---