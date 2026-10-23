# Movies Go | Performance & QA

**Evaluación de eficiencia de desempeño mediante pruebas automatizadas.**

## 🎯 Objetivo del repositorio

Este repositorio tiene como objetivo evaluar la **eficiencia de desempeño de Movies Go**, verificando qué tan rápida es la aplicación y cómo se comporta bajo situaciones de alta exigencia y estrés.

Se busca preparar una infraestructura de pruebas que permita medir tiempos de respuesta, identificar errores y analizar el comportamiento de la aplicación al aumentar la carga de trabajo. Para ello, se utilizará **k6** como herramienta de pruebas de rendimiento y **GitHub Actions** para automatizar su ejecución.

## 📁 ¿Qué contiene el repositorio?

- **`.github/workflows/`**: workflows que automatizan la preparación del entorno, la compilación del proyecto y la verificación del arranque del backend.
- **`performance/k6/`**: espacio destinado a los scripts, escenarios y configuraciones de las futuras pruebas de rendimiento.
- **`results/`**: espacio previsto para organizar los resultados y reportes de las pruebas.
- **`README.md`**: documentación general del proyecto y su funcionamiento.

## ⚙️ ¿Cómo funciona la automatización?

Mediante **GitHub Actions**, los workflows ejecutan tareas previamente definidas en un entorno temporal, pudiendo preparar las herramientas necesarias, compilar los componentes de Movies Go y verificar que el backend arranque y responda correctamente además de permitir ejecutar los escenarios de rendimiento de forma controlada y recopilar métricas para su posterior análisis, haciendo uso de K6.

Las credenciales necesarias, como la clave de OMDb, se gestionan mediante **GitHub Actions Secrets**. Esto permite utilizarlas durante la ejecución sin escribirlas directamente en los archivos del repositorio.

## 🔗 ¿Cómo funciona sin tener el código de Movies Go aquí?

El código fuente de Movies Go se mantiene en su repositorio original, separado de este repositorio de QA.

Durante cada ejecución, GitHub Actions descarga temporalmente el proyecto original en el entorno de trabajo, donde puede compilarlo o iniciarlo según el workflow correspondiente. De esta manera, las herramientas y los scripts de QA permanecen independientes, sin necesidad de duplicar el código fuente ni modificar el repositorio original.

## 🛠️ Tecnologías

- [GitHub Actions](https://docs.github.com/en/actions): automatización de workflows.
- [k6](https://grafana.com/docs/k6/latest/): pruebas de carga y rendimiento.
- Java 21, Maven y Spring Boot: backend.
- Node.js, npm y Angular: frontend.
