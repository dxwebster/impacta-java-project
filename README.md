# :dart: Sobre

Primeiro projeto Java para aprender instalação de Java Development Kit e outras ferramentas

# :rocket: Tecnologias

Neste projeto foram utilizadas as seguintes ferramentas:

- [SDKMan](https://sdkman.io/)
- [Java Development Kit (JDK)](https://sdkman.io/jdks)
- [Maven](https://sdkman.io/sdks)

# 📂 Como criar esse projeto do zero

Obs: esse tutorial é para Linux ou Mac. Se estiver com Windows, vale a pena instalar o [WSL2](https://github.com/codeedu/wsl2-docker-quickstart#instala%C3%A7%C3%A3o-do-wsl-2), você não vai se arrepender! :D

## 1. Instalar SDKMan!

SDKMan é um **gerenciador de Kits de Desenvolvimento de Softwares (SDK)** na maioria dos sistemas baseados em Unix.

Ele tem uma CLI que utilizaremos para instalar todas as ferramentas do Java.

Para instalar o SDKMan, executar:

`curl -s "https://get.sdkman.io" | bash`

Depois, para usar sua CLI, vamos executar:

`sdk <comando>`


## 2. Instalar o Java 

Instalar o Java significa instalar sua JDK, ou seja, seu kit de desenvolvimento.

Existem diversas dstribuições de JDK do Java, mas todas elas incluem:

- **Java Runtime Environment (JRE):** uma espécie de máquina virtual que executa código Java
- **Compilador Java (javac):** um compilador que converte código Java em arquivos binários

Vamos instalar o Java e suas ferramentas por meio da CLI SDKMan, escolhendo a distribuição que desejamos.

Neste caso, vamos instalar adistribuição OpenJDK (Open Java Development Kit):

`sdk install java 17-open`

## 3. Instalar o Maven 

Maven é o **gerenciador de pacotes do Java**.

Podemos instalar o Maven também pela CLI do SDKMan:

`sdk install maven`

## 4. Criar template de projeto Java

Com o Maven, podemos criar projetos java utilizando templates, chamaos de archetype. Para baixar os templates disponíveis, executar:

`mvn archetype:generate`

O terminal vai solicitar um **número ou um filtro** (choose a number or apply a filter).

Vamos filtrar por projetos de template bem básicos com a palavra-chave:

`quickstart`

O terminal vai pedir novamente um número ou filtro, mas vai dar um número como sugestão.

```
Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): 120:
```

Neste caso sugeriu o '120', digitar '120' e dar ENTER.

Depois vai solicitar para selecionar a versão. 

```
Choose org.apache.maven.archetypes:maven-archetype-quickstart version: 
1: 1.0-alpha-1
2: 1.0-alpha-2
3: 1.0-alpha-3
4: 1.0-alpha-4
5: 1.0
6: 1.1
7: 1.3
8: 1.4
Choose a number: 8: 8
```

**Selecionar sempre a última**, neste caso, a versão 8.

Depois o terminal vai solicitar que responda várias perguntas para estruturar o projeto com nomes e créditos, grupo, artefato, autor, etc. 

```
$ Define value for property 'groupId': fit
$ Define value for property 'artifactId': exemplo-java
$ Define value for property 'version' 1.0-SNAPSHOT: <ENTER>
$ Define value for property 'package' fit: <ENTER>
$ Confirm properties configuration: Y
```

Depois só acessar o projeto:

`cd exemplo-java`

E rodar um teste para verificar seu tudo ocorreu como esperado:

`mvn test`

Se aparecer a mensagem BUILD SUCESS, o projeto foi criado com sucesso!

```bash
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running fit.AppTest
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.012 s - in fit.AppTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  52.139 s
[INFO] Finished at: 2022-04-21T19:07:13-03:00
[INFO] ------------------------------------------------------------------------
```

## :memo: License ##

This project is under license from MIT.


Made with :heart: by <a href="https://github.com/dxwebster" target="_blank">dxwebster</a>

&#xa0;

<a href="#top">Back to top</a>
