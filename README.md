# GASS — Secure Password Generator & Auditor

**Gerador e Auditor de Senhas Seguras | Secure Password Generator & Auditor | Generador y Auditor de Contraseñas Seguras**

A local-first password security application built with Python, designed to generate strong passwords, audit password strength, manage credentials locally, and provide AI-assisted cybersecurity guidance — entirely offline.

**Free to use · Local-first · Multilingual · Open-source project**

> **Important:** Commercial sale of GASS is prohibited under the project's intended terms. See the licensing section below.

---

## 🇬🇧 English

### Overview

GASS (Secure Password Generator & Auditor) is a Python application designed to help users create, evaluate, and manage passwords in a private local environment.

It combines password generation, security auditing, local credential management, PDF reporting, and an embedded AI assistant in a single application. GASS runs on the user's computer and does not send passwords, audit results, or password history over the internet.

The application supports **English, Portuguese, and Spanish**, making its main interface accessible to users in all three languages.

### Key Features

- **Secure Password Generator:** Generate passwords using Python's `secrets` module, with customizable length, character sets, ambiguous-character exclusion, and pronounceable-password options.
- **Password Security Auditor:** Analyze password strength, estimated entropy, and estimated brute-force cracking time.
- **Local Breach-List Checking:** Check passwords against the included RockYou password list without sending them to an external service.
- **Batch Auditing:** Analyze multiple passwords in a single operation.
- **PDF Security Reports:** Generate educational reports containing analysis results and password recommendations.
- **Local Password Manager:** Save and organize credentials in a local database, with encrypted favorites.
- **User Isolation:** Multiple local accounts can use GASS on the same computer. Each authenticated user has a separate application history and favorites.
- **Embedded Local AI Assistant:** Ask cybersecurity and password-security questions using an integrated GGUF language model, powered by `llama-cpp-python`.
- **Local Storage:** SQLite database for persistent application data.
- **Multilingual Interface:** Portuguese, English, and Spanish.
- **Offline Operation:** All features work locally without cloud-based password processing.

### Target Audience

GASS is intended for:

- Individuals who want to improve their password security.
- Students learning about cybersecurity and password auditing.
- Developers and IT professionals who need a local password-analysis tool.
- Families, roommates, and other people sharing a computer who want separate local credential collections.
- Privacy-conscious users who prefer not to submit passwords to online services.
- Educational environments and cybersecurity demonstrations.

GASS is designed for local use, not as a centralized enterprise password-management platform.

### Privacy and Security

GASS follows a local-first design philosophy:

- Passwords and audit results are not transmitted to external servers by the application.
- Password analysis and breach-list checks run locally.
- User passwords are stored as PBKDF2 hashes.
- Favorite credentials are encrypted locally.
- Application history is filtered by the authenticated local account.
- The AI assistant runs locally using its bundled language model.

**Security note:** Local operation reduces exposure to external services but does not eliminate every security risk. Device compromise, malicious software, weak account passwords, and insecure backups can still expose information. GASS should not be considered a substitute for an independent security assessment.

### Technology Stack

| Component | Technology |
|---|---|
| Backend | Python and Flask |
| Frontend | HTML, CSS, JavaScript |
| Database | SQLite |
| Password generation | Python `secrets` |
| Credential encryption | Python `cryptography` |
| PDF reports | ReportLab |
| Local AI inference | `llama-cpp-python` and GGUF |
| Breach-list checking | Local RockYou password list |

### Installation

See **[MANUAL_INSTALACAO.md](MANUAL_INSTALACAO.md)** for installation instructions for Windows and Linux.

Quick start:

```bash
python -m venv venv
```

Activate the environment:

**Linux:**
```bash
source venv/bin/activate
```

**Windows:**
```powershell
venv\Scripts\activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Start the application:

```bash
python app.py
```

Open your browser at:

http://127.0.0.1:5000

For the local AI assistant, consult the installation manual for any additional dependencies.

---

## 🇧🇷 Português

### Visão Geral

O GASS (Gerador e Auditor de Senhas Seguras) é uma aplicação desenvolvida em Python para ajudar usuários a criar, analisar e gerenciar senhas em um ambiente local e privado.

A aplicação reúne geração de senhas, auditoria de segurança, gerenciamento local de credenciais, emissão de relatórios em PDF e um assistente de inteligência artificial integrado. O GASS funciona no computador do usuário e não envia senhas, resultados de auditoria ou histórico de senhas pela internet.

Sua interface oferece suporte a **português, inglês e espanhol**.

### Principais Recursos

- **Gerador de Senhas Seguras:** Gera senhas com o módulo `secrets` do Python, permitindo configurar o comprimento, os tipos de caracteres, a exclusão de caracteres ambíguos e opções de senhas fáceis de pronunciar.
- **Auditor de Senhas:** Analisa a força da senha, a entropia estimada e o tempo estimado para quebra por força bruta.
- **Verificação contra Vazamentos:** Compara senhas localmente com a lista de senhas RockYou incluída no projeto, sem recorrer a serviços externos.
- **Auditoria em Lote:** Permite analisar diversas senhas em uma única operação.
- **Relatórios em PDF:** Gera relatórios educacionais com os resultados da análise e recomendações de segurança.
- **Gerenciador Local de Senhas:** Permite salvar e organizar credenciais em um banco de dados local, com favoritos cifrados.
- **Isolamento entre Usuários:** Permite que diferentes pessoas utilizem o GASS no mesmo computador, cada uma com sua própria conta local, histórico e coleção de favoritos.
- **Assistente de IA Local:** Oferece respostas sobre segurança digital e senhas por meio de um modelo GGUF integrado, executado com `llama-cpp-python`.
- **Armazenamento Local:** Utiliza SQLite para persistência dos dados.
- **Interface Multilíngue:** Disponível em português, inglês e espanhol.
- **Funcionamento Offline:** Os recursos funcionam localmente, sem processamento de senhas na nuvem.

### Público-Alvo

O GASS foi desenvolvido para:

- Pessoas que desejam melhorar a segurança de suas senhas.
- Estudantes de tecnologia e segurança cibernética.
- Desenvolvedores e profissionais de TI que precisam de uma ferramenta local de análise de senhas.
- Famílias, colegas de moradia e pessoas que compartilham o mesmo computador e precisam manter suas credenciais separadas.
- Usuários preocupados com privacidade que preferem não enviar senhas para serviços online.
- Ambientes educacionais, estudos e demonstrações de segurança cibernética.

O GASS prioriza o uso local e não pretende substituir plataformas corporativas centralizadas de gerenciamento de senhas.

### Privacidade e Segurança

O GASS foi projetado com uma abordagem local-first:

- A aplicação não transmite senhas ou resultados de auditoria para servidores externos.
- As análises e verificações contra a lista de vazamentos são realizadas localmente.
- As senhas das contas locais são armazenadas como hashes PBKDF2.
- As credenciais favoritas são cifradas localmente.
- O histórico é filtrado conforme a conta autenticada.
- O assistente de IA é executado localmente com o modelo de linguagem incluído no projeto.

**Observação de segurança:** O funcionamento local reduz a exposição a serviços externos, mas não elimina todos os riscos. O comprometimento do computador, a presença de malware, senhas fracas nas contas locais e backups inseguros ainda podem expor informações. O GASS não substitui uma avaliação independente de segurança.

### Tecnologias Utilizadas

| Componente | Tecnologia |
|---|---|
| Backend | Python e Flask |
| Frontend | HTML, CSS e JavaScript |
| Banco de dados | SQLite |
| Geração de senhas | `secrets` do Python |
| Cifragem de credenciais | `cryptography` |
| Relatórios PDF | ReportLab |
| IA local | `llama-cpp-python` e GGUF |
| Verificação de vazamentos | Lista RockYou local |

### Instalação

Consulte o **[MANUAL_INSTALACAO.md](MANUAL_INSTALACAO.md)** para ver as instruções completas para Windows e Linux.

Início rápido:

```bash
python -m venv venv
```

Ative o ambiente virtual:

**Linux:**
```bash
source venv/bin/activate
```

**Windows:**
```powershell
venv\Scripts\activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Inicie a aplicação:

```bash
python app.py
```

Acesse pelo navegador:

http://127.0.0.1:5000

Para utilizar o assistente de IA local, consulte também o manual de instalação.

---

## 🇪🇸 Español

### Descripción General

GASS (Generador y Auditor de Contraseñas Seguras) es una aplicación desarrollada en Python para ayudar a los usuarios a generar, analizar y administrar contraseñas en un entorno local y privado.

La aplicación integra generación de contraseñas, auditoría de seguridad, administración local de credenciales, generación de informes en PDF y un asistente de inteligencia artificial integrado. GASS funciona en el ordenador del usuario y no transmite contraseñas, resultados de auditoría ni historiales de contraseñas a través de internet.

La interfaz está disponible en **portugués, inglés y español**.

### Funcionalidades Principales

- **Generador de Contraseñas Seguras:** Genera contraseñas mediante el módulo `secrets` de Python, con opciones para configurar la longitud, los tipos de caracteres, la exclusión de caracteres ambiguos y la generación de contraseñas fáciles de pronunciar.
- **Auditor de Contraseñas:** Analiza la fortaleza de las contraseñas, la entropía estimada y el tiempo estimado de descifrado mediante fuerza bruta.
- **Comprobación de Contraseñas Filtradas:** Compara contraseñas localmente con la lista RockYou incluida en el proyecto, sin utilizar servicios externos.
- **Auditoría por Lotes:** Permite analizar varias contraseñas en una sola operación.
- **Informes en PDF:** Genera informes educativos con los resultados del análisis y recomendaciones de seguridad.
- **Gestor Local de Contraseñas:** Permite guardar y organizar credenciales en una base de datos local, con favoritos cifrados.
- **Aislamiento entre Usuarios:** Permite que varias personas utilicen GASS en el mismo ordenador, cada una con su propia cuenta local, historial y colección de favoritos.
- **Asistente de IA Local:** Responde preguntas sobre ciberseguridad y protección de contraseñas mediante un modelo GGUF integrado, ejecutado con `llama-cpp-python`.
- **Almacenamiento Local:** Utiliza SQLite para conservar los datos.
- **Interfaz Multilingüe:** Disponible en portugués, inglés y español.
- **Funcionamiento sin Conexión:** Las funciones se ejecutan localmente, sin procesamiento de contraseñas en la nube.

### Público Objetivo

GASS está dirigido a:

- Personas que desean mejorar la seguridad de sus contraseñas.
- Estudiantes de tecnología y ciberseguridad.
- Desarrolladores y profesionales de TI que necesitan una herramienta local para analizar contraseñas.
- Familias, compañeros de piso y personas que comparten un ordenador y necesitan mantener sus credenciales separadas.
- Usuarios preocupados por la privacidad que prefieren no enviar sus contraseñas a servicios en línea.
- Entornos educativos, estudios y demostraciones de ciberseguridad.

GASS está orientado al uso local y no pretende sustituir las plataformas empresariales centralizadas de administración de contraseñas.

### Privacidad y Seguridad

GASS sigue una filosofía de funcionamiento local:

- La aplicación no transmite contraseñas ni resultados de auditoría a servidores externos.
- Los análisis y las comprobaciones contra la lista de contraseñas filtradas se realizan localmente.
- Las contraseñas de las cuentas locales se almacenan como hashes PBKDF2.
- Las credenciales favoritas se cifran localmente.
- El historial se filtra según la cuenta autenticada.
- El asistente de IA se ejecuta localmente mediante el modelo de lenguaje incluido en el proyecto.

**Nota de seguridad:** El funcionamiento local reduce la exposición a servicios externos, pero no elimina todos los riesgos. Un ordenador comprometido, el malware, las contraseñas débiles de las cuentas locales o las copias de seguridad inseguras pueden exponer información. GASS no sustituye una evaluación de seguridad independiente.

### Tecnologías Utilizadas

| Componente | Tecnología |
|---|---|
| Backend | Python y Flask |
| Frontend | HTML, CSS y JavaScript |
| Base de datos | SQLite |
| Generación de contraseñas | `secrets` de Python |
| Cifrado de credenciales | `cryptography` |
| Informes PDF | ReportLab |
| IA local | `llama-cpp-python` y GGUF |
| Comprobación de filtraciones | Lista RockYou local |

### Instalación

Consulta el **[MANUAL_INSTALACAO.md](MANUAL_INSTALACAO.md)** para obtener las instrucciones completas de instalación en Windows y Linux.

Inicio rápido:

```bash
python -m venv venv
```

Activa el entorno virtual:

**Linux:**
```bash
source venv/bin/activate
```

**Windows:**
```powershell
venv\Scripts\activate
```

Instala las dependencias:

```bash
pip install -r requirements.txt
```

Inicia la aplicación:

```bash
python app.py
```

Abre el navegador y visita:

http://127.0.0.1:5000

Para utilizar el asistente de IA local, consulta también el manual de instalación.

---

## Open-Source and Usage Policy

GASS is intended to be freely available for personal, educational, and research use. Selling GASS, its bundled application, or repackaged copies as a commercial product is prohibited under the project's intended terms.

The source code is made available for inspection, learning, and community collaboration. Any redistribution must preserve the project's applicable usage terms and attribution.

**License notice:** The project's formal license must be included in a `LICENSE` file. A restriction prohibiting commercial sale is not compatible with the standard Open Source Definition. Until a formal license is selected and published, do not assume that this README alone establishes legally enforceable licensing terms.

## Política de Uso e Licença

O GASS pretende ser disponibilizado gratuitamente para uso pessoal, educacional e de pesquisa. É proibida a venda do GASS, de sua aplicação distribuída ou de cópias reempacotadas como produto comercial, conforme os termos pretendidos para o projeto.

O código-fonte é disponibilizado para consulta, aprendizado e colaboração comunitária. Qualquer redistribuição deve respeitar os termos de uso aplicáveis e preservar a atribuição ao projeto.

**Aviso sobre a licença:** A licença formal deve ser incluída em um arquivo `LICENSE`. A proibição de uso comercial não é compatível com a definição padrão de código aberto. Até que uma licença formal seja escolhida e publicada, este README, por si só, não deve ser considerado uma licença juridicamente completa.

## Política de Uso y Licencia

GASS pretende distribuirse gratuitamente para uso personal, educativo y de investigación. Se prohíbe la venta de GASS, de su aplicación distribuida o de copias reempaquetadas como producto comercial, conforme a los términos previstos para el proyecto.

El código fuente está disponible para su consulta, aprendizaje y colaboración comunitaria. Cualquier redistribución debe respetar las condiciones de uso aplicables y conservar la atribución al proyecto.

**Aviso sobre la licencia:** La licencia formal debe incluirse en un archivo `LICENSE`. La prohibición del uso comercial no es compatible con la definición estándar de código abierto. Hasta que se elija y publique una licencia formal, este README por sí solo no debe considerarse una licencia jurídicamente completa.

---

## Project Information

**Project:** GASS — Gerador e Auditor de Senhas Seguras  
**Authors:** Davi Luiz and Gabriel Zanette  
**Type:** Local password security application  
**Languages:** Portuguese, English, Spanish  
**Execution:** Local / offline  
**License:** To be formally defined

Developed as a Technology Capstone Project (TCC).
