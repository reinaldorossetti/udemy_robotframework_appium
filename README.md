# udemy_robotframework_appium

Pré-requisitos
Antes de começar, certifique-se de ter os seguintes itens instalados e configurados em seu sistema:

Python 3.11.9: O Robot Framework e a AppiumLibrary requerem Python.
*   Verifique a instalação: `python --version` ou `python3 --version`
*   [Download Python Windows](https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe)
*   [Download Python](https://www.python.org/downloads/release/python-3119/)

The Faster CPython Project is already yielding some exciting results. Python 3.11 is up to 10-60% faster than Python 3.10. On average, we measured a 1.22x speedup on the standard benchmark suite. See Faster CPython for details.

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

## Compatibility Matrix

|Appium Python Client| Selenium binding| Python version |
|----|----|----|
|`5.1.1`+|`4.26.0`+ | 3.9+ |
|`4.5.0` - `5.1.0`|`4.26.0` - `4.31.0` | 3.9+ |
|`4.3.0` -  `4.4.0`|`4.26.0` - `4.31.0` | 3.8+ |
|`3.0.0` - `4.2.1` |`4.12.0` - `4.25.0` | 3.8+ |
|`2.10.0` - `2.11.1` |`4.1.0` - `4.11.2` | 3.7+ |
|`2.2.0` - `2.9.0` |`4.1.0` - `4.9.0` | 3.7+ |
|`2.0.0` - `2.1.4` |`4.0.0` | 3.7+ |
|`1.0.0` - `1.3.0` |`3.x`| 3.7+ |
|`0.52` and below|`3.x`| 2.7, 3.4 - 3.7 |

The Appium Python Client depends on [Selenium Python binding](https://pypi.org/project/selenium/), thus
the Selenium Python binding update might affect the Appium Python Client behavior.
For example, some changes in the Selenium binding could break the Appium client.

Instalação de Pacote
https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/

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

Download do APK do nosso primeiro exemplo:
https://github.com/serhatbolsu/robotframework-appium-sample/blob/master/demoapp/ApiDemos-debug.apk

Library Documentation:

Robot Framework:
https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html
https://github.com/robotframework/robotframework

Robot Appium:
https://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html
https://github.com/serhatbolsu/robotframework-appiumlibrary

Appium Client:
https://pypi.org/project/Appium-Python-Client/
https://github.com/appium/python-client

The Appium Python Client depends on Selenium Python binding, thus the Selenium Python binding update might affect the Appium Python Client behavior. For example, some changes in the Selenium binding could break the Appium client.

