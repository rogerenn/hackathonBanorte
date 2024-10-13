HackathonBanorte

Multi-Agentes para Asistencia Financiera

Este proyecto contiene una arquitectura de multi-agentes implementada en Python para ayudar a los usuarios a gestionar sus finanzas, resolver dudas sobre Banorte, planificar movimientos financieros y realizar inversiones.
Estructura de los Agentes
1. Agente Orquestador (orchestrator.py)

    Objetivo: Actúa como el agente principal, gestionando la interacción con el usuario y redirigiéndolo al agente correspondiente según su solicitud.
    Instrucciones:
        Saluda al usuario y pregunta cómo puede ayudarlo.
        Redirige a:
            Agente Experto Banorte: para dudas sobre Banorte.
            Agente Planificador: para planificación de movimientos.
            Agente Inversor: para análisis y asistencia en inversiones.

2. Agente Experto Banorte (automator.py)

    Objetivo: Responder preguntas del usuario relacionadas con Banorte.
    Instrucciones:
        Pregunta al usuario cuál es su duda específica.
        Usa la herramienta de Datos Banorte para obtener la respuesta adecuada.
        Repite el ciclo de preguntas y respuestas si el usuario tiene más dudas.

3. Agente Inversor (investor.py)

    Objetivo: Asiste al usuario en la gestión de sus inversiones.
    Subagentes:
        Inversor Analista: Monitorea inversiones actuales y ofrece análisis detallado.
        Inversor Proactivo: Ayuda al usuario a realizar nuevas inversiones.
    Instrucciones:
        Ofrece opciones de análisis de inversiones actuales o ayuda en nuevas inversiones.
        Usa las herramientas de Monitoreo de acciones y Compra de acciones para asistir al usuario en sus decisiones.

Instalación y Configuración
1. Clonar el Repositorio:

bash

git clone https://github.com/tu_usuario/HackathonBanorte.git
cd HackathonBanorte

2. Instalar Dependencias:

Se recomienda crear un entorno virtual para gestionar las dependencias. Puedes hacerlo con los siguientes comandos:

bash

python3 -m venv .venv
source .venv/bin/activate  # En Linux/MacOS
.venv\Scripts\activate     # En Windows
pip install -r requirements.txt

3. Configurar el Entorno:

Crea un archivo .env basado en el archivo de ejemplo proporcionado, donde se configuran las credenciales y variables de entorno necesarias para la interacción con los agentes.
Uso

Para ejecutar el sistema de agentes:

bash

python hackathon.py

Los agentes comenzarán a interactuar según los inputs del usuario, orquestados por el Agente Orquestador. Los módulos están diseñados para ser escalables y fácilmente extendibles, permitiendo agregar nuevas funcionalidades o agentes conforme sea necesario.
Estructura del Proyecto

    agents/: Contiene los archivos Python de los agentes (Orquestador, Experto Banorte, Inversor).
    chains/: Lógica de procesamiento de cadenas de acciones.
    conversation/: Manejo de la conversación entre agentes y el usuario.
    utils/: Funciones auxiliares para soporte de datos y operaciones generales.

Próximos Pasos

    Integración de nuevos agentes: Agregar más agentes para ofrecer soporte en otras áreas financieras.
    Mejora de la UI/UX: Incorporar una interfaz de usuario para interactuar visualmente con los agentes.
    Expansión multiplataforma: Extender la compatibilidad más allá de sistemas basados en Python, con versiones para web y móvil.

