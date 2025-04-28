# Getting Started with GitHub Copilot

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hi!

Ara here. I'm done preparing your exercise. Hope you enjoy! 💚

Remember, it's self-paced so feel fee to take a break! ☕️

[![](https://img.shields.io/badge/Go%20to%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/aracelivera/skills-getting-started-with-github-copilot/issues/1)

# Nubiral High School Activities API

A super simple FastAPI application that allows students to view and sign up for extracurricular activities.

## Features

- View all available extracurricular activities
- Sign up for activities

## Getting Started

1. Install the dependencies:

   ```
   pip install fastapi uvicorn
   ```

2. Run the application:

   ```
   python app.py
   ```

3. Open your browser and go to:
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with their details and current participant count |
| POST   | `/activities/{activity_name}/signup?email=student@nubiral.edu` | Sign up for an activity                                             |

## Data Model

The application uses a simple data model with meaningful identifiers:

1. **Activities** - Uses activity name as identifier:

   - Description
   - Schedule
   - Maximum number of participants allowed
   - List of student emails who are signed up

2. **Students** - Uses email as identifier:
   - Name
   - Grade level

All data is stored in memory, which means data will be reset when the server restarts.


# 🚀 Demo: Workflow CI/CD con GitHub Copilot


En la presente demo, utilizaremos GitHub Copilot como asistente principal en la creación de un pipeline de CI/CD con GitHub Actions. Incluye las etapas de build, test y deploy de una aplicación Python-FastApi en Azure App Service. 
## 📌 Objetivos
<img src="https://private-user-images.githubusercontent.com/37269996/422481316-4d22496d-850b-4785-aafe-11cba03cd5f2.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDU4MDUyMzIsIm5iZiI6MTc0NTgwNDkzMiwicGF0aCI6Ii8zNzI2OTk5Ni80MjI0ODEzMTYtNGQyMjQ5NmQtODUwYi00Nzg1LWFhZmUtMTFjYmEwM2NkNWYyLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA0MjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNDI4VDAxNDg1MlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWY1NzZlOGJhYWFhMGQxNmVmYzZhNTVlNWVjMmM1NDVlYmQ2ODg1NDBlNmFjZGE1OTA5NGJkNjM0NzJlNjAzNmQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.v-H5sC0Xd4PoAqxf9QDzuzK8ZM5bXliDw5z2Uv2s6Jc" align="right" height="200px" />

- Usar GitHub Copilot para generar un workflow completo con GitHub Actions.
- Explorar las funcionalidades de GitHub Copilot en distintos entornos: IDE, línea de comandos y GitHub Web.
- Aprovechar prompts en lenguaje natural para resolver tareas técnicas sin conocimientos previos.
- Aumentar tu productividad automatizando procesos de build, test y deploy con ayuda de IA 🤖.

---
## 🛠️ Requisitos previos

- Cuenta de [GitHub](https://github.com/) con GitHub Copilot habilitado.
- Cuenta en [Azure](https://azure.microsoft.com/) con acceso a Azure App Service.
- Visual Studio Code instalado localmente o en GitHub Workspace.
- Extensiones de VSC:
    - [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
    - [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    - [GitHub Copilot for Azure](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azure-github-copilot)    
- Clone del repositorio:

     ```bash
     git clone https://github.com/aravera-nubi/fastapi-copilot.git
     ```


## ⌨️ Paso 1:  Obtener una introducción al proyecto desde Copilot Chat
Luego de haber configurado nuestro entorno de desarrollo, usemos Copilot para aprender un poco sobre el proyecto.

1. Abre el proyecto, previamente clonado, en Visual Studio Code.

2. En la parte superior de VS Code, localiza y haz clic en el ícono de **Copilot** para abrir un panel de Copilot Chat.

   ![Copilot Chat](assets/github-chat-icon.png)


   > **Nota:** Si es la primera vez que usas GitHub Copilot, necesitarás iniciar sesión con tu cuenta de GitHub y aceptar los términos de uso para continuar.


3. Escribe el siguiente mensaje para pedirle a Copilot que te haga una introducción al proyecto:

   ```markdown
   @workspace Please briefly explain the structure of this project.
<details style="margin-left: 40px;">
<summary>Ejemplo de respuesta</summary>

Colocar la imágen/ hacer referencia a la captura.

</details > 

4. Ahora que estamos un poco más familiarizados con el proyecto, vamos a ver cómo podemos usar Copilot para ejecutarlo localmente. Ingresa el siguiente mensaje en el chat para que Copilot te guíe:

   ```markdown
   @workspace Help me run the application locally by creating a virtual environment (.venv) and installing the dependencies. I'm using Git Bash on Windows.

<details style="margin-left: 40px;">
<summary>Ejemplo de respuesta</summary>

Colocar la imágen/ hacer referencia a la captura.

</details > 


##  Paso 2:  Usar GitHub Copilot desde la terminal de VS Code para crear una nueva rama
Ahora que tenemos el proyecto corriendo localmente, vamos a crear una nueva rama para trabajar en la implementación de un pipeline de CI/CD. Usaremos GitHub Copilot para ayudarnos a recordar los comandos de la terminal.

1. Crea una nueva rama para trabajar con workflows de GitHub Actions: En el panel inferior, selecciona la pestaña **Terminal**. En el lado derecho, haz clic en el signo más `+` para crear una nueva ventana de terminal.     
   ![Terminal](assets/github-terminal-icon.png)

   > **Nota:** Si no ves el ícono de la terminal, puedes abrir una nueva terminal usando el atajo de teclado `Ctrl + Shift + \`` (windows) o `Cmd + Shift + \`` (mac).  
    
2. Dentro de la nueva ventana de terminal, usa el atajo de teclado `Ctrl + I` (windows) o `Cmd + I` (mac) para abrir el **Copilot's Terminal Inline Chat**.

   Escribe el siguiente prompt:

   ```markdown
   Hey copilot, how can I create and publish a new Git branch?


3. Copilot probablemente nos sugirió lo siguiente. En lugar de modificarlo manualmente, respondamos para decirle a Copilot que use un nombre en particular.

4. Ahora, presiona el botón **Run** para que Copilot lo ejecute por nosotros. No es necesario copiar y pegar.


##  Paso 3:  Crear carpeta y archivo .yml para el workflow de GitHub Actions

posibles prompts

Opción A : Usando el chat

```bash
@workspace ¿Cómo creo un workflow de CI/CD con GitHub Actions desde cero para mi aplicación que haga build, test y deploy en Azure App Service?
```

Acá me 

1. Opción B: Usando chat