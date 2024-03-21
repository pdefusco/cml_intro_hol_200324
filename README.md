# CML Intro HOL 20/03/24

Cloudera Machine Learning es la plataforma de aprendizaje automático nativa en Cloud de Cloudera, construida para CDP. Cloudera Machine Learning unifica la ciencia de datos y la ingeniería de datos de autoservicio en un único servicio portátil como parte de Cloud empresariales para análisis multifuncionales de datos en cualquier lugar.

CML empodera a las organizaciones para construir e implementar capacidades de aprendizaje automático e IA para negocios a gran escala, de manera eficiente y segura, donde quieran. Está diseñado para la agilidad y potencia de la computación en la nube, pero no se limita a ningún proveedor de nube o fuente de datos en particular.


### Beneficios de CML

CML es una plataforma integral para implementar capacidades de aprendizaje automático de manera colaborativa a gran escala y proporciona beneficios para cada tipo de usuario:

##### Científicos de Datos

* CML permite a los equipos de Ciencia de Datos colaborar y acelerar el desarrollo y entrega de modelos con flujos de trabajo transparentes, seguros y gobernados.
* CML Amplía los casos de uso de IA con pipelines de ML automatizados y un conjunto de herramientas de ML de producción integrado y completo.
* Facilita la toma de decisiones más rápida y confiable con visibilidad y auditabilidad de extremo a extremo de datos, procesos, modelos y paneles.

##### Equipos de IT

* CML aumenta la productividad de Ciencia de Datos con visibilidad, seguridad y gobernabilidad de todo el ciclo de vida de ML.
* CML elimina silos, puntos ciegos y la necesidad de mover/duplicar datos con una plataforma completamente integrada en todo el ciclo de vida de datos.
* CML acelera la IA con acceso a Workspace de ML contenerizados que eliminan la carga pesada y llevan los modelos a producción más rápido.

##### Analistas y Otros Business Users

* CML accede a Aplicaciones interactivas construidas e implementadas por equipos de Ciencia de Datos.
* Con CML se empodera con conocimientos predictivos para tomar decisiones comerciales de manera más inteligente.


### Capacidades Principales de CML

CML cubre el flujo de trabajo completo de aprendizaje automático, permitiendo cargas de trabajo completamente aisladas y contenerizadas, incluidos Python, R y Spark-on-Kubernetes, para ingeniería de datos a escala y aprendizaje automático con gestión distribuida de dependencias sin problemas.

* Las sesiones permiten a los científicos de datos aprovechar directamente la capacidad de cálculo de CPU, memoria y GPU disponibles en el Workspace, al mismo tiempo que están directamente conectados a los datos en el lago de datos.

* Los experimentos permiten a los científicos de datos ejecutar múltiples variaciones de cargas de trabajo de entrenamiento de modelos, rastreando los resultados de cada experimento para entrenar el mejor modelo posible.

* Los modelos pueden ser implementados en cuestión de clics, eliminando cualquier obstáculo para la producción. Se sirven como puntos finales REST de manera altamente disponible, con construcción de linaje automatizada y seguimiento de métricas para propósitos de MLOps.

* Los Job pueden ser utilizados para orquestar un pipeline automatizado completo de extremo a extremo, incluyendo monitoreo para el desvío del modelo y la activación automática de la re-entrenamiento y re-implementación del modelo según sea necesario.

* Las aplicaciones ofrecen experiencias interactivas para usuarios comerciales en cuestión de clics. Marcos como Flask y Shiny pueden ser utilizados en el desarrollo de estas aplicaciones, mientras que Cloudera Data Visualization también está disponible como una interfaz de punto y clic para construir estas experiencias.

![alt text](img/cmlarch.png)


### Cloudera Data Platform (CDP)

La Plataforma de Datos de Cloudera (CDP) es un Cloud de datos empresariales que funciona como una plataforma tanto para equipos de IT como para usuarios. Incorpora soporte para un ambiente que se ejecuta tanto en las instalaciones como en una configuración de Public Cloud.

CDP es simple de usar y segura por diseño. Ofrece un ambiente común tanto para ingenieros de datos como para científicos de datos, apoyando la colaboración de equipos de ciencia de datos. Esto incluye seguridad de datos, gobernanza, linaje y control consistentes, mientras despliega análisis en la nube eficientes y fáciles de usar, eliminando la necesidad de soluciones de TI en la sombra para los usuarios finales.

* Secure By Design: cada parte de la arquitectura e infraestructura de su plataforma y aplicación se construye teniendo en cuenta la seguridad como consideración primaria. CDP despliega automáticamente un layer unificado de gobernanza y seguridad de datos y usuarios en todos sus ambientes para permitir que los equipos de IT implementen sólidas Best Practices para la autenticación, autorización y el monitoreo de todos los procesos de Cloud.

* Track and Audit Everything: CDP proporciona registros de auditoría centrados en los datos que explican de dónde provienen los datos, cómo llegaron a su estado actual y cómo se están utilizando. Cuando esos datos son procesados y analizados, las ideas resultantes también pueden ser clasificadas, incluyendo los datos a partir de los cuales se derivaron esas ideas.

* Aligned Practices across Environments: Prácticas consistentes en la gestión de ambientes en la nube resultarán en costos operativos reducidos y prácticas de seguridad más sencillas.

![alt text](img/cmlplatform.png)


### Instrucciones Para los Ejercicios

En esta sesión introductoria te familiarizarás con los Proyectos de CML, Runtimes, Sesiones y Jobs.

* Utilizarás los Proyectos de CML para cargar rápidamente artefactos de ciencia de datos como scripts de desarrollo y conjuntos de datos, y aislar tu trabajo de los demás.

* Con los Runtimes de CML, podrás instalar rápidamente paquetes de Python, implementar aplicaciones distribuidas de Spark sin instalaciones engorrosas y aislar tus dependencias de otros container.

* Con las Sesiones de CML, desplegarás el container y todos los paquetes instalados en el Runtime para que puedas interactuar con tus datos y código de manera iterativa.

* Usando los Jobs de CML, desplegarás tu código como un batch job y opcionalmente programarás nuevas ejecuciones.


##### Despliegue de Proyecto

Descargue los archivos del proyecto en su computadora local.

1. Visite [este enlace](https://github.com/pdefusco/cml_intro_hol_200324)
2. Haz clic en "Código" y luego en "Descargar ZIP" para descargar todos los archivos.

![alt text](img/labs00.png)

Cree el proyecto.

1. Ingresa al Workspace de CML y haz clic en el ícono "Create Project".
2. En la sección "Configuración Inicial", haz clic en "Local Files" y luego en la opción "Upload Zip or Tar Archive".
3. Desplázate hacia abajo hasta la sección de Runtimes y agrega dos runtimes de Python 3.9. Agrega uno con el editor de JupyterLab y el otro con el editor de Workbench.

![alt text](img/labs000.png)

![alt text](img/labs01.png)

![alt text](img/labs02.png)

![alt text](img/labs03.png)

![alt text](img/labs04.png)

Ingresa al proyecto y familiarízate con los archivos que se han subido.

![alt text](img/labs05.png)


##### Despliegue de Sesión y Instalación de Paquetes en Runtime

Abre una sesión con las siguientes opciones de Runtime.

```
Editor: JupyterLab
Kernel: Python 3.9
Edition: Standard
Version: 2023 o 2024
Enable Spark: Spark 3.2
Resource Profile: 2 CPU / 4 GB Mem / 0 GPU
```

![alt text](img/labs06.png)

Después de unos momentos, se abrirá la interfaz de Notebook JupyterLab. Ejecute cada celda con "Shift-Enter". No se requieren cambios de código.

![alt text](img/labs07.png)

Note que el Notebook incluye algunos ejemplos de comandos "pip install". Con estos, los paquetes de Python se descargan en el Runtime del Proyecto. Si cierras tu sesión y vuelves más tarde, esos paquetes seguirán instalados en tu Proyecto.

Tu Proyecto de CML es, en efecto, tu ambiente privado de Python para exploración de datos y desarrollo de modelos, sin la molestia de instalaciones complejas y gestión de dependencias.  

##### Ejecución de Notebook

Continúe ejecutando las celdas en cada Notebook. Se proporcionan instrucciones detalladas para continuar en cada Notebook.

* El resto del Notebook 1 se centra en algunos comandos simples y la creación de una variable de ambiente del proyecto.

![alt text](img/labs08.png)

![alt text](img/labs09.png)

![alt text](img/labs10.png)

* El Notebook 2 proporciona una introducción a Spark-on-Kubernetes y las Data Connections en CML. Con CML, puedes implementar fácilmente Sesiones de CML con Spark para analizar datos y crear modelos a escala. Las "Data Connections" proporcionan código predefinido para conectar con diferentes tipos de fuentes de datos, incluida la implementación de una Sesión de Spark dentro de tu Notebook.

![alt text](img/labs11.png)

![alt text](img/labs12.png)

![alt text](img/labs14.png)

* El Notebook 3 proporciona una introducción a Apache Iceberg en CML. Iceberg es un formato de tabla que permite análisis de tipo Lakehouse en tus datos. En el contexto del aprendizaje automático, es beneficioso porque te permite cambiar entre diferentes versiones de tus datos al incluir una marca de tiempo o Snapshot ID en tu consulta.

![alt text](img/labs15.png)

![alt text](img/labs16.png)

![alt text](img/labs17.png)

Detente después de ejecutar el Notebook 3 y continúa con la siguiente sección sobre Jobs de CML.


##### Despliegue de Job

Los Jobs de CML te permiten desplegar ejecuciones programadas de tu código sin la molestia de abrir una sesión. Son ideales para casos de uso que implican la ejecución repetida de código, como Ingeniería de Datos o Inferencia de Modelos. La página de Jobs proporciona características adicionales de visibilidad para monitorear la ejecución.

Navega a la página de Jobs y crea un Job con el script "04_datagen.py". Luego, ejecútalo.

```
Name: DataGen - nombre de usuario
Script: 04_datagen.py
Enable Spark: 3.2
Schedule: Manual
Resource Profile: 2 CPU / 8 GB Mem
```

![alt text](img/labs18.png)

![alt text](img/labs19.png)

![alt text](img/labs20.png)

Este trabajo ha creado un conjunto de datos sintético con datos geoespaciales. Una vez que hayas ejecutado el Job, vuelve a abrir la Sesión de CML y ejecuta los Notebooks restantes. Utilizarás el nuevo conjunto de datos allí.

### Resumen

En esta primera sesión, comenzaste desde lo básico de CML. Creaste tu primer proyecto y sesión para explorar tus datos en un entorno aislado con tus propios paquetes de Python. Luego, creaste un trabajo para aislar un script más complejo en una ejecución separada y asignarle más recursos. En conclusion:

* CML proporciona infraestructura fácilmente escalable para satisfacer todas tus necesidades, desde el desarrollo hasta la producción.

* En el Workspace de CML hay tres roles: MLWorkspaceAdmin, MLWorkspaceBusinessUser, MLWorkspaceUser. Normalmente, a los científicos de datos se les asigna el rol de MLWorkspaceUser, a los administradores se les asigna el rol de MLWorkspaceAdmin y a los analistas se les asigna el rol de MLWorkspaceBusinessUser.

* Cada usuario despliega su Proyecto para trabajar en un ambiente aislado que incluye Runtime, datos, y archivos privados. Sin embargo, cada usuario tiene la opción de compartir su trabajo con otros invitándolos a su proyecto, o directamente cambiando la configuración de proyecto a público.

* Las Sesiones proporcionan un ambiente interactivo para la investigación y exploración de datos, y el desarrollo de modelos. Cuando el usuario abre una sesión, puede decidir qué runtime usar. La consecuencia de esta flexibilidad es que los usuarios pueden seleccionar el entorno de ejecución más adecuado para sus necesidades específicas, lo que les permite optimizar su productividad y rendimiento.

* Los Jobs permiten a los usuarios de orquestar y programar ejecuciones independientes o dependientes. El uso típico es para Jobs de ETL de Spark y puntuación por lotes.

* Spark es uno de los principales frameworks para ETL y Aprendizaje Automático a gran escala. CML proporciona la capacidad de Spark Runtime Add-On para usar Spark en una Sesión sin instalaciones avanzadas, y Spark Data Connections para desplegar una SparkSession con configuraciones recomendadas, como los archivos JAR y otras configuraciones de Iceberg.

* Apache Iceberg es un formato de tabla abierto diseñado para el almacenamiento seguro y eficiente de grandes conjuntos de datos en plataformas de almacenamiento de datos distribuidos como Apache Hadoop y Apache Spark. Iceberg facilita la creación de un modelo de lago de datos (Lakehouse) al permitir la gestión de versiones y la captura de instantáneas de datos, lo que lo hace ideal para aplicaciones de análisis de datos a gran escala.
