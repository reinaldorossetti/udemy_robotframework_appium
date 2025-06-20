# udemy_robotframework_appium

Pré-requisitos
Antes de começar, certifique-se de ter os seguintes itens instalados e configurados em seu sistema:

Python 3.13.5: O Robot Framework e a AppiumLibrary requerem Python.
*   Verifique a instalação: `python --version` ou `python3 --version`
*   [Download Python](https://www.python.org/downloads/release/python-3135/)
Java Development Kit (JDK): Necessário para o Appium e ferramentas Android.
*   Verifique a instalação: `java -version`
*   [Download JDK](https://www.oracle.com/java/technologies/downloads/)
Android Studio (para Android): Inclui o Android SDK, ferramentas de linha de comando e emuladores.
*   Configure as variáveis de ambiente `ANDROID_HOME` e adicione os diretórios `platform-tools` e `tools` ao seu `PATH`.
*   [Download Android Studio](https://developer.android.com/studio)
Xcode (para iOS, macOS apenas): Necessário para desenvolver e testar aplicações iOS, inclui simuladores.

*   Instale as ferramentas de linha de comando: `xcode-select --install`
Node.js e npm (ou yarn): Necessário para instalar e rodar o Appium Server.
*   Verifique a instalação: `node --version` e `npm --version`
*   [Download Node.js](https://nodejs.org/)


Versão do Robot Framework adotado no curso (Atual no momento do curso):
Robot Framework 7.3.1
```
pip install robotframework==7.3.1
```
Robot Appium Library
```
pip install robotframework-appiumlibrary==2.1.0
pip install Appium-Python-Client
```

Library Documentation:

Robot Framework:
https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html
https://github.com/robotframework/robotframework

Robot Appium:
https://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html
https://github.com/serhatbolsu/robotframework-appiumlibrary

Appium Client:
https://pypi.org/project/Appium-Python-Client/